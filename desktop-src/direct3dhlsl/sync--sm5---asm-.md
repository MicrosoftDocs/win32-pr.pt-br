---
title: sync (sm5 – asm)
description: Sincronização de grupo de threads ou barreira de memória.
ms.assetid: DCA637FE-8F5C-41D0-8B5E-F913463BA387
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c64532669fc94d7d2109c39e501af0825e56434f66b79e20e1641c787a1a58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852856"
---
# <a name="sync-sm5---asm"></a>sync (sm5 – asm)

Sincronização de grupo de threads ou barreira de memória.



| sync \[ \_ uglobal\|\_ugroup \] \[ \_ g \] \[ \_ t\] |
|-------------------------------------------|



 

## <a name="remarks"></a>Comentários

**A** sincronização \_ tem opções uglobal, \_ ugroup, \_ g e \_ t.

No sombreador de pixel, somente **\_ a sincronização uglobal** é permitida.

No sombreador de computação, ( \_ uglobal ou \_ ugroup \* ) e/ou \_ g devem ser especificados. \_t é opcional além disso.

### <a name="_uglobal"></a>\_uglobal

Cerca de \# memória U (UAV) global.

Todas as leituras/gravações anteriores de u memory por esse thread na ordem do programa são visíveis para todos os threads em toda a GPU antes que qualquer u memory subsequente acesse \# \# por esse thread. Toda a parte da GPU da definição é substituída por um escopo menor que global em um caso, descrito abaixo.

Isso se aplica a toda a memória UAV vinculada no estágio do sombreador atual.

\_Uglobal está disponível no sombreador de computação ou sombreador de pixel.

Para qualquer UAV vinculado que não tenha sido declarado pelo sombreador como Globally Coerente, o limite u memory uglobal só tem visibilidade dentro do grupo de threads do sombreador de computação atual para esse UAV, como se fosse ugroup em vez de \_ \# \_ \_ uglobal. Esse problema só se aplica ao sombreador de computação, pois o sombreador de pixel deve declarar todos os UAVs como Globally Coerentes.

### <a name="_ugroup"></a>\_ugroup

Cerca de memória UAV (escopo do grupo \# de threads).

Todas as leituras ou gravações anteriores de u memory por esse thread na ordem do programa são visíveis para todos os threads no grupo de threads antes que qualquer u memory subsequente acesse \# \# por esse thread.

Isso se aplica a toda a memória UAV vinculada no estágio do sombreador atual.

\_Ugroup está disponível apenas no sombreador de computação.

Se \_ ugroup for exposto, para algumas implementações. A vantagem de especificar \_ ugroup em vez de \_ uglobal é que a operação **de** sincronização pode ser concluída mais rapidamente.

Outras implementações não distinguem \_ ugroup de uglobal, portanto, ambas as operações são equivalentes e se comportam \_ \_ como uglobal. Os aplicativos podem especificar sua intenção solicitando o escopo mais estreito de **sincronização** necessário.

Mesmo se um UAV específico for declarado como Globally Coerente, uma operação de sincronização de ugroup funcionará com mais eficiência nesse UAV se uma barreira global não \_ for necessária. 

### <a name="_g"></a>\_G

g \# (memória compartilhada do grupo de threads).

Todas as leituras ou gravações de memória g anteriores por esse thread na ordem do programa são visíveis para todos os threads no grupo de threads antes que qualquer g posterior acesse a memória \# \# por esse thread.

Isso se aplica a toda a memória compartilhada g do grupo de \# threads atual.

\_g está disponível apenas no sombreador de computação.

### <a name="_t"></a>\_t

Sincronização de grupo de threads. Todos os threads em um único grupo de threads (aqueles que podem compartilhar acesso a um conjunto comum de espaço de registro compartilhado) serão executados até o ponto em que alcançarem essa instrução antes que qualquer thread possa continuar.

\_não pode ser colocado no controle de fluxo dinâmico (branches que podem variar dentro de um grupo de threads), mas pode estar presente no controle de fluxo uniforme, em que todos os threads no grupo escolhem o mesmo caminho.

\_t está disponível apenas no sombreador de computação.

Veja a seguir uma lista de variantes de 'sincronização' do sombreador de computação.

-   sync \_ g
-   sync \_ ugroup\*
-   sync \_ uglobal
-   sync \_ g \_ t
-   sync \_ ugroup \_ t\*
-   sync \_ uglobal \_ t
-   sync \_ ugroup \_ g\*
-   sync \_ uglobal \_ g
-   sync \_ ugroup \_ g \_ t\*
-   sync \_ uglobal \_ g \_ t

\*Variantes com ugroup podem não ser direcionadas pelo compilador HLSL, de acordo com a discussão anterior \_ na \_ seção ugroup acima.

A listagem de variantes de sincronização do sombreador de pixel inclui apenas \_ sincronização uglobal.

Os receptadores de memória impedem que as instruções afetadas são reordenadas por compiladores ou hardware em toda a cerca.

Várias leituras do mesmo endereço por uma invocação de sombreador que não são separadas por barreiras de memória ou gravações no endereço podem ser recolhidos juntos. O mesmo se aplica às gravações. Os acessos separados por uma barreira não podem ser mesclados nem movidos pela barreira.

As cercas de memória não são necessárias para que as operações atômicas para um determinado endereço por threads diferentes funcionem corretamente. As cercas são necessárias quando as operações atômicas e/ou de carregamento/armazenamento precisam ser sincronizadas em relação uns aos outros, pois aparecem em threads individuais do ponto de vista de outros threads.

No sombreador de pixel, as instruções [de](discard--sm4---asm-.md) descarte implicam uma cerca uglobal de sincronização, na forma em que as instruções não podem ser \_ reordenadas no **descarte.** sincronizar uglobal em pixels auxiliares (que são executados somente para dar suporte a derivados) ou pixels descartados podem ou não \_ ter nenhum efeito. Não é permitido que o auxiliar ou pixels descartados sejam escritos em UAVs se, no caso de descarte, as gravações são emitidas após o descarte. Os valores retornados de UAVs não têm permissão para contribuir com cálculos derivados. Portanto, se a sincronização u é ou não acodida para pixels auxiliares ou quando emitido \_ após um descarte é moot.

Cs \_ 4 \_ 0 e cs \_ 4 \_ 1 são suportados por essa instrução.

Essa instrução se aplica aos seguintes estágios do sombreador:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Como os UAVs estão disponíveis em todos os estágios do sombreador para o Direct3D 11.1, a variante **\_ uglobal** de sincronização dessa instrução se aplica a todos os estágios do sombreador para o runtime do Direct3D 11.1, que está disponível a partir do Windows 8.



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa instrução tem suporte nos seguintes modelos de sombreador:



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | não        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | não        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




