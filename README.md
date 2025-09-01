# Cloud-Free Area Extraction from Landsat 8 using Google Earth Engine

## English 🌍
This repository contains a Google Earth Engine (GEE) script used to extract **cloud-free areas** from **Landsat 8 imagery** for a specified study area.  
The workflow includes:

- Creating a **binary cloud mask** using the QA_PIXEL band (cloud and cirrus detection)
- Filtering Landsat 8 images by date, cloud cover (<10%), and study area geometry
- Selecting the first image and clipping it to the study area
- Converting cloud-free pixels to **vector polygons**
- Visualizing the polygons on the map
- Exporting the result as **Shapefile or GeoJSON** to Google Drive

⚠️ **Notes:**  
- The output polygons represent cloud-free areas in your study area.  
- The cloud cover threshold (`CLOUD_COVER < 10%`) in the script can be adjusted according to your study area and needs. Increasing the threshold may include more images but might also include more cloudy pixels.  

### How to Use
1. Open [Google Earth Engine Code Editor](https://code.earthengine.google.com/).  
2. Copy and paste the script from `cloud_free_polygon.js`.  
3. Define your **study area geometry** (`table`).  
4. Run the script to generate and export the cloud-free polygons.  

### Output
- Polygons representing **cloud-free areas** in the study area
- Exported to Google Drive as **SHP or GeoJSON**  
- Can be used in GIS software (QGIS, ArcGIS) for further analysis

---

## Türkçe 🇹🇷
Bu depo, belirlenen bir çalışma alanında **Landsat 8 görüntülerinden bulutsuz alanların çıkarılması** için kullanılan Google Earth Engine (GEE) kodunu içerir.  
Çalışma akışı şu adımlardan oluşmaktadır:

- QA_PIXEL bandını kullanarak **binary bulut maskesi** oluşturma (bulut ve cirrus tespiti)
- Landsat 8 görüntülerini tarih, bulut örtüsü (<%10) ve çalışma alanına göre filtreleme
- İlk görüntüyü seçme ve çalışma alanına kırpma
- Bulutsuz pikselleri **vektör poligonlara** dönüştürme
- Poligonları haritada görselleştirme
- Sonucu **Shapefile veya GeoJSON** olarak Google Drive’a aktarma

⚠️ **Notlar:**  
- Çıktı poligonları çalışma alanındaki **bulutsuz alanları** temsil eder.  
- Scriptteki bulut örtüsü filtresi (`CLOUD_COVER < 10%`) ihtiyacınıza ve çalışma alanınıza göre değiştirilebilir. Filtreden yüksek değer seçmek daha fazla görüntü getirir ancak bulutlu piksellerin sayısı da artabilir.  

### Kullanım
1. [Google Earth Engine Code Editor](https://code.earthengine.google.com/) adresini açın.  
2. `cloud_free_polygon.js` dosyasındaki kodu yapıştırın.  
3. Çalışma alanı geometrisini (`table`) tanımlayın.  
4. Scripti çalıştırarak bulutsuz alan poligonlarını oluşturun ve dışa aktarın.  

### Çıktı
- Çalışma alanındaki **bulutsuz alanları temsil eden poligonlar**  
- Google Drive’a **SHP veya GeoJSON** olarak kaydedilir  
- GIS yazılımlarında (QGIS, ArcGIS) daha ileri analizler için kullanılabilir
