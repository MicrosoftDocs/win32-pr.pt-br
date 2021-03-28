---
title: Método ID3DX11EffectGroup GetAnnotationByIndex (D3dx11effect. h)
description: Obter uma anotação por índice. | Método ID3DX11EffectGroup GetAnnotationByIndex (D3dx11effect. h)
ms.assetid: 9d3a54b1-384b-4ed4-96a3-09d6bacafda1
keywords:
- Método GetAnnotationByIndex Direct3D 11
- Método GetAnnotationByIndex Direct3D 11, interface ID3DX11EffectGroup
- Interface ID3DX11EffectGroup Direct3D 11, método GetAnnotationByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetAnnotationByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 663dc8d487552dba521c8e47f9a1eecf6db38122
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173090"
---
# <a name="id3dx11effectgroupgetannotationbyindex-method"></a>Método ID3DX11EffectGroup:: GetAnnotationByIndex

Obter uma anotação por índice.

## <a name="syntax"></a>Sintaxe


```C++
ID3DX11EffectVariable* GetAnnotationByIndex(
   UINT Index
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Índice da anotação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Ponteiro para uma interface [**ID3DX11EffectVariable**](id3dx11effectvariable.md) .

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

[ID3DX11EffectGroup](id3dx11effectgroup.md)
</dt> </dl>

 

