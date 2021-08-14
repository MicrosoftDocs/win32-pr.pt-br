---
title: Interface ID3DX11EffectPass (D3dx11effect.h)
description: Uma interface ID3DX11EffectPass encapsula as atribuições de estado dentro de uma técnica. O tempo de vida de um objeto ID3DX11EffectPass é igual ao tempo de vida de seu objeto pai ID3DX11Effect.
ms.assetid: 4d86c362-b0f8-4396-86de-c7c89710f46d
keywords:
- ID3DX11EffectPass interface Direct3D 11
- ID3DX11EffectPass interface Direct3D 11 , descrito
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

O tempo de vida **de um objeto ID3DX11EffectPass** é igual ao tempo de vida de seu objeto [**pai ID3DX11Effect.**](id3dx11effect.md)

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX11EffectPass** tem esses métodos.



| Método                                                                   | Descrição                                                       |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------|
| [**Aplicar**](id3dx11effectpass-apply.md)                                 | De definir o estado contido em uma passagem para o dispositivo.<br/>       |
| [**ComputeStateBlockMask**](id3dx11effectpass-computestateblockmask.md) | Gere uma máscara para permitir/impedir alterações de estado.<br/> |
| [**GetAnnotationByIndex**](id3dx11effectpass-getannotationbyindex.md)   | Obter uma anotação por índice.<br/>                            |
| [**GetAnnotationByName**](id3dx11effectpass-getannotationbyname.md)     | Obter uma anotação por nome.<br/>                             |
| [**GetComputeShaderDesc**](id3dx11effectpass-getcomputeshaderdesc.md)   | Obter uma descrição do sombreador de computação.<br/>                      |
| [**GetDesc**](id3dx11effectpass-getdesc.md)                             | Obter uma descrição de aprovação.<br/>                                |
| [**GetDomainShaderDesc**](id3dx11effectpass-getdomainshaderdesc.md)     | Obter uma descrição do sombreador de domínio.<br/>                       |
| [**GetGeometryShaderDesc**](id3dx11effectpass-getgeometryshaderdesc.md) | Obter uma descrição do sombreador de geometria.<br/>                     |
| [**GetHullShaderDesc**](id3dx11effectpass-gethullshaderdesc.md)         | Obter a descrição do sombreador de chassi.<br/>                           |
| [**GetPixelShaderDesc**](id3dx11effectpass-getpixelshaderdesc.md)       | Obter uma descrição do sombreador de pixel.<br/>                        |
| [**GetVertexShaderDesc**](id3dx11effectpass-getvertexshaderdesc.md)     | Obter uma descrição do sombreador de vértice.<br/>                       |
| [**IsValid**](id3dx11effectpass-isvalid.md)                             | Teste uma passagem para ver se ela contém sintaxe válida.<br/>        |



 

## <a name="remarks"></a>Comentários

Uma passagem é um bloco de código que define objetos de estado de renderização e sombreadores. Uma passagem é declarada dentro de uma técnica.

Para obter uma interface de passagem de efeito, chame um método como [**ID3DX11EffectTechnique::GetPassByName**](id3dx11effecttechnique-getpassbyname.md).

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

 

 





