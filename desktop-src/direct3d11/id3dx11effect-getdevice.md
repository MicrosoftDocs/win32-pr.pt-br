---
title: Método GetDevice ID3DX11Effect (D3dx11effect. h)
description: Obtenha o dispositivo que criou o efeito.
ms.assetid: efcc0358-9842-46eb-a521-ea220ec18735
keywords:
- Método GetDevice Direct3D 11
- Método GetDevice Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, método GetDevice
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetDevice
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25317740cade8a937aeeeac29f5a608bb4a43931
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173134"
---
# <a name="id3dx11effectgetdevice-method"></a>Método ID3DX11Effect:: GetDevice

Obtenha o dispositivo que criou o efeito.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDevice(
   ID3D11Device **ppDevice
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppDevice* 
</dt> <dd>

Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\*\***

Um ponteiro para um [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

Um efeito é criado para um dispositivo específico, chamando uma função como [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).

> [!Note]  
> O SDK do DirectX não fornece nenhum binário compilado para efeitos. Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos. Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

 





