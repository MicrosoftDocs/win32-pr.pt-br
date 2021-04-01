---
description: O nome de base da propriedade System. ItemNameDisplay.
ms.assetid: 8add2d72-efd3-4971-89d9-428190115ba0
title: System. ItemName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab5ba987d8bdcd966724c15f0632edbfc8eb3d9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921571"
---
# <a name="systemitemname"></a>System. ItemName

O nome de base da propriedade [System. ItemNameDisplay](./props-system-itemnamedisplay.md) .

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemName
   shellPKey = PKEY_ItemName
   formatID = 6B8DA074-3B5C-43BC-886F-0A2CDCE00B6F
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Comentários

Os valores de PKEY são definidos em Propkey. h.

Se o item for um arquivo, essa propriedade incluirá a extensão em todos os casos e será localizada se um nome localizado estiver disponível. Se o item for uma mensagem, o valor dessa propriedade não incluirá os prefixos de encaminhamento ou de resposta. Consulte [System. ItemNamePrefix](./props-system-itemnameprefix.md) para obter mais informações.

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

 

 
