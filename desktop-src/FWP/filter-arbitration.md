---
title: Arbitragem de filtro
description: A arbitragem de filtro é a lógica incorporada à WFP (Windows Filtering Platform) usada para determinar como os filtros interagem entre si ao tomar decisões de filtragem de tráfego de rede.
ms.assetid: d097f307-113e-4dc3-ad59-ddfb85061583
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fd7df778d1c24b7480de3321e7a1ec126d8e642
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103641026"
---
# <a name="filter-arbitration"></a>Arbitragem de filtro

A arbitragem de filtro é a lógica incorporada à WFP (Windows Filtering Platform) usada para determinar como os filtros interagem entre si ao tomar decisões de filtragem de tráfego de rede.

## <a name="filter-arbitration-behaviors"></a>Filtrar comportamentos de arbitragem

Os seguintes comportamentos caracterizam o sistema de arbitragem de filtro:

-   Todo o tráfego pode ser inspecionado. Nenhum tráfego pode ignorar filtros em uma determinada camada.
-   O tráfego pode ser bloqueado por um filtro de texto explicativo por meio de uma **veto** , mesmo que um filtro de prioridade mais alta tenha permitido.
-   Vários provedores podem inspecionar o tráfego na mesma camada. Por exemplo, o firewall seguido por filtros de IDS (sistema de detecção de intrusão) ou IPsec seguido por filtros de QoS (qualidade de serviço) pode examinar o tráfego na mesma camada.

## <a name="filtering-model"></a>Modelo de filtragem

Cada camada de filtro é dividida em subcamadas, ordenadas por prioridade (também chamada de peso). O tráfego de rede atravessa as subcamadas da prioridade mais alta para a prioridade mais baixa. Subcamadas são criadas e gerenciadas pelos desenvolvedores que usam a API WFP.

Em cada subcamada, os filtros são ordenados por peso. O tráfego de rede é indicado para correspondência de filtros de peso mais alto para o peso mais baixo.

O algoritmo de arbitragem de filtro é aplicado a todas as subcamadas dentro de uma camada e a decisão de filtragem final é feita após a avaliação de todas as subcamadas. Isso fornece vários recursos de correspondência.

Em uma subcamada, a arbitragem de filtro é executada da seguinte maneira:

-   Compute a lista de filtros de correspondência ordenados por peso do mais alto para o mais baixo.
-   Avalie filtros de correspondência na ordem até que um "permit" ou um "bloco" seja retornado (os filtros também podem retornar "Continue") ou até que a lista seja esgotada.
-   Ignore os filtros restantes e retorne a ação do último filtro avaliado.

Dentro de uma camada, a arbitragem de filtro é executada da seguinte maneira:

-   Execute a arbitragem de filtro em cada subcamada em ordem de prioridade mais alta para a prioridade mais baixa.
-   Avalie todas as subcamadas mesmo se uma subcamada de prioridade mais alta decidir bloquear o tráfego.
-   Retorne a ação resultante com base nas regras de política descritas na seção a seguir.

O diagrama a seguir ilustra uma configuração de subcamada de exemplo. As caixas externas representam camadas. As caixas internas representam subcamadas que contêm filtros. O curinga ( \* ) em um filtro significa que todo o tráfego corresponde ao filtro.

![configuração de subcamada de exemplo](images/fwp-sub-config2.png)

A única maneira de um filtro ser ignorado é se um filtro de maior peso tiver permitido ou bloqueado o tráfego dentro da mesma subcamada. Por outro lado, uma maneira de garantir que um filtro sempre veja todo o tráfego em uma camada é adicionar uma subcamada que contenha um único filtro que corresponda a todo o tráfego.

## <a name="configurable-override-policy"></a>Política de substituição configurável

As regras descritas abaixo regem as decisões de arbitragem dentro de uma camada. Essas regras são usadas pelo mecanismo de filtro para decidir qual uma das ações de subcamadas é aplicada ao tráfego de rede.

A política básica é a seguinte:

-   As ações são avaliadas em ordem de prioridade de subcamadas da prioridade mais alta para a prioridade mais baixa.
-   "Bloquear" substitui "permitir".
-   "Block" é final (não pode ser substituído) e interrompe a avaliação. O pacote é Descartado.

A política básica não oferece suporte ao cenário de uma exceção não substituída por um firewall. Exemplos típicos desse tipo de cenário são:

-   A porta de administração remota deve ser aberta mesmo na presença de um firewall de terceiros.
-   Componentes que exigem que as portas sejam abertas para funcionar (por exemplo, Universal Plug and Play UPnP). Se o administrador tiver habilitado explicitamente o componente, o firewall não deverá bloquear o tráfego silenciosamente.

Para dar suporte aos cenários acima, uma decisão de filtragem deve ser mais difícil de substituir do que outra decisão de filtragem, gerenciando a permissão de substituição de ação. Essa permissão é implementada como o sinalizador de **\_ gravação da \_ ação \_ FWPS direita** e é definida por filtro.

