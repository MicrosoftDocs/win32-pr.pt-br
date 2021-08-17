---
title: Método ID3DX11EffectVariable GetParentConstantBuffer (D3dx11effect.h)
description: Obter um buffer constante. | Método ID3DX11EffectVariable GetParentConstantBuffer (D3dx11effect.h)
ms.assetid: 43b46b05-951e-4c52-8bc7-4bb5f657ea78
keywords:
- Método GetParentConstantBuffer Direct3D 11
- Método GetParentConstantBuffer Direct3D 11 , interface ID3DX11EffectVariable
- ID3DX11EffectVariable interface Direct3D 11 , método GetParentConstantBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetParentConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2319a72e50d83f3780b68de163dc370d5627c28ab4ab84f6621c11faf6df7805
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117734109"
---
# <a name="id3dx11effectvariablegetparentconstantbuffer-method"></a>Método ID3DX11EffectVariable::GetParentConstantBuffer

Obter um buffer constante.

## <a name="syntax"></a>Sintaxe


```C++
ID3DX11EffectConstantBuffer* GetParentConstantBuffer();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***

Um ponteiro para um [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).

## <a name="remarks"></a>Comentários

As variáveis de efeito são lidas ou escritas em um buffer constante.

> [!Note]  
> O SDK do DirectX não fornece binários compilados para efeitos. Você deve usar a origem efeitos 11 para criar seu aplicativo do tipo efeitos. Para obter mais informações sobre como usar a origem dos Efeitos 11, consulte [Diferenças entre efeitos 10 e efeitos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





