---
title: Método ID3DX11EffectConstantBuffer SetTextureBuffer (D3dx11effect.h)
description: Definir um buffer de textura.
ms.assetid: b8c327e4-52ff-498e-81e9-187e58bbe5d2
keywords:
- Método SetTextureBuffer Direct3D 11
- Método SetTextureBuffer Direct3D 11 , interface ID3DX11EffectConstantBuffer
- ID3DX11EffectConstantBuffer interface Direct3D 11 , método SetTextureBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.SetTextureBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2d71b104d51b8310f2922c25e940cd559e2d47dca695cbe844e7526eb8235fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046365"
---
# <a name="id3dx11effectconstantbuffersettexturebuffer-method"></a>Método ID3DX11EffectConstantBuffer::SetTextureBuffer

Definir um buffer de textura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetTextureBuffer(
   ID3D11ShaderResourceView *pTextureBuffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTextureBuffer* 
</dt> <dd>

Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***

Um ponteiro para uma interface sombreador-exibição de recurso para acessar um buffer de textura.

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

[ID3DX11EffectConstantBuffer](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





