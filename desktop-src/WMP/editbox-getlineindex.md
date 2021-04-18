---
title: GetLineIndex de edição
description: O método getLineIndex recupera o índice de caracteres do primeiro caractere na linha com o índice de linha especificado.
ms.assetid: 1298227a-d839-44fc-bacb-44c3c968bd94
keywords:
- Admy. getLineIndex Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLineIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f55027bb7d577b7080ad2f006a5a006e718c2d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770502"
---
# <a name="editboxgetlineindex"></a>GetLineIndex de edição

O método **getLineIndex** recupera o índice de caracteres do primeiro caractere na linha com o índice de linha especificado.

``` syntax
        elementID.getLineIndex(index)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*index*
</dt> <dd>

**Número** (**longo**) que contém o índice da linha cujo índice de caracteres deve ser recuperado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método retorna um **número** (**longo**).

## <a name="remarks"></a>Comentários

Se o índice de linha especificado for 1, a linha que contém o ponto de inserção será usada.

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

[**GetLineFromChar de edição**](editbox-getlinefromchar.md)
</dt> </dl>

 

 





