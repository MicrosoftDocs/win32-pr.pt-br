---
description: Leia sobre a propriedade System.ItemFolderPathDisplay, que representa o caminho de exibição amigável da pasta pai de um item.
ms.assetid: 16f67edc-ca8a-4c2e-9d9b-be8600446e51
title: System.ItemFolderPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8fd2288f12073fe8e36707bf49aca2bc5e000d0bbe25d95fba0736b4e77af44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822336"
---
# <a name="systemitemfolderpathdisplay"></a>System.ItemFolderPathDisplay

O caminho de exibição amigável da pasta pai de um item.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemFolderPathDisplay
   shellPKey = PKEY_ItemFolderPathDisplay
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 6
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Comentários

Os valores PKEY são definidos em Propkey.h.

Se [System.ItemPathDisplay](./props-system-itempathdisplay.md) for VT \_ EMPTY, essa propriedade também deverá estar vazia. Caso contrário, ele deverá ser derivado adequadamente pela fonte de dados de System.ItemPathDisplay.

Valores de exemplo:



| Caminho                                   | ItemFolderPathDisplay    |
|----------------------------------------|--------------------------|
| c: \\ arquivos \\ pessoais \\hello.txt         | c: \\ arquivos \\ pessoais      |
| \\\\server \\ share \\ mydir \\goodnews.doc | \\\\server \\ share \\ mydir |
| \\\\server \\ share \\numbers.xls         | \\\\compartilhamento \\ de servidor        |
| c: \\ food \\ MyFolder                     | c: \\ alimentos                 |
| /Mailbox Account/Inbox/'Re: Hello!'    | /Caixa de correio/conta   |



 

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

 

 
