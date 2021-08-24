---
description: Página de Glossário
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 26a72de1-24bc-41e6-8d41-61d45f581e51
title: Glossário do COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eda1c62c8edee1e15df33b63a9d4894639dd9e5637ed3e87a747d724f9e9040e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638716"
---
# <a name="com-glossary"></a>Glossário do COM+

<dl> <dt>

<span id="cos.access_token_gloss"></span><span id="COS.ACCESS_TOKEN_GLOSS"></span>**token de acesso**
</dt> <dd>

Um objeto que descreve o contexto de segurança de um processo ou thread. As informações em um token incluem a identidade e os privilégios da conta de usuário associada ao processo ou thread. Quando um usuário faz logon, o sistema verifica a senha do usuário comparando-a com as informações armazenadas em um banco de dados de segurança. Se a senha for autenticada, o sistema produzirá um token de acesso. Cada processo executado em nome desse usuário tem uma cópia desse token de acesso.

</dd> <dt>

<span id="cos.acid_properties_gloss"></span><span id="COS.ACID_PROPERTIES_GLOSS"></span>**Propriedades ACID**
</dt> <dd>

Acrônimo cunhado pelos pioneiros de processamento de transações para Atomic, consistente, isolado e durável. Essas propriedades garantem um comportamento previsível, reforçando a função de transações como todas as proposições de tudo ou nenhum projetadas para fornecer resultados consistentes e previsíveis em um ambiente distribuído quando podem ocorrer falhas independentes.

</dd> <dt>

<span id="cos.activation_gloss"></span><span id="COS.ACTIVATION_GLOSS"></span>**ativá**
</dt> <dd>

A cadeia de eventos que resulta na criação de um objeto COM e o retorno de um ponteiro válido para uma interface nesse objeto. No COM+, um objeto é ativado em seu próprio contexto ou no seu criador (um objeto que solicitou o objeto que está sendo ativado). Os serviços COM+ dependem da ativação apropriada de um objeto com base na configuração do objeto. No decorrer da ativação, o sistema determina o contexto no qual o objeto é executado, inicializa as propriedades de contexto, verifica as permissões de acesso e estabelece uma identidade de segurança.

</dd> <dt>

<span id="cos.activation_security_gloss"></span><span id="COS.ACTIVATION_SECURITY_GLOSS"></span>**segurança de ativação**
</dt> <dd>

Uma forma de proteção de segurança que determina quem pode iniciar um servidor. A segurança de ativação é aplicada automaticamente pelo SCM (Gerenciador de controle de serviço) de um computador específico. Após o recebimento de uma solicitação de um cliente para ativar um objeto, o SCM verifica a solicitação de informações de segurança de ativação armazenadas em seu registro. A segurança de ativação também é verificada quanto a ativações de mesmo computador. Também chamado de *segurança de inicialização*.

</dd> <dt>

<span id="cos.activation_type_gloss"></span><span id="COS.ACTIVATION_TYPE_GLOSS"></span>**tipo de ativação**
</dt> <dd>

Categoria de ativação para um aplicativo COM+ que indica se o aplicativo é executado dentro ou fora do espaço de processo do cliente (dependendo se é um aplicativo de biblioteca ou de servidor, respectivamente), bem como se o aplicativo é executado como um serviço.

</dd> <dt>

<span id="cos.activity_gloss"></span><span id="COS.ACTIVITY_GLOSS"></span>**actividade**
</dt> <dd>

No COM+, um thread lógico que compreende uma ou mais transações e que contém uma coleção de componentes que são agrupados em um aplicativo COM+. Cada objeto COM pertence a uma atividade. A associação entre um objeto e uma atividade não pode ser alterada.

</dd> <dt>

<span id="cos.apartment_model_process_gloss"></span><span id="COS.APARTMENT_MODEL_PROCESS_GLOSS"></span>**processo de modelo de apartamento**
</dt> <dd>

Um processo que tem dois ou mais Apartments de thread único e nenhum Apartments multithread.

</dd> <dt>

<span id="cos.application_proxy_gloss"></span><span id="COS.APPLICATION_PROXY_GLOSS"></span>**proxy de aplicativo**
</dt> <dd>

Um conjunto de arquivos que contém informações de registro que permitem que um cliente acesse remotamente um aplicativo de servidor COM+. Quando instalado em um computador cliente, um arquivo de proxy de aplicativo grava informações sobre o aplicativo de servidor no computador cliente; o cliente pode acessar remotamente o aplicativo de servidor.

</dd> <dt>

<span id="cos.authentication_gloss"></span><span id="COS.AUTHENTICATION_GLOSS"></span>**Authentication**
</dt> <dd>

O processo de segurança de determinar que um chamador de um aplicativo realmente diz que ele é, verificando a autenticidade de uma declaração de identidade. Para aplicativos COM+, a autenticação pode ser ativada e configurada administrativamente, após a qual ela funciona de forma transparente para o aplicativo.

</dd> <dt>

<span id="cos.authorization_gloss"></span><span id="COS.AUTHORIZATION_GLOSS"></span>**nesse**
</dt> <dd>

O processo de segurança de determinar se um chamador de um aplicativo está autorizado a fazer o que ele está pedindo.

</dd> <dt>

<span id="cos.caching_resource_manager_gloss"></span><span id="COS.CACHING_RESOURCE_MANAGER_GLOSS"></span>**Gerenciador de recursos de caching**
</dt> <dd>

Um Gerenciador de recursos que atua como um front-end para outro gerenciador de recursos e que armazena em cache as informações localmente, reduzindo o custo de acesso ao recurso subjacente. Ao contrário de um Gerenciador de recursos convencional, um Gerenciador de recursos de cache não participa da recuperação porque nunca armazena permanentemente os dados subjacentes.

</dd> <dt>

<span id="cos.call_security_gloss"></span><span id="COS.CALL_SECURITY_GLOSS"></span>**chamar segurança**
</dt> <dd>

Uma forma de proteção de segurança que ajuda a controlar o acesso a métodos de um objeto de servidor depois que um servidor é iniciado.

</dd> <dt>

<span id="cos.class_gloss"></span><span id="COS.CLASS_GLOSS"></span>**classe (COM)**
</dt> <dd>

Uma implementação nomeada e concreta de uma ou mais interfaces. Uma classe COM é identificada por um CLSID e, às vezes, de um ProgID.

