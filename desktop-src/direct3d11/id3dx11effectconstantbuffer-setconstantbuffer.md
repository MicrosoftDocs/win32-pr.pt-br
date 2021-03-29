---
title: Método ID3DX11EffectConstantBuffer SetConstantBuffer (D3dx11effect. h)
description: Definir um buffer de constantes.
ms.assetid: 288e029a-e69a-4f58-be3f-8f9900c0e1dd
keywords:
- Método SetConstantBuffer Direct3D 11
- Método SetConstantBuffer Direct3D 11, interface ID3DX11EffectConstantBuffer
- Interface ID3DX11EffectConstantBuffer Direct3D 11, método SetConstantBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.SetConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12249d9830ced43c3a56a2c8cf51942e66f6494e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173159"
---
# <a name="id3dx11effectconstantbuffersetconstantbuffer-method"></a>Método ID3DX11EffectConstantBuffer:: SetConstantBuffer

Definir um buffer de constantes.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetConstantBuffer(
   ID3D11Buffer *pConstantBuffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pConstantBuffer* 
</dt> <dd>

Tipo: **[ **ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)\***

Um ponteiro para uma interface de buffer constante. Consulte [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer).

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

 

 





