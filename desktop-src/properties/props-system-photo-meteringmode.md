---
description: O modo de medição usado pela câmera, retirado das informações do EXIF (Exchangeable Image File).
ms.assetid: 9dd031a8-f1fa-4753-a86b-18051c624a00
title: System.Photo.MeteringMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd6eb62320e8561e9c486ad34816647ac9176912d49200c56409913f4efa8e19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118228126"
---
# <a name="systemphotometeringmode"></a>System.Photo.MeteringMode

O modo de medição usado pela câmera, retirado das informações do EXIF (Exchangeable Image File).

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Photo.MeteringMode
   shellPKey = PKEY_Photo_MeteringMode
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37383
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Unknown
            value = 0
            text = Unknown
            defineToken = PHOTO_METERINGMODE_UNKNOWN
         enum
            name = Average
            value = 1
            text = Average
            defineToken = PHOTO_METERINGMODE_AVERAGE
         enum
            name = Center
            value = 2
            text = Center Weighted Average
            defineToken = PHOTO_METERINGMODE_CENTER
         enum
            name = Spot
            value = 3
            text = Spot
            defineToken = PHOTO_METERINGMODE_SPOT
         enum
            name = MultiSpot
            value = 4
            text = Multi Spot
            defineToken = PHOTO_METERINGMODE_MULTISPOT
         enum
            name = Pattern
            value = 5
            text = Pattern
            defineToken = PHOTO_METERINGMODE_PATTERN
         enum
            name = Partial
            value = 6
            text = Partial
            defineToken = PHOTO_METERINGMODE_PARTIAL
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Photo.MeteringMode
   shellPKey = PKEY_Photo_MeteringMode
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37383
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Unknown
            defineName = PHOTO_METERINGMODE_UNKNOWN
         enum
            value = 1
            text = Average
            defineName = PHOTO_METERINGMODE_AVERAGE
         enum
            value = 2
            text = Center Weighted Average
            defineName = PHOTO_METERINGMODE_CENTER
         enum
            value = 3
            text = Spot
            defineName = PHOTO_METERINGMODE_SPOT
         enum
            value = 4
            text = Multi Spot
            defineName = PHOTO_METERINGMODE_MULTISPOT
         enum
            value = 5
            text = Pattern
            defineName = PHOTO_METERINGMODE_PATTERN
         enum
            value = 6
            text = Partial
            defineName = PHOTO_METERINGMODE_PARTIAL
```

## <a name="remarks"></a>Comentários

Os valores PKEY são definidos em Propkey.h.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato de arquivo de imagem que pode ser trocado para câmeras ainda digitais: exif versão 2.2](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[Propertydescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[Typeinfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[Stringformat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[Numberformat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[Filtercontrol](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
