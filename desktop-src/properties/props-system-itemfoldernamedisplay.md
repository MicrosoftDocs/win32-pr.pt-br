---
description: O nome de exibição amigável da pasta pai de um item.
ms.assetid: 4049b6cb-41a1-4df6-89d1-a2022d3a285d
title: System. ItemFolderNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d637412b02345b52fee2e1c13e8f499314af4c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170484"
---
# <a name="systemitemfoldernamedisplay"></a>System. ItemFolderNameDisplay

O nome de exibição amigável da pasta pai de um item.

Isso é derivado de [System. ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md). Se essa propriedade for VT \_ vazia, essa propriedade deverá ser também.

Se a pasta for uma pasta de arquivos, o valor será localizado se um nome localizado estiver disponível.

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

Os valores de PKEY são definidos em Propkey. h.

Se [System. ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) for VT \_ Empty, essa propriedade também deverá estar vazia. Caso contrário, ele deve ser derivado adequadamente pela fonte de dados de System. ItemFolderPathDisplay.

Exemplos:



| Caminho fornecido                             | Nome de exibição da pasta |
|----------------------------------------|---------------------|
| c: \\ Myfiles \\hello.txt de texto \\           | Texto                |
| \\\\mydir de compartilhamento de servidor \\ \\ \\goodnews.doc | mydir               |
| \\\\\\numbers.xls de compartilhamento do servidor \\         | compartilhar               |
| c: \\ pastas \\ MyFolder                  | Pastas             |
| /Mailbox conta/caixa de entrada/' re: Olá! '    | Caixa de Entrada               |



 

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

 

 
