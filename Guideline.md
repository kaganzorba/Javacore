#Java Core
[GitHub](https://github.com/kaganzorba/Javacore.git)
[JDK](https://www.oracle.com/tr/java/technologies/downloads/#jdk23-windows)
[Intellij Idea Community](https://www.jetbrains.com/idea/download/?section=windows)
[Git](https://git-scm.com/downloads)
[Java Tutorials](https://www.w3schools.com/java/default.asp)


## Git
```sh 
git init
git add .
git commit -m "add message"
git push -u origin master

git clone  https://github.com/hamitmizrak/ibb_ecodation_javacore.git
```
---

## Java Common Rules ()
```sh 
Class isimleri PascalCase göre yazılır
Class isimleri: Fiil olarak kullanmayız (mak-mek)
Class : Java 1 tane public class vardır (inner class hariç)
Class : Java static class yoktur (inner class hariç)

Paket isimleri: Küçük harflerle yazılır.
Paket isimleri: fiil olarak kullanmayız (mak-mek)
Paket kısa net bir şekilde olması gerekiyor.

Javada Her biten kelime ; ile bitirmek zorundayız.
```
---


## Java Core Information
```sh 
Java case sensitive bir dildir. (Küçük büyük harfe duyarlı yüksek seviyede bir dildir.)
```
---

## Maven Nedir ?
```sh 

```
---
### **1. Maven Nedir?**
Maven, Java projelerini oluşturmak, yönetmek ve otomatikleştirmek için kullanılan bir **build automation** (inşa otomasyonu) aracıdır. Apache tarafından geliştirilmiştir ve özellikle Java projelerinde bağımlılık yönetimi, derleme, test etme ve dağıtım süreçlerini kolaylaştırır. Maven, XML tabanlı bir yapılandırma dosyası olan `pom.xml` kullanarak projenin yapılandırmasını ve bağımlılıklarını yönetir.

**Maven’in Sağladıkları:**
- **Bağımlılık Yönetimi:** Projeye eklenmesi gereken kütüphaneleri otomatik olarak indirir.
- **Proje Yapılandırması:** Projeyi standart bir yapıda düzenler.
- **Otomatik Derleme:** Projeyi derler (`mvn compile`).
- **Test Çalıştırma:** JUnit ve TestNG gibi test araçlarıyla testleri çalıştırır (`mvn test`).
- **Paketleme:** Projeyi `jar` veya `war` formatında paketler (`mvn package`).
- **Dağıtım Yönetimi:** Uygulamayı uzak sunuculara veya depolara gönderir (`mvn deploy`).

---

## pom.xml Nedir ?
```sh 

```
### **2. `pom.xml` Nedir?**
`pom.xml` (**Project Object Model**) dosyası, Maven projelerinin merkezi yapılandırma dosyasıdır. Projenin bağımlılıklarını, sürüm bilgilerini, eklentilerini ve yapılandırmalarını içerir.

Örnek bir `pom.xml` dosyası:
```xml
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <groupId>com.example</groupId>
    <artifactId>my-app</artifactId>
    <version>1.0-SNAPSHOT</version>
    <dependencies>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-web</artifactId>
            <version>2.7.4</version>
        </dependency>
    </dependencies>
</project>
```
Bu dosya:
- Projenin kimliğini (`groupId`, `artifactId`, `version`)
- Bağımlılıklarını (`dependencies`)
- Yapılandırmalarını içerir.

---


## JDK Nedir ?
```sh 

```
### **3. JDK (Java Development Kit) Nedir?**
**JDK (Java Development Kit)**, Java ile uygulama geliştirmek için kullanılan geliştirme ortamıdır. İçerisinde:
- **JRE (Java Runtime Environment)** (Çalışma zamanı ortamı)
- **JVM (Java Virtual Machine)** (Java Sanal Makinesi)
- **Java Compiler (javac)** (Java derleyicisi)
- **Java Debugger (jdb)** (Hata ayıklayıcı)
- **Java API ve kütüphaneleri** bulunur.

JDK olmadan Java kodu yazılamaz ve çalıştırılamaz.
---

## JRE Nedir ?
```sh 

```
### **4. JRE (Java Runtime Environment) Nedir?**
**JRE (Java Runtime Environment)**, Java uygulamalarını çalıştırmak için gereken ortamdır. İçerisinde:
- **JVM (Java Virtual Machine)** bulunur.
- **Java Kütüphaneleri** içerir.
- **Çalışma zamanı dosyaları** bulunur.

Eğer sadece Java programlarını çalıştırmak istiyorsanız, JDK yerine sadece JRE yükleyebilirsiniz. Ancak, JRE **Java kodu yazmak veya derlemek için yeterli değildir**.
---

### **5. JVM (Java Virtual Machine) Nedir?**
**JVM (Java Virtual Machine)**, Java programlarını çalıştıran sanal bir makinedir. JVM sayesinde Java platform bağımsızdır çünkü Java kodu her işletim sisteminde çalışabilecek **bayt koduna** (`.class` dosyalarına) çevrilir.

JVM’in Görevleri:
- **Bayt kodunu çalıştırır.**
- **Bellek yönetimini yapar (Garbage Collection).**
- **Çoklu iş parçacığını (multithreading) destekler.**
- **Platform bağımsızlığı sağlar.**
---

## Compiler Nedir ?
```sh 

```
### **5. Compiler (Derleyici) Nedir?**
**Compiler (Derleyici)**, insan tarafından yazılan yüksek seviyeli programlama dillerini makine koduna veya bayt koduna dönüştüren bir programdır. Java’da derleyici `javac` olarak adlandırılır.

**Java'da Çalışma Süreci:**
1. **Java kodu yazılır:** `MyClass.java`
2. **Derleyici (`javac`) çalıştırılır:** `javac MyClass.java`
3. **Bayt kodu (`.class` dosyası) oluşturulur:** `MyClass.class`
4. **JVM bayt kodunu çalıştırır.**
---


## Intepreter Nedir ?
```sh 

```
### **7. Interpreter (Yorumlayıcı) Nedir?**
**Interpreter (Yorumlayıcı),** programın satır satır çalıştırılmasını sağlayan bir programdır.
Java’da **JVM içerisinde yer alan yorumlayıcı (interpreter)**, bayt kodlarını satır satır çalıştırır.

**Derleyici (Compiler) vs. Yorumlayıcı (Interpreter):**
- **Derleyici**: Tüm kodu derleyerek tek seferde çalıştırılabilir hale getirir.
- **Yorumlayıcı**: Kodu satır satır çalıştırır.

Java hem **derleyici (`javac`)** hem de **yorumlayıcı (JVM içinde)** kullanır.
---

### **8. Java Nedir?**
Java, **nesne yönelimli (OOP), platform bağımsız, güvenli, çok iş parçacıklı (multithreading) ve taşınabilir** bir programlama dilidir.

- **1995’te Sun Microsystems tarafından geliştirildi.**
- **"Bir kere yaz, her yerde çalıştır" (Write Once, Run Anywhere - WORA)** prensibiyle çalışır.
- **Mobil, web, masaüstü ve büyük ölçekli sistemlerde kullanılır.**
---

### **9. Java’nın Özellikleri Nelerdir?**
- **Platform Bağımsızdır.** (JVM sayesinde her yerde çalışır)
- **Nesne Yönelimli Programlama (OOP) Desteği** vardır.
- **Güvenlidir.** (Bellek yönetimi ve güvenlik mekanizmaları içerir)
- **Çok İş Parçacıklı (Multithreading)** çalışmayı destekler.
- **Otomatik Bellek Yönetimi (Garbage Collection)** yapar.
- **Dağıtık ve Ağ Tabanlı Uygulamaları Destekler.**
---

### **10. Data Types (Veri Tipleri) Nedir?**
Java'da değişkenlerin alabileceği veri türlerini ifade eder. İki ana kategoriye ayrılır:
1. **Primitive Types (İlkel Veri Tipleri)**
2. **Reference Types (Referans Tipleri)**
---

### **11. Primitive Types Nedir?**
Java'daki **ilkel veri tipleri (Primitive Types)** hafızada doğrudan değer saklayan basit veri türleridir.

| Veri Tipi  | Boyut | Varsayılan Değer | Aralık |
|------------|------|----------------|------------------|
| `byte`     | 1B  | 0              | -128 to 127 |
| `short`    | 2B  | 0              | -32,768 to 32,767 |
| `int`      | 4B  | 0              | -2^31 to 2^31-1 |
| `long`     | 8B  | 0L             | -2^63 to 2^63-1 |
| `float`    | 4B  | 0.0f           | ~7 basamak |
| `double`   | 8B  | 0.0d           | ~15 basamak |
| `char`     | 2B  | '\u0000'       | Unicode karakterler |
| `boolean`  | 1B  | `false`        | `true` veya `false` |
---

### **12. Wrapper Types Nedir?**
**Wrapper Class’lar,** primitive veri tiplerinin nesne olarak kullanılmasını sağlar.

Örneğin:
```java
int num = 10;
Integer obj = Integer.valueOf(num);
```

**Primitive -> Wrapper Dönüşümleri:**
- **`int -> Integer`**
- **`double -> Double`**
- **`char -> Character`**
- **`boolean -> Boolean`**

Wrapper class’lar **Java Collections API’lerinde** kullanılır çünkü koleksiyonlar yalnızca nesne saklayabilir.


## Java Core (Primitive Types)
```sh 

```
---

**`javac` (Java Compiler) ve bayt kodu (bytecode) süreci**, derleme süresi ve oluşturulan `.class` dosyasının boyutunu etkileyebilir. Aşağıda bunun nasıl gerçekleştiğine dair detaylı bir açıklama bulabilirsiniz.
---

## **1. `javac` Derleyici ve Derleme Süresi**
### **Derleme Süresini Etkileyen Faktörler**
- **Kodun Karmaşıklığı:**
    - Daha fazla **sınıf, metod ve kod satırı** içeren projeler daha uzun sürede derlenir.
    - Büyük projelerde, bağımlılıklar ve `import` edilen kütüphaneler derleme süresini uzatabilir.

- **Optimize Edilmiş Derleme (`javac` Seçenekleri)**:
    - **Incremental Compilation (Artımlı Derleme):**
        - Eğer sadece değişiklik yapılan sınıflar derlenirse, `javac` süresi kısalır.
    - **Hata Ayıklama Seçenekleri (`-g:none`)**:
        - `javac -g:none` komutu hata ayıklama bilgilerini içermeyen bir bytecode oluşturur ve derleme süresini kısaltabilir.
    - **Çoklu İş Parçacığı (Multithreading) Kullanımı:**
        - Büyük projelerde **Gradle** gibi derleme sistemleri çoklu iş parçacığı desteği sağlar, böylece derleme süresi azalır.

- **Donanım ve JVM Yapılandırması:**
    - Daha hızlı CPU ve SSD kullanan sistemlerde derleme süresi düşer.
    - Yetersiz RAM veya düşük işlem gücü derleme süresini artırır.

---

## **2. Bayt Kodu (Bytecode) ve Dosya Boyutu**
**Bytecode,** `javac` tarafından üretilen **platformdan bağımsız bir ara koddur** ve `.class` dosyalarında saklanır.

### **Bytecode Boyutunu Etkileyen Faktörler**
1. **Kodun İçeriği ve Karmaşıklığı:**
    - Uzun metotlar, fazla satır kod ve daha fazla `class` tanımlaması dosya boyutunu artırır.

2. **Yerel Değişkenler ve Sabit Havuzu (Constant Pool):**
    - Java’nın **String Constant Pool** ve diğer sabit değişkenleri yönetme mekanizması, **fazla sayıda string veya sabit tanımı içeren** kodlarda `.class` dosyasının boyutunu artırabilir.

3. **Kullanılan Optimizasyonlar:**
    - **JVM Optimizasyonları:**
        - JVM, bayt kodunu çalıştırırken **Just-In-Time (JIT) Compiler** gibi tekniklerle optimizasyon yapar.
    - **Inline Kod Kullanımı:**
        - `final` ve `static` değişkenlerin derleme zamanında yerine konulması, bytecode boyutunu artırabilir.

4. **Lombok, Annotation Processing ve Kütüphaneler:**
    - **Lombok, Spring gibi kütüphaneler** **otomatik kod üretme (code generation)** yapıyorsa, `.class` dosya boyutunu artırabilir.
    - **Annotation Processing**, derleme zamanında ek kodlar üreterek dosya boyutunu büyütebilir.

5. **Obfuscation (Kod Gizleme) ve Minifikasyon:**
    - Eğer kod **ProGuard veya R8 gibi optimizasyon araçlarıyla küçültülürse**, bytecode dosya boyutu azalır.
    - **Android projelerinde R8 ve ProGuard kullanımı**, bytecode boyutunu küçültmek için yaygın bir tekniktir.

---
