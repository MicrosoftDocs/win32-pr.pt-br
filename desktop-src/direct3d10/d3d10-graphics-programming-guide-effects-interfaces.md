---
description: 'O sistema de efeito define várias interfaces para gerenciar o estado do efeito. Há dois tipos de interfaces: aquelas usadas pelo runtime para renderizar um efeito e interfaces de reflexão para obter e definir variáveis de efeito.'
ms.assetid: 068d49d2-0e14-4080-9fee-20d984f22545
title: Interfaces do sistema de efeito (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d5d640b31d0d1db9ac9b58ed166b45acff762b30edc0e71f1d7138b5818b3e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128388"
---
# <a name="effect-system-interfaces-direct3d-10"></a>Interfaces do sistema de efeito (Direct3D 10)

O sistema de efeito define várias interfaces para gerenciar o estado do efeito. Há dois tipos de interfaces: aquelas usadas pelo runtime para renderizar um efeito e interfaces de reflexão para obter e definir variáveis de efeito.

-   [Interfaces de runtime de efeito](#effect-runtime-interfaces)
-   [Interfaces de reflexão de efeito](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a>Interfaces de runtime de efeito

Use interfaces de runtime para renderizar um efeito.



| Runtime Interfaces                                               | Descrição                                                          |
|------------------------------------------------------------------|----------------------------------------------------------------------|
| [**ID3D10Effect Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                   | Coleção de uma ou mais técnicas para renderização.                  |
| [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))                 | Uma interface para adicionar comportamentos personalizados ao ler arquivos de inclusão. |
| [**ID3D10EffectPass Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)           | Uma coleção de atribuições de estado.                                   |
| [**ID3D10EffectPool Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)           | Crie um local de memória para que as variáveis sejam compartilhadas entre efeitos. |
| [**ID3D10EffectTechnique Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique) | Uma coleção de uma ou mais passagens.                                  |



 

## <a name="effect-reflection-interfaces"></a>Interfaces de reflexão de efeito

A reflexão é implementada no sistema de efeito para dar suporte ao estado de efeito de leitura (e de escrita). Há várias maneiras de acessar variáveis de efeito.

### <a name="setting-groups-of-effect-state"></a>Definindo grupos de estado de efeito

Use essas interfaces para obter e definir um grupo de estado.



| Interfaces de reflexão                                                                  | Descrição                      |
|----------------------------------------------------------------------------------------|----------------------------------|
| [**ID3D10EffectBlendVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)               | Obter e definir o estado de combinação.         |
| [**ID3D10EffectDepthStencilVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable) | Obter e definir o estado de estêncil de profundidade. |
| [**ID3D10EffectRasterizerVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)     | Obter e definir o estado do rasterizador.    |
| [**ID3D10EffectSamplerVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)           | Obter e definir o estado do sampler.       |



 

### <a name="setting-effect-resources"></a>Definindo recursos de efeito

Use essas interfaces para obter e definir recursos.



| Interfaces de reflexão                                                                          | Descrição                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [**ID3D10EffectConstantBuffer Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | Acessar dados em um buffer de textura ou buffer constante. |
| [**ID3D10EffectDepthStencilViewVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | Acessar dados em um recurso de estêncil de profundidade.            |
| [**ID3D10EffectRenderTargetViewVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | Acessar dados em um destino de renderização.                     |
| [**ID3D10EffectShaderResourceVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | Acessar dados em um recurso de sombreador.                   |



 

### <a name="setting-other-effect-variables"></a>Definindo outras variáveis de efeito

Use essas interfaces para obter e definir o estado pelo tipo de variável.



| Interfaces de reflexão                                                      | Descrição                    |
|----------------------------------------------------------------------------|--------------------------------|
| [**ID3D10EffectMatrixVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable) | Obter e definir uma matriz.          |
| [**ID3D10EffectScalarVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable) | Obter e definir um escalar.          |
| [**ID3D10EffectShaderVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable) | Obter e definir uma variável de sombreador. |
| [**ID3D10EffectStringVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable) | Obter e definir uma cadeia de caracteres.          |
| [**ID3D10EffectType Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                     | Obter um tipo de variável.           |
| [**ID3D10EffectVectorVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable) | Obter e definir um vetor.          |



 

Todas as interfaces de reflexão derivam [**de ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Efeitos](d3d10-graphics-programming-guide-effects.md)
</dt> <dt>

[Guia de Programação para Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