</dd> <dt>

<span id="cos.cloaking_gloss"></span><span id="COS.CLOAKING_GLOSS"></span>**encobrimento**
</dt> <dd>

A capacidade do servidor de mascarar sua própria identidade ao fazer chamadas em nome de um cliente. Quando o encobrimento está habilitado, as chamadas feitas pelo servidor representando o cliente podem ser feitas sob a identidade do cliente. Quando o encobrimento estiver desabilitado, as chamadas pelo servidor serão feitas sob a identidade do servidor.

</dd> <dt>

<span id="cos.complus_application_gloss"></span><span id="COS.COMPLUS_APPLICATION_GLOSS"></span>**Aplicativo COM+**
</dt> <dd>

A unidade primária de administração e segurança para serviços de componentes. Um aplicativo COM+ é um grupo de componentes COM que, em geral, executam funções relacionadas. Esses componentes consistem mais em interfaces e métodos COM.

</dd> <dt>

<span id="cos.complus_application_pooling_gloss"></span><span id="COS.COMPLUS_APPLICATION_POOLING_GLOSS"></span>**Pool de aplicativos COM+**
</dt> <dd>

Um recurso dos serviços de componentes que permite a escala de processos single-thread e também pode ajudá-lo a se recuperar de falhas em processos únicos, fornecendo outros processos em execução capazes de lidar com ativações.

</dd> <dt>

<span id="cos.complus_application_recycling_gloss"></span><span id="COS.COMPLUS_APPLICATION_RECYCLING_GLOSS"></span>**Reciclagem de aplicativos COM+**
</dt> <dd>

Um recurso dos serviços de componentes que aumenta significativamente a estabilidade geral de seus aplicativos, permitindo que você desligue normalmente um processo associado a um aplicativo e reinicie-o.

</dd> <dt>

<span id="cos.complus_catalog_gloss"></span><span id="COS.COMPLUS_CATALOG_GLOSS"></span>**Catálogo COM+** 
</dt> <dd>

O armazenamento de dados que contém dados de configuração do COM+. O desempenho das tarefas de administração do COM+ requer a leitura e a gravação de dados armazenados no catálogo. O catálogo pode ser acessado somente por meio da ferramenta administrativa serviços de componentes ou da biblioteca COMAdmin.

</dd> <dt>

<span id="cos.complus_events_gloss"></span><span id="COS.COMPLUS_EVENTS_GLOSS"></span>**Eventos COM+**
</dt> <dd>

Os eventos COM+ correspondem e conecta editores e assinantes por meio de um sistema de eventos livremente acoplado. Um Publicador faz a chamada de método para iniciar um evento e um assinante recebe essas chamadas por meio do sistema de eventos, e não diretamente do Publicador. O serviço de eventos COM+ mantém a lista de assinantes interessados que recebem as chamadas e direciona essas chamadas sem a necessidade do conhecimento do Publicador.

</dd> <dt>

<span id="cos.complus_library_application_gloss"></span><span id="COS.COMPLUS_LIBRARY_APPLICATION_GLOSS"></span>**Aplicativo de biblioteca COM+**
</dt> <dd>

Um aplicativo COM+ que é executado no processo do cliente que o cria. Os aplicativos de biblioteca podem usar a segurança baseada em função, mas não dão suporte a acesso remoto ou a componentes na fila.

</dd> <dt>

<span id="cos.complus_object_pooling_gloss"></span><span id="COS.COMPLUS_OBJECT_POOLING_GLOSS"></span>**Pool de objetos COM+**
</dt> <dd>

Um serviço automático fornecido pelo COM+ que permite configurar um componente para que as instâncias dele sejam mantidas ativas em um pool, prontas para serem usadas por qualquer cliente que solicite o componente.

</dd> <dt>

<span id="cos.complus_partitions_gloss"></span><span id="COS.COMPLUS_PARTITIONS_GLOSS"></span>**Partições COM+**
</dt> <dd>

Um serviço COM+ que habilita o, em um único computador, a criação de espaços de execução separados para aplicativos.

</dd> <dt>

<span id="cos.complus_partition_sets_gloss"></span><span id="COS.COMPLUS_PARTITION_SETS_GLOSS"></span>**Conjuntos de partições COM+**
</dt> <dd>

Um grupo de partições COM+ que é mapeado para uma determinada ID de usuário no Active Directory.

</dd> <dt>

<span id="cos.complus_queued_components_gloss"></span><span id="COS.COMPLUS_QUEUED_COMPONENTS_GLOSS"></span>**Componentes em fila COM+**
</dt> <dd>

Um serviço COM+, baseado no enfileiramento de mensagens da Microsoft, que fornece uma maneira fácil de invocar e executar componentes de forma assíncrona. O processamento de mensagens pode ocorrer sem considerar a disponibilidade ou a acessibilidade do remetente ou do receptor.

</dd> <dt>

<span id="cos.complus_server_application_gloss"></span><span id="COS.COMPLUS_SERVER_APPLICATION_GLOSS"></span>**Aplicativo de servidor COM+**
</dt> <dd>

Um aplicativo COM+ que é executado em seu próprio processo. Os aplicativos de servidor podem dar suporte a todos os serviços COM+.

</dd> <dt>

<span id="cos.complus_soap_gloss"></span><span id="COS.COMPLUS_SOAP_GLOSS"></span>**SOAP COM+**
</dt> <dd>

Um recurso dos serviços de componentes que permite expor um aplicativo COM+ como um serviço Web XML. O SOAP COM+ também permite que você use um serviço Web XML como um componente COM.

</dd> <dt>

<span id="cos.com_component_gloss"></span><span id="COS.COM_COMPONENT_GLOSS"></span>**Componente COM**
</dt> <dd>

Uma unidade binária de código que inclui o código de empacotamento e de registro e que cria objetos COM. Todos os aplicativos COM+ consistem em um ou mais componentes COM.

</dd> <dt>

<span id="cos.commit_tree_gloss"></span><span id="COS.COMMIT_TREE_GLOSS"></span>**confirmar árvore**
</dt> <dd>

Em um sistema de transações distribuídas, a representação conceitual de uma transação é baseada nas relações hierárquicas entre os gerenciadores de transações individuais que participam de uma transação distribuída. Incluídos nessa hierarquia estão os gerenciadores de recursos inscritos associados aos gerenciadores de transações.

