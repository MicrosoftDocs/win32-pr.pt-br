---
title: Função CheckAccessFullyMapped
description: Determina se todos os valores de uma operação de exemplo, de coleta ou de carregamento acessaram blocos mapeados em um recurso de lado.
ms.assetid: 2CAB7770-143E-4E29-A57F-96C27021AC5F
keywords:
- HLSL da função CheckAccessFullyMapped
topic_type:
- apiref
api_name:
- CheckAccessFullyMapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c7310e0ebac496fc8f5a56ba3843b7496b8ce7c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641617"
---
# <a name="checkaccessfullymapped-function"></a>Função CheckAccessFullyMapped

Determina se todos os valores de uma operação de **exemplo**, de **coleta** ou de **carregamento** acessaram blocos mapeados em um [recurso de lado](/windows/desktop/direct3d11/direct3d-11-2-features).

## <a name="syntax"></a>Sintaxe

``` syntax
bool CheckAccessFullyMapped(
  in uint_only status
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*status* \[ do no\]
</dt> <dd>

Tipo: **\_ apenas uint**

O valor de status que é retornado de uma operação de **exemplo**, de **coleta** ou de **carregamento** . Como não é possível acessar esse valor de status diretamente, você precisa passá-lo para **CheckAccessFullyMapped**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **bool**

Retorna um valor **booliano** que indica se todos os valores de uma operação de **exemplo**, **coleta** ou **carregamento** acessaram blocos mapeados em um [recurso de lado](/windows/desktop/direct3d11/direct3d-11-2-features). Retorna **true** se todos os valores da operação acessaram blocos mapeados; caso contrário, retornará **false** se algum valor tiver sido obtido de um bloco não mapeado.

## <a name="remarks"></a>Comentários

### <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos | sim       |



 

Essa função tem suporte nos seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 