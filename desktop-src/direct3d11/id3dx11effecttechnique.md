---
title: Interface ID3DX11EffectTechnique (D3dx11effect.h)
description: Uma interface ID3DX11EffectTechnique é uma coleção de passagens. O tempo de vida de um objeto ID3DX11EffectTechnique é igual ao tempo de vida de seu objeto pai ID3DX11Effect.
ms.assetid: 63d52cac-287d-4432-bf2b-7b4e67e525e6
keywords:
- ID3DX11EffectTechnique interface Direct3D 11
- ID3DX11EffectTechnique interface Direct3D 11 , descrita
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
ms.openlocfilehash: 4d8970ad1e75f37e8270a013d3830216ae128e41c03d4ad5245ac6ffc7615691
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532348"
---
# <a name="id3dx11effecttechnique-interface"></a>Interface ID3DX11EffectTechnique

Uma interface **ID3DX11EffectTechnique** é uma coleção de passagens.

O tempo de vida de um objeto **ID3DX11EffectTechnique** é igual ao tempo de vida de seu objeto [**pai ID3DX11Effect.**](id3dx11effect.md)

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX11EffectTechnique** tem esses métodos.



| Método                                                                        | Descrição                                                           |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**ComputeStateBlockMask**](id3dx11effecttechnique-computestateblockmask.md) | Compute uma máscara de bloco de estado para permitir/impedir alterações de estado.<br/> |
| [**GetAnnotationByIndex**](id3dx11effecttechnique-getannotationbyindex.md)   | Obter uma anotação por índice.<br/>                                |
| [**GetAnnotationByName**](id3dx11effecttechnique-getannotationbyname.md)     | Obter uma anotação por nome.<br/>                                 |
| [**GetDesc**](id3dx11effecttechnique-getdesc.md)                             | Obter uma descrição da técnica.<br/>                               |
| [**GetPassByIndex**](id3dx11effecttechnique-getpassbyindex.md)               | Obter uma passagem por índice.<br/>                                       |
| [**GetPassByName**](id3dx11effecttechnique-getpassbyname.md)                 | Obter um nome de passagem.<br/>                                        |
| [**IsValid**](id3dx11effecttechnique-isvalid.md)                             | Teste uma técnica para ver se ela contém sintaxe válida.<br/>       |



 

## <a name="remarks"></a>Comentários

Um efeito contém uma ou mais técnicas; cada técnica contém uma ou mais passagens; cada passagem contém atribuições de estado.

Para obter uma interface de técnica de efeito, chame um método como [**ID3DX11Effect::GetTechniqueByName**](id3dx11effect-gettechniquebyname.md).

> [!Note]  
> O SDK do DirectX não fornece binários compilados para efeitos. Você deve usar a origem efeitos 11 para criar seu aplicativo do tipo efeitos. Para obter mais informações sobre como usar a origem dos Efeitos 11, consulte [Diferenças entre efeitos 10 e efeitos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Effects 11 Interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





