---
title: Método ID3DX11EffectPass GetDomainShaderDesc (D3dx11effect.h)
description: Obter uma descrição do sombreador de domínio.
ms.assetid: 02109930-0922-46b8-9381-bb75abd0c4a0
keywords:
- Método GetDomainShaderDesc Direct3D 11
- Método GetDomainShaderDesc Direct3D 11 , interface ID3DX11EffectPass
- ID3DX11EffectPass interface Direct3D 11 , método GetDomainShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetDomainShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f61de7dd44d19cb57390adf7829766fc4bffcff82bf1019b3dae1e2979ae37ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046014"
---
# <a name="id3dx11effectpassgetdomainshaderdesc-method"></a>Método ID3DX11EffectPass::GetDomainShaderDesc

Obter uma descrição do sombreador de domínio.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDomainShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDesc* 
</dt> <dd>

Tipo: **[ **D3DX11 \_ PASSAR \_ SOMBREADOR \_ DESC**](d3dx11-pass-shader-desc.md)\***

Um ponteiro para uma descrição do sombreador de domínio (consulte [**D3DX11 \_ PASSAR \_ SOMBREADOR \_ DESC**](d3dx11-pass-shader-desc.md)).

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

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

 





