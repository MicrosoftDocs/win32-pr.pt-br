---
title: GetLineFromChar de edição
description: O método getLineFromChar recupera o índice de linha para o índice de caracteres especificado.
ms.assetid: c3a29bdf-ff63-4b6d-90e8-d414dde87f85
keywords:
- Admy. getLineFromChar Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLineFromChar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3462ce628da72ca1e55df79e408fc79e0ec8b63a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780010"
---
# <a name="editboxgetlinefromchar"></a>GetLineFromChar de edição

O método **getLineFromChar** recupera o índice de linha para o índice de caracteres especificado.

``` syntax
        elementID.getLineFromChar(index)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*index*
</dt> <dd>

**Número** (**longo**) que contém o índice do caractere cujo índice de linha deve ser recuperado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método retorna um **número** (**longo**).

## <a name="remarks"></a>Comentários

Se a posição do caractere especificado for 1, esse método recuperará o índice de linha da linha atual.

Esse método só pode ser chamado depois que o controle se tornar visível.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------|
| Versão<br/> | Windows Media Player para Windows XP ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento admy**](editbox-element.md)
</dt> <dt>

[**Paminhar. getline**](editbox-getline.md)
</dt> <dt>

[**GetLineIndex de edição**](editbox-getlineindex.md)
</dt> </dl>

 

 





