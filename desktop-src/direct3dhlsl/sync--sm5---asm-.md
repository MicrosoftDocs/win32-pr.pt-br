---
title: sincronização (SM5-ASM)
description: A sincronização do grupo de threads ou a barreira de memória.
ms.assetid: DCA637FE-8F5C-41D0-8B5E-F913463BA387
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be072b51b4a18d9f1408df0907ec0a55131c18d2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988629"
---
# <a name="sync-sm5---asm"></a>sincronização (SM5-ASM)

A sincronização do grupo de threads ou a barreira de memória.



| sincronizar \[ \_ uglobal \|\_ugroup \] \[ \_ g \] \[ \_ t\] |
|-------------------------------------------|



 

## <a name="remarks"></a>Comentários

A **sincronização** tem opções \_ uglobal, \_ ugroup, \_ g e \_ t.

No sombreador de pixel, somente a **\_ uglobal de sincronização** é permitida.

No sombreador de computação, ( \_ uglobal ou \_ ugroup \* ) e/ou \_ g devem ser especificados. \_t é opcional também.

### <a name="_uglobal"></a>\_uglobal

\#Limite de memória global u (UAV).

Todas as \# leituras/gravações da memória anterior de u por este thread na ordem do programa são tornadas visíveis para todos os threads em toda a GPU antes de qualquer \# acesso à memória u subsequente por esse thread. A parte inteira da GPU da definição é substituída por um escopo menor que global em um caso, descrito abaixo.

Isso se aplica a toda a memória UAV associada no estágio atual do sombreador.

\_uglobal está disponível no sombreador de computação ou sombreador de pixel.

Para qualquer UAV associado que não tenha sido declarado pelo sombreador como coerente globalmente, o \_ limite de memória de u uglobal \# só tem visibilidade no grupo de threads do sombreador de computação atual para esse UAV, como se fosse \_ ugroup em vez de \_ uglobal. Esse problema se aplica somente ao sombreador de computação, pois o sombreador de pixel deve declarar todos os UAVs como coerentes globalmente.

### <a name="_ugroup"></a>\_ugroup

\#Limite de memória u (UAV) do escopo do grupo de threads.

Todas as \# leituras ou gravações anteriores da memória de u por este thread na ordem do programa são tornadas visíveis para todos os threads no grupo de threads antes de qualquer \# acesso à memória u subsequente por esse thread.

Isso se aplica a toda a memória UAV associada no estágio atual do sombreador.

\_ugroup está disponível somente no sombreador de computação.

Se \_ ugroup for exposto, para algumas implementações. A vantagem de especificar \_ ugroup em vez de \_ uglobal é que a operação de **sincronização** pode ser concluída mais rapidamente.

Outras implementações não distinguem \_ ugroup de \_ uglobal, portanto ambas as operações são equivalentes e se comportam como \_ uglobal. Os aplicativos podem especificar sua intenção solicitando o escopo mais estreito de **sincronização** necessário.

Mesmo que um determinado UAV seja declarado como coerente globalmente, uma \_ operação de **sincronização** ugroup funcionará com mais eficiência no UAV se uma barreira global não for necessária.

### <a name="_g"></a>\_m

\#limite de g (memória compartilhada do grupo de threads).

Todas as \# leituras ou gravações anteriores da memória por este thread na ordem do programa são tornadas visíveis para todos os threads no grupo de threads antes de qualquer \# acesso à memória de g subsequente por esse thread.

Isso se aplica a toda a memória compartilhada g do grupo de threads atual \# .

\_g está disponível somente no sombreador de computação.

### <a name="_t"></a>\_t

Sincronização de grupo de threads. Todos os threads dentro de um único grupo de threads (aqueles que podem compartilhar o acesso a um conjunto comum de espaço de registro compartilhado) serão executados até o ponto em que atingem essa instrução antes que qualquer thread possa continuar.

\_t não pode ser colocado no controle de fluxo dinâmico, (branches que poderiam variar dentro de um grupo de threads), mas podem estar presentes no controle de fluxo uniforme, onde todos os threads no grupo selecionam o mesmo caminho.

\_t está disponível somente no sombreador de computação.

Veja a seguir uma lista de variantes ' Sync ' do sombreador de cálculo.

-   sincronizar \_ g
-   sincronizar \_ ugroup\*
-   sincronizar \_ uglobal
-   sincronização \_ g \_ t
-   sincronizar \_ ugroup \_ t\*
-   sincronizar \_ uglobal \_ t
-   sincronizar \_ ugroup \_ g\*
-   sincronizar \_ uglobal \_ g
-   sincronizar \_ ugroup \_ g \_ t\*
-   sincronizar \_ uglobal \_ g \_ t

\*Variantes com \_ ugroup podem não ser direcionadas pelo compilador HLSL, de acordo com a discussão anterior na \_ seção ugroup acima.

A listagem de variantes de sincronização de sombreador de pixel inclui \_ somente uglobal de sincronização.

Os limites de memória impedem que as instruções afetadas sejam reordenadas pelos compiladores ou pelo hardware ao longo do limite.

Várias leituras do mesmo endereço por uma invocação de sombreador que não são separadas por barreiras de memória ou gravações no endereço podem ser recolhidas juntas. O mesmo se aplica às gravações. Os acessos separados por uma barreira não podem ser mesclados ou movidos pela barreira.

Os limites de memória não são necessários para operações atômicas para um determinado endereço por threads diferentes para funcionar corretamente. Os limites são necessários quando as operações Atomic e/ou Load/Store precisam ser sincronizadas em relação uma à outra, pois aparecem em threads individuais do ponto de vista de outros threads.

No sombreador de pixel, as instruções de [descarte](discard--sm4---asm-.md) implicam uma cerca de uglobal de sincronização \_ , nas instruções que não podem ser reordenadas pelo **descarte**. \_os uglobal de sincronização em pixels auxiliares (que são executados apenas para dar suporte a derivações) ou pixels descartados podem ou não ter nenhum efeito. Não é permitido que os pixels auxiliares ou descartados gravem em UAVs se, no caso de descarte, as gravações são emitidas após o descarte. Os valores retornados de UAVs não têm permissão para contribuir com cálculos derivados. Portanto, se a sincronização \_ u será atendida ou não por pixels auxiliares ou quando for emitido depois que um descarte for sentido.

cs \_ 4 \_ 0 e cs \_ 4 \_ 1 dão suporte a essa instrução.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Como UAVs estão disponíveis em todos os estágios de sombreador para o Direct3D 11,1, a variante de **sincronização \_ uglobal** desta instrução aplica-se a todos os estágios de sombreador para o tempo de execução do Direct3D 11,1, que está disponível a partir do Windows 8.



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa instrução tem suporte nos seguintes modelos de sombreador:



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | não        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | não        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




