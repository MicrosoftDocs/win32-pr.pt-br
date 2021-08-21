---
title: Método ID3DX11EffectPass GetGeometryShaderDesc (D3dx11effect.h)
description: Obter uma descrição do sombreador de geometria.
ms.assetid: 03298ec3-6b85-40bf-8920-a82c7606d326
keywords:
- Método GetGeometryShaderDesc Direct3D 11
- Método GetGeometryShaderDesc Direct3D 11 , interface ID3DX11EffectPass
- ID3DX11EffectPass interface Direct3D 11 , método GetGeometryShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetGeometryShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e93c9dfdc2525f2b730f88a9ffaeb5c68d4c9d8304410ddcf891f063cf20729
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535032"
---
# <a name="id3dx11effectpassgetgeometryshaderdesc-method"></a>Método ID3DX11EffectPass::GetGeometryShaderDesc

Obter uma descrição do sombreador de geometria.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetGeometryShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDesc* 
</dt> <dd>

Tipo: **[ **D3DX11 \_ PASSAR \_ SOMBREADOR \_ DESC**](d3dx11-pass-shader-desc.md)\***

Um ponteiro para uma descrição de sombreador de geometria (consulte [**D3DX11 \_ PASSAR \_ SOMBREADOR \_ DESC**](d3dx11-pass-shader-desc.md)).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retorna um dos códigos de [retorno do Direct3D 11 a seguir.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentários

Uma passagem de efeito pode conter atribuições de estado de renderização e atribuições de objeto de sombreador.

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

 

 





