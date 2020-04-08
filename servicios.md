---
layout: page
title: Servicios disponibles
---

 * **librAIry-BioNLP**: Un [servicio abierto](https://librairy.github.io/bio-nlp/) para la anotación de textos con códigos ATC (Sistema de Clasificación Anatómica, Terapéutica, Química) de principios activos (nivel 5) y subgrupos químicos (nivel 4), que puede ser utilizado por cualquier usuario o desarrollador que desee realizar anotaciones sobre textos ([código fuente](https://github.com/librairy/bio-nlp)).

 * **CORD19-Repository**: Un repositorio documental que facilita el procesamiento automático de las publicaciones científicas disponibles en el corpus CORD-19 mediante la creación de los siguientes recursos: 
 
    * Colecciones en SOLR: 
      * 33.244 [artículos científicos](http://librairy.linkeddata.es/data/#/covid/core-overview) anotados con los medicamentos (códigos ATC) y enfermedades. Con estos recursos se pueden buscar los artículos científicos que: [mencionen la cloroquina](http://librairy.linkeddata.es/data/covid/select?q=labels5_t:P01BA01&fl=id,name_s,url_s), [utilicen medicamentos que combinan penicilina y/o inhibidores de la beta-lactamasa](http://librairy.linkeddata.es/data/covid/select?q=labels4_t:J01CR&fl=id,name_s,url_s), [describan tratamientos antivirales con Interferon](https://librairy.linkeddata.es/solr/covid/select?q=annot_cliner_treatments_t:antiviral_therapy%20AND%20labels5_t:S01AD05&fl=id,name_s,url_s) 
      * 5.298.063 [frases extraídas automáticamente de los artículos](http://librairy.linkeddata.es/data/#/covid-sentences/core-overview) y anotadas también con los medicamentos (ATC) y enfermedades. 

    * [Dashboard](https://librairy.linkeddata.es/data/dashboard), con grafos y estadísticas sobre la colección de artículos. Se debe cargar el [GIST](https://gist.github.com/cbadenes/4f726911fd9908ffc3a46837b15d8011) 4f726911fd9908ffc3a46837b15d8011 para poder acceder a los datos de este índice.
    
    * [Explorador](https://librairy.github.io/covid19/explorer.html), mediante etiquetas creadas a partir de las anotaciones y a partir de las representaciones vectoriales de las publicaciones, permite filtrar y relacionar los documentos.

 * Un [modelo probabilístico de tópicos entrenado con este corpus de documentos](http://librairy.linkeddata.es/covid19-model/). Este modelo identifica los términos más descriptivos, en el contexto de este corpus, para 3.253 medicamentos identificados a través de su código ATC. Para cualquier texto este modelo nos puede decir los medicamentos que se han utilizado más habitualmente en textos similares. Por ejemplo, las palabras que aparecen asociadas más frecuentemente a la combinación de los principios activos estreptomicina e isoniazida, utilizados para el tratamiento de la tuberculosis (cuyo tópico se corresponde con el código ATC: J04AM01) [son](http://librairy.linkeddata.es/covid19-model/topics/3/words): feline, fcov, fipv, fcv, fecv, ccov, mnv, norovirus, fip y serotype.

 * Un grafo de principios activos, relacionados entre sí por las intersecciones en las distribuciones de palabras de los documentos en los que aparecen, de acuerdo con el modelo de tópicos anterior. La [representación visual de este grafo](https://librairy.github.io/covid19/graph.html) está disponible en formato reutilizable para que pueda ser utilizado por los investigadores. Algunas otras representaciones se ofrecen a continuación:

![Grafo](../img/servicios/graph-1.png "Grafo")
![Grafo 2](../img/servicios/graph-2.png "Grafo 2")

 * Una [interfaz de navegación](http://demo.inno.oeg-upm.net), desarrollada en colaboración con el [AI.nnovation Space](https://www.ainnovation.upm.es/), que permite hacer búsquedas de palabras clave o términos compuestos generados automáticamente a partir de los textos, y navegar por los artículos científicos cuyo formato PDF está disponible de manera abierta. Por el momento, estos documentos representan una muy pequeña fracción de todos los artículos publicados en el corpus (menos del 3%), aunque se irán incorporando al sistema según se vayan liberando. Por ejemplo, como se muestra en la figura, si se teclea la palabra “molecule”, el sistema sugiere, entre otros, los siguientes términos compuestos: “surface molecules”, “cell-adhesion molecules”, “biological macro-molecules”, lo que puede ayudar en dicha navegación.

![Grafo 2](../img/servicios/keyq.png "Grafo 2")
