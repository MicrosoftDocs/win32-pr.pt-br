---
description: Identifica a extensão de arquivo do item baseado em arquivo, incluindo o período à esquerda.
ms.assetid: b72c695e-bdbd-471d-b902-9e30a62facd4
title: System. FileExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe9e989e88a1ff5eb5b525f5cb1904584aeb58a5700123651a256e040b6d2ac1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118053256"
---
# <a name="systemfileextension"></a>System. FileExtension

Identifica a extensão de arquivo do item baseado em arquivo, incluindo o período à esquerda. Essa propriedade é derivada de System. FileName. Se System. FileName não tiver uma extensão de arquivo ou for VT \_ Empty, o valor dessa propriedade deverá ser VT \_ vazio.

Para obter o tipo de qualquer item (incluindo um item que não é um arquivo), use System. ItemType.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.FileExtension
   shellPKey = PKEY_FileExtension
   formatID = E4F10A3C-49E6-405D-8288-A23BD4EEAA6C
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Comentários

Os valores de PKEY são definidos em Propkey. h.

Se [System. FileName](./props-system-filename.md) for VT \_ vazio, essa propriedade também deverá estar vazia. Caso contrário, essa propriedade deve ser derivada adequadamente pela fonte de dados de System. FileName. Se System. FileName não incluir uma extensão de arquivo, [System. FileExtension]() deverá ser VT \_ vazio. Para obter o tipo de qualquer item (incluindo um item que não é um arquivo), use [System. ItemType](./props-system-itemtype.md).

Exemplos de propriedade de extensão de arquivo e caminho. 

| Caminho                               | Extensão do arquivo |
|------------------------------------|----------------|
| c: \\ arquivos \\ \\hello.txt pessoais     | .txt           |
| \\\\mydir de compartilhamento de servidor \\ \\ \\news.doc | .doc           |
| \\\\\\numbers.xls de compartilhamento do servidor \\     | .xls           |
| \\\\\\pasta de compartilhamento do servidor \\          | VT \_ vazio      |
| c: \\ itens \\ MyFolder                | VT \_ vazio      |
| \[desktop\]                        | VT \_ vazio      |



 

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

 

 
