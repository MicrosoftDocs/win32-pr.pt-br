---
description: HLSL opções de compilação.
ms.assetid: vs|directx_sdk|~\d3d10_shader.htm
title: D3D10_SHADER constantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16480e2aceada7f5ed05912eca59cc88886ac9b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457090"
---
# <a name="d3d10_shader-constants"></a>\_Constantes do sombreador d3d10

HLSL opções de compilação.



| \#definir                                        | Descrição                                                                                                                                                                                                                                    |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D10 do \_ sombreador \_ Evite \_ controle de fluxo \_             | Diga ao compilador para não permitir o controle de fluxo (quando possível).                                                                                                                                                                                       |
| \_Depuração do sombreador d3d10 \_                            | Insira as informações de arquivo/linha/tipo/símbolo de depuração.                                                                                                                                                                                                |
| O \_ sombreador d3d10 \_ habilita a \_ restrição               | Por padrão, o compilador HLSL desabilita a restrição na sintaxe preterida. A especificação desse sinalizador habilita a restrição que pode não permitir a sintaxe herdada.                                                                                         |
| D3D10 \_ Shader \_ habilitar \_ compatibilidade com versões anteriores \_ | Isso permite que os sombreadores mais antigos compilem para 4 \_ 0 destinos.                                                                                                                                                                                         |
| D3D10 \_ Shader \_ Force \_ vs \_ software \_ sem \_ aceitar     | Compile um sombreador de vértice para o próximo perfil de sombreador mais alto. Essa opção ativa a depuração (e otimizações desativadas).                                                                                                                           |
| D3D10 \_ Shader \_ Force \_ PS \_ software \_ não \_ aceitar     | Compile um sombreador de pixel para o próximo perfil de sombreador mais alto. Essa opção ativa a depuração (e otimizações desativadas).                                                                                                                            |
| D3D10 do \_ sombreador \_ IEEE \_ estrito                 | Habilita a restrição de IEEE.                                                                                                                                                                                                                       |
| \_Sombreador d3d10 \_ sem \_ preshadr                    | Desabilita os preshaders. O uso desse sinalizador fará com que o compilador não retire a expressão estática para avaliação.                                                                                                                                 |
| \_LEVEL0 de otimização do sombreador d3d10 \_ \_             | Nível de otimização mais baixo. Pode produzir um código mais lento, mas fará isso mais rapidamente. Isso pode ser útil em um ciclo de desenvolvimento de sombreador altamente iterativo.                                                                                             |
| \_LEVEL1 de otimização do sombreador d3d10 \_ \_             | Segundo nível de otimização mais baixo.                                                                                                                                                                                                              |
| \_LEVEL2 de otimização do sombreador d3d10 \_ \_             | Segundo nível de otimização mais alto.                                                                                                                                                                                                             |
| \_LEVEL3 de otimização do sombreador d3d10 \_ \_             | Nível de otimização mais alto. Produzirá o melhor código possível, mas pode levar muito mais tempo para fazer isso. Isso será útil para as compilações finais de um aplicativo em que o desempenho é o fator mais importante.                                 |
| \_Linha de matriz do pacote de sombreador d3d10 \_ \_ \_ \_ principal         | A menos que especificado explicitamente, as matrizes serão empacotadas na ordem de linha principal na entrada e na saída do sombreador.                                                                                                                                   |
| \_Coluna de matriz do pacote de sombreador d3d10 \_ \_ \_ \_ principal      | A menos que especificado explicitamente, as matrizes serão empacotadas na ordem de coluna principal na entrada e na saída do sombreador. Isso geralmente é mais eficiente, pois permite que a multiplicação de matriz de vetor seja executada usando uma série de produtos de ponto. |
| \_Precisão parcial do sombreador d3d10 \_ \_               | Forçar a conclusão de todos os cálculos com precisão parcial; Isso pode ser executado mais rapidamente em alguns hardwares.                                                                                                                                                |
| \_Sombreador d3d10 \_ prefiro o \_ controle de fluxo \_            | Diga ao compilador para usar o controle de fluxo (quando possível).                                                                                                                                                                                             |
| \_Otimização de \_ ignorar SOMBREAdor d3d10 \_               | Ignorar otimização durante geração de código; geralmente recomendado somente para depuração.                                                                                                                                                                |
| \_Validação de \_ ignorar SOMBREAdor d3d10 \_                 | Não valide o código gerado em relação a funcionalidades e restrições conhecidas. Use isso apenas com sombreadores que foram compilados com êxito no passado. Os sombreadores são sempre validados pelo DirectX antes de serem definidos para o dispositivo.         |
| Os \_ avisos do sombreador d3d10 \_ \_ são \_ erros            | Informe o compilador HLSL para tratar todos os avisos como erros ao compilar o código do sombreador. Para obter o novo código de sombreador, você deve usar essa opção para resolver todos os avisos e garantir o menor número possível de defeitos de código difíceis de encontrar.             |



 

Essas constantes são definidas como macros em d3d10shader. h.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes do sombreador](d3d10-graphics-reference-d3d10-shader-constants.md)
</dt> </dl>

 

 



