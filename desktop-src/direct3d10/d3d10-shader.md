---
description: Opções de compilação HLSL.
ms.assetid: vs|directx_sdk|~\d3d10_shader.htm
title: D3D10_SHADER constantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e965c050d3643e80b493875b27ba5a9b774b351487e191584f40297819758f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118303519"
---
# <a name="d3d10_shader-constants"></a>Constantes de SOMBREADOR D3D10 \_

Opções de compilação HLSL.



| \#Definir                                        | Descrição                                                                                                                                                                                                                                    |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D10 \_ SOMBREADOR \_ EVITAR CONTROLE DE \_ \_ FLUXO             | Diga ao compilador para não permitir o controle de fluxo (quando possível).                                                                                                                                                                                       |
| DEPURAÇÃO DO SOMBREADOR D3D10 \_ \_                            | Insira informações de arquivo/linha/tipo/símbolo de depuração.                                                                                                                                                                                                |
| D3D10 \_ SHADER \_ ENABLE \_ STRICTNESS               | Por padrão, o compilador HLSL desabilita a estrita na sintaxe preterida. Especificar esse sinalizador permite a estrita que pode não permitir a sintaxe herdado.                                                                                         |
| D3D10 \_ SHADER \_ ENABLE \_ BACKWARDS \_ COMPATIBILITY | Isso permite que sombreadores mais antigos compilem para 4 \_ destinos 0.                                                                                                                                                                                         |
| D3D10 \_ SHADER \_ FORCE VS SOFTWARE NÃO \_ \_ \_ \_ OPT     | Compile um sombreador de vértice para o próximo perfil de sombreador mais alto. Essa opção liga a depuração (e otimizações são desligadas).                                                                                                                           |
| D3D10 \_ SHADER \_ FORCE \_ PS \_ SOFTWARE \_ NO \_ OPT     | Compile um sombreador de pixel para o próximo perfil de sombreador mais alto. Essa opção liga a depuração (e otimizações são desligadas).                                                                                                                            |
| ESTRITA \_ \_ IEEE DO SOMBREADOR D3D10 \_                 | Habilita a estrita IEEE.                                                                                                                                                                                                                       |
| SOMBREADOR D3D10 \_ \_ SEM \_ PRESHADER                    | Desabilita pré-sombreadores. Usar esse sinalizador fará com que o compilador não estornar a expressão estática para avaliação.                                                                                                                                 |
| NÍVEL DE OTIMIZAÇÃO DO SOMBREADOR D3D100 \_ \_ \_             | Nível de otimização mais baixo. Pode produzir código mais lento, mas fará isso mais rapidamente. Isso pode ser útil em um ciclo de desenvolvimento de sombreador altamente iterativo.                                                                                             |
| D3D10 NÍVEL DE \_ OTIMIZAÇÃO \_ DO \_ SOMBREADOR1             | Segundo nível de otimização mais baixo.                                                                                                                                                                                                              |
| NÍVEL DE OTIMIZAÇÃO DO SOMBREADOR D3D102 \_ \_ \_             | Segundo nível de otimização mais alto.                                                                                                                                                                                                             |
| NÍVEL DE OTIMIZAÇÃO DO SOMBREADOR D3D103 \_ \_ \_             | Nível de otimização mais alto. Produzirá o melhor código possível, mas poderá levar muito mais tempo para fazer isso. Isso será útil para builds finais de um aplicativo em que o desempenho é o fator mais importante.                                 |
| D3D10 \_ SHADER \_ PACK \_ MATRIX \_ ROW \_ MAJOR         | A menos que explicitamente especificado, as matrizes serão empacotadas em ordem de linha principal na entrada e na saída do sombreador.                                                                                                                                   |
| COLUNA PRINCIPAL DA MATRIZ DO SOMBREADOR D3D10 \_ \_ \_ \_ \_      | A menos que explicitamente especificado, as matrizes serão empacotadas em ordem de coluna principal na entrada e na saída do sombreador. Isso geralmente é mais eficiente, pois permite que a multiplicação de matriz de vetor seja executada usando uma série de produtos de ponto. |
| PRECISÃO PARCIAL DO \_ SOMBREADOR D3D10 \_ \_               | Forçar todos os cálculos a serem feitos com precisão parcial; isso pode ser executado mais rapidamente em algum hardware.                                                                                                                                                |
| O SOMBREADOR D3D10 \_ PREFERE O CONTROLE DE \_ \_ \_ FLUXO            | Diga ao compilador para usar o controle de fluxo (quando possível).                                                                                                                                                                                             |
| OTIMIZAÇÃO DE IGNORAR \_ SOMBREADOR D3D10 \_ \_               | Ignorar a otimização durante a geração de código; geralmente recomendado apenas para depuração.                                                                                                                                                                |
| VALIDAÇÃO DE IGNORAR \_ SOMBREADOR D3D10 \_ \_                 | Não valide o código gerado em relação a funcionalidades e restrições conhecidas. Use isso somente com sombreadores que foram compilados com êxito no passado. Os sombreadores são sempre validados pelo DirectX antes de eles são definidos para o dispositivo.         |
| AVISOS DO SOMBREADOR D3D10 \_ \_ SÃO \_ \_ ERROS            | Informe o compilador HLSL para tratar todos os avisos como erros ao compilar o código do sombreador. Para o novo código de sombreador, você deve usar essa opção para resolver todos os avisos e garantir o menor possível de defeitos de código difíceis de encontrar.             |



 

Essas constantes são definidas como macros em d3d10shader.h.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes do sombreador](d3d10-graphics-reference-d3d10-shader-constants.md)
</dt> </dl>

 

 



