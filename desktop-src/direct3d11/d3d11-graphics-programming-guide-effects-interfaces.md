---
title: Interfaces do sistema de efeito (Direct3D 11)
description: O sistema de efeitos define várias interfaces para o gerenciamento do estado de efeito.
ms.assetid: 5cba6055-d153-4837-9a08-96efbde5f48f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af76a54be06e52e320743ca945abb31d1d50d213
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635250"
---
# <a name="effect-system-interfaces-direct3d-11"></a>Interfaces do sistema de efeito (Direct3D 11)

O sistema de efeitos define várias interfaces para o gerenciamento do estado de efeito. Há dois tipos de interfaces: aqueles usados pelo tempo de execução para renderizar uma interface de efeito e reflexão para obter e definir variáveis de efeito.

-   [Interfaces de tempo de execução de efeito](#effect-runtime-interfaces)
-   [Interfaces de reflexão de efeito](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a>Interfaces de tempo de execução de efeito

Use interfaces de tempo de execução para renderizar um efeito.



| Interfaces de tempo de execução                                       | Description                                                    |
|----------------------------------------------------------|----------------------------------------------------------------|
| [**ID3DX11Effect**](id3dx11effect.md)                   | Coleção de um ou mais grupos e técnicas para renderização. |
| [**ID3DX11EffectPass**](id3dx11effectpass.md)           | Uma coleção de atribuições de estado.                             |
| [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md) | Uma coleção de um ou mais passos.                            |
| [**ID3DX11EffectGroup**](id3dx11effectgroup.md)         | Uma coleção de uma ou mais técnicas.                        |



 

## <a name="effect-reflection-interfaces"></a>Interfaces de reflexão de efeito

A reflexão é implementada no sistema de efeitos para dar suporte ao estado de efeito de leitura (e gravação). Há várias maneiras de acessar variáveis de efeito.

### <a name="setting-groups-of-effect-state"></a>Definindo grupos de estado de efeito

Use essas interfaces para obter e definir um grupo de estado.



| Interfaces de reflexão                                                          | Description                      |
|--------------------------------------------------------------------------------|----------------------------------|
| [**ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md)               | Obter e definir o estado de mesclagem.         |
| [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md) | Obter e definir o estado de estêncil de profundidade. |
| [**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)     | Obter e definir o estado do rasterizador.    |
| [**ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md)           | Obter e definir o estado de amostra.       |



 

### <a name="setting-effect-resources"></a>Definindo recursos de efeito

Use essas interfaces para obter e definir recursos.



| Interfaces de reflexão                                                                        | Description                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)                           | Acessar dados em um buffer de textura ou buffer de constantes. |
| [**ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md)       | Acesse dados em um recurso de estêncil de profundidade.            |
| [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)       | Acessar dados em um destino de renderização.                     |
| [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)           | Acessar dados em um recurso de sombreador.                   |
| [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md) | Acesse dados em uma exibição de acesso não ordenada.            |



 

### <a name="setting-other-effect-variables"></a>Definindo outras variáveis de efeito

Use essas interfaces para obter e definir o estado pelo tipo de variável.



| Interfaces de reflexão                                                            | Description               |
|----------------------------------------------------------------------------------|---------------------------|
| [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) | Obter uma instância de classe.     |
| [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)         | Obter e definir uma interface. |
| [**ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md)               | Obter e definir uma matriz.     |
| [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)               | Obter e definir um escalar.     |
| [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)               | Obter uma variável de sombreador.    |
| [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)               | Obter e definir uma cadeia de caracteres.     |
| [**ID3DX11EffectType**](id3dx11effecttype.md)                                   | Obter um tipo de variável.      |
| [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)               | Obter e definir um vetor.     |



 

Todas as interfaces de reflexão derivam de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Efeitos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[Guia de programação para Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

 




