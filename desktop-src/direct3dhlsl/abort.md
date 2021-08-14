---
title: Função abort (Corecrt \_ terminate.h)
description: Envia uma mensagem de erro para a fila de informações e encerra a chamada de desenho ou expedição atual que está sendo executada.
ms.assetid: b8ce153b-0d1c-4294-b88e-b7e50e708ab9
keywords:
- função abort HLSL
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
ms.openlocfilehash: 4a708d2893a19369d2db42f4551e3fafa4a1ff7a4680bf8676de32f79764289b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118795520"
---
# <a name="abort-function"></a>Função abort

Envia uma mensagem de erro para a fila de informações e encerra a chamada de desenho ou expedição atual que está sendo executada.

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

Essa operação não faz nada em rasterizadores que não deem suporte a ela.

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                                        | Com suporte |
|---------------------------------------------------------------------|-----------|
| [Modelo de sombreador 4 (DirectX HLSL) ou posterior.](dx-graphics-hlsl-sm3.md) | sim       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Corecrt \_ terminate.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