</dd> <dt>

<span id="cos.com_object_gloss"></span><span id="COS.COM_OBJECT_GLOSS"></span>**Objeto COM**
</dt> <dd>

No modelo de programação COM, uma estrutura de programação que encapsula os dados e a funcionalidade, que são definidos e alocados como uma única unidade e para o qual o único acesso público é através das interfaces da estrutura de programação. Um objeto COM deve dar suporte a, no mínimo, a interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , que mantém a existência do objeto enquanto ele está sendo usado e fornece acesso às outras interfaces do objeto.

</dd> <dt>

<span id="cos.compensating_resource_manager_gloss"></span><span id="COS.COMPENSATING_RESOURCE_MANAGER_GLOSS"></span>**Gerenciador de recursos de compensação (CRM)**
</dt> <dd>

Um recurso COM+ que permite que recursos não transacionais participem de uma transação de confirmação de duas fases com o Microsoft Coordenador de Transações Distribuídas (DTC). Normalmente, o CRMs não fornece os recursos de isolamento de gerenciadores de recursos completos, mas eles fornecem atomicidade transacional e durabilidade ao gravar em um log.

</dd> <dt>

<span id="cos.component_services_administrative_tool_gloss"></span><span id="COS.COMPONENT_SERVICES_ADMINISTRATIVE_TOOL_GLOSS"></span>**Ferramenta administrativa serviços de componentes**
</dt> <dd>

Um snap-in de interface do usuário por meio do qual administradores e desenvolvedores podem criar, configurar e manter aplicativos COM+, bem como administrar transações distribuídas e bancos de dados residentes na memória. A ferramenta administrativa serviços de componentes também pode ser usada para exibir eventos do sistema e gerenciar serviços do sistema locais no computador em que a ferramenta está instalada.

</dd> <dt>

<span id="cos.conceptual_model_gloss"></span><span id="COS.CONCEPTUAL_MODEL_GLOSS"></span>**modelo conceitual**
</dt> <dd>

A primeira etapa na fase de design do aplicativo COM+, em que o desenvolvedor define os problemas de negócios a serem resolvidos e decide quais componentes e serviços são necessários.

</dd> <dt>

<span id="cos.concurrency_gloss"></span><span id="COS.CONCURRENCY_GLOSS"></span>**corrente**
</dt> <dd>

A capacidade de mais de uma transação ou processo de acessar os mesmos dados ao mesmo tempo. O COM+ geralmente gerencia a simultaneidade por meio da sincronização.

</dd> <dt>

<span id="cos.configured_component_gloss"></span><span id="COS.CONFIGURED_COMPONENT_GLOSS"></span>**componente configurado**
</dt> <dd>

Um componente COM que foi instalado em um aplicativo COM+. Depois de instalado, o componente é configurado no catálogo COM+ para usar os serviços COM+ disponíveis.

</dd> <dt>

<span id="cos.context_gloss"></span><span id="COS.CONTEXT_GLOSS"></span>**noticioso**
</dt> <dd>

Um conjunto de propriedades de tempo de execução associadas a um ou mais objetos COM que são usados para fornecer serviços para esses objetos. Cada objeto COM é executado em um único contexto de ativação para desativação (sempre dentro do mesmo apartamento). Inicializado quando um objeto é ativado, as propriedades de contexto, como propriedades de contexto de segurança, representam as necessidades de tempo de execução de um objeto.

</dd> <dt>

<span id="cos.data_tier_gloss"></span><span id="COS.DATA_TIER_GLOSS"></span>**camada de dados**
</dt> <dd>

No modelo de arquitetura de três camadas para aplicativos de negócios, a camada de acesso do DBMS, que pode ser acessada por meio da camada intermediária, ou do serviço de negócios, e às vezes por meio da camada de apresentação ou de serviços do usuário. A camada de dados consiste em componentes de acesso a dados (em vez de conexões brutas de DBMS) para auxiliar no compartilhamento de recursos e permitir que os clientes sejam configurados sem instalar as bibliotecas DBMS e os drivers ODBC em cada cliente. Também chamada de *camada de serviços de dados*.

</dd> <dt>

<span id="cos.deadlock_gloss"></span><span id="COS.DEADLOCK_GLOSS"></span>**bloqueado**
</dt> <dd>

Em aplicativos multissegmentados, um problema de Threading que ocorre quando cada membro de um conjunto de threads está aguardando outro membro do conjunto.

</dd> <dt>

<span id="cos.delegation_gloss"></span><span id="COS.DELEGATION_GLOSS"></span>**Delegação**
</dt> <dd>

Uma forma de representação que autoriza um servidor a agir em nome de um cliente, dando ao servidor a capacidade de representar clientes pela rede.

</dd> <dt>

<span id="cos.distributed_transaction_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_GLOSS"></span>**transação distribuída**
</dt> <dd>

Uma transação que envolve vários gerenciadores de recursos, que podem estar no mesmo computador ou em computadores diferentes.

</dd> <dt>

<span id="cos.distributed_transaction_coordinator_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_COORDINATOR_GLOSS"></span>**Coordenador de Transações Distribuídas (DTC)**
</dt> <dd>

Um serviço do sistema que gerencia transações e comunicações relacionadas à transação que são distribuídas por dois ou mais gerenciadores de recursos em um ou mais sistemas para garantir as transações ACID corretas.

</dd> <dt>

<span id="cos.dynamic_cloaking_gloss"></span><span id="COS.DYNAMIC_CLOAKING_GLOSS"></span>**encobrimento dinâmico**
</dt> <dd>

Uma forma de encobrir onde a identidade do cliente original é descoberta como o token de acesso de thread do servidor em cada chamada de método para o servidor downstream. Embora a identidade apresentada possa ser determinada dinamicamente, a sobrecarga necessária para fazer isso pode ser consideravelmente mais cara. Para aplicativos COM+, a configuração padrão é para o recurso de encobrimento dinâmico porque fornece a flexibilidade que geralmente é exigida pelas circunstâncias que precisam usar a representação em primeiro lugar.

</dd> <dt>

<span id="cos.enumerator_object_gloss"></span><span id="COS.ENUMERATOR_OBJECT_GLOSS"></span>**objeto Enumerator**
</dt> <dd>

