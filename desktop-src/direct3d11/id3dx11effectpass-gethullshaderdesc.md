---
title: Método ID3DX11EffectPass GetHullShaderDesc (D3dx11effect.h)
description: Obter a descrição do sombreador de chassi.
ms.assetid: 1a683e61-da9a-4d78-8073-a6104625852b
keywords:
- Método GetHullShaderDesc Direct3D 11
- Método GetHullShaderDesc Direct3D 11 , interface ID3DX11EffectPass
- ID3DX11EffectPass interface Direct3D 11 , método GetHullShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetHullShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 609a41a71dad2918665b28bd600b89fa699b05a712aa776ea91fb438333c4f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046004"
---
# <a name="id3dx11effectpassgethullshaderdesc-method"></a>Método ID3DX11EffectPass::GetHullShaderDesc

Obter a descrição do sombreador de chassi.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetHullShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDesc* 
</dt> <dd>

Tipo: **[ **D3DX11 \_ PASSAR \_ SOMBREADOR \_ DESC**](d3dx11-pass-shader-desc.md)\***

Um ponteiro para uma descrição do sombreador de chassi (consulte [**D3DX11 \_ PASSAR \_ SOMBREADOR \_ DESC**](d3dx11-pass-shader-desc.md)).

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

 

 





