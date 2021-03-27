---
title: Efeitos 11 interfaces
description: Esta seção contém informações de referência para as interfaces de modelo de objeto de componente (COM) da origem do Effects 11.
ms.assetid: 1b997513-73f7-423a-8af3-1c9fa0d2f469
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215e319720f2afc4cf74f6c49056de35fb59d004
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104967237"
---
# <a name="effects-11-interfaces"></a>Efeitos 11 interfaces

Esta seção contém informações de referência para as interfaces de modelo de objeto de componente (COM) da origem do Effects 11.


## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                   | Descrição                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3DX11Effect**](id3dx11effect.md)<br/>                                                       | Uma interface [**ID3DX11Effect**](id3dx11effect.md) gerencia um conjunto de objetos de estado, recursos e sombreadores para implementar um efeito de renderização.<br/>                                                                                                                                                    |
| [**ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md)<br/>                             | A interface Blend-Variable acessa o estado de mesclagem.<br/>                                                                                                                                                                                                                                                 |
| [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)<br/>             | Acessa uma instância de classe.<br/>                                                                                                                                                                                                                                                                         |
| [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)<br/>                           | Uma interface de buffer constante acessa buffers constantes ou buffers de textura.<br/>                                                                                                                                                                                                                          |
| [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md)<br/>               | Uma interface de profundidade-estêncil-variável acessa o estado de estêncil de profundidade.<br/>                                                                                                                                                                                                                                   |
| [**ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md)<br/>       | Uma interface de profundidade-estêncil-exibição-variável acessa uma exibição de estêncil de profundidade.<br/>                                                                                                                                                                                                                             |
| [**ID3DX11EffectGroup**](id3dx11effectgroup.md)<br/>                                             | A interface [**ID3DX11EffectGroup**](id3dx11effectgroup.md) acessa um grupo de efeitos.<br/> O tempo de vida de um objeto [**ID3DX11EffectGroup**](id3dx11effectgroup.md) é igual ao tempo de vida de seu objeto [**ID3DX11Effect**](id3dx11effect.md) pai.<br/>                               |
| [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)<br/>                     | Acessa uma variável de interface.<br/>                                                                                                                                                                                                                                                                    |
| [**ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md)<br/>                           | Uma interface de matriz-variável acessa uma matriz.<br/>                                                                                                                                                                                                                                                     |
| [**ID3DX11EffectPass**](id3dx11effectpass.md)<br/>                                               | Uma interface [**ID3DX11EffectPass**](id3dx11effectpass.md) encapsula as atribuições de estado dentro de uma técnica.<br/> O tempo de vida de um objeto [**ID3DX11EffectPass**](id3dx11effectpass.md) é igual ao tempo de vida de seu objeto [**ID3DX11Effect**](id3dx11effect.md) pai.<br/>           |
| [**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)<br/>                   | Uma interface de variável rasterizadora acessa o estado do rasterizador.<br/>                                                                                                                                                                                                                                         |
| [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)<br/>       | Uma interface render-Target-View acessa um destino render.<br/>                                                                                                                                                                                                                                           |
| [**ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md)<br/>                         | Uma interface de amostra acessa o estado de amostra.<br/>                                                                                                                                                                                                                                                        |
| [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)<br/>                           | Uma interface de variável escalar de efeito acessa valores escalares.<br/>                                                                                                                                                                                                                                        |
| [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)<br/>           | Uma interface de recurso de sombreador acessa um recurso de sombreador.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)<br/>                           | Uma interface de sombreador-variável acessa uma variável de sombreador.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)<br/>                           | Uma interface de variável de cadeia de caracteres acessa uma variável de cadeia de caracteres.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)<br/>                                     | Uma interface [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md) é uma coleção de passagens.<br/> O tempo de vida de um objeto [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md) é igual ao tempo de vida de seu objeto [**ID3DX11Effect**](id3dx11effect.md) pai.<br/>               |
| [**ID3DX11EffectType**](id3dx11effecttype.md)<br/>                                               | A interface [**ID3DX11EffectType**](id3dx11effecttype.md) acessa variáveis de efeito por tipo.<br/> O tempo de vida de um objeto [**ID3DX11EffectType**](id3dx11effecttype.md) é igual ao tempo de vida de seu objeto [**ID3DX11Effect**](id3dx11effect.md) pai.<br/>                          |
| [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md)<br/> | Acessa uma exibição de acesso não ordenada.<br/>                                                                                                                                                                                                                                                                 |
| [**ID3DX11EffectVariable**](id3dx11effectvariable.md)<br/>                                       | A interface [**ID3DX11EffectVariable**](id3dx11effectvariable.md) é a classe base para todas as variáveis de efeito.<br/> O tempo de vida de um objeto [**ID3DX11EffectVariable**](id3dx11effectvariable.md) é igual ao tempo de vida de seu objeto [**ID3DX11Effect**](id3dx11effect.md) pai.<br/> |
| [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)<br/>                           | Uma interface de vetor-Variable acessa um vetor de quatro componentes.<br/>                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência dos efeitos 11](d3d11-graphics-reference-effects11.md)
</dt> </dl>

 

 