Habilita a enumeração de itens nas coleções.

</dd> <dt>

<span id="cos.event_gloss"></span><span id="COS.EVENT_GLOSS"></span>**circunstância**
</dt> <dd>

Uma ação reconhecida por um objeto, como clicar no mouse ou pressionar uma tecla, e para a qual você pode escrever código para responder.

</dd> <dt>

<span id="cos.event_class_object_gloss"></span><span id="COS.EVENT_CLASS_OBJECT_GLOSS"></span>**objeto de classe de evento**
</dt> <dd>

Um componente configurado que fornece um registro persistente no sistema de eventos COM+ para descrever os Publicadores e as interfaces de acionamento associadas a esses Publicadores.

</dd> <dt>

<span id="cos.event_method_gloss"></span><span id="COS.EVENT_METHOD_GLOSS"></span>**método de evento**
</dt> <dd>

Um método em uma interface COM+ que identifica um evento COM+. Os métodos de evento devem ser nomeados exclusivamente e podem conter apenas parâmetros de entrada. O valor de retorno deve ser um **HRESULT**.

</dd> <dt>

<span id="cos.event_object_gloss"></span><span id="COS.EVENT_OBJECT_GLOSS"></span>**objeto de evento**
</dt> <dd>

Um objeto COM que pode sinalizar um ou mais threads que um evento ocorreu. Qualquer thread dentro de um processo pode criar um objeto de evento.

</dd> <dt>

<span id="cos.exception_gloss"></span><span id="COS.EXCEPTION_GLOSS"></span>**Exception**
</dt> <dd>

Uma condição anormal ou um erro que ocorre durante a execução de um programa e que requer a execução de software fora do fluxo de controle normal.

</dd> <dt>

<span id="cos.failover_gloss"></span><span id="COS.FAILOVER_GLOSS"></span>**pós-falha**
</dt> <dd>

Em um sistema de rede de cluster, o processo de realocar um recurso sobrecarregado ou com falha, como um servidor, uma unidade de disco ou uma rede, para seu componente de backup.

</dd> <dt>

<span id="cos.free_threaded_process_gloss"></span><span id="COS.FREE_THREADED_PROCESS_GLOSS"></span>**processo de thread livre**
</dt> <dd>

Um processo que tem um apartamento multithread e nenhum Apartments de thread único.

</dd> <dt>

<span id="cos.global_commit_coordinator_gloss"></span><span id="COS.GLOBAL_COMMIT_COORDINATOR_GLOSS"></span>**Coordenador de confirmação global**
</dt> <dd>

em um sistema de transações distribuídas baseado no Microsoft Windows, o gerenciador de transações raiz da árvore de confirmação. Esse coordenador toma a decisão de confirmar ou anular uma determinada transação e nunca é duvidoso.

</dd> <dt>

<span id="cos.impersonation_gloss"></span><span id="COS.IMPERSONATION_GLOSS"></span>**representação**
</dt> <dd>

A capacidade de execução de um thread em um contexto de segurança diferente daquele do processo que possui o thread. O thread do servidor usa um token de acesso que representa as credenciais do cliente e, com isso, ele pode acessar recursos que o cliente pode acessar.

</dd> <dt>

<span id="cos.impersonation_level_gloss"></span><span id="COS.IMPERSONATION_LEVEL_GLOSS"></span>**nível de representação**
</dt> <dd>

A configuração usada pelo cliente para conceder ao servidor um nível específico de autoridade para executar ações em nome do cliente. No COM+, isso pode ser definido somente para aplicativos de servidor COM+.

</dd> <dt>

<span id="cos.interception_gloss"></span><span id="COS.INTERCEPTION_GLOSS"></span>**interceptação**
</dt> <dd>

Para um objeto ativado em um determinado contexto, o processo de tratamento de chamadas para esse objeto entre o limite de contexto. Chamadas no contexto são manipuladas com proxies de interface leves que manipularão qualquer mediação necessária para ajustar o ambiente de tempo de execução de um que acomoda o chamador para um que acomoda o receptor.

</dd> <dt>

<span id="cos.interface_gloss"></span><span id="COS.INTERFACE_GLOSS"></span>**interface**
</dt> <dd>

Na programação baseada em COM, uma coleção de funções públicas relacionadas que fornecem acesso a um objeto COM. O conjunto de interfaces em um objeto COM compõe um contrato que especifica como programas e outros objetos podem interagir com o objeto COM.

</dd> <dt>

<span id="cos.interface_proxy_gloss"></span><span id="COS.INTERFACE_PROXY_GLOSS"></span>**proxy de interface**
</dt> <dd>

Um objeto específico de interface que empacota (empacota) parâmetros para essa interface em preparação para uma chamada de método remota e desempacota (unmarshals) os valores de retorno do stub da interface. Um proxy é executado no espaço de endereço do remetente e se comunica com um stub correspondente no espaço de endereço do destinatário.

</dd> <dt>

<span id="cos.interface_stub_gloss"></span><span id="COS.INTERFACE_STUB_GLOSS"></span>**stub da interface**
</dt> <dd>

Um objeto específico da interface que desempacota parâmetros empacotados, chama o método necessário e pacotes (Marshals) retorna valores do método chamado. O stub é executado no espaço de endereço do destinatário e se comunica com um proxy de interface correspondente no espaço de endereço do remetente.

</dd> <dt>

<span id="cos.interior_object_gloss"></span><span id="COS.INTERIOR_OBJECT_GLOSS"></span>**objeto interior**
</dt> <dd>

Em uma hierarquia transacional, qualquer objeto sob o objeto raiz.

</dd> <dt>

<span id="cos.just_in_time_activation_gloss"></span><span id="COS.JUST_IN_TIME_ACTIVATION_GLOSS"></span>**ativação JIT (just-in-time)**
</dt> <dd>

Um serviço automático fornecido pelo COM+ que permite que os recursos do servidor ocioso sejam usados de forma mais produtiva. Quando um componente é configurado como JIT ativado, o COM+ pode desativar uma instância dele enquanto um cliente ainda mantém uma referência ativa ao objeto. Na próxima vez que o cliente chamar um método no objeto, o COM+ reativará o objeto de forma transparente para o cliente, just-in-time.

</dd> <dt>

