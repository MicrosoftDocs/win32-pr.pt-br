---
title: O que há de novo para a API do servidor HTTP versão 2,0
description: Os recursos a seguir estão disponíveis na API do servidor HTTP versão 2,0.
ms.assetid: 236fdbb0-dead-4b73-9ef6-be2d502b5243
keywords:
- O que há de novo para a API do servidor HTTP versão 2,0
- API do servidor HTTP versão 2,0, o que há de novo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 932a27a45768d0cb00cde4cb89fc4e5d424d1f94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005135"
---
# <a name="whats-new-for-http-server-version-20-api"></a>O que há de novo para a API do servidor HTTP versão 2,0

A API do servidor HTTP versão 2,0 adiciona objetos de configuração de propriedade e gerenciamento avançado da fila de solicitações. Para obter mais informações e uma lista completa de funções, consulte o tópico de [referência do servidor http versão 2,0](http-server-api-version-2-0-reference.md) . Os recursos a seguir estão disponíveis na API do servidor HTTP versão 2,0.

## <a name="configuration-objects"></a>Objetos de configuração

Os objetos de configuração de grupo de URL e de sessão de servidor permitem que os aplicativos configurem o serviço HTTP. A sessão de servidor é o objeto de configuração de nível superior que substitui as configurações padrão da API do servidor HTTP para todos os grupos de URLs criados na sessão. O grupo de URLs, criado em uma sessão de servidor, mantém um conjunto de URLs que recebem as definições de configuração para o grupo. Para obter mais informações, consulte o tópico [arquitetura de http versão 2,0](http-version-2-0-architecture.md) .

## <a name="property-configuration-in-version-20"></a>Configuração de propriedade na versão 2,0

A configuração é executada na sessão do servidor ou nos objetos do grupo de URLs. As configurações de todo o servidor são definidas no objeto de configuração de sessão de servidor. Os grupos de URLs, criados na sessão de servidor, herdam as configurações de sessão de servidor. As configurações definidas no grupo de URLs substituem as configurações de sessão do servidor. As configurações que podem ser definidas pelo aplicativo incluem tempos limite de conexão, limites de conexões, autenticação e registro em log. Para obter mais informações, consulte o tópico [Configurando propriedades em http versão 2,0](configuring-properties-in-http-version-2-0.md) .

## <a name="process-isolation-on-request-queues"></a>Isolamento de processos em filas de solicitações

A fila de solicitações da versão 2,0 dá suporte ao isolamento do processo, permitindo que vários processos de trabalho executem e/s na fila de solicitações. As propriedades de configuração definidas na fila de solicitações permitem que os aplicativos tenham mais controle sobre o serviço. O recurso de fila de solicitação nomeado permite que os aplicativos criem filas de solicitação e as protejam com ACLs (listas de controle de acesso). Os aplicativos que operam em contas de usuário diferentes da conta que criou a fila de solicitações podem abrir a fila de solicitações, receber solicitações e enviar respostas. Para obter mais informações, consulte o tópico [isolamento de processo](process-isolation.md) .

## <a name="full-kernel-mode-ssl"></a>SSL de modo kernel completo

A segurança SSL do modo kernel está habilitada por padrão; também há suporte para certificados de cliente para autenticação mútua. O desempenho é aumentado ao concluir as operações SSL no modo kernel, reduzindo assim as transições entre o kernel e o modo de usuário. Para obter mais informações, consulte o tópico [SSL do modo kernel](kernel-mode-ssl.md) .

## <a name="kernel-mode-response-cache"></a>Cache de resposta do modo kernel

As respostas com conteúdo estático podem ser armazenadas em cache no modo kernel, fornecendo maior desempenho no cache de modo de usuário. A estrutura da política de cache é enviada com a resposta. Para obter mais informações, consulte o [cache do modo kernel no tópico HTTP 2,0](kernel-mode-cache-in-http-2-0.md) .

## <a name="authentication"></a>Autenticação

