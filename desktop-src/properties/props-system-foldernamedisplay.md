---
description: Essa propriedade é semelhante a System. ItemNameDisplay, exceto que só é definida para pastas, para arquivos que estará vazia.
ms.assetid: 4517a4bf-3cc1-4835-b21b-03de5b33db0c
title: System. FolderNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7b6f7d22eb7f835510b8ebe7cfe3ede01fcdea4a1cf86207e7733602b9b0ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033554"
---
# <a name="systemfoldernamedisplay"></a>System. FolderNameDisplay

Essa propriedade é semelhante a System. ItemNameDisplay, exceto que só é definida para pastas, para arquivos que estará vazia. Isso é útil para separar arquivos e pastas usando isso como a primeira chave de classificação. Quando System. MyDate é usado como uma segunda chave de classificação, ele produz resultados com pastas primeiro ordenadas por nome e, em seguida, os arquivos ordenados por data.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1

```
propertyDescription
   name = System.FolderNameDisplay
   shellPKey = PKEY_FolderNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 25
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
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

 

 
