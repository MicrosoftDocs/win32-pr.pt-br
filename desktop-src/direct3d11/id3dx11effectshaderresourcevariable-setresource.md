---
title: Método ID3DX11EffectShaderResourceVariable SetResource (D3dx11effect.h)
description: Definir um recurso de sombreador.
ms.assetid: f85c33ff-dc00-4421-939c-74f9317faadc
keywords:
- Método SetResource Direct3D 11
- Método SetResource Direct3D 11 , interface ID3DX11EffectShaderResourceVariable
- ID3DX11EffectShaderResourceVariable interface Direct3D 11 , método SetResource
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable.SetResource
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf0db2db1886298633ba70fa9af6ce1d475b5c511487b35e65d20373f8282f3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118533434"
---
# <a name="id3dx11effectshaderresourcevariablesetresource-method"></a>Método ID3DX11EffectShaderResourceVariable::SetResource

Definir um recurso de sombreador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetResource(
   ID3D11ShaderResourceView *pResource
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Presource* 
</dt> <dd>

Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***

O endereço de um ponteiro para uma interface shader-resource-view. Consulte [**ID3D11ShaderResourceView.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)

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

[ID3DX11EffectShaderResourceVariable](id3dx11effectshaderresourcevariable.md)
</dt> </dl>

 

 





