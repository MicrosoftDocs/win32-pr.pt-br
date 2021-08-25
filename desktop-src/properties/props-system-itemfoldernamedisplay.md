---
description: O nome de exibição amigável da pasta pai de um item.
ms.assetid: 4049b6cb-41a1-4df6-89d1-a2022d3a285d
title: System.ItemFolderNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c8e8ca12af7c7665a2fd4b64f2911a1e6dbc99805cf4355ea1bb1ceec764c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119945166"
---
# <a name="systemitemfoldernamedisplay"></a>System.ItemFolderNameDisplay

O nome de exibição amigável da pasta pai de um item.

Isso é derivado de [System.ItemFolderPathDisplay.](./props-system-itemfolderpathdisplay.md) Se essa propriedade for VT \_ EMPTY, essa propriedade também deverá ser.

Se a pasta for uma pasta de arquivo, o valor será localizado se um nome localizado estiver disponível.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemFolderNameDisplay
   shellPKey = PKEY_ItemFolderNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 2
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Comentários

Os valores PKEY são definidos em Propkey.h.

Se [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) for VT \_ EMPTY, essa propriedade também deverá estar vazia. Caso contrário, ele deverá ser derivado adequadamente pela fonte de dados de System.ItemFolderPathDisplay.

Exemplos:



| Caminho determinado                             | Nome de exibição da pasta |
|----------------------------------------|---------------------|
| c: \\ MyFiles \\ Text \\hello.txt           | Texto                |
| \\\\server \\ share \\ mydir \\goodnews.doc | Mydir               |
| \\\\server \\ share \\numbers.xls         | compartilhar               |
| c: \\ Pastas \\ MyFolder                  | Pastas             |
| /Mailbox Account/Inbox/'Re: Hello!'    | Caixa de Entrada               |



 

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

 

 