O algoritmo de avaliação mantém a ação atual ("permitir" ou "bloquear") junto com o sinalizador de **\_ gravação da \_ ação \_ FWPS direita** . O sinalizador controla se uma subcamada de prioridade mais baixa tem permissão para substituir a ação. Ao configurar ou redefinir o sinalizador **de \_ \_ \_ gravação da ação direita FWPS** na estrutura [FWPS \_ classificar \_ OUT0](/windows/win32/api/fwpstypes/ns-fwpstypes-fwps_classify_out0) , um provedor rege como as ações podem ou não podem ser substituídas. Se o sinalizador for definido, isso indica que a ação pode ser substituída. Se o sinalizador estiver ausente, a ação não poderá ser substituída.



| Ação | Permitir substituição (a \_ gravação da ação FWPS direita \_ \_ está definida) | Descrição                                                                                                          |
|--------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Permitir | Sim                                                | O tráfego pode ser bloqueado em outra subcamada. Isso é chamado de uma permissão flexível.<br/>                            |
| Permitir | Não                                                 | O tráfego pode ser bloqueado em outra subcamada apenas por uma **veto** de texto explicativo. Isso é chamado de permissão rígida.<br/> |
| Bloquear  | Sim                                                | O tráfego pode ser permitido em outra subcamada. Isso é chamado de bloqueio flexível.<br/>                           |
| Bloquear  | Não                                                 | O tráfego não pode ser permitido em outra subcamada. Isso é chamado de bloqueio rígido.<br/>                        |



 

A ação de filtro pode ser definida definindo o membro de **tipo** na estrutura [**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0) para o **\_ \_ bloco de ação fwp** ou a **\_ ação fwp \_ permitir**. Junto com o tipo de ação, um filtro também expõe o sinalizador de **\_ \_ \_ ação limpar \_ sinalizador \_ do filtro FWPM**. Se esse sinalizador for desmarcado, o tipo de ação será difícil e não poderá ser substituído, exceto quando uma permissão rígida for substituída por um **veto** , conforme explicado posteriormente, caso contrário, será Soft, o que pode ser substituído por uma ação de prioridade alta.

A tabela a seguir lista o comportamento padrão para ações de filtro e de texto explicativo.

| Ação         | Comportamento padrão |
|----------------|------------------|
| Permissão de filtro  | Permissão de software      |
| Permissão de texto explicativo | Permissão de software      |
| Bloco de filtro   | Bloqueio de hardware       |
| Bloco de texto explicativo  | Bloqueio flexível       |



 

Uma **veta** é uma ação de "bloqueio" retornada pelo filtro quando o sinalizador de **\_ \_ \_ gravação da ação direita FWPS** foi redefinido antes de chamar o filtro. Uma **veta** bloqueará o tráfego que foi permitido com uma permissão rígida.

Quando um **veto** é emitido, é uma indicação de conflito na configuração. As ações a seguir são executadas para mitigar o conflito.

-   O tráfego está bloqueado.
-   Um evento de auditoria é gerado.
-   Uma notificação é gerada.
    > [!Note]  
    > A notificação é recebida por todas as entidades que assinaram a ela. Isso normalmente inclui o firewall (para detectar configurações incorretas) ou aplicativos (para detectar se seu filtro específico é substituído).

     

    > [!Note]  
    > Não há nenhuma interface do usuário (IU) obrigatória instanciada quando um filtro de "permissão rígida" é substituído. As notificações da substituição são enviadas para qualquer provedor que está registrado para recebê-las, que permite firewalls ou os aplicativos que criaram os filtros de "permissão", para mostrar a interface do usuário solicitando a ação. Não há nenhum valor em ter uma notificação de interface do usuário da plataforma para esses eventos de substituição, pois os ISVs de firewall que não desejam bloquear silenciosamente podem fazer isso registrando em um local diferente na WFP ou (menos preferencial) lidar com toda a lógica em um driver de chamada. Os ISVs que consideram a solicitação de usuários é uma boa ideia que desejarão ter a experiência do usuário e criar sua própria interface.

     

O comportamento de mitigação descrito acima garante que um filtro de "permissão rígida" não seja substituído silenciosamente por um filtro de "bloqueio" e cubra o cenário em que uma porta de administração remota não tem permissão para ser bloqueada pelo firewall. Para substituir silenciosamente os filtros de "permissão rígida", um firewall precisa adicionar seus filtros em uma subcamada de prioridade mais alta.

> [!Note]  
> Como não há arbitragem de camada cruzada, o tráfego permitido com "permissão rígida" ainda pode ser bloqueado em outra camada. É responsabilidade do autor da política garantir que o tráfego seja permitido em cada camada, se necessário.

 

Aplicativos de usuário solicitando que as portas sejam abertas adicione filtros substituíveis a uma subcamada de baixa prioridade. O firewall pode assinar o filtro adicionar eventos de notificação e adicionar um filtro de correspondência após a validação de usuário (ou política).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atribuição de peso de filtro](filter-weight-assignment.md)
</dt> </dl>

 

