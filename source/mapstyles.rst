.. sectionauthor:: Артём Светлов <artem.svetlov@nextgis.ru>

.. _ngw_style_create:
    
Стили векторных слоёв
=====================

Стили служат для описания способов визуализации геоданных и являются одним из ресурсов NextGIS Web. 
Именно стиль добавляется на карты для представления на ней геоданных.

Форматы
----------------------------------

Сейчас NextGIS Web поддерживает две библиотеки рендеринга: ``Mapserver`` и ``QGIS``. 
Стиль Mapserver можно писать самому в текстовом виде или импортировать из стилей QGIS, у него мало 
настроек отображения. 
Стиль QGIS можно только загружать из стилей QGIS, у него гораздо больше настроек. 

Создания стиля
----------------------------------

Стиль связан с конкретным слоем, поэтому вы не найдете пункт "Стиль" в основном списке ресурсов. 
Для создания стиля необходимо сначала зайти в ресурс слоя, для которого вы его создаёте:

.. figure:: _static/ngweb_layer_properties_window.png
   :name: ngweb_layer_properties_window_pic
   :align: center
   :width: 16cm
 
   Окно свойств слоя.

В окне свойств поля выбрать:
``Создать ресурс --> Стиль MapServer`` или ``Создать ресурс --> Стиль QGIS``.  При этом откроется окно, в 
котором можно импортировать стиль из QGIS в формате ``QML`` или ввести его вручную. 
Рассмотрим вариант с созданием слоя со Стилем QGIS:

.. figure:: _static/ngweb_window_create_resource.png
   :name: ngweb_window_create_resource_pic
   :align: center
   :width: 16cm

   Окно Создать ресурс.

В окне "Создать ресурс" на вкладке "Ресурс" внести данные в поле обязательное к заполнению - ``Наименование``, 
на вкладке "Стиль QGIS" следует в поле ``Файл QML`` нажать на "Выбрать файл" или перетащите его в эту область:

.. figure:: _static/ngweb_download_file.png
   :name: ngweb_download_file_pic
   :align: center
   :width: 16cm

   Загрузка файла QML.

.. warning::
   
   Необходимый для загрузки файл должен быть получен с помощью :program:`NextGIS QGIS` и сохранен на компьютере.

После загрузки файла QML нажмите на кнопку "Создать". После обработки запроса, откроется 
окно файла со стилем QGIS:

.. figure:: _static/ngweb_file_QGIS_style.png
   :name: ngweb_file_QGIS_style_pic
   :align: center
   :width: 16cm

   Окно файла со стилем QGIS.

Для добавление на веб-карту слоя со стилем QGIS необходимо вернуться к окну "Основная 
группа ресурсов" и выбрать в группе дочерних ресурсов веб-карту, на которой необходимо 
отразить слой со стилем QGIS. Напротив названия веб-карты выбираем и нажимаем значок карандаша,
что ведет к возможности редактирования веб-карты. Откроется окно "Обновить ресурс". 
Далее следует выбрать вкладку "Слои", которая предоставляет следующие возможности:

1. Добавить слой.
2. Добавить группу.
3. Удалить.

Выбираем вкладку "Добавить слой". В открывшемся окне выбрать слой со стилем QGIS и 
нажимаем на кнопку "ОК". И далее нажимаем на кнопку "Сохранить":
  
.. figure:: _static/ngweb_select_file_upload_web_map.png
   :name: ngweb_select_file_upload_web_map_pic
   :align: center
   :width: 16cm
   
   Выбор файла со стилем QGIS для загрузки на веб-карту.

После обработки запроса откроется окно веб-карты с правами пользователя и возможными 
действиями с веб-картой (удалить, изменить, открыть). Справа на экране в блоке действий 
с веб-картой выбираем вкладку "Веб-карта" и нажимаем на кнопку "Открыть". Откроется окно с
картой. Слева от карты - дерево слоев. Для включения видимости слоя на карте по-умолчанию 
следует проставить отметку напротив слоя:

.. figure:: _static/ngweb_Map_and_tree_layers.png
   :name: ngweb_Map_and_tree_layers_pic
   :align: center
   :width: 16cm

   Веб-карта со слоем стиля QGIS и деревo слоев.

Рассмотрим вариант с созданием слоя со ``Стилем Mapserver``. Для создания стиля необходимо 
сначала зайти в слой, для которого вы его создаёте (см. :numref:`ngweb_layer_properties_window_pic`).

В окне свойств поля выбрать:
``Создать ресурс --> Стиль MapServer``: (см. :numref:`ngweb_window_create_resource_pic`).

В окне "Создать ресурс" на вкладке "Ресурс" заполняем поле обязательное к заполнению - ``Наименование``. 
Далее, выбрав вкладку "Стиль MapServer", следует нажать на кнопку "Импорт стиля QGIS" или построчно ввести стиль вручную:

.. figure:: _static/ngweb_create_resource_mapsrev.png
   :name: ngweb_create_resource_mapsrev_pic
   :align: center
   :width: 16cm
 
   Окно "Создать ресурс".

При нажатии на кнопку "Импорт стиля QGIS" откроется окно, в котором предлагается выбрать 
файл или перетащить файл в открывшуюся область/окно:

.. figure:: _static/ngweb_select_and_download_file.png
   :name: ngweb_select_and_download_file_pic
   :align: center
   :width: 16cm

   Выбор и загрузка файла со стилем QGIS.

.. warning::
   
   Необходимый для загрузки файл должен быть получен с помощью :program:`NextGIS QGIS` и сохранен на компьютере.

.. figure:: _static/ngweb_Style_import_QGIS.png
   :name: ngweb_Style_import_QGIS_pic
   :align: center
   :width: 16cm

   Импорт стиля QGIS.

После импорта файла со стилем QGIS нажимаем на кнопку "ОК". После закрытия окна 
"Импорт стиля QGIS", нажимаем кнопку "Создать". Начнется процесс обработки запроса, 
по окончании которого откроется окно файла со стилем Mapserver:

.. figure:: _static/ngweb_File_format_window_MapServer.png
   :name: ngweb_File_format_window_MapServer_pic
   :align: center
   :width: 16cm

   Окно файла со стилем Mapserver.

Для добавление на веб-карту слоя со стилем Mapserver необходимо вернуться к окну 
"Основная группа ресурсов" и выбрать в группе дочерних ресурсов веб-карту, на которой 
необходимо отразить слой со стилем Mapserver. Напротив названия веб-карты выбираем 
и нажимаем значок карандаша, что ведет к возможности редактирования веб-карты. 
Откроется окно "Обновить ресурс". Далее следует выбрать вкладку "Слои", которая предоставляет 
следующие возможности:

1. Добавить слой.
2. Добавить группу.
3. Удалить.

