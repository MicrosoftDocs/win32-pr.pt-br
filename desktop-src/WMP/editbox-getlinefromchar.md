---
title: EDITBOX.getLineFromChar
description: O método getLineFromChar recupera o índice de linha para o índice de caracteres especificado.
ms.assetid: c3a29bdf-ff63-4b6d-90e8-d414dde87f85
keywords:
- EDITBOX.getLineFromChar Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLineFromChar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 110030c3c756a91c993857cef125c51669f71eb9a358eb7261205fde0b0ad4a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749302"
---
# <a name="editboxgetlinefromchar"></a>EDITBOX.getLineFromChar

O **método getLineFromChar** recupera o índice de linha para o índice de caracteres especificado.

``` syntax
        elementID.getLineFromChar(index)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Índice*
</dt> <dd>

**Número** (**longo**) que contém o índice do caractere cujo índice de linha deve ser recuperado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método retorna um **Número** (**long**).

## <a name="remarks"></a>Comentários

Se a posição de caractere especificada for 1, esse método recuperará o índice de linha da linha atual.

Esse método só pode ser chamado depois que o controle se torna visível.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------|
| Versão<br/> | Windows Media Player para Windows XP ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento EDITBOX**](editbox-element.md)
</dt> <dt>

[**EDITBOX.getLine**](editbox-getline.md)
</dt> <dt>

[**EDITBOX.getLineIndex**](editbox-getlineindex.md)
</dt> </dl>

 

 





