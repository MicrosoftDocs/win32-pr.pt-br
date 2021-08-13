---
title: Effects 11 Interfaces
description: Esta seção contém informações de referência para as interfaces COM (component object model) da fonte Effects 11.
ms.assetid: 1b997513-73f7-423a-8af3-1c9fa0d2f469
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b20713f5a40b2d8b85edb92166b7e64af18fefee62e5267adcffa25356c6f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118537698"
---
# <a name="effects-11-interfaces"></a>Effects 11 Interfaces

Esta seção contém informações de referência para as interfaces COM (component object model) da fonte Effects 11.


## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                   | Descrição                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3DX11Effect**](id3dx11effect.md)<br/>                                                       | Uma [**interface ID3DX11Effect**](id3dx11effect.md) gerencia um conjunto de objetos de estado, recursos e sombreadores para implementar um efeito de renderização.<br/>                                                                                                                                                    |
| [**ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md)<br/>                             | A interface blend-variable acessa o estado blend.<br/>                                                                                                                                                                                                                                                 |
| [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)<br/>             | Acessa uma instância de classe.<br/>                                                                                                                                                                                                                                                                         |
| [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)<br/>                           | Uma interface de buffer constante acessa buffers constantes ou buffers de textura.<br/>                                                                                                                                                                                                                          |
| [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md)<br/>               | Uma interface de variável de estêncil de profundidade acessa o estado de estêncil de profundidade.<br/>                                                                                                                                                                                                                                   |
| [**ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md)<br/>       | Uma interface depth-stencil-view-variable acessa uma exibição de estêncil de profundidade.<br/>                                                                                                                                                                                                                             |
| [**ID3DX11EffectGroup**](id3dx11effectgroup.md)<br/>                                             | A interface [**ID3DX11EffectGroup**](id3dx11effectgroup.md) acessa um grupo efeito.<br/> O tempo de vida [**de um objeto ID3DX11EffectGroup**](id3dx11effectgroup.md) é igual ao tempo de vida de seu objeto [**pai ID3DX11Effect.**](id3dx11effect.md)<br/>                               |
| [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)<br/>                     | Acessa uma variável de interface.<br/>                                                                                                                                                                                                                                                                    |
| [**ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md)<br/>                           | Uma interface de matriz variável acessa uma matriz.<br/>                                                                                                                                                                                                                                                     |
| [**ID3DX11EffectPass**](id3dx11effectpass.md)<br/>                                               | Uma interface [**ID3DX11EffectPass**](id3dx11effectpass.md) encapsula as atribuições de estado dentro de uma técnica.<br/> O tempo de vida [**de um objeto ID3DX11EffectPass**](id3dx11effectpass.md) é igual ao tempo de vida de seu objeto [**pai ID3DX11Effect.**](id3dx11effect.md)<br/>           |
| [**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)<br/>                   | Uma interface rasterizer-variable acessa o estado do rasterizador.<br/>                                                                                                                                                                                                                                         |
| [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)<br/>       | Uma interface de exibição de destino de renderização acessa um destino de renderização.<br/>                                                                                                                                                                                                                                           |
| [**ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md)<br/>                         | Uma interface de amostra acessa o estado do amostrador.<br/>                                                                                                                                                                                                                                                        |
| [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)<br/>                           | Uma interface effect-scalar-variable acessa valores escalares.<br/>                                                                                                                                                                                                                                        |
| [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)<br/>           | Uma interface sombreador-recurso acessa um recurso de sombreador.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)<br/>                           | Uma interface de variável de sombreador acessa uma variável de sombreador.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)<br/>                           | Uma interface de variável de cadeia de caracteres acessa uma variável de cadeia de caracteres.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)<br/>                                     | Uma interface [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md) é uma coleção de passagens.<br/> O tempo de vida de um objeto [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md) é igual ao tempo de vida de seu objeto [**pai ID3DX11Effect.**](id3dx11effect.md)<br/>               |
| [**ID3DX11EffectType**](id3dx11effecttype.md)<br/>                                               | A interface [**ID3DX11EffectType**](id3dx11effecttype.md) acessa variáveis de efeito por tipo.<br/> O tempo de vida [**de um objeto ID3DX11EffectType**](id3dx11effecttype.md) é igual ao tempo de vida de seu objeto [**pai ID3DX11Effect.**](id3dx11effect.md)<br/>                          |
| [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md)<br/> | Acessa uma exibição de acesso não organizado.<br/>                                                                                                                                                                                                                                                                 |
| [**ID3DX11EffectVariable**](id3dx11effectvariable.md)<br/>                                       | A interface [**ID3DX11EffectVariable**](id3dx11effectvariable.md) é a classe base para todas as variáveis de efeito.<br/> O tempo de vida [**de um objeto ID3DX11EffectVariable**](id3dx11effectvariable.md) é igual ao tempo de vida de seu objeto [**pai ID3DX11Effect.**](id3dx11effect.md)<br/> |
| [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)<br/>                           | Uma interface vector-variable acessa um vetor de quatro componentes.<br/>                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de Efeitos 11](d3d11-graphics-reference-effects11.md)
</dt> </dl>

 

 





