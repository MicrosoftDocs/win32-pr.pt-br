---
description: O nome de tipo amigável do item.
ms.assetid: 5d4c86da-6317-4a34-88d6-caf794aaa165
title: System. ItemTypeText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f145aa2491f3352c4691be95c0e8ae16a75e8e0880732904e983fbf02c167dbd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553746"
---
# <a name="systemitemtypetext"></a>System. ItemTypeText

O nome de tipo amigável do item. Esse valor não se destina a ser analisado programaticamente.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemTypeText
   shellPKey = PKEY_ItemTypeText
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 4
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Comentários

Os valores de PKEY são definidos em Propkey. h.

Se [System. ItemType](./props-system-itemtype.md) for VT \_ vazio, o valor dessa propriedade também será um VT \_ vazio. Se o item for um arquivo, o valor dessa propriedade será o mesmo que se você passasse o valor System. ItemType do arquivo para [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay).

Essa propriedade não deve ser confundida com [System. Kind](./props-system-kind.md), que é um nome de tipo amigável de alto nível. Por exemplo, para um arquivo de documento .doc, as várias propriedades são como mostrado aqui:



| Propriedade                                               | Valor                   |
|--------------------------------------------------------|-------------------------|
| [Sistema. Kind](./props-system-kind.md)                 | Documento                |
| [System. ItemType](./props-system-itemtype.md)         | .doc                    |
| [System. ItemTypeText]() | Microsoft Word Document |



 

Valores de exemplo:



| Caminho                                   | ItemTypeText            |
|----------------------------------------|-------------------------|
| c: \\ barra de mydir \\ \\hello.txt              | Arquivo de texto               |
| \\\\mydir de compartilhamento de servidor \\ \\ \\goodnews.doc | Microsoft Word Document |
| \\\\\\pasta de compartilhamento do servidor \\              | Pasta de arquivos             |
| c: \\ mydir \\ MyFolder                    | Pasta de arquivos             |
| /Mailbox conta/caixa de entrada/' re: Olá! '    | Outlook Mensagem de email  |



 

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

 

 
