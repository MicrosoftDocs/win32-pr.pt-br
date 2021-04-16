---
description: O nome do arquivo, incluindo sua extensão.
ms.assetid: 40940026-6c67-4196-aff6-5f846dc94f27
title: System. FileName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8f535eff4625178b3c32a04ea6d325505266a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779329"
---
# <a name="systemfilename"></a>System. FileName

O nome do arquivo, incluindo sua extensão. System. FileExtension é derivado dessa propriedade.

É possível que o item não exista em um sistema de arquivos (ou seja, ele não pode ser aberto usando CreateFile). No entanto, se o item for representado como um arquivo e seu nome seguir a sintaxe padrão de nomenclatura de arquivo do Win32, a fonte de dados deverá emitir essa propriedade. Se o item não for um arquivo, a fonte de dados deverá emitir essa propriedade como VT \_ Empty.

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

Os valores de PKEY são definidos em Propkey. h.

Talvez o item não exista em um sistema de arquivos (ou seja, ele não pode ser aberto usando CreateFile), mas se o item for representado como um arquivo do sensor lógico e seu nome seguir a sintaxe de nomeação de arquivo Win32 padrão, a fonte de dados deverá emitir essa propriedade. Se um item não for um arquivo, o valor dessa propriedade será VT \_ Empty. Consulte System. ItemNameDisplay. Isso tem o mesmo valor que System. ParsingName para itens que são fornecidos pela pasta de arquivos do Shell.

A tabela a seguir lista exemplos de valores de propriedade Path e filename:



| Caminho                               | Valor da propriedade |
|------------------------------------|----------------|
| c: \\ arquivos \\ \\hello.txt pessoais     | olá.txt      |
| \\\\mydir de compartilhamento de servidor \\ \\ \\news.doc | news.doc       |
| \\\\\\numbers.xls de compartilhamento do servidor \\     | numbers.xls    |
| c: \\ itens \\ MyFolder                | MyFolder       |
| \[mensagem de email\]                  | VT \_ vazio      |
| \[Song. WMA no dispositivo portátil\]    | Song. WMA       |



 

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

 

 
