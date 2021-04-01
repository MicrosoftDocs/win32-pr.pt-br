---
description: 'Esta seção contém informações sobre as seguintes interfaces de sistema de efeito:'
ms.assetid: ebe0afc7-6261-4c96-a54e-9b491e240c03
title: Interfaces de efeito (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1946e7b9e3711bf2d79c0876efca1c533e0ff4ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646278"
---
# <a name="effect-interfaces-direct3d-10"></a>Interfaces de efeito (Direct3D 10)

Esta seção contém informações sobre as seguintes interfaces de sistema de efeito:



| Interfaces                                                                                     | Descrição                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**Interface ID3D10EffectBlendVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)                       | Acessa o estado de mesclagem.                                            |
| [**Interface ID3D10EffectConstantBuffer**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | Acessa um buffer de textura ou um buffer de constantes.                  |
| [**Interface ID3D10EffectDepthStencilVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable)         | Acessa o estado de estêncil de profundidade.                                    |
| [**Interface ID3D10EffectDepthStencilViewVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | Acessa uma exibição de estêncil de profundidade.                                   |
| [**Interface ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                                                 | Encapsula o estado do pipeline em uma ou mais técnicas de renderização. |
| [**Interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))                                               | Métodos implementados pelo usuário para ler arquivos de inclusão.              |
| [**Interface ID3D10EffectMatrixVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable)                     | Acessa uma matriz.                                               |
| [**Interface ID3D10EffectPass**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)                                         | Encapsula o estado de efeito em uma passagem.                             |
| [**Interface ID3D10EffectPool**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)                                         | Identifica variáveis de efeito compartilhado.                              |
| [**Interface ID3D10EffectRasterizerVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)             | Acessa o estado do rasterizador.                                       |
| [**Interface ID3D10EffectRenderTargetViewVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | Acessa um destino de renderização.                                        |
| [**Interface ID3D10EffectSamplerVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)                   | Acessa o estado de amostra.                                          |
| [**Interface ID3D10EffectScalarVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable)                     | Acessa uma variável escalar.                                      |
| [**Interface ID3D10EffectShaderResourceVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | Acessa um recurso de sombreador.                                      |
| [**Interface ID3D10EffectShaderVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable)                     | Acessa uma variável de sombreador.                                      |
| [**Interface ID3D10EffectStringVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable)                     | Acessa uma cadeia de caracteres.                                               |
| [**Interface ID3D10EffectTechnique**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique)                               | Encapsula um ou mais passos.                                 |
| [**Interface ID3D10EffectType**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                                         | Implementa métodos para acessar variáveis de efeito.               |
| [**Interface ID3D10EffectVectorVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable)                     | Acessa um vetor.                                               |



 

Há dois tipos de interfaces na estrutura de efeito: renderizando interfaces para renderizar um efeito e interfaces de reflexão para obter e definir variáveis de efeito com a API. Todas as interfaces de reflexão derivam da [**interface ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de efeito](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 