<span id="cos.legacy_component_gloss"></span><span id="COS.LEGACY_COMPONENT_GLOSS"></span>**componente herdado**
</dt> <dd>

Um componente não configurado que foi instalado em um aplicativo COM+.

</dd> <dt>

<span id="cos.listener_gloss"></span><span id="COS.LISTENER_GLOSS"></span>**Listener**
</dt> <dd>

Um elemento de arquitetura do serviço de componentes em fila do COM+. O ouvinte é um objeto COM que abre a fila de mensagens associada ao seu aplicativo host e aguarda que as mensagens cheguem. À medida que as mensagens chegam, o ouvinte despacha threads que processam mensagens.

</dd> <dt>

<span id="cos.logical_model_gloss"></span><span id="COS.LOGICAL_MODEL_GLOSS"></span>**modelo lógico**
</dt> <dd>

A segunda etapa em um processo de design de aplicativo COM+, em que o modelo conceitual é dividido em camadas lógicas da arquitetura de três camadas, da seguinte maneira: a camada de apresentação ou os serviços de usuário; a camada intermediária ou os serviços corporativos; e a camada de dados ou serviços de dados.

</dd> <dt>

<span id="cos.loosely_couple_event_gloss"></span><span id="COS.LOOSELY_COUPLE_EVENT_GLOSS"></span>**evento livremente acoplado**
</dt> <dd>

Um evento cujo remetente (Publicador) e destinatário (assinante) não estão ligados de forma rigorosa. Em um sistema de eventos menos rígido, como eventos COM+, as informações de eventos de editores diferentes são mantidas em um repositório de eventos. Os assinantes consultam esse armazenamento e selecionam os eventos que desejam receber. A seleção de informações de evento no repositório de eventos cria uma assinatura. Quando ocorre um evento, o sistema de eventos examina esse banco de dados e encontra os assinantes interessados, cria um novo objeto de cada classe interessada e chama um método nesse objeto.

</dd> <dt>

<span id="cos.marshaling_gloss"></span><span id="COS.MARSHALING_GLOSS"></span>**marshaling**
</dt> <dd>

O processo de empacotamento e desempacotamento de parâmetros do método de interface entre limites de thread ou processo para que uma chamada de procedimento remota possa ocorrer.

</dd> <dt>

<span id="cos.message_mover_gloss"></span><span id="COS.MESSAGE_MOVER_GLOSS"></span>**movimentador de mensagem**
</dt> <dd>

O elemento arquitetônico do serviço de componentes em fila do COM+ que move mensagens com falha de volta para sua fila de entrada para que elas possam ser repetidas.

</dd> <dt>

<span id="cos.meta_event_gloss"></span><span id="COS.META_EVENT_GLOSS"></span>**meta-evento**
</dt> <dd>

Um tipo de evento usado pelo sistema de eventos COM+ para notificar os assinantes interessados sempre que os objetos ou assinaturas da classe de evento forem criados, modificados ou removidos.

</dd> <dt>

<span id="cos.method_gloss"></span><span id="COS.METHOD_GLOSS"></span>**forma**
</dt> <dd>

Na programação baseada em COM, um processo executado por um objeto COM quando recebe uma mensagem.

</dd> <dt>

<span id="cos.middle_tier_gloss"></span><span id="COS.MIDDLE_TIER_GLOSS"></span>**camada intermediária**
</dt> <dd>

No modelo de arquitetura de três camadas para aplicativos de negócios, a camada que consiste na lógica de negócios e nas regras de dados. Os componentes que compõem a camada intermediária podem ser usados para impor regras de negócio, como algoritmos de negócios, regulamentos legais ou governamentais, e regras de dados, que são projetadas para manter as estruturas de dados consistentes em um ou vários bancos de dado. Como esses componentes de camada intermediária não estão vinculados a um cliente específico, eles podem ser usados por todos os aplicativos e podem ser movidos para locais diferentes conforme o tempo de resposta e outras regras exigem. Também chamada de *camada de serviços comerciais* ou camada de *lógica de negócios*.

</dd> <dt>

<span id="cos.mixed_model_process_gloss"></span><span id="COS.MIXED_MODEL_PROCESS_GLOSS"></span>**processo de modelo misto**
</dt> <dd>

Um processo que tem um apartamento multithread e um ou mais Apartments de thread único.

</dd> <dt>

<span id="cos.moniker_gloss"></span><span id="COS.MONIKER_GLOSS"></span>**moniker**
</dt> <dd>

Um nome que identifica exclusivamente um objeto COM. Da mesma forma que um caminho identifica um arquivo no sistema de arquivos, um moniker identifica um objeto COM no namespace do diretório.

</dd> <dt>

<span id="cos.msi_file_gloss"></span><span id="COS.MSI_FILE_GLOSS"></span>**Arquivo de.msi**
</dt> <dd>

Um arquivo criado pela ferramenta administrativa serviços de componentes quando você exporta um aplicativo COM+ ou proxy de aplicativo para instalação em outro computador. o arquivo de .msi pode ser instalado em qualquer cliente baseado em Windows usando Windows Installer.

</dd> <dt>

<span id="cos.multithreaded_apartment_model_gloss"></span><span id="COS.MULTITHREADED_APARTMENT_MODEL_GLOSS"></span>**modelo de apartamento multithread**
</dt> <dd>

Um modelo de apartamento no qual todos os threads no processo que foram inicializados como de thread livre residem em um único apartamento. Portanto, não há necessidade de realizar marshaling entre threads. Os threads não precisam recuperar e despachar mensagens porque o COM não usa mensagens de janela neste modelo.

</dd> <dt>

<span id="cos.nested_transaction_gloss"></span><span id="COS.NESTED_TRANSACTION_GLOSS"></span>**transação aninhada**
</dt> <dd>

Uma transação secundária iniciada de dentro de um limite de transação primária ou pai existente. A transação primária não é confirmada até que todas as suas transações subordinadas ou aninhadas sejam confirmadas. COM+ não dá suporte a transações aninhadas.

</dd> <dt>

<span id="cos.neutral_apartment_model_gloss"></span><span id="COS.NEUTRAL_APARTMENT_MODEL_GLOSS"></span>**modelo de apartamento neutro**
</dt> <dd>

