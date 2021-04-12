---
description: Carregar uma textura de uma textura.
ms.assetid: 126e71e1-a3b2-418b-be35-434a2e9472ca
title: Função D3DX10LoadTextureFromTexture (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10LoadTextureFromTexture
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: e8dc65c9bff78484f09c355f8eb3d9626372b9b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298536"
---
# <a name="d3dx10loadtexturefromtexture-function"></a>Função D3DX10LoadTextureFromTexture

Carregar uma textura de uma textura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10LoadTextureFromTexture(
   ID3D10Resource           *pSrcTexture,
   D3DX10_TEXTURE_LOAD_INFO *pLoadInfo,
   ID3D10Resource           *pDstTexture
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSrcTexture* 
</dt> <dd>

Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Ponteiro para a textura de origem. Consulte [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> <dt>

*pLoadInfo* 
</dt> <dd>

Tipo: **[ **\_ informações de \_ carregamento \_ de textura D3DX10**](d3dx10-texture-load-info.md)\***

Ponteiro para parâmetros de carregamento de textura. Consulte [**\_ informações de \_ carregamento \_ de textura do D3DX10**](d3dx10-texture-load-info.md).

</dd> <dt>

*pDstTexture* 
</dt> <dd>

Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Ponteiro para a textura de destino. Consulte a [**interface ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de textura no D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




