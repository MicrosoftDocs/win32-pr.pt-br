---
title: Função errorf
description: Envia uma mensagem de erro para a fila de informações.
ms.assetid: bf4dc6dc-b36e-4b71-ad61-b7a5ba332879
keywords:
- Função errorf HLSL
topic_type:
- apiref
api_name:
- errorf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0651a27419a369721806e9aa4717a20088f8f5fbbaa0063628d2feb69648c7cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562676"
---
# <a name="errorf-function"></a>Função errorf

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

*Argumento...* 
</dt> <dd>

Argumentos opcionais.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Essa operação não faz nada em dispositivos que não são compatíveis com ela.

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                                        | Com suporte |
|---------------------------------------------------------------------|-----------|
| [Modelo de sombreador 4 (DirectX HLSL) ou posterior.](dx-graphics-hlsl-sm3.md) | sim       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




