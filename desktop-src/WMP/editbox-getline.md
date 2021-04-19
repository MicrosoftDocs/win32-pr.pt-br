---
title: Paminhar. getline
description: O método getline recupera o texto para a linha com o índice especificado.
ms.assetid: a692c32b-86b9-419e-a3a5-464687be04da
keywords:
- Admy. getline Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3b0b9a15f9eff8c2612e7a242a205c1d9411a60c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811114"
---
# <a name="editboxgetline"></a>Paminhar. getline

O método **getline** recupera o texto para a linha com o índice especificado.

``` syntax
        elementID.getLine(index)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*index*
</dt> <dd>

**Número** (**longo**) que contém o índice da linha a ser recuperada.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método retorna uma **cadeia de caracteres**.

## <a name="remarks"></a>Comentários

Se o índice não for válido, uma cadeia de caracteres vazia será retornada. Esse método só pode ser chamado depois que o controle se tornar visível.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------|
| Versão<br/> | Windows Media Player para Windows XP ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento admy**](editbox-element.md)
</dt> <dt>

[**GetLineFromChar de edição**](editbox-getlinefromchar.md)
</dt> <dt>

[**GetLineIndex de edição**](editbox-getlineindex.md)
</dt> </dl>

 

 