Выбираем вкладку "Добавить слой". В открывшемся окне выбрать слой со стилем Mapserver 
и нажимаем на кнопку "ОК". И далее нажимаем на кнопку "Сохранить" (см. :numref:`ngweb_select_file_upload_web_map_pic`).

После обработки запроса откроется окно веб-карты с правами пользователя и возможными 
действиями с веб-картой (удалить, изменить, открыть). Справа на экране в блоке действий 
с веб-картой выбираем вкладку "Веб-карта" и нажимаем на кнопку "Открыть". Откроется окно с картой. 
Слева от карты - дерево слоев. Для включения видимости слоя на карте по-умолчанию следует проставить 
отметку напротив слоя (см. :numref:`ngweb_Map_and_tree_layers_pic`).

При импорте стиля Mapserver из формата QML, он сконвертируется во внутренний формат системы. Следует 
заметить, что на данный момент конвертируются только основные возможности отрисовки геометрий.
Если в импортируем стиле идет выборка по условию, то вариант для пустого 
значения нужно размещать последним (при импорте из QGIS он попадает первым).

.. warning:: 
   Если вы создали векторный слой, но у вас отсутствует пункт "Стиль Mapserver" в разделе "Создать ресурс", 
   проверьте, установлен ли пакет ``nextgis_mapserver``. Это можно сделать в ``Панели инструментов --> Версии пакетов``.
   
.. only:: latex   
   Если этого пакета нет, установка произведена не корректно, проверьте выполненные шаги: http://docs.nextgis.ru/docs_ngweb/source/install.html

.. only:: html
   Если этого пакета нет, установка произведена не корректно, проверьте выполненные шаги: :ref:`ngw_sysadmin_tasks` 

Создать или изменить стиль, который привязан к конкретному слою, можно путем ручного 
ввода текста/кода или редактирования имеющегося текста/кода (подробнее см. подразд. :ref:`ngw_mapstyles`).        

.. _ngw_mapstyles:

Теги языка картостилей Mapserver
----------------------------------

Для правки стиля, или написания нового рекомендуется взять код какого-нибудь 
существующего стиля из примера, и потом дополнять его, а не писать с нуля.
  
Общие теги
~~~~~~~~~~~~~~~~~ 
  
* <color red="255" green="170" blue="127"/> - цвет заливки или линии
* <outlinecolor red="106" green="106" blue="106"/> - цвет обводки
* <width>0.5</width> - толщина линии или границы полигона в пикселях.
* <outlinewidth>3</outlinewidth> - ширина обводки
* <minscaledenom>1</minscaledenom> - не рисовать объект на масштабе больше указанного (когда карта крупнее чем) \
* <maxscaledenom>100000</maxscaledenom> - не рисовать объект на масштабе меньше указанного (когда карта мельче чем) 

Значки
~~~~~~~~~~~~~~~~~

.. figure:: _static/mapstyle_hatch_demo.png
   :name: ngweb_mapstyle_hatch_demo_pic
   :align: center
   :width: 16cm

   Демонстрация различных видов штриховок.

* <symbol>std:circle</symbol> - тип значка

   * std:rectangle - квадратик
   * std:circle - кружок
   * std:diamond - ромбик
   * std:triangle - треугольник острием вверх
   * std:triangle-equilateral - треугольник острием вниз
   * std:star - пятиконечная звёздочка
   * std:pentagon - пятиугольник
   * std:arrow - стрелка (по умолчанию вверх, можно поворачивать тегом <angle>45</angle>)
   * std:cross - +
   * std:xcross - x
   * std:line - коротенькая линия
   * std:hatch - длинная линия, стыкующаяся в текстуру

Эти значки можно использовать для рисования линии, заливки полигонов, или обозначения точек. 
Так же их можно комбинировать в такую конструкцию:

.. code-block:: xml

        <class>
            <expression>"industrial"</expression>
            <!-- Промзоны -->
            <style> <!-- штриховка направо -->
                <color red="255" green="50" blue="50"/>
                <width>1.4</width>
                <symbol>std:hatch</symbol>
                <gap>10</gap>
                <size>5</size>
                <angle>45</angle>
            </style>
            <style> <!-- штриховка налево-->
                <color red="255" green="50" blue="50"/>
                <width>1.4</width>
                <symbol>std:hatch</symbol>
                <gap>10</gap>
                <size>5</size>
                <angle>-45</angle>
            </style>
            <style> <!-- Обводка -->
                <outlinecolor red="255" green="50" blue="50"/>
                <width>0.5</width>
            </style>
 </class>

* <size>2</size> - размер значка в пикселях

Линейные объекты
~~~~~~~~~~~~~~~~

* <gap>10</gap> - шаг пунктира (используется вместе с <symbol>std:circle</symbol>)
* <width>8</width> - ширина линии в пикселах
* <classitem>PLACE</classitem> - выборка по атрибуту с названием PLACE. Так же смотрите пример в  #Выборка.
  Поддерживаются следующие операторы
  
  * имя атрибута
  * !=
  * >=
  * <=
  * <
  * >
  * =* - сравнение строк без учёта раскладки.

  * =
  * lt - меньше
  * gt - больше
  * ge - больше или равно
  * le - меньше или равно
  * eq - равно
  * ne - не равно
  * and - И
  * && - И
  * or - ИЛИ
  * || - ИЛИ
  
* <linejoin>round</linejoin> - рисование линии в углах поворота
* <linecap>round</linecap> - рисование начала и конца линии

.. figure:: _static/admin_mapstyles_linecap.png
   :name: ngweb_admin_mapstyles_linecap.png
   :align: center
   :width: 10cm

   <linecap>butt</linecap> / <linecap>round</linecap> / <linecap>square</linecap>

* <pattern>2.5 4.5</pattern> - шаблон пунктира 
* <angle> - угол поворота значка. Так же можно поворачивать штриховку.

Подписи
~~~~~~~~

