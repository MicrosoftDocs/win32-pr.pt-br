---
title: Método ID3DX11Effect GetTechniqueByIndex (D3dx11effect. h)
description: Obtenha uma técnica por índice. | Método ID3DX11Effect GetTechniqueByIndex (D3dx11effect. h)
ms.assetid: ee9c0cc3-0ca1-42e8-bd37-5878fd56cff1
keywords:
- Método GetTechniqueByIndex Direct3D 11
- Método GetTechniqueByIndex Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, método GetTechniqueByIndex
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetTechniqueByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81d3be5ec403fb25ab3a49792ed77fd4d96bf571
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930698"
---
# <a name="id3dx11effectgettechniquebyindex-method"></a>Método ID3DX11Effect:: GetTechniqueByIndex

Obtenha uma técnica por índice.

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

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Um índice de base zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***

Um ponteiro para um [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).

## <a name="remarks"></a>Comentários

Um efeito contém uma ou mais técnicas; cada técnica contém uma ou mais passagens. Você pode acessar uma técnica usando seu nome ou com um índice.

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

 

