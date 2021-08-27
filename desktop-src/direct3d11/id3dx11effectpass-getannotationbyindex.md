---
title: Método ID3DX11EffectPass GetAnnotationByIndex (D3dx11effect.h)
description: Obter uma anotação por índice. | Método ID3DX11EffectPass GetAnnotationByIndex (D3dx11effect.h)
ms.assetid: 734eeeca-58c2-4f0c-84d1-2898394a03d6
keywords:
- Método GetAnnotationByIndex Direct3D 11
- Método GetAnnotationByIndex Direct3D 11 , interface ID3DX11EffectPass
- ID3DX11EffectPass interface Direct3D 11 , método GetAnnotationByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetAnnotationByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50cb2f1df512f8726874896b7cb7c2948b6dd33b672a66f7670b75d5520cb6af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046034"
---
# <a name="id3dx11effectpassgetannotationbyindex-method"></a>Método ID3DX11EffectPass::GetAnnotationByIndex

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

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Um índice baseado em zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Um ponteiro para um [**ID3DX11EffectVariable.**](id3dx11effectvariable.md)

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

 

