---
description: Representa uma URL bem formada que aponta para o item.
ms.assetid: d592f12b-f8c2-406f-a031-eeb8212e64f7
title: System.ItemUrl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79fe179849c7991a65db5412543815d78ac8dc21682511e27d6251253b3b1366
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118970365"
---
# <a name="systemitemurl"></a>System.ItemUrl

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

Os valores PKEY são definidos em Propkey.h.

Para referenciar itens de namespace do Shell por meio de APIs do Shell, use [System.ParsingPath](./props-system-parsingpath.md).

Valores de exemplo:



| Tipo de item | Exemplo                        |
|-----------|--------------------------------|
| Arquivo      | file:///c:/mydir/bar/hello.txt |
| Arquivo      | csc://{GUID}/...               |
| Mensagem   | mapi://...                     |



 

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

 

 
