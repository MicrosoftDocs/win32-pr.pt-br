---
title: printf - função
description: Envia uma mensagem de sombreador personalizado para a fila de informações.
ms.assetid: 0c6c15fc-1da5-4a26-ade0-5a0489e4f564
keywords:
- função printf HLSL
topic_type:
- apiref
api_name:
- printf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74492cc613e22f335eace684300f0380e5751a95
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103916810"
---
# <a name="printf-function"></a>printf - função

Envia uma mensagem de sombreador personalizado para a fila de informações.

## <a name="syntax"></a>Sintaxe

``` syntax
void printf(
   string format,
    argument ...
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*format* 
</dt> <dd>

A cadeia de caracteres de formato.

</dd> <dt>

*argumento...* 
</dt> <dd>

Argumentos opcionais.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Esta operação não faz nada em dispositivos que não dão suporte a ele.

### <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                        | Com suporte |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4 (DirectX HLSL) ou posterior.](dx-graphics-hlsl-sm3.md) | sim       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




