---
description: 'O sistema de efeitos define várias interfaces para o gerenciamento do estado de efeito. Há dois tipos de interfaces: aqueles usados pelo tempo de execução para renderizar uma interface de efeito e reflexão para obter e definir variáveis de efeito.'
ms.assetid: 068d49d2-0e14-4080-9fee-20d984f22545
title: Interfaces do sistema de efeito (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b40b21d98bedaec65550343260e7c52e2df1c302
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089046"
---
# <a name="effect-system-interfaces-direct3d-10"></a>Interfaces do sistema de efeito (Direct3D 10)

O sistema de efeitos define várias interfaces para o gerenciamento do estado de efeito. Há dois tipos de interfaces: aqueles usados pelo tempo de execução para renderizar uma interface de efeito e reflexão para obter e definir variáveis de efeito.

-   [Interfaces de tempo de execução de efeito](#effect-runtime-interfaces)
-   [Interfaces de reflexão de efeito](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a>Interfaces de tempo de execução de efeito

Use interfaces de tempo de execução para renderizar um efeito.



| Interfaces de tempo de execução                                               | Descrição                                                          |
|------------------------------------------------------------------|----------------------------------------------------------------------|
| [**Interface ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                   | Coleção de uma ou mais técnicas para renderização.                  |
| [**Interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))                 | Uma interface para adicionar comportamentos personalizados ao ler arquivos de inclusão. |
| [**Interface ID3D10EffectPass**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)           | Uma coleção de atribuições de estado.                                   |
| [**Interface ID3D10EffectPool**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)           | Crie um local de memória para as variáveis a serem compartilhadas entre os efeitos. |
| [**Interface ID3D10EffectTechnique**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique) | Uma coleção de um ou mais passos.                                  |



 

## <a name="effect-reflection-interfaces"></a>Interfaces de reflexão de efeito

A reflexão é implementada no sistema de efeitos para dar suporte ao estado de efeito de leitura (e gravação). Há várias maneiras de acessar variáveis de efeito.

### <a name="setting-groups-of-effect-state"></a>Definindo grupos de estado de efeito

Use essas interfaces para obter e definir um grupo de estado.



| Interfaces de reflexão                                                                  | Descrição                      |
|----------------------------------------------------------------------------------------|----------------------------------|
| [**Interface ID3D10EffectBlendVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)               | Obter e definir o estado de mesclagem.         |
| [**Interface ID3D10EffectDepthStencilVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable) | Obter e definir o estado de estêncil de profundidade. |
| [**Interface ID3D10EffectRasterizerVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)     | Obter e definir o estado do rasterizador.    |
| [**Interface ID3D10EffectSamplerVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)           | Obter e definir o estado de amostra.       |



 

### <a name="setting-effect-resources"></a>Definindo recursos de efeito

Use essas interfaces para obter e definir recursos.



| Interfaces de reflexão                                                                          | Descrição                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [**Interface ID3D10EffectConstantBuffer**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | Acessar dados em um buffer de textura ou buffer de constantes. |
| [**Interface ID3D10EffectDepthStencilViewVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | Acesse dados em um recurso de estêncil de profundidade.            |
| [**Interface ID3D10EffectRenderTargetViewVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | Acessar dados em um destino de renderização.                     |
| [**Interface ID3D10EffectShaderResourceVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | Acessar dados em um recurso de sombreador.                   |



 

### <a name="setting-other-effect-variables"></a>Definindo outras variáveis de efeito

Use essas interfaces para obter e definir o estado pelo tipo de variável.



| Interfaces de reflexão                                                      | Descrição                    |
|----------------------------------------------------------------------------|--------------------------------|
| [**Interface ID3D10EffectMatrixVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable) | Obter e definir uma matriz.          |
| [**Interface ID3D10EffectScalarVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable) | Obter e definir um escalar.          |
| [**Interface ID3D10EffectShaderVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable) | Obter e definir uma variável de sombreador. |
| [**Interface ID3D10EffectStringVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable) | Obter e definir uma cadeia de caracteres.          |
| [**Interface ID3D10EffectType**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                     | Obter um tipo de variável.           |
| [**Interface ID3D10EffectVectorVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable) | Obter e definir um vetor.          |



 

Todas as interfaces de reflexão derivam da [**interface ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Effect](d3d10-graphics-programming-guide-effects.md)
</dt> <dt>

[Guia de programação para Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
