---
description: Intensidade do sinal do dispositivo.
ms.assetid: 662d39a6-f2f5-4556-a6de-bbcc655b4adb
title: System. Devices. SignalStrength
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901179dcf142f03ffceea14778f2763f73f16276
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748473"
---
# <a name="systemdevicessignalstrength"></a>System. Devices. SignalStrength

Intensidade do sinal do dispositivo.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Devices.SignalStrength
   shellPKey = PKEY_Devices_SignalStrength
   formatID = 49CD1F76-5626-4B17-A4E8-18B4AA1A2213
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Byte
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = None
            value = 0
            text = No signal
            defineToken = SIGNALSTRENGTH_NONE
         enum
            name = Weak
            value = 1
            text = Weak signal
            defineToken = SIGNALSTRENGTH_WEAK
         enum
            name = Average
            value = 2
            text = Average signal
            defineToken = SIGNALSTRENGTH_AVERAGE
         enum
            name = Strong
            value = 3
            text = Strong signal
            defineToken = SIGNALSTRENGTH_STRONG
         enum
            name = Excellent
            value = 4
            text = Excellent signal
            defineToken = SIGNALSTRENGTH_EXCELLENT
```

## <a name="remarks"></a>Comentários

Os valores de PKEY são definidos em Propkey. h.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

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

 

 
