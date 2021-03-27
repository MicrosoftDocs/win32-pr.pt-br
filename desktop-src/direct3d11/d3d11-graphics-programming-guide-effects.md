---
title: Efeitos (Direct3D 11)
description: Um efeito do DirectX é uma coleção de estado de pipeline, definida por expressões escritas em HLSL e alguma sintaxe específica para a estrutura de efeito.
ms.assetid: d52a2cad-eac9-4442-9ee5-114bebe0f245
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8952a35e1212f7d50956cc54e7a046db9f87b3b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641374"
---
# <a name="effects-direct3d-11"></a>Efeitos (Direct3D 11)

Um efeito do DirectX é uma coleção de estado de pipeline, definida por expressões escritas em [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-reference) e alguma sintaxe específica para a estrutura de efeito.

Depois de compilar um efeito, use as APIs de estrutura de efeito para renderizar. A funcionalidade de efeito pode variar de algo tão simples quanto um sombreador de vértice que transforma a geometria e um sombreador de pixel que gera uma cor sólida, para uma técnica de renderização que requer várias passagens, usa cada estágio do pipeline de gráficos e manipula o estado do sombreador, bem como o estado do pipeline não associado aos sombreadores programáveis.

A primeira etapa é organizar o estado que você deseja controlar em um efeito. Isso inclui o estado do sombreador (vértice, envoltória, domínio, geometria, pixel e sombreadores de computação), o estado de textura e amostra usado pelos sombreadores e outro Estado de pipeline não programável. Você pode criar um efeito na memória como uma cadeia de caracteres de texto, mas, normalmente, o tamanho é grande o suficiente para que seja útil armazenar o estado de efeito em um arquivo de efeito (um arquivo de texto que termina em uma extensão. FX). Para usar um efeito, você deve compilá-lo (para verificar a sintaxe do HLSL, bem como a sintaxe da estrutura de efeito), inicializar o estado do efeito por meio de chamadas à API e modificar o loop de renderização para chamar as APIs de renderização.

Um efeito encapsula todo o estado de renderização exigido por um efeito específico em uma única função de renderização chamada técnica. Uma passagem é um subconjunto de uma técnica que contém o estado de renderização. Para implementar um efeito de renderização de várias passagens, implemente um ou mais passos dentro de uma técnica. Por exemplo, digamos que você queria renderizar uma geometria com um conjunto de buffers de profundidade/estêncil e, em seguida, desenhar alguns sprites sobre isso. Você pode implementar a renderização de geometria na primeira passagem e o desenho sprite na segunda passagem. Para renderizar o efeito, basta renderizar as duas passagens em seu loop de processamento. Você pode implementar qualquer número de técnicas em um efeito. É claro que quanto maior o número de técnicas, maior o tempo de compilação para o efeito. Uma maneira de explorar essa funcionalidade é criar efeitos com técnicas que são projetadas para serem executadas em hardwares diferentes. Isso permite que um aplicativo faça o downgrade do desempenho com base nos recursos de hardware detectados.

Um conjunto de técnicas pode ser agrupado em um grupo (que usa a sintaxe "fxgroup"). As técnicas podem ser agrupadas de qualquer forma. Por exemplo, vários grupos podem ser criados, um por material; cada material pode ter uma técnica para cada nível de hardware; cada técnica teria um conjunto de passagens que definem o material no hardware específico.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                                | Descrição                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Organizando o estado em um efeito](d3d11-graphics-programming-guide-effects-organize.md)<br/>                    | Com o Direct3D 11, o estado do efeito para determinados estágios de pipeline é organizado por estruturas.<br/>                                                                   |
| [Interfaces do sistema de efeito](d3d11-graphics-programming-guide-effects-interfaces.md)<br/>                       | O sistema de efeitos define várias interfaces para o gerenciamento do estado de efeito.<br/>                                                                                  |
| [Especializando interfaces](d3d11-graphics-reference-effect-specializing.md)<br/>                               | O [**ID3DX11EffectVariable**](id3dx11effectvariable.md) tem vários métodos para converter a interface no tipo específico de interface de que você precisa.<br/> |
| [Interfaces e classes em efeitos](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md)<br/>  | Há várias maneiras de usar classes e interfaces nos efeitos 11.<br/>                                                                                         |
| [Renderizando um efeito](d3d11-graphics-programming-guide-effects-render.md)<br/>                                | Um efeito pode ser usado para armazenar informações ou para renderizar usando um grupo de estado.<br/>                                                                         |
| [Clonando um efeito](d3d11-graphics-programming-guide-effects-cloning.md)<br/>                                 | A clonagem de um efeito cria uma segunda cópia praticamente idêntica do efeito.<br/>                                                                                 |
| [Sintaxe de fluxo horizontal](d3d11-graphics-reference-effect-streamout.md)<br/>                                        | Um sombreador Geometry com fluxo horizontal é declarado com uma sintaxe específica.<br/>                                                                                  |
| [Diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md)<br/> | Este tópico mostra as diferenças entre os efeitos 10 e 11.<br/>                                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

