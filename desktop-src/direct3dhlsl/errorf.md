---
title: função errorf
description: Envia uma mensagem de erro para a fila de informações.
ms.assetid: bf4dc6dc-b36e-4b71-ad61-b7a5ba332879
keywords:
- HLSL da função errorf
topic_type:
- apiref
api_name:
- errorf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76c8fbcd9b6cb15dbbb735296a3aada8f5e568cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006406"
---
# <a name="errorf-function"></a>função errorf

Envia uma mensagem de erro para a fila de informações.

## <a name="syntax"></a>Sintaxe

``` syntax
void errorf(
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

 

 




