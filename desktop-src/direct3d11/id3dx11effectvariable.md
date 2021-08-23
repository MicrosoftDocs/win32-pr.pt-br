---
title: Interface ID3DX11EffectVariable (D3dx11effect. h)
description: A interface ID3DX11EffectVariable é a classe base para todas as variáveis de efeito. O tempo de vida de um objeto ID3DX11EffectVariable é igual ao tempo de vida de seu objeto ID3DX11Effect pai.
ms.assetid: 07f1b7d7-c266-49ae-b79a-7a645521df89
keywords:
- Interface ID3DX11EffectVariable Direct3D 11
- Interface ID3DX11EffectVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3340ba231785edb9446c8578d886fca4a28ecbb09e69230d7f8661a5650afa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045804"
---
# <a name="id3dx11effectvariable-interface"></a>Interface ID3DX11EffectVariable

A interface **ID3DX11EffectVariable** é a classe base para todas as variáveis de efeito.

O tempo de vida de um objeto **ID3DX11EffectVariable** é igual ao tempo de vida de seu objeto [**ID3DX11Effect**](id3dx11effect.md) pai.

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX11EffectVariable** tem esses métodos.



| Método                                                                           | Descrição                                            |
|:---------------------------------------------------------------------------------|:-------------------------------------------------------|
| [**Asblend**](id3dx11effectvariable-asblend.md)                                 | Obter uma variável de combinação de efeito.<br/>                |
| [**AsClassInstance**](id3dx11effectvariable-asclassinstance.md)                 | Obtenha uma variável de instância de classe.<br/>              |
| [**AsConstantBuffer**](id3dx11effectvariable-asconstantbuffer.md)               | Obter um buffer de constantes.<br/>                      |
| [**AsDepthStencil**](id3dx11effectvariable-asdepthstencil.md)                   | Obtenha uma variável de estêncil de profundidade.<br/>               |
| [**AsDepthStencilView**](id3dx11effectvariable-asdepthstencilview.md)           | Obtenha uma variável de exibição de estêncil de profundidade.<br/>          |
| [**Asinterface**](id3dx11effectvariable-asinterface.md)                         | Obter uma variável de interface.<br/>                  |
| [**Asmatrix**](id3dx11effectvariable-asmatrix.md)                               | Obter uma variável de matriz.<br/>                      |
| [**Asrasterizador**](id3dx11effectvariable-asrasterizer.md)                       | Obter uma variável de rasterizador.<br/>                  |
| [**AsRenderTargetView**](id3dx11effectvariable-asrendertargetview.md)           | Obter uma variável render-Target-View.<br/>          |
| [**De exemplo**](id3dx11effectvariable-assampler.md)                             | Obter uma variável de amostra.<br/>                     |
| [**Asscaler**](id3dx11effectvariable-asscalar.md)                               | Obter uma variável escalar.<br/>                      |
| [**Asshadr**](id3dx11effectvariable-asshader.md)                               | Obter uma variável de sombreador.<br/>                      |
| [**AsShaderResource**](id3dx11effectvariable-asshaderresource.md)               | Obter uma variável de recurso de sombreador.<br/>             |
| [**AsString**](id3dx11effectvariable-asstring.md)                               | Obter uma variável de cadeia de caracteres.<br/>                      |
| [**AsUnorderedAccessView**](id3dx11effectvariable-asunorderedaccessview.md)     | Obter uma variável de exibição de acesso não ordenado.<br/>      |
| [**Asvector**](id3dx11effectvariable-asvector.md)                               | Obter uma variável de vetor.<br/>                      |
| [**GetAnnotationByIndex**](id3dx11effectvariable-getannotationbyindex.md)       | Obter uma anotação por índice.<br/>                 |
| [**GetAnnotationByName**](id3dx11effectvariable-getannotationbyname.md)         | Obter uma anotação por nome.<br/>                  |
| [**GetDesc**](id3dx11effectvariable-getdesc.md)                                 | Obtenha uma descrição.<br/>                          |
| [**GetElement**](id3dx11effectvariable-getelement.md)                           | Obter um elemento de matriz.<br/>                       |
| [**GetMemberByIndex**](id3dx11effectvariable-getmemberbyindex.md)               | Obter um membro de estrutura por índice.<br/>            |
| [**GetMemberByName**](id3dx11effectvariable-getmemberbyname.md)                 | Obter um membro da estrutura por nome.<br/>             |
| [**GetMemberBySemantic**](id3dx11effectvariable-getmemberbysemantic.md)         | Obtenha um membro de estrutura por semântica.<br/>         |
| [**GetParentConstantBuffer**](id3dx11effectvariable-getparentconstantbuffer.md) | Obter um buffer de constantes.<br/>                      |
| [**GetRawValue**](id3dx11effectvariable-getrawvalue.md)                         | Obter dados.<br/>                                   |
| [**GetType**](id3dx11effectvariable-gettype.md)                                 | Obter informações de tipo.<br/>                       |
| [**IsValid**](id3dx11effectvariable-isvalid.md)                                 | Compare o tipo de dados com os dados armazenados.<br/> |
| [**SetRawValue**](id3dx11effectvariable-setrawvalue.md)                         | Definir dados.<br/>                                   |



 

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

[Efeitos 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfaces D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





