---
title: Operação WFP
description: Windows A WFP (Plataforma de Filtragem) executa suas tarefas integrando as seguintes entidades básicas Camadas, Filtros, Shims e Textos explicadores.
ms.assetid: bf88ace7-1160-434b-9be0-3f9db6aa2e87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8254ed468b856392477a643ce13f2b609245031f7363865b8c93ccfda64ba9fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015384"
---
# <a name="wfp-operation"></a>Operação WFP

Windows A WFP (Plataforma de Filtragem) executa suas tarefas integrando as seguintes entidades básicas: *Camadas,* *Filtros, Shims* e *Textos explicadores.*

## <a name="layers"></a>Camadas

Uma *camada* é um contêiner gerenciado pelo mecanismo de filtro cuja função é organizar filtros em conjuntos. Uma camada não é um módulo na pilha de rede. Cada camada tem um esquema que define o tipo de filtros que podem ser adicionados a ela. Consulte [Condições de filtragem disponíveis em cada camada de filtragem](filtering-conditions-available-at-each-filtering-layer.md) para obter mais informações.

As camadas podem conter sub camadas para gerenciar requisitos de filtro conflitantes, como "Bloquear portas TCP acima de 1024" e "Abrir porta 1080". As regras para gerenciar conflitos de filtragem são determinadas pela [Mediação de Filtro.](filter-arbitration.md)

O WFP contém um conjunto de [sub-camadas.](management-filtering-sublayer-identifiers.md) Cada camada herda todas as sub-camadas internas. Os usuários também podem adicionar suas próprias sub camadas.

A lista de camadas do mecanismo de filtro é fornecida no tópico da seção de referência [**Filtrando identificadores de camada**](management-filtering-layer-identifiers-.md).

## <a name="filters"></a>Filtros

Um *filtro* é uma regra que é corresponder a pacotes de entrada ou saída. A regra informa ao mecanismo de filtragem o que fazer com o pacote, incluindo chamar um módulo de chamada para inspeção profunda de fluxo ou pacote. Por exemplo, um filtro pode especificar "Bloquear tráfego com uma porta TCP maior que 1024" ou "Chamar o IDS para todo o tráfego que não está protegido".

Um filtro de tempo de inicialização é um filtro que é imposto no tempo de inicialização assim que o driver de pilha TCP/IP (tcpip.sys) é iniciado. Um filtro de tempo de inicialização é desabilitado quando o BFE é iniciado. Um filtro é marcado como tempo de inicialização definindo o sinalizador [**\_ FWPM FILTER FLAG \_ \_ BOOTTIME**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0) quando [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0) é invocado.

Um filtro de tempo de run time é um filtro que é imposto após o início do BFE. Um filtro em tempo de run time pode ser estático, dinâmico ou persistente, dependendo de como ele foi criado. Consulte [Gerenciamento de Objetos](object-management.md) para obter mais informações sobre os diferentes tipos de filtros de tempo de run-time e seu tempo de vida.

## <a name="shims"></a>Calços

Um *shim* é um componente de modo kernel que toma decisões de filtragem classificando em relação às camadas do mecanismo de filtro. Cada shim classifica em uma ou mais camadas. Por exemplo, o shim módulo de camada de transporte classifica em relação à camada de Transporte de Entrada, à camada de Transporte de Saída e às camadas Conexão e Receive-Accept ALE para o primeiro pacote de um fluxo.

À medida que pacotes, fluxos e eventos atravessam a pilha de rede, os shims os analisam para extrair as condições e valores classificáveis e, em seguida, chamam o mecanismo de filtro para avaliá-los em relação aos filtros em uma determinada camada. O mecanismo de filtro pode invocar um ou mais callouts como parte da classificação. Os shims fazem a re soltar pacotes, fluxos e eventos reais com base no resultado da classificação executada pelo mecanismo de filtro.

## <a name="callouts"></a>Chamadas

Um *callout* é um conjunto de funções expostas por um driver e usadas para filtragem especializada. Eles são usados para executar a análise e a manipulação dos pacotes, como verificação de vírus, verificação de controles dos pais quanto a conteúdo inadequado, análise de dados de pacote para ferramentas de monitoramento. Alguns textos explicadores, como o driver NAT (Conversão de Endereços de Rede), são integrados ao sistema operacional. Outros, como um callout de Controle dos Pais HTTP ou o IDS (Sistema de Detecção de Intrusão), podem ser fornecidos por ISVs (fornecedores independentes de software). As funções de texto explicativa são invocadas pelo mecanismo de filtro quando um filtro de texto explicador correspondente é correspondido em uma determinada camada.

Os callouts podem ser registrados em qualquer uma das camadas WFP do modo kernel. Os textos explicadores podem retornar uma ação ("Bloquear", "Permitir" e, ao executar a inspeção de fluxo, "Adiar", "Precisa de mais dados", "Soltar conexão") e podem modificar e proteger o tráfego de rede de entrada e saída.

