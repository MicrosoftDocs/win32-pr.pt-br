---
description: Define opções para executar cálculos de distância poliedt, ao ajustar uma textura a uma superfície curva. Use esse sinalizador para escolher entre os cálculos de alta qualidade versus rápidos ao calcular um Atlas de textura.
ms.assetid: 76649c57-e5ae-4e0d-a7ab-f56385a327c2
title: Enumeração D3DXUVATLAS (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVATLAS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 1edcf2b1cbe2363f805bee1f5eb67f5558702ea9e163a865e1a6c51d6f5ed6ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523832"
---
# <a name="d3dxuvatlas-enumeration"></a>Enumeração D3DXUVATLAS

Define opções para executar cálculos de distância poliedt, ao ajustar uma textura a uma superfície curva. Use esse sinalizador para escolher entre os cálculos de alta qualidade versus rápidos ao calcular um Atlas de textura.

## <a name="syntax"></a>Syntax


```C++
typedef enum _D3DXUVATLAS { 
  D3DXUVATLAS_DEFAULT           = 1,
  D3DXUVATLAS_GEODESIC_FAST     = 2,
  D3DXUVATLAS_GEODESIC_QUALITY  = 3
} D3DXUVATLAS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXUVATLAS_DEFAULT"></span><span id="d3dxuvatlas_default"></span>**D3DXUVATLAS \_ padrão**
</dt> <dd>

As malhas com mais de 25K faces terão o método de distância rápida geodasic aplicado a elas, enquanto as malhas com menos de 25K faces terão o método de distância poliedro de qualidade mais alto aplicado a elas em vez disso.

</dd> <dt>

<span id="D3DXUVATLAS_GEODESIC_FAST"></span><span id="d3dxuvatlas_geodesic_fast"></span>**\_Fast poliedt D3DXUVATLAS \_**
</dt> <dd>

Usa aproximações para melhorar a velocidade do gráfico ao custo de ampliação ou mais gráficos de saída para a malha.

</dd> <dt>

<span id="D3DXUVATLAS_GEODESIC_QUALITY"></span><span id="d3dxuvatlas_geodesic_quality"></span>**\_Qualidade de poliedro D3DXUVATLAS \_**
</dt> <dd>

Fornece gráficos de melhor qualidade, mas requer mais tempo e memória do que o rápido.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




