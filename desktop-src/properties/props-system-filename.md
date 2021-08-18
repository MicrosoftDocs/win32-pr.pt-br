---
description: O nome do arquivo, incluindo sua extensão.
ms.assetid: 40940026-6c67-4196-aff6-5f846dc94f27
title: System.FileName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff8a92febe0a4f2dfe8cc9d5741118fdb76bcb56c7bcd1ef5c3d881e8c0f9abf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119096915"
---
# <a name="systemfilename"></a>System.FileName

O nome do arquivo, incluindo sua extensão. System.FileExtension é derivado dessa propriedade.

É possível que o item não exista em um sistema de arquivos (ou seja, ele pode não ser aberto usando CreateFile). No entanto, se o item for representado como um arquivo e seu nome seguir a sintaxe padrão de nomeação de arquivo Win32, a fonte de dados deverá emitir essa propriedade. Se o item não for um arquivo, a fonte de dados deverá emitir essa propriedade como VT \_ EMPTY.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.FileName
   shellPKey = PKEY_FileName
   formatID = 41CF5AE0-F75A-4806-BD87-59C7D9248EB9
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.FileName
   shellPKey = PKEY_FileName
   formatID = 41CF5AE0-F75A-4806-BD87-59C7D9248EB9
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            setValue = 0
            text = 0-9
         enumRange
            minValue = A
            setValue = A
            text = A-H
         enumRange
            minValue = I
            setValue = I
            text = I-P
         enumRange
            minValue = Q
            setValue = Q
            text = Q-Z
```

## <a name="remarks"></a>Comentários

Os valores PKEY são definidos em Propkey.h.

O item pode não existir em um sistema de arquivos (ou seja, ele pode não ser aberto usando CreateFile), mas se o item for representado como um arquivo do sentido lógico e seu nome seguir a sintaxe padrão de nomenminação de arquivo Win32, a fonte de dados deverá emitir essa propriedade. Se um item não for um arquivo, o valor dessa propriedade será VT \_ EMPTY. Consulte System.ItemNameDisplay. Isso tem o mesmo valor que System.ParsingName para itens fornecidos pela pasta de arquivos do Shell.

A tabela a seguir lista exemplos de valores de propriedade path e filename:



| Caminho                               | Valor da propriedade |
|------------------------------------|----------------|
| c: \\ arquivos \\ pessoais \\hello.txt     | olá.txt      |
| \\\\server \\ share \\ mydir \\news.doc | news.doc       |
| \\\\server \\ share \\numbers.xls     | numbers.xls    |
| c: \\ Stuff \\ MyFolder                | Myfolder       |
| \[mensagem de email\]                  | VT \_ VAZIO      |
| \[song.wma no dispositivo portátil\]    | song.wma       |



 

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

 

 
