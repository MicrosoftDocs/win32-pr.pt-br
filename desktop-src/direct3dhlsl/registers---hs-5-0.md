---
title: Registros – hs_5_0
description: Um sombreador de chassi consiste em três fases distintas fase de ponto de controle, fase de bifurcação e fase de junção. Cada fase tem seus próprios conjuntos de registros de entrada e saída.
ms.assetid: 82F689EF-D3F4-40B5-9A2C-1F97F4CE6501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3891130b4a952cb991615dbcc386e245d5eb8abedc2d8cec0b441eb6b3c2fbae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854026"
---
# <a name="registers---hs_5_0"></a>Registros – hs \_ 5 \_ 0

Um sombreador de chassi consiste em três fases distintas: fase do ponto de controle, fase de bifurcação e fase de junção. Cada fase tem seus próprios conjuntos de registros de entrada e saída.

## <a name="control-point-phase"></a>Fase do ponto de controle

a fase \_ do ponto de controle \_ \_ hs é um programa de sombreador com o modelo de registro a seguir.

### <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                     | Contagem                 | R/W | Dimensão | Indexável por r\# | Padrões | Requer DCL |
|---------------------------------------------------|-----------------------|-----|-----------|------------------|----------|--------------|
| Temp de 32 bits (r \# )                                 | 4096(r \# +x \# \[ n \] )    | R/W | 4         | Não               | Nenhum     | Sim          |
| Matriz Temporária indexável de 32 bits (x \# \[ n \] )            | 4096(r \# +x \# \[ n \] )    | R/W | 4         | Sim              | Nenhum     | Sim          |
| Entrada de 32 bits (elemento v \[ v v \] \[ \] )             | 32(element) \* 32(vert) | R   | 4         | Sim              | Nenhum     | Sim          |
| Entrada UINT de 32 bits vOutputControlPointID(23.7)     | 1                     | R   | 1         | Não               | Nenhum     | Sim          |
| PrimitiveID de entrada UINT de 32 bits (vPrim)             | 1                     | R   | 1         | Não               | N/D      | Sim          |
| Elemento em um recurso de entrada (t \# )                | 128                   | R   | 128       | Sim              | Nenhum     | Sim          |
| Sampler (s \# )                                     | 16                    | R   | 1         | Sim              | Nenhum     | Sim          |
| Referência constantBuffer (índice \# \[ cb \] )          | 15                    | R   | 4         | Sim              | Nenhum     | Sim          |
| Referência de ConstantBuffer imediata (índice icb \[ \] ) | 1                     | R   | 4         | Sim (conteúdo)   | Nenhum     | Sim          |



 

### <a name="output-registers"></a>Registros de saída



| Tipo de registro                           | Contagem | R/W | Dimensão | Indexável por r\# | Padrões | Requer DCL |
|-----------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| Elemento de dados de vértice de saída de 32 bits (o \# ) | 32    | W   | 4         | Sim              | Nenhum     | Sim          |



 

Cada registro de saída da fase do ponto de controle do sombreador do chassi é de até 4 vetores, dos quais até 32 registros podem ser declarados. Também há de 1 a 32 pontos de controle de saída declarados, o que dimensiona a quantidade de armazenamento necessária. Vamos nos referir ao número máximo de agregação permitida de escalares em todas as saídas da fase do ponto de controle do sombreador do chassi como \# o máximo de saída de \_ \_ cp.

\#cp \_ output max = \_ 3968 escalares.

Esse limite é baseado em um ponto de design para determinado hardware de 4096 \* armazenamento de 32 bits aqui. O valor da saída do ponto de controle é 3968=4096-128, que é 32(pontos de controle) \* 4(componentes) \* 32(elementos) – 4(componentes) \* 32(elementos). A subtração reserva 128 escalares (um ponto de controle) de espaço dedicado às fases 2 e 3 do sombreador do chassi. A opção de reservar 128 escalares para constantes de patch – em vez de permitir que a quantidade seja simplesmente qualquer um dos escalares 4096 do armazenamento não é usada por pontos de controle de saída – acomoda os limites de outro design de hardware específico. A fase do ponto de controle pode declarar 32 pontos de controle de saída, mas eles simplesmente não podem ser totalmente 32 elementos com quatro componentes cada, porque o armazenamento total seria muito alto.

## <a name="fork-phase"></a>Fase de bifurcação

Os registros a seguir são visíveis no modelo de fase \_ de \_ bifurcação hs.

Os recursos de entrada (t \# ), samplers (s), buffers constantes (cb ) e buffer constante \# imediato (icb) abaixo são todos estado compartilhado com todas as outras fases de sombreador de \# chassi. Ou seja, do ponto de vista da API/DDI, o sombreador de chassi tem um único conjunto de estado de recurso de entrada para todas as fases. Isso ocorre com o fato de que, do ponto de vista da API/DDI, o sombreador de chassi é um único sombreador atômico; as fases dentro dela são detalhes de implementação.

### <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                                                         | Contagem              | R/W | Dimensão                           | Indexável por r\# | Padrões | Requer DCL |
|---------------------------------------------------------------------------------------|--------------------|-----|-------------------------------------|------------------|----------|--------------|
| Temp de 32 bits (r \# )                                                                     | 4096(r \# +x \# \[ n \] ) | R/W | 4                                   | Não               | Nenhum     | Sim          |
| Matriz Temporária indexável de 32 bits (x \# \[ n \] )                                                | 4096(r \# +x \# \[ n \] ) | R/W | 4                                   | Sim              | Nenhum     | Sim          |
| Pontos de Controle de Entrada de 32 bits (elemento \[ vértice vicp \] \[ ) \] (fase de ponto de controle anterior)     | 32 Veja a observação abaixo  | R   | 4(component) \* 32(element) \* 32(vert) | Sim              | Nenhum     | Sim          |
| Pontos de Controle de Saída de 32 bits (elemento de \[ vértice vocp \] \[ ) \] \] (fase pós-ponto de controle) | 32 Veja a observação abaixo  | R   | 4(component) \* 32(element) \* 32(vert) | Sim              | Nenhum     | Sim          |
| PrimitiveID de entrada UINT de 32 bits (vPrim)                                                 | 1                  | R   | 1                                   | Não               | N/D      | Sim          |
| ForkInstanceID de entrada UINT de 32 bits(23.8) (v ForkInstanceID)                              | 1                  | R   | 1                                   | Não               | N/D      | Sim          |
| Elemento em um recurso de entrada (t \# )                                                    | 128                | R   | 128                                 | Sim              | Nenhum     | Sim          |
| Sampler (s \# )                                                                         | 16                 | R   | 1                                   | Sim              | Nenhum     | Sim          |
| Referência constantBuffer (índice \# \[ cb \] )                                              | 15                 | R   | 4                                   | Sim              | Nenhum     | Sim          |
| Referência de ConstantBuffer imediata (índice icb \[ \] )                                     | 1                  | R   | 4                                   | Sim (conteúdo)   | Nenhum     | Sim          |



 

> [!Note]
> As declarações do vicp (registro de ponto de controle de entrada) da fase de bifurcação do sombreador do chassi devem ser qualquer subconjunto, ao longo do eixo do elemento, da entrada do ponto de controle do sombreador de chassi (fase de ponto de \[ \] pré-controle). Da mesma forma, as declarações para inserir os pontos de controle de saída (vocp) devem ser qualquer subconjunto, ao longo do eixo do elemento, dos pontos de controle de saída do sombreador de chassi (fase de ponto de \[ \] pós-controle).
> 
> Ao longo do eixo de vértice, o número de pontos de controle a serem lidos para cada um dos vicp e vocp deve ser semelhante a um subconjunto da contagem de pontos de controle de entrada do sombreador de chassi e contagem de pontos de controle de saída do sombreador de \[ \] chassi, respectivamente. Por exemplo, se o eixo de vértice dos registros vocp for declarado com n vértices, isso disponibiliza os pontos de controle de saída da fase do ponto de controle \[ 0..n-1 como entrada somente leitura para a fase de \] bifurcação.

### <a name="output-registers"></a>Registros de saída



| Registre-se                                        | Contagem               | R/W | Dimensão | Indexável por r\# | Padrões | Requer DCL |
|-------------------------------------------------|---------------------|-----|-----------|------------------|----------|--------------|
| Elemento de dados constante patch de saída de 32 bits (o \# ) | 32 Consulte a observação 1 abaixo | W   | 4         | Sim              | Nenhum     | Sim          |



 

> [!Note]  
> As saídas da fase de bifurcação e junção do sombreador envoltória são um conjunto compartilhado de registros de vetor 4 4. As saídas de cada programa de fase de bifurcação ou junção não podem se sobrepor entre si. Os valores interpretados pelo sistema, como TessFactors, são provenientes desse espaço.

## <a name="join-phase"></a>Fase de ingresso

Os seguintes registros são visíveis no modelo de \_ fase de junção HS \_ . Há três conjuntos de registros de entrada: pontos de controle de entrada de fase de ponto de controle (vicp), pontos de controle de saída de fase de ponto de controle vocp (vocp) e constantes de patch (VCP). o VPC é a saída agregada de todos os programas de fase de bifurcação do envoltória Shader. Os registros de saída da fase de junção do sombreador envoltória \# estão no mesmo espaço de registro que as saídas da fase de bifurcação do sombreador hulll.

Os recursos de entrada (t \# ), os exemplos (s \# ), os buffers de constante (CB \# ) e o buffer de constante (ICB) abaixo são todos os Estados compartilhados com todas as outras fases do sombreador envoltória. Ou seja, do ponto de vista da API/DDI, o sombreador envoltória tem um único conjunto de estado de recurso de entrada para todas as fases. Isso vai com o fato de que, do ponto de vista da API/DDI, o sombreador envoltória é um único sombreador atômico; as fases dentro dela são detalhes da implementação.

### <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                                                       | Contagem               | R/W | Dimensão                           | Indexável por r\# | Padrões | Requer DCL |
|-------------------------------------------------------------------------------------|---------------------|-----|-------------------------------------|------------------|----------|--------------|
| Temp de 32 bits (r \# )                                                                   | 4096 (r \# + x \# \[ n \] )  | R/W | 4                                   | Não               | Nenhum     | Sim          |
| Matriz temporária indexável de 32 bits (x \# \[ n \] )                                              | 4096 (r \# + x \# \[ n \] )  | R/W | 4                                   | Sim              | Nenhum     | Sim          |
| Pontos de controle de entrada de 32 bits \[ ( \] \[ elemento \] de vértice vicp) (fase de ponto de pré-controle)   | 32 consulte a observação 1 abaixo | R   | 4 (componente) \* 32 (elemento) \* 32 (Vert) | Sim              | Nenhum     | Sim          |
| Pontos de controle de saída de 32 bits ( \[ elemento de vértice vocp \] \[ \] ) (fase de ponto de pós-controle) | 32 consulte a observação 1 abaixo | R   | 4 (componente) \* 32 (elemento) \* 32 (Vert) | Sim              | Nenhum     | Sim          |
| Entrada de 32 bits ( \[ elemento VPC \] ) (dados constantes de patch)                                 | 32 consulte a observação 2 abaixo | R   | 4                                   | Sim              | Nenhum     | Sim          |
| Primitivaid de entrada UINT de 32 bits (vPrim)                                               | 1                   | R   | 1                                   | Não               | N/D      | Sim          |
| JoinInstanceID de entrada UINT de 32 bits (vJoinInstanceID)                                  | 1                   | R   | 1                                   | Não               | N/D      | Sim          |
| Elemento em um recurso de entrada (t \# )                                                  | 128                 | R   | 128                                 | Sim              | Nenhum     | Sim          |
| Amostra (s \# )                                                                       | 16                  | R   | 1                                   | Sim              | Nenhum     | Sim          |
| Referência de ConstantBuffer ( \# \[ índice CB \] )                                            | 15                  | R   | 4                                   | Sim              | Nenhum     | Sim          |
| Referência imediata de ConstantBuffer ( \[ índice de ICB \] )                                   | 1                   | R   | 4                                   | Sim (conteúdo)   | Nenhum     | Sim          |



 

**Observação 1:** As declarações do vicp (registro de ponto de controle de entrada) da fase de junção do sombreador do chassi devem ser qualquer subconjunto, ao longo do eixo do elemento, da entrada do ponto de controle do sombreador de chassi (fase de ponto de \[ \] pré-controle). Da mesma forma, as declarações para inserir os pontos de controle de saída (vocp) devem ser qualquer subconjunto, ao longo do eixo do elemento, dos pontos de controle de saída do sombreador de chassi (fase de ponto de \[ \] pós-controle).

Ao longo do eixo de vértice, o número de pontos de controle a serem lidos para cada um dos vicp e vocp deve ser semelhante a um subconjunto da contagem de pontos de controle de entrada do sombreador de chassi e contagem de pontos de controle de saída do sombreador de \[ \] chassi, respectivamente. Por exemplo, se o eixo de vértice dos registros vocp for declarado com n vértices, isso disponibiliza os pontos de controle de saída da fase do ponto de controle \[ 0..n-1 como entrada somente leitura para a fase de \] junção.

**Observação 2:** Além da entrada do ponto de controle, a fase de junção do sombreador de chassi também vê como entrada os dados constantes de patch calculados pelos programas de fase de bifurcação do sombreador de chassi. Isso aparece na fase de bifurcação do sombreador do chassi conforme o vpc \# é registrado. Os registros vpc de entrada da fase de junção do sombreador de chassi compartilham o mesmo espaço de registro que a saída da fase de bifurcação do sombreador do \# \# chassi. As declarações dos registros de o não devem se sobrepor a nenhum programa de fase de bifurcação do sombreador de chassi declaração de saída; a fase de junção do sombreador de chassi está adicionando à saída de dados constantes do patch agregado para o sombreador de \# \# chassi.

### <a name="output-registers"></a>Registros de saída



| Tipo de registro                                   | Contagem             | R/W | Dimensão | Indexável por r\# | Padrões | Requer DCL |
|-------------------------------------------------|-------------------|-----|-----------|------------------|----------|--------------|
| Elemento de dados constante patch de saída de 32 bits (o \# ) | 32 Veja a observação abaixo | W   | 4         | Sim              | Nenhum     | Sim          |



 

> [!Note]  
> As saídas da bifurcação e da fase de junção do sombreador de chassi são um conjunto compartilhado de quatro registros de quatro vetores. As saídas de cada programa de fase de bifurcação ou junção não podem se sobrepor entre si. Valores interpretados pelo sistema, como o TessFactors, são lançados desse espaço.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




