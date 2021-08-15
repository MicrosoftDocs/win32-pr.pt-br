---
title: Função RWTexture2D::Load(int)
description: Lê dados de textura. | Função RWTexture2D::Load(int)
ms.assetid: AEBB9C78-BE4B-4121-93CC-EE03B9925CF0
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
ms.openlocfilehash: 913cf8372cb08860db639a9ba10bed872648526e7c8850e2e101912fb9f1354e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510909"
---
# <a name="rwtexture2dloadint-function"></a>Função RWTexture2D::Load(int)

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

O tipo de retorno corresponde ao tipo na declaração para o [**objeto RWTexture2D.**](sm5-object-rwtexture2d.md)

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos de carregamento](rwtexture2d-load.md)
</dt> </dl>

 

 




