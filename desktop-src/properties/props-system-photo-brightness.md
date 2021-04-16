---
description: O valor de brilho da imagem, em unidades de APEX, geralmente no intervalo de-99,99 a 99,99.
ms.assetid: 533f6934-dec8-455a-937c-d4e144be4335
title: System. Photo. Brightness
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 131b7e2d51f402aa8da4d5e9b266fe1fc1b39b29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772582"
---
# <a name="systemphotobrightness"></a>System. Photo. Brightness

O valor de brilho da imagem, em unidades de APEX, geralmente no intervalo de-99,99 a 99,99.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Photo.Brightness
   shellPKey = PKEY_Photo_Brightness
   formatID = 1A701BF6-478C-4361-83AB-3701BB053C58
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a>Comentários

Os valores de PKEY são definidos em Propkey. h.

Consulte a especificação EXIF 2,2, anexo C, para obter uma comparação de números de [System. Photo. Brightness]() e Foot-Lambert medidas. Essa propriedade é calculada de [System. Photo. BrightnessNumerator](./props-system-photo-brightnessnumerator.md) e [System. Photo. BrightnessDenominator](./props-system-photo-brightnessdenominator.md). Se o numerador do valor registrado for FFFFFFFF. H, "desconhecido" deve ser indicado.

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

 

 
