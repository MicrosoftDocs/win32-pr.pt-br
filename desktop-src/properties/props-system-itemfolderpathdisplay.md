---
description: O caminho de exibição amigável para o usuário da pasta pai de um item.
ms.assetid: 16f67edc-ca8a-4c2e-9d9b-be8600446e51
title: System. ItemFolderPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c4ae4c9178356d36c644f1bc886d63331155e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765114"
---
# <a name="systemitemfolderpathdisplay"></a>System. ItemFolderPathDisplay

O caminho de exibição amigável para o usuário da pasta pai de um item.

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

Os valores de PKEY são definidos em Propkey. h.

Se [System. ItemPathDisplay](./props-system-itempathdisplay.md) for VT \_ Empty, essa propriedade também deverá estar vazia. Caso contrário, ele deve ser derivado adequadamente pela fonte de dados de System. ItemPathDisplay.

Valores de exemplo:



| Caminho                                   | ItemFolderPathDisplay    |
|----------------------------------------|--------------------------|
| c: \\ arquivos \\ \\hello.txt pessoais         | c: \\ arquivos \\ pessoais      |
| \\\\mydir de compartilhamento de servidor \\ \\ \\goodnews.doc | \\\\\\mydir de compartilhamento de servidor \\ |
| \\\\\\numbers.xls de compartilhamento do servidor \\         | \\\\compartilhamento de servidor \\        |
| c: \\ comida na minha \\ pasta                     | c: \\ comida                 |
| /Mailbox conta/caixa de entrada/' re: Olá! '    | Conta de/Mailbox/caixa de entrada   |



 

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

 

 
