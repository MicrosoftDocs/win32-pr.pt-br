---
description: Leia sobre a propriedade System. ItemPathDisplayNarrow, que representa o caminho de exibição amigável para o item.
ms.assetid: 5dd44e13-bc5c-4e32-b5eb-2c7c40e10dfb
title: System. ItemPathDisplayNarrow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b84455a8b69ebf42cb91c191d1c275b70eeeb5ac
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403889"
---
# <a name="systemitempathdisplaynarrow"></a>System. ItemPathDisplayNarrow

O caminho de exibição amigável para o item.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemPathDisplayNarrow
   shellPKey = PKEY_ItemPathDisplayNarrow
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 8
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Comentários

Os valores de PKEY são definidos em Propkey. h.

Para otimizar uma coluna de exibição estreita, o formato da cadeia de caracteres deve ser personalizado para que o nome venha primeiro.

Se o item for um arquivo, o valor da propriedade excluirá a extensão do arquivo, mas incluirá nomes localizados, se estiverem presentes. Se o item for uma mensagem, o valor incluirá [System. ItemNamePrefix](./props-system-itemnameprefix.md). Para analisar um caminho de item, use [System. ItemUrl](./props-system-itemurl.md) ou [System. ParsingPath](./props-system-parsingpath.md).

Valores de exemplo:



| Caminho                                   | ItemPathDisplayName                 |
|----------------------------------------|-------------------------------------|
| c: \\ barra de mydir \\ \\hello.txt              | Olá (c: \\ barra de mydir \\ )              |
| \\\\mydir de compartilhamento de servidor \\ \\ \\goodnews.doc | GoodNews ( \\ \\ servidor \\ de \\ mydir de compartilhamento) |
| \\\\\\pasta de compartilhamento do servidor \\              | pasta ( \\ \\ compartilhamento do servidor \\ )          |
| c: \\ mydir \\ MyFolder                    | MyFolder (c: \\ mydir)                |
| /Mailbox conta/caixa de entrada/' re: Olá! '    | Re: Olá! (Conta do/Mailbox/caixa de entrada) |



 

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

 

 