A \_ resposta http e as \_ estruturas de solicitação HTTP são atualizadas para incluir informações de autenticação. A autenticação no lado do servidor tem suporte para os seguintes esquemas: Negotiate, NTLM, Basic e Digest. Os aplicativos podem especificar os esquemas de autenticação com suporte e definir a ordem de preferência para esses esquemas.

## <a name="object-scoped-versioning"></a>Controle de versão com escopo de objeto

A API do servidor HTTP versão 1,0 passou as informações de versão na chamada para HTTPInitialize. A versão foi definida globalmente para todos os aplicativos no mesmo processo. Na API do servidor HTTP versão 2,0, as informações de versão são fornecidas quando o objeto é criado. Para obter mais informações, consulte [controle de versão na API do servidor http versão 2,0](versioning-in-http-2-0.md).

## <a name="logging"></a>Log

A partir da versão 2,0, o registro em log é configurável por meio da API do servidor HTTP. O registro em log habilitado em uma sessão de servidor serve como forma centralizada de registro em log para o serviço. O registro em log também pode ser habilitado em um grupo de URLs para arquivos de log individualizados. O aplicativo especifica o formato dos arquivos de log, bem como os campos que são registrados em log quanto a erros e transações bem-sucedidas.

## <a name="graceful-request-queue-shutdown"></a>Desligamento de fila de solicitação normal

Os aplicativos podem desligar a fila de solicitações e lidar normalmente com solicitações pendentes na fila antes de encerrar o processo da fila de solicitações. Quando a fila de solicitações é desligada, a API do servidor HTTP para de enfileirar solicitações e redirecionar solicitações pendentes na fila de solicitações.

## <a name="demand-start-on-a-request-queue"></a>Início da demanda em uma fila de solicitações

O recurso de início de demanda na fila de solicitações permite que o aplicativo do controlador adie a instanciação do processo de trabalho até que a primeira solicitação chegue à fila de solicitações. Assim, os aplicativos podem evitar o consumo de recursos até que sejam necessários. Para obter mais informações, consulte o tópico [demanda inicial em filas de solicitação da versão 2,0](demand-start-on-version-2-0-request-queues.md) .

## <a name="port-sharing"></a>Compartilhamento de porta

Os aplicativos baseados em API do servidor HTTP compartilham automaticamente o espaço de escuta de IP com outros aplicativos não HTTP baseados na API do servidor no computador; a lista de escuta de IP não é mais necessária. Quando o aplicativo registra uma URL, a API do servidor HTTP escuta somente no endereço IP e no par de portas especificados.

## <a name="etw-support"></a>Suporte a ETW

O rastreamento avançado usando o ETW (rastreamento de eventos para Windows) permite que os aplicativos tenham mais recursos de diagnóstico. O rastreamento de eventos está disponível para registros e reservas de URL, configuração de propriedade, eventos de cache, autenticação e registro em log para citar alguns.

## <a name="performance-counters"></a>Contadores de desempenho

A ferramenta de contador de desempenho permite que os aplicativos recuperem contadores de serviço e diagnostiquem o desempenho do serviço. Os contadores globais controlam o desempenho do serviço, os contadores de site rastreiam o desempenho do grupo de URLs e os contadores de fila de solicitação acompanham o desempenho da fila de solicitações.

## <a name="international-domain-names-idn"></a>IDNs (nomes de domínio internacional)

Partes internacionalizadas de host e caminho da URL permitem o registro de caminhos e nomes de domínio não ASCII. A API do servidor HTTP processa as URLs Unicode para obedecer aos padrões de IDN.

## <a name="netsh-extensions"></a>Extensões NetSH

O utilitário netsh substitui a ferramenta de HttpCfg.exe disponível no Windows Server 2003 e no Windows XP com Service Pack 2 (SP2). A extensão netsh fornece um meio de gerenciar, diagnosticar e configurar o serviço HTTP. Os administradores podem consultar e definir configurações de todo o servidor, como registros de namespace e certificados SSL.

 

 




