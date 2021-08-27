---
title: Efeitos (Direct3D 11)
description: Saiba mais sobre os efeitos do Direct3D 11. Um efeito é o estado do pipeline, definido por expressões escritas em HLSL e alguma sintaxe específica à estrutura de efeito.
ms.assetid: d52a2cad-eac9-4442-9ee5-114bebe0f245
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fe4cdb204e498a0c6a8f4d5f6e4656446c0f0a3f4d660f2e0e2a33e8515a0e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990096"
---
# <a name="effects-direct3d-11"></a>Efeitos (Direct3D 11)

Um efeito DirectX é uma coleção de estado de pipeline, definida por expressões escritas [em HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-reference) e alguma sintaxe específica à estrutura de efeito.

Depois de compilar um efeito, use as APIs da estrutura de efeito para renderizar. A funcionalidade de efeito pode variar de algo tão simples quanto um sombreador de vértice que transforma geometria e um sombreador de pixel que saída de uma cor sólida, até uma técnica de renderização que requer várias passagens, usa cada estágio do pipeline gráfico e manipula o estado do sombreador, bem como o estado do pipeline não associado aos sombreadores programáveis.

A primeira etapa é organizar o estado que você deseja controlar em um efeito. Isso inclui o estado do sombreador (vértice, chassi, domínio, geometria, pixel e sombreadores de computação), a textura e o estado de amostra usados pelos sombreadores e outro estado de pipeline não programável. Você pode criar um efeito na memória como uma cadeia de caracteres de texto, mas normalmente, o tamanho fica grande o suficiente para armazenar o estado de efeito em um arquivo de efeito (um arquivo de texto que termina em uma extensão .fx). Para usar um efeito, você deve compilá-lo (para verificar a sintaxe HLSL, bem como a sintaxe da estrutura de efeito), inicializar o estado de efeito por meio de chamadas à API e modificar o loop de renderização para chamar as APIs de renderização.

Um efeito encapsula todo o estado de renderização exigido por um efeito específico em uma única função de renderização chamada técnica. Uma passagem é um subconjunto de uma técnica que contém o estado de renderização. Para implementar um efeito de renderização de várias passagens, implemente uma ou mais passagens dentro de uma técnica. Por exemplo, digamos que você quisesse renderizar alguma geometria com um conjunto de buffers de profundidade/estêncil e, em seguida, desenhar alguns sprites sobre isso. Você pode implementar a renderização de geometria na primeira passagem e o desenho de sprite na segunda passagem. Para renderizar o efeito, você simplesmente renderiza ambas as passagens em seu loop de renderização. Você pode implementar qualquer número de técnicas em um efeito. É claro que, quanto maior o número de técnicas, maior o tempo de compilação para o efeito. Uma maneira de explorar essa funcionalidade é criar efeitos com técnicas projetadas para executar em um hardware diferente. Isso permite que um aplicativo downgrade normalmente o desempenho com base nos recursos de hardware detectados.

Um conjunto de técnicas pode ser agrupado em um grupo (que usa a sintaxe "fxgroup"). As técnicas podem ser agrupadas de qualquer maneira. Por exemplo, vários grupos podem ser criados, um por material; cada material pode ter uma técnica para cada nível de hardware; cada técnica teria um conjunto de passagens que definem o material no hardware específico.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                                | Descrição                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Organizando o estado em um efeito](d3d11-graphics-programming-guide-effects-organize.md)<br/>                    | Com o Direct3D 11, o estado de efeito para determinados estágios de pipeline é organizado por estruturas.<br/>                                                                   |
| [Interfaces do sistema de efeito](d3d11-graphics-programming-guide-effects-interfaces.md)<br/>                       | O sistema de efeito define várias interfaces para gerenciar o estado do efeito.<br/>                                                                                  |
| [Especializando interfaces](d3d11-graphics-reference-effect-specializing.md)<br/>                               | [**ID3DX11EffectVariable**](id3dx11effectvariable.md) tem vários métodos para transformar a interface no tipo específico de interface de que você precisa.<br/> |
| [Interfaces e classes em efeitos](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md)<br/>  | Há muitas maneiras de usar classes e interfaces no Effects 11.<br/>                                                                                         |
| [Renderizar um efeito](d3d11-graphics-programming-guide-effects-render.md)<br/>                                | Um efeito pode ser usado para armazenar informações ou renderizar usando um grupo de estado.<br/>                                                                         |
| [Clonando um efeito](d3d11-graphics-programming-guide-effects-cloning.md)<br/>                                 | Clonar um efeito cria uma segunda cópia quase idêntica do efeito.<br/>                                                                                 |
| [Sintaxe do Stream Out](d3d11-graphics-reference-effect-streamout.md)<br/>                                        | Um sombreador de geometria com fluxo de saída é declarado com uma sintaxe específica.<br/>                                                                                  |
| [Diferenças entre efeitos 10 e efeitos 11](d3d11-graphics-programming-guide-effects-differences.md)<br/> | Este tópico mostra as diferenças entre Efeitos 10 e Efeitos 11.<br/>                                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

