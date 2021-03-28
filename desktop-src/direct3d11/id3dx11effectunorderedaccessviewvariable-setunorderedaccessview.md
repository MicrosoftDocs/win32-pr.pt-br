---
title: Método ID3DX11EffectUnorderedAccessViewVariable SetUnorderedAccessView (D3dx11effect. h)
description: Defina um modo de exibição de acesso não ordenado.
ms.assetid: a147879c-c5cf-4453-b27f-8716cb33962b
keywords:
- Método SetUnorderedAccessView Direct3D 11
- Método SetUnorderedAccessView Direct3D 11, interface ID3DX11EffectUnorderedAccessViewVariable
- Interface ID3DX11EffectUnorderedAccessViewVariable Direct3D 11, método SetUnorderedAccessView
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.SetUnorderedAccessView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d665ab5b298e3a7549fb068cf0fcc4cce644765
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989281"
---
# <a name="id3dx11effectunorderedaccessviewvariablesetunorderedaccessview-method"></a>Método ID3DX11EffectUnorderedAccessViewVariable:: SetUnorderedAccessView

Defina um modo de exibição de acesso não ordenado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetUnorderedAccessView(
   ID3D11UnorderedAccessView *pResource
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*origem* 
</dt> <dd>

Tipo: **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\***

Ponteiro para um [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview).

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

[ID3DX11EffectUnorderedAccessViewVariable](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

 





