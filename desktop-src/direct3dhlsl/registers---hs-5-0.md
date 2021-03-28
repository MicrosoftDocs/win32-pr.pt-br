---
title: Registros-hs_5_0
description: Um sombreador envoltória consiste em três fases distintas fase do ponto de controle, fase de bifurcação e junção. Cada fase tem seus próprios conjuntos de registros de entrada e de saída.
ms.assetid: 82F689EF-D3F4-40B5-9A2C-1F97F4CE6501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aca1377c7ca6b56434c361ba06b01cf659319f6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104298028"
---
# <a name="registers---hs_5_0"></a>Registros-HS \_ 5 \_ 0

Um sombreador envoltória consiste em três fases distintas: fase de ponto de controle, fase de bifurcação e fase de junção. Cada fase tem seus próprios conjuntos de registros de entrada e de saída.

## <a name="control-point-phase"></a>Fase de ponto de controle

\_ \_ a fase de ponto de controle HS \_ é um programa sombreador com o seguinte modelo de registro.

### <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                     | Contagem                 | R/W | Dimensão | Indexável por r\# | Padrões | Requer DCL |
|---------------------------------------------------|-----------------------|-----|-----------|------------------|----------|--------------|
| Temp de 32 bits (r \# )                                 | 4096 (r \# + x \# \[ n \] )    | R/W | 4         | Não               | Nenhum     | Yes          |
| Matriz temporária indexável de 32 bits (x \# \[ n \] )            | 4096 (r \# + x \# \[ n \] )    | R/W | 4         | Sim              | Nenhum     | Yes          |
| Entrada de 32 bits (elemento de vértice de v \[ \] \[ \] )             | 32 (elemento) \* 32 (Vert) | R   | 4         | Sim              | Nenhum     | Yes          |
| vOutputControlPointID de entrada UINT de 32 bits (23.7)     | 1                     | R   | 1         | Não               | Nenhum     | Yes          |
| Primitivaid de entrada UINT de 32 bits (vPrim)             | 1                     | R   | 1         | Não               | N/D      | Sim          |
| Elemento em um recurso de entrada (t \# )                | 128                   | R   | 128       | Yes              | Nenhum     | Yes          |
| Amostra (s \# )                                     | 16                    | R   | 1         | Sim              | Nenhum     | Yes          |
| Referência de ConstantBuffer ( \# \[ índice CB \] )          | 15                    | R   | 4         | Sim              | Nenhum     | Yes          |
| Referência imediata de ConstantBuffer ( \[ índice de ICB \] ) | 1                     | R   | 4         | Sim (conteúdo)   | Nenhum     | Yes          |



 

### <a name="output-registers"></a>Registros de saída



| Tipo de registro                           | Contagem | R/W | Dimensão | Indexável por r\# | Padrões | Requer DCL |
|-----------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| Elemento de dados de vértice de saída de 32 bits (o \# ) | 32    | W   | 4         | Sim              | Nenhum     | Yes          |



 

Cada registro de saída da fase do ponto de controle do sombreador envoltória é de até um vetor 4, do qual até 32 registros podem ser declarados. Também há de 1 a 32 pontos de controle de saída declarados, que escala a quantidade de armazenamento necessária. Vamos nos referir ao número agregado máximo permitido de escalares em toda a saída da fase do ponto de controle do sombreador envoltória como a \# saída de CP \_ \_ Max.

\#saída de CP \_ \_ max = 3968 escalars.

Esse limite se baseia em um ponto de design para determinado hardware de 4096 de \* armazenamento de 32 bits aqui. O valor da saída do ponto de controle é 3968 = 4096-128, que é 32 (pontos de controle) \* 4 (componentes) \* 32 (elementos)-4 (componentes) \* 32 (elementos). A subtração reserva 128 escalars (um ponto de controle) de espaço dedicado ao sombreador envoltória Phase 2 e 3. A escolha de reservar 128 escalares para constantes de patches – em vez de permitir que o valor seja simplesmente o que os escalares 4096 de armazenamento não é usado pelos pontos de controle de saída – acomoda os limites de outro design de hardware específico. A fase de ponto de controle pode declarar 32 pontos de controle de saída, mas eles simplesmente não podem ser totalmente 32 elementos com 4 componentes cada, pois o armazenamento total seria muito alto.

## <a name="fork-phase"></a>Fase de bifurcação

Os seguintes registros são visíveis no modelo de \_ fase de bifurcação HS \_ .

Os recursos de entrada (t \# ), os exemplos (s \# ), os buffers de constante (CB \# ) e o buffer de constante (ICB) abaixo são todos os Estados compartilhados com todas as outras fases do sombreador envoltória. Ou seja, do ponto de vista da API/DDI, o sombreador envoltória tem um único conjunto de estado de recurso de entrada para todas as fases. Isso vai com o fato de que, do ponto de vista da API/DDI, o sombreador envoltória é um único sombreador atômico; as fases dentro dela são detalhes da implementação.

### <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                                                         | Contagem              | R/W | Dimensão                           | Indexável por r\# | Padrões | Requer DCL |
|---------------------------------------------------------------------------------------|--------------------|-----|-------------------------------------|------------------|----------|--------------|
| Temp de 32 bits (r \# )                                                                     | 4096 (r \# + x \# \[ n \] ) | R/W | 4                                   | Não               | Nenhum     | Yes          |
| Matriz temporária indexável de 32 bits (x \# \[ n \] )                                                | 4096 (r \# + x \# \[ n \] ) | R/W | 4                                   | Sim              | Nenhum     | Yes          |
| Pontos de controle de entrada de 32 bits \[ ( \] \[ elemento \] de vértice vicp) (fase de ponto de pré-controle)     | 32 consulte a observação abaixo  | R   | 4 (componente) \* 32 (elemento) \* 32 (Vert) | Yes              | Nenhum     | Yes          |
| Pontos de controle de saída de 32 bits ( \[ elemento de vértice vocp \] \[ \] \] ) (fase de ponto de pós-controle) | 32 consulte a observação abaixo  | R   | 4 (componente) \* 32 (elemento) \* 32 (Vert) | Yes              | Nenhum     | Yes          |
| Primitivaid de entrada UINT de 32 bits (vPrim)                                                 | 1                  | R   | 1                                   | Não               | N/D      | Sim          |
| ForkInstanceID de entrada UINT de 32 bits (23.8) (vForkInstanceID)                              | 1                  | R   | 1                                   | Não               | N/D      | Sim          |
| Elemento em um recurso de entrada (t \# )                                                    | 128                | R   | 128                                 | Yes              | Nenhum     | Yes          |
| Amostra (s \# )                                                                         | 16                 | R   | 1                                   | Sim              | Nenhum     | Yes          |
| Referência de ConstantBuffer ( \# \[ índice CB \] )                                              | 15                 | R   | 4                                   | Sim              | Nenhum     | Yes          |
| Referência imediata de ConstantBuffer ( \[ índice de ICB \] )                                     | 1                  | R   | 4                                   | Sim (conteúdo)   | Nenhum     | Yes          |



 

> [!Note]
> As declarações de registro do ponto de controle de entrada (vicp) da fase de bifurcação do sombreador envoltória devem ser qualquer subconjunto, ao longo do \[ eixo do elemento \] , da entrada do ponto de controle do sombreador envoltória (fase de ponto de pré-controle). Da mesma forma, as declarações para inserir os pontos de controle de saída (vocp) devem ser qualquer subconjunto, ao longo do \[ eixo do elemento \] , dos pontos de controle de saída do sombreador envoltória (fase de ponto de controle posterior).
> 
> Ao longo do \[ eixo de vértices \] , o número de pontos de controle a serem lidos para cada vicp e vocp deve ser, de forma semelhante, um subconjunto da contagem de pontos de controle de entrada do sombreador envoltória e do ponto de controle de saída do sombreador de envoltória, respectivamente. Por exemplo, se o eixo de vértice dos registros vocp for declarado com n vértices, isso tornará os pontos de controle de saída da fase do ponto de controle \[ 0.. n-1 \] disponíveis como entrada somente leitura para a fase de bifurcação.

### <a name="output-registers"></a>Registros de saída



| Registre-se                                        | Contagem               | R/W | Dimensão | Indexável por r\# | Padrões | Requer DCL |
|-------------------------------------------------|---------------------|-----|-----------|------------------|----------|--------------|
| Elemento de dados constante de patch de saída de 32 bits (o \# ) | 32 consulte a observação 1 abaixo | W   | 4         | Sim              | Nenhum     | Yes          |



 

> [!Note]  
> As saídas da fase de bifurcação e junção do sombreador envoltória são um conjunto compartilhado de registros de vetor 4 4. As saídas de cada programa de fase de bifurcação ou junção não podem se sobrepor entre si. Os valores interpretados pelo sistema, como TessFactors, são provenientes desse espaço.

## <a name="join-phase"></a>Fase de junção

Os seguintes registros são visíveis no modelo de \_ fase de junção HS \_ . Há três conjuntos de registros de entrada: pontos de controle de entrada de fase de ponto de controle (vicp), pontos de controle de saída de fase de ponto de controle vocp (vocp) e constantes de patch (VCP). o VPC é a saída agregada de todos os programas de fase de bifurcação do envoltória Shader. Os registros de saída da fase de junção do sombreador envoltória \# estão no mesmo espaço de registro que as saídas da fase de bifurcação do sombreador hulll.

Os recursos de entrada (t \# ), os exemplos (s \# ), os buffers de constante (CB \# ) e o buffer de constante (ICB) abaixo são todos os Estados compartilhados com todas as outras fases do sombreador envoltória. Ou seja, do ponto de vista da API/DDI, o sombreador envoltória tem um único conjunto de estado de recurso de entrada para todas as fases. Isso vai com o fato de que, do ponto de vista da API/DDI, o sombreador envoltória é um único sombreador atômico; as fases dentro dela são detalhes da implementação.

### <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                                                       | Contagem               | R/W | Dimensão                           | Indexável por r\# | Padrões | Requer DCL |
|-------------------------------------------------------------------------------------|---------------------|-----|-------------------------------------|------------------|----------|--------------|
| Temp de 32 bits (r \# )                                                                   | 4096 (r \# + x \# \[ n \] )  | R/W | 4                                   | Não               | Nenhum     | Yes          |
| Matriz temporária indexável de 32 bits (x \# \[ n \] )                                              | 4096 (r \# + x \# \[ n \] )  | R/W | 4                                   | Sim              | Nenhum     | Yes          |
| Pontos de controle de entrada de 32 bits \[ ( \] \[ elemento \] de vértice vicp) (fase de ponto de pré-controle)   | 32 consulte a observação 1 abaixo | R   | 4 (componente) \* 32 (elemento) \* 32 (Vert) | Yes              | Nenhum     | Yes          |
| Pontos de controle de saída de 32 bits ( \[ elemento de vértice vocp \] \[ \] ) (fase de ponto de pós-controle) | 32 consulte a observação 1 abaixo | R   | 4 (componente) \* 32 (elemento) \* 32 (Vert) | Yes              | Nenhum     | Yes          |
| Entrada de 32 bits ( \[ elemento VPC \] ) (dados constantes de patch)                                 | 32 consulte a observação 2 abaixo | R   | 4                                   | Sim              | Nenhum     | Yes          |
| Primitivaid de entrada UINT de 32 bits (vPrim)                                               | 1                   | R   | 1                                   | Não               | N/D      | Sim          |
| JoinInstanceID de entrada UINT de 32 bits (vJoinInstanceID)                                  | 1                   | R   | 1                                   | Não               | N/D      | Sim          |
| Elemento em um recurso de entrada (t \# )                                                  | 128                 | R   | 128                                 | Yes              | Nenhum     | Yes          |
| Amostra (s \# )                                                                       | 16                  | R   | 1                                   | Sim              | Nenhum     | Yes          |
| Referência de ConstantBuffer ( \# \[ índice CB \] )                                            | 15                  | R   | 4                                   | Sim              | Nenhum     | Yes          |
| Referência imediata de ConstantBuffer ( \[ índice de ICB \] )                                   | 1                   | R   | 4                                   | Sim (conteúdo)   | Nenhum     | Yes          |



 

**Observação 1:** As declarações de registro do ponto de controle de entrada (vicp) da fase de junção do sombreador envoltória devem ser qualquer subconjunto, ao longo do \[ eixo do elemento \] , da entrada do ponto de controle do sombreador envoltória (fase de ponto de pré-controle). Da mesma forma, as declarações para inserir os pontos de controle de saída (vocp) devem ser qualquer subconjunto, ao longo do \[ eixo do elemento \] , dos pontos de controle de saída do sombreador envoltória (fase de ponto de controle posterior).

Ao longo do \[ eixo de vértices \] , o número de pontos de controle a serem lidos para cada vicp e vocp deve ser, de forma semelhante, um subconjunto da contagem de pontos de controle de entrada do sombreador envoltória e do ponto de controle de saída do sombreador de envoltória, respectivamente. Por exemplo, se o eixo de vértice dos registros de vocp for declarado com n vértices, isso tornará os pontos de controle de saída da fase do ponto de controle \[ 0.. n-1 \] disponíveis como entrada somente leitura para a fase de junção.

**Observação 2:** Além da entrada do ponto de controle, a fase de junção do sombreador envoltória também vê como entrada os dados constantes do patch computados pelos programas de fase de bifurcação do sombreador envoltória. Isso aparece na fase de bifurcação do sombreador envoltória conforme o VPC é \# registrado. Os registros do VPC de entrada da fase de junção do sombreador envoltória \# compartilham o mesmo espaço de registro que os registros de saída da fase de bifurcação do sombreador envoltória \# . As declarações dos registros do o \# não devem se sobrepor a nenhuma declaração de saída do envoltória Shader Fork Phase \# . a fase de junção do sombreador envoltória está adicionando à saída de dados constante do patch agregado para o sombreador envoltória.

### <a name="output-registers"></a>Registros de saída



| Tipo de registro                                   | Contagem             | R/W | Dimensão | Indexável por r\# | Padrões | Requer DCL |
|-------------------------------------------------|-------------------|-----|-----------|------------------|----------|--------------|
| Elemento de dados constante de patch de saída de 32 bits (o \# ) | 32 consulte a observação abaixo | W   | 4         | Sim              | Nenhum     | Yes          |



 

> [!Note]  
> As saídas da fase de bifurcação e junção do sombreador envoltória são um conjunto compartilhado de registros de vetor 4 4. As saídas de cada programa de fase de bifurcação ou junção não podem se sobrepor entre si. Os valores interpretados pelo sistema, como TessFactors, são provenientes desse espaço.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




