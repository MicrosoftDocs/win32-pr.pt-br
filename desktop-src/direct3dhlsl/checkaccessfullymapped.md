---
title: Função CheckAccessFullyMapped
description: Determina se todos os valores de uma operação de Exemplo, Coleta ou Carregamento acessaram blocos mapeados em um recurso lado a lado.
ms.assetid: 2CAB7770-143E-4E29-A57F-96C27021AC5F
keywords:
- Função CheckAccessFullyMapped HLSL
topic_type:
- apiref
api_name:
- CheckAccessFullyMapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e7241fa5546edffb2b7c5ff36d2e43919e6d0b6fef9ff617c0fb63a674ffee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516669"
---
# <a name="checkaccessfullymapped-function"></a>Função CheckAccessFullyMapped

Determina se todos os valores de  **uma** operação de exemplo , **Coletar** ou Carregar acessaram blocos mapeados em um recurso lado a [lado.](/windows/desktop/direct3d11/direct3d-11-2-features)

## <a name="syntax"></a>Sintaxe

``` syntax
bool CheckAccessFullyMapped(
  in uint_only status
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*status* \[ Em\]
</dt> <dd>

Tipo: **somente \_ uint**

O valor de status retornado de uma operação **De exemplo,** **Coletar** **ou** Carregar. Como não é possível acessar esse valor de status diretamente, você precisa passá-lo para **CheckAccessFullyMapped.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **bool**

Retorna um **valor booliana** que indica se todos os valores de uma operação sample **,** **Gather** ou **Load** acessaram blocos mapeados em um recurso lado a [lado.](/windows/desktop/direct3d11/direct3d-11-2-features) Retornará **TRUE** se todos os valores da operação acessarem blocos mapeados; caso contrário, **retornará FALSE** se quaisquer valores foram retirados de um lado não mapeado.

## <a name="remarks"></a>Comentários

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) e modelos de sombreador superior | sim       |



 

Essa função tem suporte nos seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 