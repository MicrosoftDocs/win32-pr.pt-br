---
description: O prefixo de um item, usado para mensagens de email em que o assunto começa com o prefixo &\# 0034; Re:&\# 0034;.
ms.assetid: 3c257edc-b7f7-498d-8347-0be4fca41023
title: System.ItemNamePrefix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd7830f63c3e9e0f6026099c95d11820a1d8592928cece72ebe72d76936d8467
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119598456"
---
# <a name="systemitemnameprefix"></a>System.ItemNamePrefix

O prefixo de um item, usado para mensagens de email em que o assunto começa com o prefixo "Re:".

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemNamePrefix
   shellPKey = PKEY_ItemNamePrefix
   formatID = D7313FF1-A77A-401C-8C99-3DBDD68ADD36
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Comentários

Os valores PKEY são definidos em Propkey.h.

Se o item for um arquivo, o valor dessa propriedade será VT \_ EMPTY. Se o item for uma mensagem, o valor dessa propriedade será os prefixos de encaminhamento ou resposta (incluindo os dois-pontos delimitadores, mas nenhum espaço em branco) ou VT EMPTY se não houver \_ prefixo.

Valores de exemplo:



| System.ItemNamePrefix | System.ItemName  | System.ItemNameDisplay |
|-----------------------|------------------|------------------------|
| VT \_ VAZIO             | "Ótimo dia"      | "Ótimo dia"            |
| "Re:"                 | "Ótimo dia"      | "Re: Ótimo dia"        |
| "Fwd: "               | "Orçamento mensal" | "Fwd: orçamento mensal"  |
| VT \_ VAZIO             | accounts.xls     | accounts.xls           |



 

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

 

 