Um modelo de threading no qual os objetos seguem as diretrizes para Apartments multithread, mas podem ser executados em qualquer tipo de thread. O modelo de apartamento neutro é o modelo de Threading recomendado para componentes COM e aplicativos COM+.

</dd> <dt>

<span id="cos.persistent_object_gloss"></span><span id="COS.PERSISTENT_OBJECT_GLOSS"></span>**objeto persistente**
</dt> <dd>

Um objeto COM que pode salvar seu estado interno quando solicitado por um cliente e que esteja em conformidade com os padrões definidos pelo COM por meio dos quais os clientes podem solicitar que os objetos sejam inicializados, carregados e salvos em e de um repositório de dados (por exemplo, arquivo simples, armazenamento estruturado ou memória). É responsabilidade do cliente gerenciar o local onde os dados persistentes do objeto são armazenados, mas não o formato dos dados.

</dd> <dt>

<span id="cos.persistent_object_interface_gloss"></span><span id="COS.PERSISTENT_OBJECT_INTERFACE_GLOSS"></span>**interface de objeto persistente**
</dt> <dd>

Uma interface COM implementada por um objeto persistente. Os clientes usam interfaces de objeto persistentes para informar a esses objetos persistentes quando e onde armazenar seu estado.

</dd> <dt>

<span id="cos.phase_zero_notification_interface_gloss"></span><span id="COS.PHASE_ZERO_NOTIFICATION_INTERFACE_GLOSS"></span>**interface de notificação de fase zero**
</dt> <dd>

Interface COM+ que permite que os aplicativos detectem quando uma transação está pronta para prosseguir com um protocolo de confirmação de duas fases para que possa executar as operações de notificação necessárias e se comunicar com o Gerenciador de transações quando as operações forem concluídas.

</dd> <dt>

<span id="cos.physical_model_gloss"></span><span id="COS.PHYSICAL_MODEL_GLOSS"></span>**modelo físico**
</dt> <dd>

A terceira e última etapa no processo de design do aplicativo COM+, em que o desenvolvedor determina onde os componentes residem fisicamente e como eles devem ser codificados.

</dd> <dt>

<span id="cos.player_gloss"></span><span id="COS.PLAYER_GLOSS"></span>**Player**
</dt> <dd>

O elemento de arquitetura do serviço de componentes em fila do COM+ que recupera a mensagem de uma fila e, em seguida, carrega o objeto de servidor e os stubs de interface padrão para desempacotar dados e invocar métodos de servidor. O Player desempacota o contexto de segurança do cliente no lado do servidor e, em seguida, invoca o componente do servidor e faz as mesmas chamadas de método. As chamadas de método não são reproduzidas pelo Player até que o componente cliente seja concluído e a transação que registrou o método chame confirmações.

</dd> <dt>

<span id="cos.presentation_tier_gloss"></span><span id="COS.PRESENTATION_TIER_GLOSS"></span>**camada de apresentação**
</dt> <dd>

No modelo de arquitetura de três camadas para aplicativos de negócios, a camada que apresenta os dados para o usuário e, opcionalmente, permite a manipulação de dados e a entrada de dados. Os dois tipos principais de interface do usuário para a camada de apresentação são o aplicativo tradicional e o aplicativo baseado na Web. Também chamada de *camada de serviços de usuário*.

</dd> <dt>

<span id="cos.primary_access_token_gloss"></span><span id="COS.PRIMARY_ACCESS_TOKEN_GLOSS"></span>**token de acesso primário**
</dt> <dd>

Descreve o contexto de segurança da conta de usuário associada a um processo.

</dd> <dt>

<span id="cos.proxy_manager_gloss"></span><span id="COS.PROXY_MANAGER_GLOSS"></span>**Gerenciador de proxy**
</dt> <dd>

No empacotamento padrão, um componente que gerencia todos os proxies de interface para um único objeto.

</dd> <dt>

<span id="cos.pseudo_object_gloss"></span><span id="COS.PSEUDO_OBJECT_GLOSS"></span>**pseudo objeto**
</dt> <dd>

Um tipo de objeto contido, como uma seleção de usuário em um documento, um intervalo de células em uma planilha ou um intervalo de caracteres em um documento de texto. Esse tipo de objeto é chamado de pseudo-objeto porque não é tratado como um objeto distinto até que um usuário marque a seleção.

</dd> <dt>

<span id="cos.publisher_gloss"></span><span id="COS.PUBLISHER_GLOSS"></span>**programa**
</dt> <dd>

O remetente de um evento. Na arquitetura de eventos COM+, o Publicador faz a chamada de método para iniciar um evento.

</dd> <dt>

<span id="cos.queue_moniker_gloss"></span><span id="COS.QUEUE_MONIKER_GLOSS"></span>**moniker da fila**
</dt> <dd>

O moniker usado para ativar um componente enfileirado.

</dd> <dt>

<span id="cos.race_condition_gloss"></span><span id="COS.RACE_CONDITION_GLOSS"></span>**condição de corrida**
</dt> <dd>

Em um aplicativo multithread, uma condição que ocorre quando vários threads acessam um item de dados sem coordenação, possivelmente causando resultados inconsistentes, dependendo de qual thread atinge o item de dados primeiro. O COM fornece algumas funções projetadas especificamente para ajudar a evitar condições de corrida em servidores fora do processo.

</dd> <dt>

<span id="cos.recorder_gloss"></span><span id="COS.RECORDER_GLOSS"></span>**gravador**
</dt> <dd>

O elemento arquitetônico do serviço de componentes em fila do COM+ que realiza marshaling do contexto de segurança do cliente em uma mensagem e registra todas as chamadas de método para um objeto. O gravador é um Gerenciador de proxy fornecido pelo sistema que seleciona interfaces das interfaces queuable no catálogo COM+.

</dd> <dt>

<span id="cos.resource_dispenser_gloss"></span><span id="COS.RESOURCE_DISPENSER_GLOSS"></span>**dispensador de recursos**
</dt> <dd>

No modelo de programação COM+, um componente que gerencia o estado compartilhado não durável em nome dos componentes do aplicativo dentro de um processo. Os dispensadores de recursos são semelhantes aos gerenciadores de recursos, mas sem a garantia de durabilidade.

</dd> <dt>

<span id="cos.resource_manager_gloss"></span><span id="COS.RESOURCE_MANAGER_GLOSS"></span>**Gerenciador de recursos**
</dt> <dd>

