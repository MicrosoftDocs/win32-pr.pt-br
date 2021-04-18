---
description: Representa uma URL bem formada que aponta para o item.
ms.assetid: d592f12b-f8c2-406f-a031-eeb8212e64f7
title: System. ItemUrl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02beb9629661a052d2ec1fae7c7a34e999e777e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813653"
---
# <a name="systemitemurl"></a>System. ItemUrl

Representa uma URL bem formada que aponta para o item.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemUrl
   shellPKey = PKEY_ItemUrl
   formatID = 49691C90-7E17-101A-A91C-08002B2ECDA9
   propID = 9
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Comentários

Os valores de PKEY são definidos em Propkey. h.

Para referenciar itens de namespace do Shell por meio de APIs do Shell, use [System. ParsingPath](./props-system-parsingpath.md).

Valores de exemplo:



| Tipo de item | Exemplo                        |
|-----------|--------------------------------|
| Arquivo      | hello.txt file:///c:/mydir/bar/ |
| Arquivo      | CSC://{GUID}/...               |
| Mensagem   | mapi://...                     |



 

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

 

 
