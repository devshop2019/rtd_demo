KXN hướng dẫn
====================================

:term:`kxn_glossary`
:term:`Hshop.vn`

Text Format
------------

* Đây là một đoạn văn bản bình thường. Chỉ viết ra cho dài để có nội dung hướng dẫn về một số kiểu như:
    #. *in nghiêng* 
    #. **in đậm**
    #. ``nhấn mạnh``.

* Đây là đoạn văn bản số hai. Cũng chỉ để:
    * ``hiển thị``.
    * test ``pulleted``:
        * Dòng 1
        * Dòng 2
    * Test ``numbered``:
        #. Num 1.
        #. Num 2.
        #. Num 3.
        #. Num 4.

Tạo lưu ý
----------

.. caution::
    Cảnh bảo điều gì đó!

.. danger::
    Nguy hiểm

.. tip::
    Gợi ý

code mẫu note::

    .. note::
        * Ghi chú 1
        * Ghi chú 2
        * Ghi chú 3
        * Ghi chú 4

    
.. note::
    * Ghi chú 1
    * Ghi chú 2
    * Ghi chú 3
    * Ghi chú 4

Một đoạn văn bản bên ngoài note.

Image
------

* Hình cùng folder kxnguideline với file *kxn_HuongDan.rst*:
     ``.. image:: imageSameFolder.png``

    .. image:: imageSameFolder.png

* Hình khác folder với file *kxn_HuongDan.rst*: 
    ``.. image:: /Guidelines/imageOutside1folder.png``

    .. image:: /Guidelines/imageOutside1folder.png

* Hình ở folder images ngoài cùng: 
    ``.. image:: /images/imageInsideImageCore1.png``

    .. image:: /images/imageInsideImageCore1.png

* Hình nằm trong thư mục đồng cấp với file *kxn_HuongDan.rst*:
    ``.. image:: kxnguideline_images/kxnguideline_images_1.png``

    .. image:: kxnguideline_images/kxnguideline_images_1.png

* Hình nằm trong thư mục đồng cấp với file *kxn_HuongDan.rst* fix width::

    .. image:: kxnguideline_images/kxnguideline_images_1.png
        :width: 200px
        :scale: 50 %
        :alt: alternate name image
        :align: left


.. image:: kxnguideline_images/kxnguideline_images_1.png
    :width: 200px
    :align: center

Chữ sẽ nằm bên hong phải của hình.


.. figure:: kxnguideline_images/kxnguideline_images_1.png
    :width: 80%
    :align: center
    :alt: Most searched terms

    Most searched





haha
~~~~~

* Hình nằm trong thư mục đồng cấp với file *kxn_HuongDan.rst* fix scale::

    .. image:: kxnguideline_images/kxnguideline_images_1.png``
        :scale: 50 %
        :alt: alternate name image
        :align: center


.. image:: kxnguideline_images/kxnguideline_images_1.png
    :scale: 50 %
    :alt: alternate name image
    :align: center


Hiberlink:
------------

Code chèn link `hshop <https://documatt.com/restructuredtext-reference/element/code-block.html>`_::

    `hshop <https://documatt.com/restructuredtext-reference/element/code-block.html>`_




Code mẫu:
----------

Đây là code Arduino:

.. code-block:: cpp

    void setup(){
        Serial.begin(9600);
    }

.. tip::
    Tham khảo thêm `tại đây <https://documatt.com/restructuredtext-reference/element/code-block.html>`_

    Code example::

        .. code-block:: cpp

            void setup(){
                Serial.begin(9600);
            }



Hiển thị nội dung của một file .rst khác sang kxn_HuongDan.rst
----------------------------------------------------------------

.. include:: /template/kxn_template.rst


