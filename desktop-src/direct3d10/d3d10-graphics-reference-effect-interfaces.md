---
description: 'Esta seção contém informações sobre as seguintes interfaces do sistema de efeitos:'
ms.assetid: ebe0afc7-6261-4c96-a54e-9b491e240c03
title: Interfaces de efeito (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d07e6ecf45f4ef052c7d576849a55d00ef0f877dde7c41fa5dc80b7592761325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118303969"
---
# <a name="effect-interfaces-direct3d-10"></a>Interfaces de efeito (Direct3D 10)

Esta seção contém informações sobre as seguintes interfaces do sistema de efeitos:



| Interfaces                                                                                     | Descrição                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**ID3D10EffectBlendVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)                       | Acessa o estado de combinação.                                            |
| [**ID3D10EffectConstantBuffer Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | Acessa um buffer de textura ou um buffer constante.                  |
| [**ID3D10EffectDepthStencilVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable)         | Acessa o estado de estêncil de profundidade.                                    |
| [**ID3D10EffectDepthStencilViewVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | Acessa uma exibição de estêncil de profundidade.                                   |
| [**ID3D10Effect Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                                                 | Encapsula o estado do pipeline em uma ou mais técnicas de renderização. |
| [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))                                               | Os métodos implementados pelo usuário para leitura incluem arquivos.              |
| [**ID3D10EffectMatrixVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable)                     | Acessa uma matriz.                                               |
| [**ID3D10EffectPass Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)                                         | Encapsula o estado de efeito em uma passagem.                             |
| [**ID3D10EffectPool Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)                                         | Identifica variáveis de efeito compartilhado.                              |
| [**ID3D10EffectRasterizerVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)             | Acessa o estado do rasterizador.                                       |
| [**ID3D10EffectRenderTargetViewVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | Acessa um destino de renderização.                                        |
| [**ID3D10EffectSamplerVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)                   | Acessa o estado do amostrador.                                          |
| [**ID3D10EffectScalarVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable)                     | Acessa uma variável escalar.                                      |
| [**ID3D10EffectShaderResourceVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | Acessa um recurso de sombreador.                                      |
| [**ID3D10EffectShaderVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable)                     | Acessa uma variável de sombreador.                                      |
| [**ID3D10EffectStringVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable)                     | Acessa uma cadeia de caracteres.                                               |
| [**ID3D10EffectTechnique Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique)                               | Encapsula uma ou mais passagens.                                 |
| [**ID3D10EffectType Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                                         | Implementa métodos para acessar variáveis de efeito.               |
| [**ID3D10EffectVectorVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable)                     | Acessa um vetor.                                               |



 

Há dois tipos de interfaces na estrutura de efeito: interfaces de renderização para renderizar um efeito e interfaces de reflexão para obter e definir variáveis de efeito com a API. Todas as interfaces de reflexão derivam [**de ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de efeito](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 
