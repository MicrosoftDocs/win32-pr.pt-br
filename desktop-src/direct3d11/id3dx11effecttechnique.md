---
title: Interface ID3DX11EffectTechnique (D3dx11effect. h)
description: Uma interface ID3DX11EffectTechnique é uma coleção de passagens. O tempo de vida de um objeto ID3DX11EffectTechnique é igual ao tempo de vida de seu objeto ID3DX11Effect pai.
ms.assetid: 63d52cac-287d-4432-bf2b-7b4e67e525e6
keywords:
- Interface ID3DX11EffectTechnique Direct3D 11
- Interface ID3DX11EffectTechnique Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e582d8f94b2dbcbb2052a8cf3a59d8ba514367cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968688"
---
# <a name="id3dx11effecttechnique-interface"></a>Interface ID3DX11EffectTechnique

Uma interface **ID3DX11EffectTechnique** é uma coleção de passagens.

O tempo de vida de um objeto **ID3DX11EffectTechnique** é igual ao tempo de vida de seu objeto [**ID3DX11Effect**](id3dx11effect.md) pai.

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX11EffectTechnique** tem esses métodos.



| Método                                                                        | Descrição                                                           |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**ComputeStateBlockMask**](id3dx11effecttechnique-computestateblockmask.md) | Compute uma máscara de bloco de estado para permitir/impedir alterações de estado.<br/> |
| [**GetAnnotationByIndex**](id3dx11effecttechnique-getannotationbyindex.md)   | Obter uma anotação por índice.<br/>                                |
| [**GetAnnotationByName**](id3dx11effecttechnique-getannotationbyname.md)     | Obter uma anotação por nome.<br/>                                 |
| [**GetDesc**](id3dx11effecttechnique-getdesc.md)                             | Obtenha uma descrição técnica.<br/>                               |
| [**GetPassByIndex**](id3dx11effecttechnique-getpassbyindex.md)               | Obter uma passagem por índice.<br/>                                       |
| [**GetPassByName**](id3dx11effecttechnique-getpassbyname.md)                 | Obter uma passagem por nome.<br/>                                        |
| [**IsValid**](id3dx11effecttechnique-isvalid.md)                             | Teste uma técnica para ver se ela contém uma sintaxe válida.<br/>       |



 

## <a name="remarks"></a>Comentários

Um efeito contém uma ou mais técnicas; cada técnica contém uma ou mais passagens; cada passagem contém atribuições de estado.

Para obter uma interface de técnica de efeito, chame um método como [**ID3DX11Effect:: GetTechniqueByName**](id3dx11effect-gettechniquebyname.md).

> [!Note]  
> O SDK do DirectX não fornece nenhum binário compilado para efeitos. Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos. Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Efeitos 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfaces D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





