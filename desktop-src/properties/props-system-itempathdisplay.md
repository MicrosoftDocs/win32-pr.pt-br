---
description: Leia sobre a propriedade System.ItemPathDisplay, que representa o caminho de exibição amigável para o item.
ms.assetid: 27e4490b-7914-4b38-9799-e9d5dc407f13
title: System.ItemPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88a58d48740c6f7a2f9db0e496a951105c176ca7eba3dd205c2971188af7fd55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118231659"
---
# <a name="systemitempathdisplay"></a>System.ItemPathDisplay

O caminho de exibição amigável para o item.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemPathDisplay
   shellPKey = PKEY_ItemPathDisplay
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 7
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Comentários

Os valores PKEY são definidos em Propkey.h.

Se o item for um arquivo ou pasta, essa propriedade incluirá a extensão em todos os casos e será localizada se um nome localizado estiver disponível. Para outros itens, esse é o equivalente amigável, supondo que o item exista no armazenamento hierárquico.

Ao [contrário de System.ItemUrl,](./props-system-itemurl.md)esse valor da propriedade não inclui o esquema de URL. Para analisar um caminho de item, use System.ItemUrl ou [System.ParsingPath.](./props-system-parsingpath.md) Para referenciar itens de namespace do Shell usando APIs do Shell, use System.ParsingPath.

Valores de exemplo:



| Caminho                                   | ItemPathDisplay                        |
|----------------------------------------|----------------------------------------|
| c: \\ mydir \\ bar \\hello.txt              | c: \\ mydir \\ bar \\hello.txt              |
| \\\\server \\ share \\ mydir \\goodnews.doc | \\\\server \\ share \\ mydir \\goodnews.doc |
| \\\\server \\ share \\numbers.xls         | \\\\server \\ share \\numbers.xls         |
| c: \\ mydir \\ MyFolder                    | c: \\ mydir \\ MyFolder                    |
| /Mailbox Account/Inbox/'Re: Hello!'    | /Mailbox Account/Inbox/'Re: Hello!'    |



 

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

 

 
