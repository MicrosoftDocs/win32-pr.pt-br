---
description: O colorspace inserido na imagem. Extraído das informações do arquivo de imagem intercambiável (EXIF).
ms.assetid: 2375e132-e400-419f-a0f9-cbb6f9acdf45
title: System. Image. ColorSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024d99e0f88fd793d0a0f8207b43a52c7be47c30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797628"
---
# <a name="systemimagecolorspace"></a>System. Image. ColorSpace

O colorspace inserido na imagem. Extraído das informações do arquivo de imagem intercambiável (EXIF).

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Image.ColorSpace
   shellPKey = PKEY_Image_ColorSpace
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 40961
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt16
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = SRGB
            value = 1
            text = sRGB
            defineToken = IMAGE_COLORSPACE_SRGB
         enum
            name = Uncalibrated
            value = 0xFFFF
            text = Uncalibrated
            defineToken = IMAGE_COLORSPACE_UNCALIBRATED
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Image.ColorSpace
   shellPKey = PKEY_Image_ColorSpace
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 40961
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt16
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 1
            text = sRGB
            defineName = IMAGE_COLORSPACE_SRGB
         enum
            value = 0xFFFF
            text = Uncalibrated
            defineName = IMAGE_COLORSPACE_UNCALIBRATED
```

## <a name="remarks"></a>Comentários

Os valores de PKEY são definidos em Propkey. h.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato de arquivo de imagem intercambiável para câmeras digitais ainda: Exif versão 2,2](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[stringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[numberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
