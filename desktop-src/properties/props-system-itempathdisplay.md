---
description: Leia sobre a propriedade System. ItemPathDisplay, que representa o caminho de exibição amigável para o item.
ms.assetid: 27e4490b-7914-4b38-9799-e9d5dc407f13
title: System. ItemPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ddad0edbc1a77a3de1fab7956d8ce6e6f906f06
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403899"
---
# <a name="systemitempathdisplay"></a>System. ItemPathDisplay

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

Os valores de PKEY são definidos em Propkey. h.

Se o item for um arquivo ou uma pasta, essa propriedade incluirá a extensão em todos os casos e será localizada se um nome localizado estiver disponível. Para outros itens, esse é o equivalente amigável, supondo que o item exista no armazenamento hierárquico.

Ao contrário de [System. ItemUrl](./props-system-itemurl.md), esse valor de propriedade não inclui o esquema de URL. Para analisar um caminho de item, use System. ItemUrl ou [System. ParsingPath](./props-system-parsingpath.md). Para referenciar itens de namespace do shell usando APIs do Shell, use System. ParsingPath.

Valores de exemplo:



| Caminho                                   | ItemPathDisplay                        |
|----------------------------------------|----------------------------------------|
| c: \\ barra de mydir \\ \\hello.txt              | c: \\ barra de mydir \\ \\hello.txt              |
| \\\\mydir de compartilhamento de servidor \\ \\ \\goodnews.doc | \\\\mydir de compartilhamento de servidor \\ \\ \\goodnews.doc |
| \\\\\\numbers.xls de compartilhamento do servidor \\         | \\\\\\numbers.xls de compartilhamento do servidor \\         |
| c: \\ mydir \\ MyFolder                    | c: \\ mydir \\ MyFolder                    |
| /Mailbox conta/caixa de entrada/' re: Olá! '    | /Mailbox conta/caixa de entrada/' re: Olá! '    |



 

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

 

 
