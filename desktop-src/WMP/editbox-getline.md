---
title: Paminhar. getline
description: O método getline recupera o texto para a linha com o índice especificado.
ms.assetid: a692c32b-86b9-419e-a3a5-464687be04da
keywords:
- Windows Media Player admy. getline
topic_type:
- apiref
api_name:
- EDITBOX.getLine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 28d555cb684fa849b5fc7cdb42ebaf0ab4fb278b4ef126845add2f12ddf59948
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118578832"
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

 

 





