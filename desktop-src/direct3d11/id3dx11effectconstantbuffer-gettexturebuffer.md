---
title: Método ID3DX11EffectConstantBuffer GetTextureBuffer (D3dx11effect. h)
description: Obter um buffer de textura.
ms.assetid: 8d09e67c-358e-49ee-8ca4-e1f548b52c3a
keywords:
- Método GetTextureBuffer Direct3D 11
- Método GetTextureBuffer Direct3D 11, interface ID3DX11EffectConstantBuffer
- Interface ID3DX11EffectConstantBuffer Direct3D 11, método GetTextureBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.GetTextureBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d03000338c725e71096e57715a49a70b4347b358
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968673"
---
# <a name="id3dx11effectconstantbuffergettexturebuffer-method"></a>Método ID3DX11EffectConstantBuffer:: GetTextureBuffer

Obter um buffer de textura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetTextureBuffer(
   ID3D11ShaderResourceView **ppTextureBuffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppTextureBuffer* 
</dt> <dd>

Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***

O endereço de um ponteiro para uma interface de exibição de recurso de sombreador para acessar um buffer de textura. Consulte [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).

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

[ID3DX11EffectConstantBuffer](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





