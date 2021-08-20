---
title: Função RWTexture3D::Load(int)
description: Lê dados de textura. | Função RWTexture3D::Load(int)
ms.assetid: 93C4FFFF-8695-4BAF-BAE4-A2704332E6A9
keywords:
- Função de carregamento HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d233559739e86a1cf5a8cbdc9af18ea6c12550c5f6118d63b5382689cd80bba2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671886"
---
# <a name="rwtexture3dloadint-function"></a>Função RWTexture3D::Load(int)

Lê dados de textura.

## <a name="syntax"></a>Sintaxe


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Localização* \[ Em\]
</dt> <dd>

Tipo: **int**

O local da textura.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo:

O tipo de retorno corresponde ao tipo na declaração para o [**objeto RWTexture3D.**](sm5-object-rwtexture3d.md)

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos de carregamento](rwtexture3d-load.md)
</dt> </dl>

 

 