Um serviço que gerencia dados persistentes ou duráveis em bancos de dado, filas de mensagens duráveis ou sistemas de arquivos transacionais. É o Gerenciador de recursos que sabe como armazenar dados e executar a recuperação de desastres. Os aplicativos de servidor COM+ usam os gerenciadores de recursos para manter o estado durável de um aplicativo, como o registro de estoque disponível, pedidos pendentes e contas a receber. Os gerenciadores de recursos trabalham em cooperação com o Microsoft Coordenador de Transações Distribuídas (DTC) para garantir a atomicidade e o isolamento de um aplicativo.

</dd> <dt>

<span id="cos.role_baed_security_gloss"></span><span id="COS.ROLE_BAED_SECURITY_GLOSS"></span>**segurança baseada em função**
</dt> <dd>

Um serviço de segurança COM+ fornecido para aplicativos COM+. Uma função representa uma categoria de usuários definida para um aplicativo COM+ com a finalidade de determinar as permissões de acesso aos recursos do aplicativo. As funções são atribuídas por um desenvolvedor a componentes, interfaces e métodos. Os usuários são atribuídos por um administrador às funções apropriadas, permitindo que um usuário em uma determinada função acesse todos os recursos aos quais essa função está atribuída.

</dd> <dt>

<span id="cos.root_object_gloss"></span><span id="COS.ROOT_OBJECT_GLOSS"></span>**objeto raiz**
</dt> <dd>

O primeiro objeto de uma transação, chamado de raiz da transação e sempre colocado em um novo limite transacional. Pode haver apenas um objeto raiz em uma transação. Todos os outros objetos na hierarquia transacional sob o objeto raiz são chamados de objetos interiores.

</dd> <dt>

<span id="cos.root_transaction_manager_gloss"></span><span id="COS.ROOT_TRANSACTION_MANAGER_GLOSS"></span>**Gerenciador de transações raiz**
</dt> <dd>

O Gerenciador de transações no sistema que inicia uma transação. A transação não é finalizada até que o Gerenciador de transações raiz determine o status da transação (confirmada ou anulada).

</dd> <dt>

<span id="cos.semaphore_gloss"></span><span id="COS.SEMAPHORE_GLOSS"></span>**sinal**
</dt> <dd>

Um objeto de kernel usado para arbitrar o acesso a um recurso compartilhado.

</dd> <dt>

<span id="cos.service_control_manager_gloss"></span><span id="COS.SERVICE_CONTROL_MANAGER_GLOSS"></span>**SCM (Gerenciador de controle de serviço)**
</dt> <dd>

um processo do Microsoft Windows server que gerencia todos os serviços no registro de Windows.

</dd> <dt>

<span id="cos.shared_property_manager_gloss"></span><span id="COS.SHARED_PROPERTY_MANAGER_GLOSS"></span>**Gerenciador de propriedades compartilhadas (SPM)**
</dt> <dd>

No com+, um dispensador de recursos que você pode usar para compartilhar o estado não persistente entre vários objetos dentro de um processo de servidor.

</dd> <dt>

<span id="cos.single_threaded_process_gloss"></span><span id="COS.SINGLE_THREADED_PROCESS_GLOSS"></span>**processo de thread único**
</dt> <dd>

Um processo que consiste em apenas um apartamento de thread único, que por sua vez consiste em exatamente um thread. Todos os objetos COM que residem em um apartamento de thread único podem receber chamadas de método somente de um thread que pertence a esse apartamento.

</dd> <dt>

<span id="cos.soap_gloss"></span><span id="COS.SOAP_GLOSS"></span>**SOAP**
</dt> <dd>

Um protocolo simples baseado em XML para a troca de informações estruturadas e de tipo na Web. O protocolo não contém nenhuma semântica de aplicativo ou de transporte, o que o torna altamente modular e extensível.

</dd> <dt>

<span id="cos.split_registration_gloss"></span><span id="COS.SPLIT_REGISTRATION_GLOSS"></span>**dividir registro**
</dt> <dd>

para componentes que já são componentes COM e são usados no ambiente de serviços COM+, a disposição de registro na qual o aspecto básico de com do registro é armazenado no registro de Windows e novos serviços e atributos COM+ (por exemplo, componentes na fila) são armazenados no banco de dados de registro do com+. cada atributo de componente é armazenado no registro de Windows ou no banco de dados de registro do COM+. os novos componentes COM são registrados exclusivamente no banco de dados de registro do COM+, com alguma duplicação no registro de Windows para que as ferramentas existentes possam usá-los.

</dd> <dt>

<span id="cos.stateful_gloss"></span><span id="COS.STATEFUL_GLOSS"></span>**dinâmico**
</dt> <dd>

Ou pertencer a um sistema ou processo que monitora todos os detalhes do estado de uma atividade na qual ele participa.

</dd> <dt>

<span id="cos.stateless_gloss"></span><span id="COS.STATELESS_GLOSS"></span>**sem**
</dt> <dd>

Ou pertencer a um sistema ou processo que participa da atividade sem monitorar todos os detalhes de seu estado.

</dd> <dt>

<span id="cos.static_cloaking_gloss"></span><span id="COS.STATIC_CLOAKING_GLOSS"></span>**encobrimento estático**
</dt> <dd>

Uma forma de encobrir onde a identidade do cliente original pode ser apresentada uma vez a um servidor downstream, definindo a identidade do cliente original uma vez no proxy. Essa identidade do cliente é apresentada como um token de thread do servidor que será usado em chamadas de método subsequentes.

</dd> <dt>

<span id="cos.subscriber_gloss"></span><span id="COS.SUBSCRIBER_GLOSS"></span>**farão**
</dt> <dd>

O receptor de um evento. Na arquitetura de Eventos COM+, o assinante recebe as chamadas feitas pelo editor.

</dd> <dt>

<span id="cos.subscription_object_gloss"></span><span id="COS.SUBSCRIPTION_OBJECT_GLOSS"></span>**objeto subscription**
</dt> <dd>

No sistema eventos COM+, um objeto criado por um assinante para solicitar e gerenciar a entrega de eventos.

</dd> <dt>

<span id="cos.synchronization_gloss"></span><span id="COS.SYNCHRONIZATION_GLOSS"></span>**Sincronização**
</dt> <dd>

