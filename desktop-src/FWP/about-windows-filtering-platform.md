---
title: sobre a plataforma de filtragem de Windows
description: Windows a WFP (plataforma de filtragem) é uma plataforma de processamento de tráfego de rede projetada para substituir as interfaces de filtragem de tráfego de rede Windows XP e Windows Server 2003.
ms.assetid: 6faad008-b2f6-4f45-89c7-ae98c2f58ce1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a81f4f67c2f3281a6fa6b5d3220f9e2157643dfd7cf3bac34ea55743024946
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069486"
---
# <a name="about-windows-filtering-platform"></a>sobre a plataforma de filtragem de Windows

Windows a WFP (plataforma de filtragem) é uma plataforma de processamento de tráfego de rede projetada para substituir as interfaces de filtragem de tráfego de rede Windows XP e Windows Server 2003. A WFP consiste em um conjunto de ganchos na pilha de rede e em um mecanismo de filtragem que coordena as interações de pilha de rede.

## <a name="the-wfp-components"></a>Os componentes de WFP

### <a name="filter-engine"></a>Mecanismo de filtro

a principal infraestrutura de filtragem de várias camadas, hospedada no modo kernel e no modo de usuário, que substitui os vários módulos de filtragem no subsistema de rede Windows XP e Windows Server 2003.

-   Filtra o tráfego de rede em qualquer camada do sistema em qualquer campo de dados que um Shim possa fornecer.
-   Implementa os filtros de "texto explicativo" invocando os textos explicativos durante a classificação.
-   Retorna as ações "permitir" ou "bloquear" para o Shim que a invocou para imposição.
-   Fornece arbitragem entre diferentes fontes de política. Por exemplo, determina a prioridade quando um aplicativo é configurado para proteger qualquer tráfego de rede relacionado a ele, mas o firewall local é configurado para impedir o tráfego protegido do aplicativo.<br/>

### <a name="base-filtering-engine-bfe"></a>Mecanismo de filtragem base (BFE)

um serviço que controla a operação da plataforma de filtragem de Windows. Ele executa as seguintes tarefas.

-   Aceita filtros e outras definições de configuração para a plataforma.
-   Relata o estado atual do sistema, incluindo estatísticas.
-   Impõe o modelo de segurança para aceitar a configuração na plataforma. Por exemplo, um administrador local pode adicionar filtros, mas outros usuários só podem exibi-los.<br/>
-   Direciona definições de configuração para outros módulos no sistema. Por exemplo, as políticas de negociação de IPsec vão para módulos de chaveamento IKE/AuthIP, filtros acessam o mecanismo de filtro.<br/>

### <a name="shims"></a>Shims

Componentes do modo kernel que residem entre a pilha de rede e o mecanismo de filtro. Os shims fazem a decisão de filtragem classificando em relação ao mecanismo de filtro. A seguir está uma lista de shims disponíveis.

-   Shim de aplicação da camada de aplicativo (EPA).
-   Shim do módulo da camada de transporte.
-   Shim do módulo da camada de rede.
-   Shim de erro do protocolo ICMP.
-   Descartar Shim.
-   Shim de fluxo.

### <a name="callouts"></a>Textos explicativos

Conjunto de funções expostas por um driver e usadas para filtragem especializada. Além das ações básicas de "permitir" e "bloquear", os textos explicativos podem modificar e proteger o tráfego de rede de entrada e saída. consulte o tópico [Windows Drivers da plataforma de filtragem de texto explicativos](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) na documentação do Windows Driver Kit (WDK) para obter mais informações sobre textos explicativos. A WFP fornece textos explicativos internos que realizam as seguintes tarefas.<br/>

-   Execute o processamento IPsec.
-   Ajuste o comportamento de filtragem com estado.
-   Execute a filtragem de modo furtivo (queda silenciosa de pacotes que não foram solicitados).
-   Controle o descarregamento de Chimney TCP.
-   Interaja com o serviço Teredo.

<br/> O mecanismo de filtro permite que os textos explicativos de terceiros se registrem em cada uma de suas camadas de modo kernel.<br/>

### <a name="application-programming-interface"></a>Interface de programação de aplicativo

Um conjunto de tipos de dados e funções disponíveis aos desenvolvedores para criar e gerenciar aplicativos de filtragem de rede. Esses tipos de dados e funções são agrupados em vários [conjuntos de API](api-sets.md).

## <a name="wfp-features"></a>Recursos de WFP

-   Fornece uma infraestrutura de filtragem de pacotes em que os ISVs (fornecedores independentes de software) podem conectar módulos de filtragem especializados.
-   Funciona com IPv4 e IPv6.
-   Permite filtragem, modificação e reinjeção de dados.
-   Executa o processamento de pacotes e de fluxo.
-   Permite que a filtragem de pacotes seja habilitada por aplicativo, por usuário e por conexão, além de por interface de rede ou por porta.
-   Fornece segurança de tempo de inicialização até que o BFE (mecanismo de filtragem base) possa ser iniciado.
-   Habilita a filtragem de conexão com estado.
-   Manipula dados de pré e pós-criptografados por IPsec.
-   Permite a integração de políticas de filtragem de firewall e IPsec.
-   Fornece uma infraestrutura de gerenciamento de política para determinar quando filtros específicos devem ser ativados. Isso inclui a mediação de requisitos conflitantes de vários filtros fornecidos por diferentes fornecedores.
-   Lida com a maior parte da remontagem de pacotes e o controle de estado.
-   Inclui um sistema de notificação de usuário genérico que informa os assinantes de alterações no sistema de filtragem.
-   Implementa funções de enumeração que relatam o estado do sistema.
-   Usa eventos de rede para registrar erros de IPsec e quedas de pacotes.
-   Dá suporte a uma [classe auxiliar NDF (](/windows/desktop/NDF/extensible-helper-classes)estrutura de diagnóstico de rede).
-   O oferece suporte às [extensões de soquete seguro](/windows/desktop/WinSock/winsock-secure-socket-extensions) para a API do Winsock, o que permite que os aplicativos de rede protejam seu tráfego configurando a WFP.
-   Em camadas de aplicação de camada de aplicativo (ALE), afeta minimamente o desempenho da rede processando apenas o primeiro pacote em uma conexão.
-   Integra o descarregamento de hardware em que os módulos de texto explicativo em modo kernel podem usar o hardware para executar uma inspeção de pacote específica.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Arquitetura WFP](windows-filtering-platform-architecture-overview.md)
</dt> <dt>

[Operação WFP](basic-operation.md)
</dt> <dt>

[Aplicação da camada de aplicativo (EPA)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Configuração de IPsec](ipsec-configuration.md)
</dt> <dt>

[Configuração de WFP](wfp-configuration.md)
</dt> <dt>

[Monitoramento de WFP](wfp-monitoring.md)
</dt> <dt>

[API WFP](api-sets.md)
</dt> </dl>

 

