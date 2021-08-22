---
title: Método GetDesc ID3DX11EffectTechnique (D3dx11effect.h)
description: Obter uma descrição da técnica.
ms.assetid: ed82d873-0540-4aa8-ac0f-198852b886ad
keywords:
- Método GetDesc Direct3D 11
- Método GetDesc Direct3D 11 , interface ID3DX11EffectTechnique
- ID3DX11EffectTechnique interface Direct3D 11 , método GetDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad72387b59690d747d5b86927062e8ee8a0ec51ba2f81d746112d65e72d5782f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532524"
---
# <a name="id3dx11effecttechniquegetdesc-method"></a>Método ID3DX11EffectTechnique::GetDesc

Obter uma descrição da técnica.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDesc(
   D3DX11_TECHNIQUE_DESC *pDesc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDesc* 
</dt> <dd>

Tipo: **[ **D3DX11 \_ TECHNIQUE \_ DESC**](d3dx11-technique-desc.md)\***

Um ponteiro para uma descrição de técnica (consulte [**D3DX11 \_ TECHNIQUE \_ DESC**](d3dx11-technique-desc.md)).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retorna um dos códigos de [retorno do Direct3D 11 a seguir.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentários

> [!Note]  
> O SDK do DirectX não fornece binários compilados para efeitos. Você deve usar a origem efeitos 11 para criar seu aplicativo do tipo efeitos. Para obter mais informações sobre como usar a origem dos Efeitos 11, consulte [Diferenças entre efeitos 10 e efeitos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX11EffectTechnique](id3dx11effecttechnique.md)
</dt> </dl>

 

 





