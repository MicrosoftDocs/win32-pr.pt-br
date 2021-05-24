---
title: Usando valores de System-Generated
description: Os valores gerados pelo sistema são gerados pelo estágio IA (com base na semântica de entrada fornecida pelo usuário) para permitir determinadas eficiências em operações de sombreador.
ms.assetid: eed1e377-4b0e-4958-b6d4-945b2a952ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccdc723d335fd78277051099ec05b43ed954174d
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335200"
---
# <a name="using-system-generated-values"></a>Usando valores de System-Generated

Os valores gerados pelo sistema são gerados pelo estágio IA (com base na [semântica](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)de entrada fornecida pelo usuário) para permitir determinadas eficiências em operações de sombreador.

Anexando dados, como uma ID de instância (visível ao VS), uma ID de vértice (visível para VS) ou uma ID primitiva (visível para GS/PS), um estágio subsequente do sombreador pode procurar esses valores do sistema para otimizar o processamento nesse estágio. Por exemplo, o estágio do VS pode procurar a ID da instância para obter dados adicionais por vértice para o sombreador ou para executar outras operações; os estágios GS e PS podem usar a ID primitiva para capturar dados por primitivos da mesma maneira.

-   [VertexID](#vertexid)
-   [Primitivaid](#primitiveid)
-   [InstanceID](#instanceid)
-   [Exemplo](#example)
-   [Tópicos relacionados](#related-topics)

## <a name="vertexid"></a>VertexID

Uma ID de vértice é usada por cada estágio do sombreador para identificar cada vértice. É um inteiro sem sinal de 32 bits, cujo valor padrão é 0. Ele é atribuído a um vértice quando o primitivo é processado pelo estágio IA. Anexe a semântica de ID de vértice à declaração de entrada do sombreador para informar ao estágio IA para gerar uma ID por vértice.

O IA adicionará uma ID de vértice a cada vértice para uso por estágios de sombreador. Para cada chamada de desenho, a ID de vértice é incrementada em 1. Entre as chamadas desenho indexadas, a contagem é redefinida de volta para o valor inicial. Para [**ID3D11DeviceContext::D rawindexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed) e [**ID3D11DeviceContext::D rawindexedinstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced), a ID de vértice representa o valor de índice. Se a ID do vértice estourar (exceder 2 ³ ² – 1), ela será encapsulada em 0.

Para todos os tipos primitivos, os vértices têm uma ID de vértice associada a eles (independentemente da adjacência).

## <a name="primitiveid"></a>PrimitiveID

Uma ID primitiva é usada por cada estágio do sombreador para identificar cada primitiva. É um inteiro sem sinal de 32 bits, cujo valor padrão é 0. Ele é atribuído a um primitivo quando o primitivo é processado pelo estágio IA. Para informar ao estágio IA para gerar uma ID primitiva, anexe a semântica de ID primitiva à declaração de entrada do sombreador.

O estágio IA adicionará uma ID primitiva a cada primitiva para uso pelo sombreador geometry ou pelo estágio pixel shader (o que for o primeiro estágio ativo após o estágio IA). Para cada chamada de desenho indexada, a ID primitiva é incrementada em 1, no entanto, a ID primitiva é redefinida para 0 sempre que uma nova instância é iniciada. Todas as outras chamadas de desenho não alteram o valor da ID da instância. Se a ID da instância estouro (excede 2 Vezes– 1), ela é envolvada para 0.

O estágio do sombreador de pixel não tem uma entrada separada para uma ID primitiva; no entanto, qualquer entrada de sombreador de pixel que especifica uma ID primitiva usa um modo de interpolação constante.

Não há suporte para gerar automaticamente uma ID primitiva para primitivos adjacentes. Para tipos primitivos com adjacency, como uma faixa de triângulo com adjacency, uma ID primitiva só é mantida para os primitivos interiores (os primitivos não adjacentes), assim como o conjunto de primitivos em uma faixa de triângulo sem adjacency.

## <a name="instanceid"></a>InstanceID

Uma ID de instância é usada por cada estágio do sombreador para identificar a instância da geometria que está sendo processada no momento. É um inteiro sem sinal de 32 bits, cujo valor padrão é 0.

O estágio IA adicionará uma ID de instância a cada vértice se a declaração de entrada do sombreador de vértice incluir a semântica de ID da instância. Para cada chamada de desenho indexada, a ID da instância é incrementada em 1. Todas as outras chamadas de desenho não alteram o valor da ID da instância. Se a ID da instância estouro (excede 2 Vezes– 1), ela é envolvada para 0.

## <a name="example"></a>Exemplo

A ilustração a seguir mostra como os valores do sistema são anexados a uma faixa de triângulo de instância no estágio ia.

![Ilustração de valores do sistema para uma faixa de triângulos instanciada](images/d3d10-ia-example.png)

Estas tabelas mostram os valores do sistema gerados para ambas as instâncias da mesma faixa de triângulos. A primeira instância (instância U) é mostrada em azul, a segunda instância (instância V) é mostrada em verde. As linhas sólidas conectam os vértices aos primitivos, as linhas tracejadas conectam os vértices adjacentes.

As tabelas a seguir mostram os valores gerados pelo sistema para a instância U.



| Dados de vértice    | C,U | D,U | E,U | F,U | G,U | H,U | I,U | J,U | K,U | L,U |
|----------------|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **VertexID**   | 0   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   |
| **InstanceID** | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   |



 



|                 | Valor    | Valor    | Valor    |
|-----------------|-----|-----|-----|
| **PrimitiveID** | 0   | 1   | 2   |
| **InstanceID**  | 0   | 0   | 0   |



 

As tabelas a seguir mostram os valores gerados pelo sistema para a instância V.



| Dados de vértice    | C,V | D,V | E,V | F,V | G,V | H,V | I,V | J,V | K,V | L,V |
|----------------|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **VertexID**   | 0   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   |
| **InstanceID** | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   |



 



|                 |Valor     | Valor    |  Valor   |
|-----------------|-----|-----|-----|
| **PrimitiveID** | 0   | 1   | 2   |
| **InstanceID**  | 1   | 1   | 1   |



 

O assembler de entrada gera as IDs (vértice, primitivo e instância); observe também que cada instância recebe uma ID de instância exclusiva. Os dados terminam com o corte de faixa, que separa cada instância da faixa de triângulo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Estágio do Assembler de Entrada](d3d10-graphics-programming-guide-input-assembler-stage.md)
</dt> </dl>

 

 