---
title: Operação WFP
description: A WFP (Windows Filtering Platform) executa suas tarefas integrando as seguintes camadas, filtros, shims e textos explicativos básicos de entidades.
ms.assetid: bf88ace7-1160-434b-9be0-3f9db6aa2e87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e7a7d38bd0de5b1f549e2187c414644bf68442
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105778775"
---
# <a name="wfp-operation"></a>Operação WFP

A WFP (Windows Filtering Platform) executa suas tarefas integrando as seguintes entidades básicas: *camadas*, *filtros*, *shims* e *textos explicativos*.

## <a name="layers"></a>Camadas

Uma *camada* é um contêiner gerenciado pelo mecanismo de filtro cuja função é para organizar os filtros em conjuntos. Uma camada não é um módulo na pilha de rede. Cada camada tem um esquema que define o tipo de filtros que podem ser adicionados a ele. Consulte [condições de filtragem disponíveis em cada camada de filtragem](filtering-conditions-available-at-each-filtering-layer.md) para obter mais informações.

As camadas podem conter subcamadas para gerenciar requisitos de filtro conflitantes, como "bloquear portas TCP acima de 1024" e "abrir porta 1080". As regras para gerenciar conflitos de filtragem são determinadas pela [arbitragem de filtro](filter-arbitration.md).

A WFP contém um conjunto de [subcamadas internas](management-filtering-sublayer-identifiers.md). Cada camada herda todas as subcamadas internas. Os usuários também podem adicionar suas próprias subcamadas.

A lista de camadas do mecanismo de filtro é fornecida no tópico seção de referência [**identificadores de camada de filtragem**](management-filtering-layer-identifiers-.md).

## <a name="filters"></a>Filtros

Um *filtro* é uma regra que é correspondida com os pacotes de entrada ou de saída. A regra diz ao mecanismo de filtragem o que fazer com o pacote, incluindo para chamar um módulo de texto explicativo para inspeção profunda de pacotes ou fluxos. Por exemplo, um filtro pode especificar "bloquear o tráfego com uma porta TCP maior que 1024" ou "chamar para IDS para todo o tráfego não protegido".

Um filtro de tempo de inicialização é um filtro que é imposto no momento da inicialização assim que o driver de pilha TCP/IP (tcpip.sys) é iniciado. Um filtro de tempo de inicialização é desabilitado quando o BFE é iniciado. Um filtro é marcado como tempo de inicialização, definindo o sinalizador [**FWPM do sinalizador de filtro de \_ \_ \_ inicialização**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0) quando [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0) é invocado.

Um filtro de tempo de execução é um filtro que é imposto após a inicialização do BFE. Um filtro de tempo de execução pode ser estático, dinâmico ou persistente, dependendo da maneira como ele foi criado. Consulte [Gerenciamento de objetos](object-management.md) para obter mais informações sobre os diferentes tipos de filtros de tempo de execução e seu tempo de vida.

## <a name="shims"></a>Shims

Um *Shim* é um componente do modo kernel que toma decisões de filtragem classificando em relação às camadas do mecanismo de filtro. Cada Shim é classificado em uma ou mais camadas. Por exemplo, o Shim do módulo da camada de transporte é classificada em relação à camada de transporte de entrada, à camada de transporte de saída e às camadas de Receive-Accept e conexão ALE para o primeiro pacote de um fluxo.

Como os pacotes, fluxos e eventos atravessam a pilha de rede, os shims os analisam para extrair as condições e os valores de classificáveis e, em seguida, chamar o mecanismo de filtro para avaliá-los em relação aos filtros em uma determinada camada. O mecanismo de filtro pode invocar um ou mais textos explicativos como parte da classificação. Os shims fazem o descarte real de pacotes, fluxos e eventos com base no resultado da classificação executada pelo mecanismo de filtro.

## <a name="callouts"></a>Textos explicativos

Um *texto explicativo* é um conjunto de funções expostas por um driver e usadas para filtragem especializada. Eles são usados para executar a análise e a manipulação dos pacotes, como a verificação de vírus, os controles dos pais verificam a existência de conteúdo impróprio, análise de dados de pacotes para ferramentas de monitoramento. Alguns textos explicativos, como o driver NAT (conversão de endereços de rede), são incorporados ao sistema operacional. Outros, como um texto explicativo de controle de pais HTTP ou o balão IDS (sistema de detecção de intrusão), podem ser fornecidos por ISVs (fornecedores independentes de software). As funções de texto explicativo são invocadas pelo mecanismo de filtro quando um filtro de texto explicativo correspondente é correspondido em uma determinada camada.

Os textos explicativos podem ser registrados em qualquer uma das camadas WFP do modo kernel. Os textos explicativos podem retornar uma ação ("bloquear", "permitir" e, ao executar a inspeção de fluxo, "adiar", "precisa de mais dados", "remover conexão") e podem modificar e proteger o tráfego de rede de entrada e saída.

