---
title: Interface ID3DX11EffectPass (D3dx11effect. h)
description: Uma interface ID3DX11EffectPass encapsula as atribuições de estado dentro de uma técnica. O tempo de vida de um objeto ID3DX11EffectPass é igual ao tempo de vida de seu objeto ID3DX11Effect pai.
ms.assetid: 4d86c362-b0f8-4396-86de-c7c89710f46d
keywords:
- Interface ID3DX11EffectPass Direct3D 11
- Interface ID3DX11EffectPass Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectPass
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33b24fe0154e447cd993e8e7e939a9a023ed37183a56980dab8f5d803a0ea41e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045970"
---
# <a name="id3dx11effectpass-interface"></a>Interface ID3DX11EffectPass

Uma interface **ID3DX11EffectPass** encapsula as atribuições de estado dentro de uma técnica.

O tempo de vida de um objeto **ID3DX11EffectPass** é igual ao tempo de vida de seu objeto [**ID3DX11Effect**](id3dx11effect.md) pai.

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX11EffectPass** tem esses métodos.



| Método                                                                   | Descrição                                                       |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------|
| [**Usar**](id3dx11effectpass-apply.md)                                 | Defina o estado contido em uma passagem para o dispositivo.<br/>       |
| [**ComputeStateBlockMask**](id3dx11effectpass-computestateblockmask.md) | Gere uma máscara para permitir/impedir alterações de estado.<br/> |
| [**GetAnnotationByIndex**](id3dx11effectpass-getannotationbyindex.md)   | Obter uma anotação por índice.<br/>                            |
| [**GetAnnotationByName**](id3dx11effectpass-getannotationbyname.md)     | Obter uma anotação por nome.<br/>                             |
| [**GetComputeShaderDesc**](id3dx11effectpass-getcomputeshaderdesc.md)   | Obtenha uma descrição do sombreador de computação.<br/>                      |
| [**GetDesc**](id3dx11effectpass-getdesc.md)                             | Obtenha uma descrição de Pass.<br/>                                |
| [**GetDomainShaderDesc**](id3dx11effectpass-getdomainshaderdesc.md)     | Obtenha uma descrição do sombreador de domínio.<br/>                       |
| [**GetGeometryShaderDesc**](id3dx11effectpass-getgeometryshaderdesc.md) | Obtenha uma descrição do sombreador Geometry.<br/>                     |
| [**GetHullShaderDesc**](id3dx11effectpass-gethullshaderdesc.md)         | Obtenha a descrição de envoltória-Shader.<br/>                           |
| [**GetPixelShaderDesc**](id3dx11effectpass-getpixelshaderdesc.md)       | Obtenha uma descrição do sombreador de pixel.<br/>                        |
| [**GetVertexShaderDesc**](id3dx11effectpass-getvertexshaderdesc.md)     | Obter uma descrição de sombreador de vértice.<br/>                       |
| [**IsValid**](id3dx11effectpass-isvalid.md)                             | Teste uma passagem para ver se ela contém uma sintaxe válida.<br/>        |



 

## <a name="remarks"></a>Comentários

Uma passagem é um bloco de código que define os objetos de estado de renderização e os sombreadores. Uma passagem é declarada dentro de uma técnica.

Para obter uma interface de passagem de efeito, chame um método como [**ID3DX11EffectTechnique:: GetPassByName**](id3dx11effecttechnique-getpassbyname.md).

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

 

 





