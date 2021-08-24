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
ms.openlocfilehash: 47131cacef436572f519b394a02b4aaa357a426dd80a192868712cb3d7779e24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672516"
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

 

 