No COM+, um serviço que flui do componente para o componente e proíbe que mais de um chamador entre no componente a qualquer momento. A sincronização determina quando os threads podem expedir chamadas para um objeto .

</dd> <dt>

<span id="cos.three_tier_architectural_model_gloss"></span><span id="COS.THREE_TIER_ARCHITECTURAL_MODEL_GLOSS"></span>**modelo de arquitetura de três camadas**
</dt> <dd>

A estrutura fundamental para o modelo de design lógico segmenta os componentes de um aplicativo em três camadas de serviços da seguinte maneira: a camada de apresentação ou os serviços de usuário; a camada intermediária ou os serviços de negócios; e a camada de dados ou serviços de dados. Essas camadas não correspondem necessariamente a locais físicos em vários computadores em uma rede, mas sim a camadas lógicas do aplicativo.

</dd> <dt>

<span id="cos.tightly_couple_event_gloss"></span><span id="COS.TIGHTLY_COUPLE_EVENT_GLOSS"></span>**evento firmemente a coupleado**
</dt> <dd>

Um evento cujo remetente (publicador) e receptor (assinante) estão intimamente vinculados. Em um sistema de eventos firmemente a coupleado, o editor é fornecido com uma interface na qual chamar um método quando ocorre uma alteração. O assinante sabe de qual editor solicitar notificação e as interfaces que são expostas. Um sistema de eventos firmemente a coupleado requer que o publicador e o assinante sejam executados em todos os momentos.

</dd> <dt>

<span id="cos.trace_log_gloss"></span><span id="COS.TRACE_LOG_GLOSS"></span>**log de rastreamento**
</dt> <dd>

Um arquivo de log gerado automaticamente pelo Coordenador de Transações Distribuídas da Microsoft que mostra dados relacionados a uma ou mais transações distribuídas. Exemplos de dados em um log de rastreamento são a ID da transação, o tempo de transação e as mensagens que indicam o resultado da transação.

</dd> <dt>

<span id="cos.transaction_gloss"></span><span id="COS.TRANSACTION_GLOSS"></span>**Transação**
</dt> <dd>

Uma unidade de trabalho na qual uma série de operações relacionadas ocorre durante um processo de aplicativo. Uma transação é executada exatamente uma vez e é atômica– todo o trabalho é feito ou nenhum deles é feito.

</dd> <dt>

<span id="cos.transaction_internet_protocol_gloss"></span><span id="COS.TRANSACTION_INTERNET_PROTOCOL_GLOSS"></span>**TIP (Transaction Internet Protocol)**
</dt> <dd>

O Transaction Internet Protocol é um protocolo de confirmação de duas fases padrão que permite que os gerenciadores de transações heterogêneas coordenem transações distribuídas, especialmente pela Internet. O protocolo de confirmação de duas fases TIP é simples de implementar e é independente do protocolo de comunicação de aplicativo para aplicativo, de forma que ele possa ser usado com qualquer protocolo de aplicativo, mas especialmente HTTP.

</dd> <dt>

<span id="cos.transaction_manager_gloss"></span><span id="COS.TRANSACTION_MANAGER_GLOSS"></span>**gerenciador de transações**
</dt> <dd>

A parte do DTC (Coordenador de Transações Distribuídas da Microsoft) que é executada em cada computador que participa de uma transação distribuída e gerencia as atividades relacionadas à confirmação ou anulação dessa parte da transação.

</dd> <dt>

<span id="cos.transaction_processing_application_gloss"></span><span id="COS.TRANSACTION_PROCESSING_APPLICATION_GLOSS"></span>**aplicativo de processamento de transações**
</dt> <dd>

Uma coleção de operações de transação que automatizam uma determinada tarefa de negócios.

</dd> <dt>

<span id="cos.transaction_processing_system_gloss"></span><span id="COS.TRANSACTION_PROCESSING_SYSTEM_GLOSS"></span>**sistema de processamento de transações**
</dt> <dd>

Um sistema completo, composto por hardware e software do computador, que hospeda um aplicativo de processamento de transações para executar transações de rotina necessárias para realizar negócios.

</dd> <dt>

<span id="cos.two_phase_commit_protocol_gloss"></span><span id="COS.TWO_PHASE_COMMIT_PROTOCOL_GLOSS"></span>**protocolo de commit em duas fases**
</dt> <dd>

Um protocolo usado somente em transações distribuídas garante que o resultado de uma transação seja consistente em todos os gerenciadores de transações que participam da transação. O protocolo opera em duas fases distintas para, em última análise, fazer commit ou anular uma transação: a fase um avalia a condição de cada gerenciador de recursos e a fase dois conclui a transação.

</dd> <dt>

<span id="cos.unconfigured_component_gloss"></span><span id="COS.UNCONFIGURED_COMPONENT_GLOSS"></span>**componente não configurado**
</dt> <dd>

Um componente COM que não foi configurado no catálogo COM+. Componentes não configurados não podem usar serviços COM+.

</dd> <dt>

<span id="cos.whereabouts_gloss"></span><span id="COS.WHEREABOUTS_GLOSS"></span>**Paradeiro**
</dt> <dd>

Para transações DTC, uma estrutura de dados opaca que representa o endereço do gerenciador de transações do gerenciador de recursos.

</dd> <dt>

<span id="cos.xa_interfaces_gloss"></span><span id="COS.XA_INTERFACES_GLOSS"></span>**Interfaces XA**
</dt> <dd>

Um conjunto padrão de interfaces de programação que permitem que os desenvolvedores de aplicativos COM+ acessem bancos de dados compatíveis com XA e criem gerenciadores de recursos que operam com bancos de dados relacionais, enxuamento de mensagens, arquivos transacionais e bancos de dados orientados a objeto. Embora a Microsoft não dá suporte direto ao protocolo XA, a Microsoft dá suporte a recursos de tradução entre transações OLE e XA.

</dd> <dt>

<span id="cos.xml_web_services_gloss"></span><span id="COS.XML_WEB_SERVICES_GLOSS"></span>**Serviços Web XML**
</dt> <dd>

Unidades de lógica do aplicativo que fornece dados e serviços para outros aplicativos. Os aplicativos acessam serviços Web XML por meio de protocolos Web padrão, como SOAP.

</dd> </dl>

 

 
