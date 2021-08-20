---
title: Propriedade IManipulationProcessor MinimumScaleRotateRadius
description: Especifica a grande quantidade de contatos de distância em um gesto de escala ou de giro precisar ser para disparar a manipulação.
ms.assetid: b4c49f41-c5ea-4c6a-872b-2d982e588b09
keywords:
- propriedade MinimumScaleRotateRadius Windows toque
- propriedade MinimumScaleRotateRadius Windows toque, interface IManipulationProcessor
- interface IManipulationProcessor Windows toque, propriedade MinimumScaleRotateRadius
topic_type:
- apiref
api_name:
- IManipulationProcessor.MinimumScaleRotateRadius
- IManipulationProcessor.get_MinimumScaleRotateRadius
- IManipulationProcessor.put_MinimumScaleRotateRadius
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location:
- manipulations.h
ms.openlocfilehash: 81ad10d5b041469daff216b7a23a4f5b6f4b3922e3bce438c2183e2551acf5d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118030073"
---
# <a name="imanipulationprocessorminimumscalerotateradius-property"></a>Propriedade IManipulationProcessor:: MinimumScaleRotateRadius

Especifica a grande quantidade de contatos de distância em um gesto de escala ou de giro precisar ser para disparar a manipulação.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_MinimumScaleRotateRadius(
  [in]  FLOAT MinimumScaleRotateRadius
);

HRESULT get_MinimumScaleRotateRadius(
  [out] FLOAT *MinimumScaleRotateRadius
);
```



## <a name="property-value"></a>Valor da propriedade

Especifica a distância mínima entre os contatos para disparar gestos de escala ou de giro.

## <a name="error-codes"></a>Códigos do Erro

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa propriedade é definida em centipixels (100ths de um pixel).

 

Definir esse valor fará com que o processador de manipulação ignore gestos com um raio muito pequeno. Isso será útil se você quiser impedir que um usuário manipule um objeto em um raio muito pequeno. Por exemplo, se você estiver usando um processador de manipulação com um círculo e quiser garantir que ele mantenha um raio maior que 100 pixels, você definirá esse valor como 10000.

## <a name="examples"></a>Exemplos


```C++
pManip->put_MinimumScaleRotateRadius(4000.0f);  
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)
</dt> </dl>

 

 