* <labelitem>a_hsnmbr</labelitem> - название атрибута, из которого берётся подпись.
* <minscaledenom>100</minscaledenom> - не выводить подпись на масштабе крупнее 1:1000
* <maxscaledenom>100000</maxscaledenom> - не выводить подпись на масштабе мельче 1:100000
* LABELCACHE [on|off] - не проверял, нашел в исхониках
* <position>ur</position> - направление сдвига подписи.

   * ur - ↗ вверх вправо (в книгах по картографии рекомендуют так делать по умолчанию.
   * ul - ↖
   * uc - ↑
   * cl - ←
   * cc - строго по центру
   * cr - →
   * ll - ↙
   * lc - ↓
   * lr - ↘
   * auto

* <Maxoverlapangle> - ?  

Неизвестные атрибуты
~~~~~~~~~~~~~~~~~~~~~~~

* MAXGEOWIDTH
* MINGEOWIDTH
* OFFSITE
* OPACITY [integer|alpha]
* SIZEUNITS [feet|inches|kilometers|meters|miles|nauticalmiles|pixels]
* SYMBOLSCALEDENOM [double]
* TYPE [chart|circle|line|point|polygon|raster|query]

.. _ngw_mapserver_templates:

Примеры картостилей Mapserver (OSM-default)
--------------------------------------------

Полигональный слой с ограничением по масштабу и подписями
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: xml

	<map>
	  <layer>
	    <labelitem>a_hsnmbr</labelitem>
	    <class>
	      <style>
		<color red="255" green="170" blue="127"/>
		<outlinecolor red="106" green="106" blue="106"/>
		<width>0.425196850394</width>
		<maxscaledenom>10000</maxscaledenom> <!-- Ограничение по масштабу -->
	      </style>
	      <label>
		<type>truetype</type>
		<font>regular</font>
		<size>8.25</size>
		<color blue="0" green="0" red="0"/>
		<outlinewidth>3</outlinewidth>
		<outlinecolor blue="255" green="255" red="255"/>
		<position>ur</position>
		<maxscaledenom>10000</maxscaledenom>
	      </label>
	    </class>
	  </layer>
	</map>


Точечный белый кружок
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: xml

     <style>
       <color red="255" green="255" blue="255"/>
       <outlinecolor red="0" green="0" blue="0"/>
       <size>8.50393700787</size>
       <symbol>std:circle</symbol>
     </style>



Линия из маленьких чёрных кружков
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: xml

     <style>
       <angle>auto</angle>
       <gap>-10</gap>
       <color red="255" green="255" blue="255"/>
       <outlinecolor red="0" green="0" blue="0"/>
       <size>2</size>
       <symbol>std:circle</symbol>
     </style>


Выборка
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: xml

	<map>
	  <layer>
	    <labelitem>NAME</labelitem>
	    <classitem>PLACE</classitem>
	    <class>
	      <expression>"city"</expression>
	      <style>
		<color red="255" green="170" blue="0"/>
		<outlinecolor red="0" green="0" blue="0"/>
		<size>11.3385826772</size>
		<symbol>std:circle</symbol>

	      </style>
	      <style>
		<color red="255" green="170" blue="0"/>
		<outlinecolor red="0" green="0" blue="0"/>
		<size>5.66929133858</size>
		<symbol>std:circle</symbol>

	      </style>
	      <label>
		<type>truetype</type>
		<font>regular</font>
		<size>18</size>
		<color blue="0" green="0" red="0"/>
		<outlinewidth>3</outlinewidth>
		<outlinecolor blue="255" green="255" red="255"/>
		 <position>ur</position>
	      </label>
	    </class>
	    <class>
	      <expression>"town"</expression>
	      <style>
		<color red="255" green="255" blue="255"/>
		<outlinecolor red="0" green="0" blue="0"/>
		<size>11.3385826772</size>
		<symbol>std:circle</symbol>

	      </style>
	      <style>
		<color red="0" green="0" blue="0"/>
		<outlinecolor red="0" green="0" blue="0"/>
		<size>5.66929133858</size>
		<symbol>std:circle</symbol>

	      </style>
	      <label>
		<type>truetype</type>
		<font>regular</font>
		<size>14</size>
		<color blue="0" green="0" red="0"/>
		<outlinewidth>3</outlinewidth>
		<outlinecolor blue="255" green="255" red="255"/>
		 <position>ur</position>
	      </label>
	    </class>
	    <class>
	      <expression>"village"</expression>
	      <style>
		<color red="255" green="255" blue="255"/>
		<outlinecolor red="0" green="0" blue="0"/>
		<size>6.8031496063</size>
		<symbol>std:circle</symbol>

	      </style>
	      <label>
		<type>truetype</type>
		<font>regular</font>
		<size>8.25</size>
		<color blue="0" green="0" red="0"/>
		<outlinewidth>3</outlinewidth>
		<outlinecolor blue="255" green="255" red="255"/>
		<position>ur</position>
	      </label>
	    </class>
	    <class>
	      <expression>"hamlet"</expression>
	      <style>
		<color red="255" green="255" blue="255"/>
		<outlinecolor red="0" green="0" blue="0"/>
		<size>4.25196850394</size>
		<symbol>std:circle</symbol>

	      </style>
	      <label>
		<type>truetype</type>
		<font>regular</font>
		<size>8.25</size>
		<color blue="0" green="0" red="0"/>
		<outlinewidth>3</outlinewidth>
		<outlinecolor blue="255" green="255" red="255"/>
		<position>ur</position>
	      </label>
	    </class>
	    <class>
	      <expression>"locality"</expression>
	      <style>
		<color red="255" green="255" blue="255"/>
		<outlinecolor red="0" green="0" blue="0"/>
		<size>2.83464566929</size>
		<symbol>std:circle</symbol>

	      </style>
	      <label>
		<type>truetype</type>
		<font>regular</font>
		<size>6.5</size>
		<color blue="0" green="0" red="0"/>
		<outlinewidth>3</outlinewidth>
		<outlinecolor blue="255" green="255" red="255"/>
		<position>ur</position>
	      </label>
	    </class>
	    <class>
	      <expression>''</expression>
	      <style>
		<color red="255" green="255" blue="255"/>
		<outlinecolor red="0" green="0" blue="0"/>
		<size>2.83464566929</size>
		<symbol>std:circle</symbol>

	      </style>
	      <label>
		<type>truetype</type>
		<font>regular</font>
		<size>8.25</size>
		<color blue="0" green="0" red="0"/>
		<outlinewidth>3</outlinewidth>
		<outlinecolor blue="255" green="255" red="255"/>
		<position>ur</position>
	      </label>
	    </class>
	  </layer>
	</map>


Площадной слой с классификацией по значению поля и подписями
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: xml

	<map>
	<layer>
	  <labelitem>NAME</labelitem>
	    <class>
	      <expression>(([num] gt 18) and ([num] le 26.1))</expression>
	      <style>
		<color red="255" green="255" blue="212"/>
		<outlinecolor blue="64" green="64" red="64"/>

	      </style>
	       <label>
		<type>truetype</type>
		<font>regular</font>
		<size>8.25</size>
		<color blue="0" green="0" red="0"/>
		<outlinewidth>3</outlinewidth>
		<outlinecolor blue="255" green="255" red="255"/>
		<position>ur</position>
		<maxscaledenom>7000000</maxscaledenom>
	      </label>
	    </class>
	  
	      <class>
	      <expression>(([num] gt 26.1) and ([num] le 28.1))</expression>
	      <style>
	       <color red="254" green="217" blue="142"/>
		<outlinecolor blue="64" green="64" red="64"/>

	      </style>
		 <label>
		<type>truetype</type>
		<font>regular</font>
		<size>8.25</size>
		<color blue="0" green="0" red="0"/>
		<outlinewidth>3</outlinewidth>
		<outlinecolor blue="255" green="255" red="255"/>
		<position>ur</position>
		<maxscaledenom>7000000</maxscaledenom>
	      </label>
	    </class>
	  
	  
	    <class>
	      <expression>(([num] gt 28.1) and ([num] le 30))</expression>
	      <style>
	       <color red="254" green="153" blue="41"/>
		<outlinecolor blue="64" green="64" red="64"/>

	      </style>
	       <label>
		<type>truetype</type>
		<font>regular</font>
		<size>8.25</size>
		<color blue="0" green="0" red="0"/>
		<outlinewidth>3</outlinewidth>
		<outlinecolor blue="255" green="255" red="255"/>
		<position>ur</position>
		<maxscaledenom>7000000</maxscaledenom>
	      </label>
	    </class>
	  
	  </layer>
	</map>


Кластеризация точек на сервере
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: xml

	<map>
	  <symbol>
	    <type>ellipse</type>
	    <name>shop</name>
	    <anchorpoint x="0.5" y="0.5" />
	    <points>1 1</points>
	    <filled>true</filled>
	  </symbol>
	  <layer>
	    <labelitem>Cluster:FeatureCount</labelitem>
	    <classitem>Cluster:FeatureCount</classitem>
	    <cluster>
	      <maxdistance>20</maxdistance>
	      <region>"ellipse"</region>
	    </cluster>
	    <class>
	      <expression>("[Cluster:FeatureCount]" != "1")</expression>
	      <style>
		<symbol>shop</symbol>
		<size>20</size>
		<color blue="0" green="0" red="180"/>
		<outlinecolor blue="64" green="64" red="64"/>
	      </style>
	      <label>
		<type>truetype</type>
		<font>bold-italic</font>
		<size>10</size>
		<color blue="255" green="255" red="255"/>
		<outlinewidth>1</outlinewidth>
		<outlinecolor blue="0" green="0" red="0"/>
		<position>cc</position>
		<offset x="10" y="0" />
	      </label>
	    </class>
	    <class>
	      <expression>"1"</expression>
	      <style>
		<symbol>shop</symbol>
		<size>10</size>
		<color blue="0" green="0" red="180"/>
		<outlinecolor blue="64" green="64" red="64"/>
	      </style>
	    </class>

	  </layer>
	</map>

OSM settlement-point
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: xml

	<!-- Стиль с разделением по масштабам-->
	<!-- Версия 2015-07-24 -->
	<map>
	  <layer>
	    <labelitem>NAME</labelitem>
	    <classitem>PLACE</classitem>
	    <class>
	      <expression>"city"</expression> <!-- Большой город -->
	      <style>
		<color red="255" green="170" blue="0"/>
		<outlinecolor red="0" green="0" blue="0"/>
		<size>11.3385826772</size>
		<symbol>std:circle</symbol>

	      </style>
	      <style>
		<color red="255" green="170" blue="0"/>
		<outlinecolor red="0" green="0" blue="0"/>
		<size>5.66929133858</size>
		<symbol>std:circle</symbol>

	      </style>
	      <label>
		<type>truetype</type>
		<font>regular</font>
		<size>18</size>
		<color blue="0" green="0" red="0"/>
		<outlinewidth>3</outlinewidth>
		<outlinecolor blue="255" green="255" red="255"/>
		 <position>ur</position>
	      </label>
	    </class>
	    <class>
	      <expression>"town"</expression> <!-- Средний или малый город -->
	      <style>
		<color red="255" green="255" blue="255"/>
		<outlinecolor red="0" green="0" blue="0"/>
		<size>11.3385826772</size>
		<symbol>std:circle</symbol>
		<maxscaledenom>6000000</maxscaledenom>

	      </style>
	      <style>
		<color red="0" green="0" blue="0"/>
		<outlinecolor red="0" green="0" blue="0"/>
		<size>5.66929133858</size>
		<symbol>std:circle</symbol>
		<maxscaledenom>6000000</maxscaledenom>

	      </style>
	      <label>
		<type>truetype</type>
		<font>regular</font>
		<size>14</size>
		<color blue="0" green="0" red="0"/>
		<outlinewidth>3</outlinewidth>
		<outlinecolor blue="255" green="255" red="255"/>
		 <position>ur</position>
		<maxscaledenom>6000000</maxscaledenom>
	      </label>
	    </class>
	    <class>
	      <expression>"village"</expression> <!-- Посёлок  -->
	      <style>
		<color red="255" green="255" blue="255"/>
		<outlinecolor red="0" green="0" blue="0"/>
		<size>6.8031496063</size>
		<symbol>std:circle</symbol>
		<maxscaledenom>1000000</maxscaledenom>

	      </style>
	      <label>
		<type>truetype</type>
		<font>regular</font>
		<size>8.25</size>
		<color blue="0" green="0" red="0"/>
		<outlinewidth>3</outlinewidth>
		<outlinecolor blue="255" green="255" red="255"/>
		<position>ur</position>
		<maxscaledenom>1000000</maxscaledenom>
	      </label>
	    </class>
	    <class>
	      <expression>"hamlet"</expression> <!-- Деревня -->
	      <style>
		<color red="255" green="255" blue="255"/>
		<outlinecolor red="0" green="0" blue="0"/>
		<size>4.25196850394</size>
		<symbol>std:circle</symbol>
		<maxscaledenom>500000</maxscaledenom>

	      </style>
	      <label>
		<type>truetype</type>
		<font>regular</font>
		<size>8.25</size>
		<color blue="0" green="0" red="0"/>
		<outlinewidth>3</outlinewidth>
		<outlinecolor blue="255" green="255" red="255"/>
		<position>ur</position>
		<maxscaledenom>500000</maxscaledenom>
	      </label>
	    </class>
	    <class>
	      <expression>"locality"</expression> <!-- Необитаемая местность -->
	      <style>
		<color red="255" green="255" blue="255"/>
		<outlinecolor red="0" green="0" blue="0"/>
		<size>2.83464566929</size>
		<symbol>std:circle</symbol>
		<maxscaledenom>500000</maxscaledenom>

	      </style>
	      <label>
		<type>truetype</type>
		<font>regular</font>
		<size>6.5</size>
		<color blue="0" green="0" red="0"/>
		<outlinewidth>3</outlinewidth>
		<outlinecolor blue="255" green="255" red="255"/>
		<position>ur</position>
		<maxscaledenom>500000</maxscaledenom>
	      </label>
	    </class>
	    <class>
	      <expression>''</expression>
	      <style>
		<color red="255" green="255" blue="255"/>
		<outlinecolor red="0" green="0" blue="0"/>
		<size>2.83464566929</size>
		<symbol>std:circle</symbol>

	      </style>
	      <label>
		<type>truetype</type>
		<font>regular</font>
		<size>8.25</size>
		<color blue="0" green="0" red="0"/>
		<outlinewidth>3</outlinewidth>
		<outlinecolor blue="255" green="255" red="255"/>
		<position>ur</position>
	      </label>
	    </class>
	  </layer>
	</map>


OSM highway-lowzoom
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Дороги общего пользования (мелкие вынесены в отдельный стиль дальше, 
чтобы можно было отдельно включать-выключать). Цветовая схема - с openstreetmap.de

.. figure:: _static/mastyles_osm-highway-lowzoom.png
   :name: ngweb_mastyles_osm-highway-lowzoom
   :align: center
   :width: 10cm

   Фрагмент цветовой схемы дорог общего пользования. 

.. code-block:: xml


    <map>
    <!-- Highways for low-zoom from openstreetmap (from motorway to residential) version 2015-11-06 -->
        <layer>
            <classitem>Highway</classitem>
            <labelitem>Name</labelitem>
            <class>
                <expression>"motorway"</expression>
                <style>
                    <color red="185" green="49" blue="49" />
                    <linejoin>round</linejoin>
                    <width>8</width>
                    <linecap>round</linecap>
                </style>
                <style>
                    <color red="226" green="114" blue="114" />
                    <linejoin>round</linejoin>
                    <width>4</width>
                    <linecap>round</linecap>
                </style>
                <style>
                    <color red="255" green="255" blue="255" />
                    <linejoin>round</linejoin>
                    <width>1</width>
                    <linecap>round</linecap>
                </style>
                <label>
                    <type>truetype</type>
                    <font>regular</font>
                    <size>7</size>
                    <color blue="0" green="0" red="0" />
                    <outlinewidth>1</outlinewidth>
                    <outlinecolor blue="255" green="255" red="255" />
                    <angle>follow</angle>
                    <antialias>true</antialias>
                    <repeatdistance>300</repeatdistance>
                    <maxoverlapangle>20.0</maxoverlapangle>
                </label>
            </class>
            <class>
                <expression>"motorway_link"</expression>
                <style>
                    <color red="185" green="49" blue="49" />
                    <linejoin>round</linejoin>
                    <width>8</width>
                    <linecap>round</linecap>
                </style>
                <style>
                    <color red="226" green="114" blue="114" />
                    <linejoin>round</linejoin>
                    <width>4</width>
                    <linecap>round</linecap>
                </style>
                <style>
                    <color red="255" green="255" blue="255" />
                    <linejoin>round</linejoin>
                    <width>1</width>
                    <linecap>round</linecap>
                </style>
            </class>
            <class>
                <expression>"trunk"</expression>
                <style>
                    <color red="185" green="49" blue="49" />
                    <linejoin>round</linejoin>
                    <width>8</width>
                    <linecap>round</linecap>
                </style>
                <style>
                    <color red="226" green="114" blue="114" />
                    <linejoin>round</linejoin>
                    <width>4</width>
                    <linecap>round</linecap>
                </style>
                <style>
                    <color red="255" green="255" blue="255" />
                    <linejoin>round</linejoin>
                    <width>1</width>
                    <linecap>round</linecap>
                </style>
                <label>
                    <type>truetype</type>
                    <font>regular</font>
                    <size>7</size>
                    <color blue="0" green="0" red="0" />
                    <outlinewidth>1</outlinewidth>
                    <outlinecolor blue="255" green="255" red="255" />
                    <angle>follow</angle>
                    <antialias>true</antialias>
                    <repeatdistance>300</repeatdistance>
                    <maxoverlapangle>20.0</maxoverlapangle>
                </label>
            </class>
            <class>
                <expression>"trunk_link"</expression>
                <style>
                    <color red="185" green="49" blue="49" />
                    <linejoin>round</linejoin>
                    <width>8</width>
                    <linecap>round</linecap>
                </style>
                <style>
                    <color red="226" green="114" blue="114" />
                    <linejoin>round</linejoin>
                    <width>4</width>
                    <linecap>round</linecap>
                </style>
                <style>
                    <color red="255" green="255" blue="255" />
                    <linejoin>round</linejoin>
                    <width>1</width>
                    <linecap>round</linecap>
                </style>
            </class>
            <class>
                <expression>"primary"</expression>
                <style>
                    <color red="141" green="67" blue="70" />
                    <linejoin>round</linejoin>
                    <width>6.4062992126</width>
                    <linecap>round</linecap>
                </style>
                <style>
                    <color red="226" green="114" blue="114" />
                    <linejoin>round</linejoin>
                    <width>3.57165354331</width>
                    <linecap>round</linecap>
                </style>
                <label>
                    <type>truetype</type>
                    <font>regular</font>
                    <size>7</size>
                    <color blue="0" green="0" red="0" />
                    <outlinewidth>1</outlinewidth>
                    <outlinecolor blue="255" green="255" red="255" />
                    <angle>follow</angle>
                    <antialias>true</antialias>
                    <repeatdistance>300</repeatdistance>
                    <maxoverlapangle>20.0</maxoverlapangle>
                </label>
            </class>
            <class>
                <expression>"primary_link"</expression>
                <style>
                    <color red="141" green="67" blue="70" />
                    <linejoin>round</linejoin>
                    <width>6.4062992126</width>
                    <linecap>round</linecap>
                </style>
                <style>
                    <color red="226" green="114" blue="114" />
                    <linejoin>round</linejoin>
                    <width>3.57165354331</width>
                    <linecap>round</linecap>
                </style>
            </class>
            <class>
                <expression>"secondary"</expression>
                <style>
                    <color red="163" green="123" blue="72" />
                    <linejoin>round</linejoin>
                    <width>4</width>
                    <linecap>round</linecap>
                </style>
                <style>
                    <color red="246" green="232" blue="86" />
                    <linejoin>round</linejoin>
                    <width>3</width>
                    <linecap>round</linecap>
                </style>
                <label>
                    <type>truetype</type>
                    <font>regular</font>
                    <size>7</size>
                    <color blue="0" green="0" red="0" />
                    <outlinewidth>1</outlinewidth>
                    <outlinecolor blue="255" green="255" red="255" />
                    <angle>follow</angle>
                    <antialias>true</antialias>
                    <repeatdistance>300</repeatdistance>
                    <maxoverlapangle>20.0</maxoverlapangle>
                </label>
            </class>
            <class>
                <expression>"secondary_link"</expression>
                <style>
                    <color red="163" green="123" blue="72" />
                    <linejoin>round</linejoin>
                    <width>4</width>
                    <linecap>round</linecap>
                </style>
                <style>
                    <color red="246" green="232" blue="86" />
                    <linejoin>round</linejoin>
                    <width>3</width>
                    <linecap>round</linecap>
                </style>
            </class>
            <class>
                <expression>"tertiary"</expression>
                <style>
                    <color red="187" green="187" blue="187" />
                    <linejoin>round</linejoin>
                    <width>4</width>
                    <linecap>round</linecap>
                </style>
                <style>
                    <color red="255" green="255" blue="179" />
                    <linejoin>round</linejoin>
                    <width>3</width>
                    <linecap>round</linecap>
                </style>
                <label>
                    <type>truetype</type>
                    <font>regular</font>
                    <size>7</size>
                    <color blue="0" green="0" red="0" />
                    <outlinewidth>1</outlinewidth>
                    <outlinecolor blue="255" green="255" red="255" />
                    <angle>follow</angle>
                    <antialias>true</antialias>
                    <repeatdistance>300</repeatdistance>
                    <maxoverlapangle>20.0</maxoverlapangle>
                </label>
            </class>
            <class>
                <expression>"tertiary_link"</expression>
                <style>
                    <color red="187" green="187" blue="187" />
                    <linejoin>round</linejoin>
                    <width>4</width>
                    <linecap>round</linecap>
                </style>
                <style>
                    <color red="255" green="255" blue="179" />
                    <linejoin>round</linejoin>
                    <width>3</width>
                    <linecap>round</linecap>
                </style>
            </class>
            <class>
                <expression>"unclassified"</expression>
                <style>
                    <color red="187" green="187" blue="187" />
                    <linejoin>round</linejoin>
                    <width>4</width>
                    <linecap>round</linecap>
                </style>
                <style>
                    <color red="255" green="255" blue="179" />
                    <linejoin>round</linejoin>
                    <width>3</width>
                    <linecap>round</linecap>
                </style>
                <label>
                    <type>truetype</type>
                    <font>regular</font>
                    <size>7</size>
                    <color blue="0" green="0" red="0" />
                    <outlinewidth>1</outlinewidth>
                    <outlinecolor blue="255" green="255" red="255" />
                    <angle>follow</angle>
                    <antialias>true</antialias>
                    <repeatdistance>300</repeatdistance>
                    <maxoverlapangle>20.0</maxoverlapangle>
                    <minscaledenom>1</minscaledenom>
		            <maxscaledenom>40000</maxscaledenom> 
                </label>
            </class>
            <class>
                <expression>"residential"</expression>
                <style>
                    <color red="187" green="187" blue="187" />
                    <linejoin>round</linejoin>
                    <width>2</width>
                    <linecap>round</linecap>
                </style>
                <style>
                    <color red="255" green="255" blue="179" />
                    <linejoin>round</linejoin>
                    <width>1</width>
                    <linecap>round</linecap>
                </style>
                <label>
                    <type>truetype</type>
                    <font>regular</font>
                    <size>7</size>
                    <color blue="0" green="0" red="0" />
                    <outlinewidth>1</outlinewidth>
                    <outlinecolor blue="255" green="255" red="255" />
                    <angle>follow</angle>
                    <antialias>true</antialias>
                    <repeatdistance>300</repeatdistance>
                    <maxoverlapangle>20.0</maxoverlapangle>
                    <minscaledenom>1</minscaledenom>
		            <maxscaledenom>40000</maxscaledenom> 
                </label>
            </class>
            <class>
                <expression>"living_street"</expression>
                <style>
                    <color red="187" green="187" blue="187" />
                    <linejoin>round</linejoin>
                    <width>2</width>
                    <linecap>round</linecap>
                </style>
                <style>
                    <color red="255" green="255" blue="179" />
                    <linejoin>round</linejoin>
                    <width>1</width>
                    <linecap>round</linecap>
                </style>
                <label>
                    <type>truetype</type>
                    <font>regular</font>
                    <size>7</size>
                    <color blue="0" green="0" red="0" />
                    <outlinewidth>1</outlinewidth>
                    <outlinecolor blue="255" green="255" red="255" />
                    <angle>follow</angle>
                    <antialias>true</antialias>
                    <repeatdistance>300</repeatdistance>
                    <maxoverlapangle>20.0</maxoverlapangle>
                    <minscaledenom>1</minscaledenom>
		            <maxscaledenom>40000</maxscaledenom> 
                </label>
            </class>
        </layer>
    </map>


OSM highway-maxzoom
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Дороги подъездные, технологические, грунтовые, пешеходные


.. figure:: _static/mastyles_osm-highway-highzoom.png
   :name: ngweb_mastyles_osm-highway-highzoom
   :align: center
   :width: 10cm

   Фрагмент изображения карты дорог.

.. code-block:: xml

    <map>
     <!-- Highways for high-zoom from openstreetmap (from service to track) version 2015-11-06 -->
        <layer>
            <classitem>Highway</classitem>
            <labelitem>Name</labelitem>
            <class>
                <expression>"service"</expression>
                <style>
                    <color red="187" green="187" blue="187" />
                    <linejoin>round</linejoin>
                    <width>2</width>
                    <linecap>round</linecap>
                </style>
                <style>
                    <color red="255" green="255" blue="255" />
                    <linejoin>round</linejoin>
                    <width>1</width>
                    <linecap>round</linecap>
                </style>
            </class>
            <class>
                <expression>"footway"</expression>
                <style>
                    <color red="255" green="0" blue="0" />
                    <linejoin>round</linejoin>
                    <width>1</width>
                    <linecap>round</linecap>
                </style>
                <label>
                    <type>truetype</type>
                    <font>regular</font>
                    <size>7</size>
                    <color blue="0" green="0" red="0" />
                    <outlinewidth>1</outlinewidth>
                    <outlinecolor blue="255" green="255" red="255" />
                    <angle>follow</angle>
                    <antialias>true</antialias>
                    <repeatdistance>300</repeatdistance>
                    <maxoverlapangle>20.0</maxoverlapangle>
                </label>
            </class>
            <class>
                <expression>"pedestrian"</expression>
                <style>
                    <color red="255" green="0" blue="0" />
                    <linejoin>round</linejoin>
                    <width>2</width>
                    <linecap>round</linecap>
                </style>
            </class>
            <class>
                <expression>"path"</expression>
                <style>
                    <color red="255" green="0" blue="0" />
                    <linejoin>round</linejoin>
                    <width>1</width>
                    <linecap>round</linecap>
                    <pattern>5 5</pattern>
                </style>
            </class>
            <class>
                <expression>"track"</expression>
                <style>
                    <color red="153" green="116" blue="43" />
                    <linejoin>round</linejoin>
                    <width>2</width>
                    <pattern>16 8</pattern>
                    <linecap>round</linecap>
                </style>
            </class>
        </layer>
    </map>

OSM railway-line
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: xml

	<!-- Стиль railway-line с разделением по масштабам 
	version 2015-07-24 -->
	<map>
	  <layer>
	    <classitem>RAILWAY</classitem>
	    <class>
	      <expression>"abandoned"</expression>
	      <style>
		<color red="255" green="255" blue="255"/>
		<linejoin>round</linejoin>
		<width>2.83464566929</width>
		<linecap>round</linecap>
	      </style>
	      <style>
		<pattern>2.35275590551 4.70551181102</pattern>
		<color red="165" green="165" blue="165"/>
		<linejoin>round</linejoin>
		<width>2.35275590551</width>
		<linecap>round</linecap>   
	      </style>
	    </class>
		<class>
	      <expression>"razed"</expression>
	      <style>
		<color red="255" green="255" blue="255"/>
		<linejoin>round</linejoin>
		<width>2.83464566929</width>
		<linecap>round</linecap>
	      </style>
	      <style>
		<pattern>2.35275590551 4.70551181102</pattern>
		<color red="255" green="165" blue="210"/>
		<linejoin>round</linejoin>
		<width>2.35275590551</width>
		<linecap>round</linecap>   
	      </style>
	    </class>
	    <class>
	      <expression>"construction"</expression>
	      <style>
		<color red="255" green="255" blue="255"/>
		<linejoin>round</linejoin>
		<width>2.83464566929</width>
		<linecap>round</linecap>     
	      </style>
	      <style>
		<pattern>2.35275590551 4.70551181102</pattern>
		<color red="255" green="0" blue="127"/>
		<linejoin>round</linejoin>
		<width>2.35275590551</width>
		<linecap>round</linecap>    
	      </style>
	    </class>
	    <class>
	      <expression>"crossing"</expression>
	      <style>
		<color red="37" green="37" blue="255"/>
		<linejoin>bevel</linejoin>
		<width>0.737007874016</width>
		<linecap>square</linecap>
	      </style>
	    </class>
	    <class>
	      <expression>"light_rail"</expression>
	      <style>
		<color red="0" green="0" blue="0"/>
		<linejoin>bevel</linejoin>
		<width>1.41732283465</width>
		<linecap>square</linecap>
	      </style>
	    </class>
	    <class>
	      <expression>"narrow_gauge"</expression>
	      <style>
		<color red="150" green="150" blue="150"/>
		<linejoin>bevel</linejoin>
		<width>1.41732283465</width>
		<linecap>square</linecap> 
	      </style>
	    </class>
	    <class>
	      <expression>"platform"</expression>
	      <style>
		<color red="0" green="0" blue="0"/>
		<linejoin>bevel</linejoin>
		<width>4.25196850394</width>
		<linecap>square</linecap>   
	      </style>
	    </class>
	    <class>
	      <expression>"rail"</expression>
	      <style>
		<color red="0" green="0" blue="0"/>
		<linejoin>bevel</linejoin>
		<width>2.83464566929</width>
		<linecap>square</linecap> 
		<maxscaledenom>25000</maxscaledenom> <!-- Чёрно-белая линия на крупном масштабе -->
	      </style>
	      <style>
		<pattern>9.41102362205 14.1165354331</pattern>
		<color red="255" green="255" blue="255"/>
		<linejoin>bevel</linejoin>
		<width>2.35275590551</width>
		<linecap>square</linecap>
		<maxscaledenom>25000</maxscaledenom> <!-- Чёрно-белая линия на крупном масштабе -->
	      </style>
	       <style>
		
		<color red="0" green="0" blue="0"/>
		<linejoin>bevel</linejoin>
		<width>2</width>
		<linecap>square</linecap>
		<minscaledenom>25000</minscaledenom> <!-- Чёрная линия на среднем масштабе -->
	      </style>
	    </class>
	    <class>
	      <expression>"siding"</expression>
	      <style>
		<color red="145" green="145" blue="145"/>
		<linejoin>bevel</linejoin>
		<width>1.41732283465</width>
		<linecap>square</linecap>  
	      </style>
	    </class>
	    <class>
	      <expression>"subway"</expression>
	      <style>
		<pattern>1.41732283465 2.83464566929</pattern>
		<color red="155" green="155" blue="155"/>
		<linejoin>round</linejoin>
		<width>1.41732283465</width>
		<linecap>round</linecap>
	      </style>
	    </class>
	    <class>
	      <expression>"tram"</expression>
	      <style>
		<color red="0" green="0" blue="0"/>
		<linejoin>bevel</linejoin>
		<width>1.41732283465</width>
		<linecap>square</linecap>
	      </style>
	    </class>
	  </layer>
	</map>


OSM water-line
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: xml

	<!-- Стиль water-line с разделением по масштабам-->
	<!-- Версия 2015-07-24 -->
	<map>
	  <layer>
	    <classitem>Waterway</classitem>
	    <labelitem>name</labelitem>
	    <class>
	      <expression>"river"</expression>
	      <style>
		<color red="102" green="153" blue="204"/>
		<linejoin>round</linejoin>
		<width>3</width>
		<linecap>round</linecap>
		<!-- Остались необработанные атрибуты: width_unit, offset_unit, customdash_unit -->
	      </style>
	      <label>
		<type>truetype</type> <!-- Подпись -->
		<font>bold</font>
		<size>7</size>
		<color blue="255" green="255" red="255"/>
		<outlinewidth>1</outlinewidth>
		<outlinecolor red="102" green="153" blue="204"/>
		<angle>auto</angle>
		<repeatdistance>300</repeatdistance>
		<maxoverlapangle>90.0</maxoverlapangle>
		<maxscaledenom>500000</maxscaledenom>
	      </label>
	      </class> 
	    
	      <class>
	      <expression>"canal"</expression>  
	      <style><!-- вертикальные линии -->
		<angle>auto</angle>
		<gap>-8.50393700787</gap>
		<!-- Остались необработанные атрибуты: interval_unit, placement, offset_unit, offset -->
		<color red="102" green="153" blue="204"/>
		<outlinecolor red="0" green="0" blue="0"/>
		<size>15.66929133858</size>
		<symbol>std:line</symbol>
		<!-- Остались необработанные атрибуты: outline_width, offset_unit, outline_width_unit, size_unit -->
	      </style>
	      <style>
		<color red="102" green="153" blue="204"/>
		<linejoin>round</linejoin>
		<width>3</width>
		<linecap>round</linecap>
		<!-- Остались необработанные атрибуты: width_unit, offset_unit, customdash_unit -->
	      </style>
	      <label>
		<type>truetype</type> <!-- Подпись -->
		<font>bold</font>
		<size>7</size>
		<color blue="255" green="255" red="255"/>
		<outlinewidth>1</outlinewidth>
		<outlinecolor red="102" green="153" blue="204"/>
		<angle>auto</angle>
		<repeatdistance>300</repeatdistance>
		<maxoverlapangle>90.0</maxoverlapangle>
		<maxscaledenom>500000</maxscaledenom>
	      </label>
	      </class> 
	    
	      <class>
	      <expression>"stream"</expression>
	      <style>
		<color red="102" green="153" blue="204"/>
		<linejoin>round</linejoin>
		<width>1.5</width>
		<linecap>round</linecap>
		<maxscaledenom>250000</maxscaledenom>
		<!-- Остались необработанные атрибуты: width_unit, offset_unit, customdash_unit -->
	      </style>
	      </class> 
	    
	      <class>
	      <expression>"drain"</expression>
	      <style>
		<color red="102" green="153" blue="204"/>
		<linejoin>round</linejoin>
		<width>1</width>
		<linecap>round</linecap>
		<maxscaledenom>250000</maxscaledenom>
		<!-- Остались необработанные атрибуты: width_unit, offset_unit, customdash_unit -->
	      </style>
	      </class> 
	  </layer>
	</map>

OSM water-polygon
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: xml

	<!-- стиль water-polygon
	Версия 2015-07-24 
	Нужно добавить 
	-водохранилища
	-штриховку для болот
	-->
	<map>
	  <layer>
	    <labelitem>NAME</labelitem>
	    <classitem>NATURAL</classitem>
	    <class>
	      <expression>"water"</expression> <!-- Вода -->
	      <style>
		<color red="102" green="153" blue="204"/>
		<outlinecolor red="102" green="153" blue="204"/>
	      </style>
		 <label>
		<type>truetype</type>
		<font>regular</font>
		<size>7</size>
		<color red="102" green="153" blue="204"/>
		<outlinewidth>2</outlinewidth>
		<outlinecolor red="255" green="255" blue="222"/>
		<!-- Ограничение подписи по масштабу -->
		<minscaledenom>1</minscaledenom>
		<maxscaledenom>100000</maxscaledenom>    
	      </label>
	    </class>
	    <class>
	      <expression>"wetland"</expression> <!-- Болото -->
		  <style>
		<color red="102" green="153" blue="204"/>
		<outlinecolor red="102" green="153" blue="204"/>
	      </style>
		 <label>
		<type>truetype</type>
		<font>regular</font>
		<size>7</size>
		<color red="102" green="153" blue="204"/>
		<outlinewidth>2</outlinewidth>
		<outlinecolor red="255" green="255" blue="222"/>
		<!-- Ограничение подписи по масштабу -->
		<minscaledenom>1</minscaledenom>
		<maxscaledenom>100000</maxscaledenom>    
	      </label>
	    </class>
	  </layer>
	</map>


Стиль OSM-dark
----------------------------------

OSM landuse-polygon
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Стили NextGIS Web поддерживают различные штриховки (см. :numref:`ngweb_mapstyle_hatch_demo_pic`).

.. code-block:: xml


	<map> <!-- Демонстрация штриховок, предполагается что под этим слоем будет чёрный фон-->
	    <layer>
		<labelitem>OSM_ID</labelitem>
		<classitem>LANDUSE</classitem>
		<class>
		    <expression>"residential"</expression>
		    <!-- Жилые зоны -->
		    <style>
		        <!-- штриховка направо -->
		        <color red="255" green="185" blue="33"/>
		        <width>1.4</width>
		        <symbol>std:line</symbol>
		        <gap>3</gap>
		        <size>1</size>
		        <angle>90</angle>
		    </style>
		    <style>
		        <!-- Обводка -->
		        <outlinecolor red="255" green="185" blue="33"/>
		        <width>0.5</width>
		    </style>
		</class>
		<class>
		    <expression>"grass"</expression>
		    <!-- Газоны зоны -->
		    <style>
		        <!-- Линии -->
		        <color red="20" green="255" blue="33"/>
		        <width>1</width>
		        <symbol>std:line</symbol>
		        <gap>6</gap>
		        <size>4</size>
		        <angle>0</angle>
		        <pattern>2.5 4.5</pattern>
		    </style>
		    <style>
		        <!-- Обводка -->
		        <outlinecolor red="20" green="255" blue="33"/>
		        <width>0.5</width>
		    </style>
		</class>
		<class>
		    <expression>"commercial"</expression>
		    <!-- Жилые зоны -->
		    <style>
		        <!-- штриховка направо -->
		        <color red="133" green="33" blue="25"/>
		        <width>1.4</width>
		        <symbol>std:line</symbol>
		        <gap>10</gap>
		        <size>5</size>
		        <angle>45</angle>
		    </style>
		    <style>
		        <!-- Обводка -->
		        <outlinecolor red="133" green="33" blue="25"/>
		        <width>0.5</width>
		    </style>
		</class>
		<class>
		    <expression>"industrial"</expression>
		    <!-- Промзоны -->
		    <style>
		        <!-- штриховка направо -->
		        <color red="255" green="50" blue="50"/>
		        <width>0.4</width>
		        <symbol>std:hatch</symbol>
		        <gap>10</gap>
		        <size>5</size>
		        <angle>45</angle>
		    </style>
		    <style>
		        <!-- штриховка налево-->
		        <color red="255" green="50" blue="50"/>
		        <width>0.4</width>
		        <symbol>std:hatch</symbol>
		        <gap>10</gap>
		        <size>5</size>
		        <angle>-45</angle>
		    </style>
		    <style>
		        <!-- Обводка -->
		        <outlinecolor red="255" green="50" blue="50"/>
		        <width>0.5</width>
		    </style>
		</class>
		<class>
		    <expression>"cemetery"</expression>
		    <!-- Кладбоны -->
		    <style>
		        <!-- оградки -->
		        <color red="14" green="166" blue="0"/>
		        <width>1.4</width>
		        <symbol>std:rectangle</symbol>
		        <gap>20</gap>
		        <size>11</size>
		        <angle>0</angle>
		    </style>
		    <style>
		        <!-- оградки -->
		        <color red="0" green="0" blue="0"/>
		        <width>1.2</width>
		        <symbol>std:rectangle</symbol>
		        <gap>20</gap>
		        <size>10</size>
		        <angle>0</angle>
		    </style>
		    <style>
		        <!-- кресты -->
		        <color red="14" green="166" blue="0"/>
		        <width>1.4</width>
		        <symbol>std:cross</symbol>
		        <gap>20</gap>
		        <size>9</size>
		        <angle>0</angle>
		    </style>
		    <style>
		        <!-- Обводка -->
		        <outlinecolor red="14" green="166" blue="0"/>
		        <width>0.5</width>
		    </style>
		</class>
	    </layer>
	</map>