Depois que um callout é registrado com o mecanismo de filtro, ele pode receber o tráfego de rede a ser processado. O tráfego pode ser pacotes, fluxos ou eventos, dependendo da camada. Um agente de aplicativo ou firewall faz com que o tráfego seja passado para um callout adicionando um filtro cuja ação é "Callout" e cuja ID de chamada é o identificador desse chamador. Os callouts podem instruir o mecanismo de filtro a retornar "Bloquear" ou "Permitir" para o shim. Os callouts também podem retornar "Continuar" para permitir que outros filtros processem o pacote.

Vários callouts podem ser expostos por um driver de chamada.

Um callout precisa ser adicionado (com [**FwpmCalloutAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutadd0)) e registrado (com [FwpsCalloutRegister](/windows-hardware/drivers/ddi/_netvista/)) antes que possa ser usado. Uma chamada para **FwpmCalloutAdd0** é necessária antes da criação de filtros que referenciam o callout. Uma chamada para FwpsCalloutRegister é necessária antes que o WFP possa invocar o chamador quando os filtros de chamada são correspondentes. Por padrão, os filtros que referenciam os callouts que foram adicionados, mas ainda não foram registrados com o mecanismo de filtro, são tratados como filtros "Bloquear". A ordem de chamada **de FwpmCalloutAdd0** e FwpsCalloutRegister não importa. Um callout persistente precisa ser adicionado apenas uma vez e precisa ser registrado sempre que o driver que implementa o callout for iniciado (por exemplo, após uma reinicialização).

## <a name="classification"></a>classificação

Classificação é o processo de aplicar filtros ao tráfego de rede (pacote, fluxo ou evento) para determinar um resultado de "Permitir" ou "Bloquear" para esse tráfego. Para um pacote, fluxo ou evento, há uma chamada de classificação por camada.

Durante a classificação, as propriedades (por exemplo, endereço de origem) do pacote, fluxo ou evento são comparadas com condições de filtro definidas em filtros na camada em que a classificação é invocada. Quando as correspondeções são encontradas, o algoritmo [Filter Algorithm](filter-arbitration.md) é usado para determinar o resultado do processo de classificação.

Uma solicitação de classificação é disparada por um shim.

As ações de classificação podem ser:

-   Permitir
-   Bloquear
-   Balão
    -   Permitir
    -   Bloquear
    -   Continuar
    -   Adiar
    -   Precisa de mais dados
    -   Soltar conexão

## <a name="wfp-operation"></a>Operação WFP

No momento da inicialização, assim que o driver de pilha TCP/IP (tcpip.sys) é iniciado, o mecanismo de filtro de modo kernel impõe a política de segurança do sistema por meio de filtros de tempo de inicialização.

Depois que o BFE (Mecanismo de Filtragem Base) é iniciado no modo de usuário, os filtros persistentes são adicionados à plataforma, os filtros de tempo de inicialização são desabilitados e as notificações são enviadas aos drivers de texto explicativo que assinaram usando [FwpmBfeStateSubscribeChanges0](/windows-hardware/drivers/ddi/fwpmk/nf-fwpmk-fwpmbfestatesubscribechanges0). As notificações são expedidas imediatamente após a conclusão da inicialização do BFE. A plataforma agora está pronta para que os callouts sejam registrados e para que os objetos em tempo de run-time sejam adicionados.

A transição do tempo de inicialização para filtros persistentes pode ser de vários segundos ou até mesmo mais tempo em um computador lento. Ele é atômico, portanto, se um provedor tiver um tempo de inicialização e um filtro persistente, nunca haverá uma janela quando nenhum deles estiver em vigor.

Depois que o BFE é iniciado, os filtros de tempo de executar podem ser adicionados por agentes de firewall ou por soluções de firewall personalizadas. O BFE processa esses filtros e os envia para a camada de mecanismo de filtro apropriada para imposição. O BFE também aceita configurações de autenticação e envia essas configurações para os módulos de chave IPsec (IKE/AuthIP). Confira [Configuração do IPsec](ipsec-configuration.md) para obter mais informações.

A qualquer momento, filtros e configurações de autenticação podem ser adicionados, removidos ou alterados no sistema por meio da interface RPC exposta pelo BFE. As sub camadas e os módulos de chamada podem ser adicionados ou removidos da mesma forma.

Fluxo de dados:

1.  Um pacote entra na pilha de rede.
2.  A pilha de rede localiza e chama um shim.
3.  O shim invoca o processo de classificação em uma camada específica.
4.  Durante a classificação, os filtros são corresponderes e a ação resultante é tomada. (Consulte [Filtragem de Filtragem](filter-arbitration.md).)
5.  Se algum filtro de chamada for correspondido durante o processo de classificação, os callouts correspondentes serão invocados.
6.  O shim atua na decisão final de filtragem (por exemplo, soltar o pacote).

O fluxo de dados de saída segue um padrão semelhante.

Os tópicos a seguir descrevem ainda mais a operação do WFP.

-   [Fluxos de pacotes TCP](tcp-packet-flows.md)
-   [Fluxos de pacotes UDP](udp-packet-flows.md)
-   [Filtragem de filtragem](filter-arbitration.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de objeto](object-model.md)
</dt> <dt>

[Gerenciamento de objetos](object-management.md)
</dt> </dl>

 

 