---
title: função Abort (Corecrt \_ encerrar. h)
description: Envia uma mensagem de erro para a fila de informações e encerra a chamada de emissão ou expedição atual que está sendo executada.
ms.assetid: b8ce153b-0d1c-4294-b88e-b7e50e708ab9
keywords:
- anular função HLSL
topic_type:
- apiref
api_name:
- abort
api_location:
- corecrt_terminate.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9428a03b422aed9ff6fae097459a53369d3a30e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968712"
---
# <a name="abort-function"></a>Função abort

Envia uma mensagem de erro para a fila de informações e encerra a chamada de emissão ou expedição atual que está sendo executada.

## <a name="syntax"></a>Sintaxe

``` syntax
void abort(
    
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

 
</dt> <dd>

Nenhum

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Esta operação não faz nada em rasterizadores que não dão suporte a ele.

### <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                        | Com suporte |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4 (DirectX HLSL) ou posterior.](dx-graphics-hlsl-sm3.md) | sim       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Corecrt \_ encerrar. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





