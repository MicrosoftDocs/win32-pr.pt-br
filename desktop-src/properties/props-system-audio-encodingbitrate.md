---
description: Indica a taxa média de dados em Hertz (Hz) para o arquivo de áudio em bits por segundo.
ms.assetid: 570711c2-ef9b-4b3a-9b5f-94a6601fa3d4
title: System.Audio.EncodingBitrate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce2aa4f560ee0efc63838f11be2a66370f06c06e3f7b1f34c9af736d4e350d32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118232891"
---
# <a name="systemaudioencodingbitrate"></a>System.Audio.EncodingBitrate

Indica a taxa média de dados em Hertz (Hz) para o arquivo de áudio em bits por segundo.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Audio.EncodingBitrate
   shellPKey = PKEY_Audio_EncodingBitrate
   formatID = 64440490-4C8B-11D1-8B70-080036B11A03
   propID = 4
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = AMBroadcast
            minValue = 0
            setValue = 0
            text = Voice and AM Broadcast (0 - 32 Kbps)
            defineToken = ENCODINGBITRATE_AM_BROADCAST
         enumRange
            name = FMBroadcast
            minValue = 32769
            setValue = 32769
            text = FM Broadcast (32 - 64 Kbps)
            defineToken = ENCODINGBITRATE_FM_BROADCAST
         enumRange
            name = HighQuality
            minValue = 65537
            setValue = 65537
            text = High Quality (64 - 128 Kbps)
            defineToken = ENCODINGBITRATE_HIGH_QUALITY
         enumRange
            name = NearCDQuality
            minValue = 131073
            setValue = 131073
            text = Near CD Quality (over 128 Kbps)
            defineToken = ENCODINGBITRATE_NEAR_CD_QUALITY
         enumRange
            name
            minValue = 4294967295
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Audio.EncodingBitrate
   shellPKey = PKEY_Audio_EncodingBitrate
   formatID = 64440490-4C8B-11D1-8B70-080036B11A03
   propID = 4
   SearchInfo
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            setValue = 0
            text = Voice and AM Broadcast (0 - 32 Kbps)
         enumRange
            minValue = 32769
            setValue = 32769
            text = FM Broadcast (32 - 64 Kbps)
         enumRange
            minValue = 65537
            setValue = 65537
            text = High Quality (64 - 128 Kbps)
         enumRange
            minValue = 131073
            setValue = 131073
            text = Near CD Quality (over 128 Kbps)
         enumRange
            minValue = 4294967295
```

## <a name="remarks"></a>Comentários

Os valores PKEY são definidos em Propkey.h.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

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

 

 
