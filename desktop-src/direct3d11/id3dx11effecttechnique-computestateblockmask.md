---
title: Método ID3DX11EffectTechnique ComputeStateBlockMask (D3dx11effect. h)
description: Compute uma máscara de bloco de estado para permitir/impedir alterações de estado.
ms.assetid: 4fd6061d-6ca5-4e3f-b031-fae98f3de057
keywords:
- Método ComputeStateBlockMask Direct3D 11
- Método ComputeStateBlockMask Direct3D 11, interface ID3DX11EffectTechnique
- Interface ID3DX11EffectTechnique Direct3D 11, método ComputeStateBlockMask
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.ComputeStateBlockMask
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d15a159c15f35d530559b4ad6d84dd815e5964a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172947"
---
# <a name="id3dx11effecttechniquecomputestateblockmask-method"></a>Método ID3DX11EffectTechnique:: ComputeStateBlockMask

Compute uma máscara de bloco de estado para permitir/impedir alterações de estado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ComputeStateBlockMask(
   D3DX11_STATE_BLOCK_MASK *pStateBlockMask
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStateBlockMask* 
</dt> <dd>

Tipo: **[ **\_ máscara de \_ bloco \_ de estado D3DX11**](d3dx11-state-block-mask.md)\***

Um ponteiro para uma máscara de bloco de estado ( [**consulte \_ \_ \_ máscara de bloco de estado D3DX11**](d3dx11-state-block-mask.md)).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

> [!Note]  
> O SDK do DirectX não fornece nenhum binário compilado para efeitos. Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos. Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX11EffectTechnique](id3dx11effecttechnique.md)
</dt> </dl>

 

 