Depois que um texto explicativo é registrado com o mecanismo de filtro, ele pode receber o tráfego de rede para processar. O tráfego pode ser pacotes, fluxos ou eventos, dependendo da camada. Um agente de aplicativo ou firewall faz com que o tráfego seja passado para um texto explicativo, adicionando um filtro cuja ação é "texto explicativo" e cuja ID do texto explicativo é o identificador do texto explicativo. Os textos explicativos podem instruir o mecanismo de filtro para retornar "bloquear" ou "permitir" para o Shim. Os textos explicativos também podem retornar "continuar" para permitir que outros filtros processem o pacote.

Vários textos explicativos podem ser expostos por um driver de texto explicativo.

Um texto explicativo precisa ser adicionado (com [**FwpmCalloutAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutadd0)) e registrado (com [FwpsCalloutRegister](/windows-hardware/drivers/ddi/_netvista/)) antes de poder ser usado. Uma chamada para **FwpmCalloutAdd0** é necessária antes da criação de filtros que fazem referência ao texto explicativo. Uma chamada para FwpsCalloutRegister é necessária antes que a WFP possa invocar o texto explicativo quando os filtros de texto explicativo forem correspondidos. Por padrão, os filtros que fazem referência a textos explicativos que foram adicionados, mas que ainda não foram registrados com o mecanismo de filtro, são tratados como filtros de "bloqueio". A ordem de chamar **FwpmCalloutAdd0** e FwpsCalloutRegister não importa. Um texto explicativo persistente precisa ser adicionado apenas uma vez e precisa ser registrado toda vez que o driver que implementa o texto explicativo é iniciado (por exemplo, após uma reinicialização).

## <a name="classification"></a>Classificação

Classificação é o processo de aplicação de filtros ao tráfego de rede (pacote, fluxo ou evento) para determinar um resultado de "permitir" ou "bloquear" para esse tráfego. Para um pacote, fluxo ou evento, há uma chamada de classificação por camada.

Durante a classificação, as propriedades (por exemplo, endereço de origem) do pacote, fluxo ou evento são comparadas com condições de filtro definidas em filtros na camada em que a classificação é invocada. Quando as correspondências são encontradas, o algoritmo de [arbitragem de filtro](filter-arbitration.md) é usado para determinar o resultado do processo de classificação.

Uma solicitação de classificação é disparada por um Shim.

As ações de classificação também podem ser:

-   Permitir
-   Bloquear
-   Balão
    -   Permitir
    -   Bloquear
    -   Continuar
    -   Ferida
    -   Precisa de mais dados
    -   Remover conexão

## <a name="wfp-operation"></a>Operação WFP

No momento da inicialização, assim que o driver de pilha TCP/IP (tcpip.sys) é iniciado, o mecanismo de filtro do modo kernel impõe a política de segurança do sistema por meio de filtros de tempo de inicialização.

Depois que o mecanismo de filtragem base (BFE) é iniciado no modo de usuário, os filtros persistentes são adicionados à plataforma, os filtros de tempo de inicialização são desabilitados e as notificações são enviadas para esses drivers de texto explicativo que se inscreveram usando [FwpmBfeStateSubscribeChanges0](/windows-hardware/drivers/ddi/fwpmk/nf-fwpmk-fwpmbfestatesubscribechanges0). As notificações são expedidas imediatamente após a conclusão da inicialização de BFE. Agora, a plataforma está pronta para que os textos explicativos sejam registrados e que os objetos em tempo de execução sejam adicionados.

A transição dos filtros de tempo de inicialização para persistente pode ser de vários segundos, ou ainda mais em um computador lento. É atômico, portanto, se um provedor tiver um filtro de tempo de inicialização e persistente, nunca haverá uma janela quando nenhum estiver em vigor.

Após o início do BFE, os filtros de tempo de execução podem ser adicionados por agentes de firewall ou por soluções de firewall personalizadas. O BFE processa esses filtros e os envia para a camada apropriada do mecanismo de filtro para imposição. O BFE também aceita configurações de autenticação e envia essas configurações para os módulos de chaveamento de IPsec (IKE/AuthIP). Consulte [configuração de IPSec](ipsec-configuration.md) para obter mais informações.

A qualquer momento, as configurações de filtros e de autenticação podem ser adicionadas, removidas ou alteradas no sistema por meio da interface RPC exposta pelo BFE. Subcamadas e módulos de texto explicativo podem ser adicionados ou removidos da mesma forma.

Fluxo de dados:

1.  Um pacote entra na pilha de rede.
2.  A pilha de rede localiza e chama um Shim.
3.  O Shim invoca o processo de classificação em uma camada específica.
4.  Durante a classificação, os filtros são correspondidos e a ação resultante é executada. (Consulte [arbitragem de filtro](filter-arbitration.md).)
5.  Se qualquer filtro de texto explicativo for correspondido durante o processo de classificação, os textos explicativos correspondentes serão invocados.
6.  O Shim age na decisão de filtragem final (por exemplo, descartar o pacote).

O fluxo de dados de saída segue um padrão semelhante.

Os tópicos a seguir descrevem mais detalhadamente a operação da WFP.

-   [Fluxos de pacotes TCP](tcp-packet-flows.md)
-   [Fluxos de pacotes UDP](udp-packet-flows.md)
-   [Arbitragem de filtro](filter-arbitration.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de objeto](object-model.md)
</dt> <dt>

[Gerenciamento de objetos](object-management.md)
</dt> </dl>

 

 