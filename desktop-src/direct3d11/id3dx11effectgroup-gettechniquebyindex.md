---
title: Método ID3DX11EffectGroup GetTechniqueByIndex (D3dx11effect.h)
description: Obter uma técnica por índice. | Método ID3DX11EffectGroup GetTechniqueByIndex (D3dx11effect.h)
ms.assetid: b0962957-20d1-4ec6-9f8e-acc7a62c5f4e
keywords:
- Método GetTechniqueByIndex Direct3D 11
- Método GetTechniqueByIndex Direct3D 11 , interface ID3DX11EffectGroup
- ID3DX11EffectGroup interface Direct3D 11 , método GetTechniqueByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetTechniqueByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 654b090b3481a915557569e0801e75b8ad089c66cfca4a893d6f865345088171
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046284"
---
# <a name="id3dx11effectgroupgettechniquebyindex-method"></a>Método ID3DX11EffectGroup::GetTechniqueByIndex

Obter uma técnica por índice.

## <a name="syntax"></a>Sintaxe


```C++
ID3DX11EffectTechnique* GetTechniqueByIndex(
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

Tipo: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***

Um ponteiro para um [**ID3DX11EffectTechnique.**](id3dx11effecttechnique.md)

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

[ID3DX11EffectGroup](id3dx11effectgroup.md)
</dt> </dl>

 

