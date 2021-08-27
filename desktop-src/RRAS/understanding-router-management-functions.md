---
title: Noções básicas sobre funções de gerenciamento de roteador
description: As seções a seguir discutem os diferentes tipos de funções de gerenciamento de roteador e o que você deve saber para usá-las com eficiência.
ms.assetid: 2f6831f2-39be-43b1-80bd-9a36c0f8a2af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85aac5cc2ec0167527f07c04459ec0aed7dbc248bed727fb4a949765c2fdcc4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025396"
---
# <a name="understanding-router-management-functions"></a>Noções básicas sobre funções de gerenciamento de roteador

As seções a seguir discutem os diferentes tipos de funções de gerenciamento de roteador e o que você deve saber para usá-las com eficiência.

Todas as funções de gerenciamento de roteador exigem privilégios de administrador. Um usuário no grupo Power User não tem privilégios suficientes para usar as funções de gerenciamento de roteador.

## <a name="the-different-classes-of-router-management-functions"></a>As diferentes classes de funções de gerenciamento de roteador

As funções de gerenciamento de roteador podem ser divididas nas funções de administração e nas funções de configuração. As [funções de administração](router-administration-functions.md) têm um prefixo MprAdmin e as funções [de](router-configuration-functions.md) configuração têm um prefixo MprConfig. Apesar da nomeação, ambos os conjuntos de funções são usados para gerenciamento de roteador. As funções MprAdmin operam diretamente no roteador em execução. As funções MprConfig têm funcionalidade semelhante, mas operam na configuração do roteador armazenada no Registro. Ambos os tipos de funções passam blocos [de informações](router-information-functions.md).

As funções de gerenciamento de roteador também podem ser divididas com base em quais componentes do roteador eles gerenciam: interfaces, gerenciadores de roteador ou clientes do gerenciador de roteador.

As [funções de interface do roteador](router-interface-functions.md) têm um prefixo de MprAdminInterface ou MprConfigInterface. Use essas funções para acessar interfaces. As [funções de gerenciador de roteador](router-manager-transport-functions.md) têm um prefixo MprAdminTransport ou MprConfigTransport. Use essas funções para acessar os gerenciadores de roteador. Por fim, as funções de cliente do gerenciador [de](router-manager-client-interfacetransport-functions.md) roteador têm um prefixo de MprAdminInterfaceTransport ou MprConfigInterfaceTransport. Use essas funções para acessar os clientes em execução no roteador.

Um subconjunto de funções MprAdmin são as [funções MprAdminMib](/windows/desktop/RRAS/about-router-management-with-mib). Elas também operam apenas na rota em execução. No entanto, essas funções não passam blocos de informações. Essas funções fornecem flexibilidade adicional para o designer de protocolo, especialmente para recuperar informações que não são de configuração, como estatísticas.

## <a name="ensuring-that-changes-occur-immediately-and-are-persistent"></a>Garantir que as alterações ocorram imediatamente e sejam persistentes

Um desenvolvedor pode fazer alterações na configuração do roteador diretamente usando as [funções de configuração do roteador](router-configuration-functions.md). No entanto, as alterações feitas na configuração não entre em vigor até que o roteador seja reiniciado, pois essa é a única vez que o DIM lê a configuração do Registro.

Um desenvolvedor pode fazer alterações no roteador em execução usando as funções [de administração do roteador](router-administration-functions.md). No entanto, essas alterações não são persistentes: como elas não foram escritas no Registro, elas serão perdidas se o roteador for reiniciado.

Para fazer alterações imediatas e persistentes, um desenvolvedor precisa usar a administração do roteador e as funções de configuração do roteador. Se o roteador não estiver em execução, o desenvolvedor só precisará chamar as funções de configuração de roteador apropriadas.

Para consultar informações do roteador em execução, use as funções de administração do roteador. Se o roteador não estiver em execução, consulte as informações usando as funções de configuração do roteador.

As [**funções MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) [**e MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) são suportadas pela estrutura [**\_ MPR INTERFACE \_ 2.**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_2) No entanto, [**MprConfigInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacecreate) e [**MprConfigInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo) não. Para criar uma interface discada por demanda persistente após uma reinicialização, chame **MprAdminInterfaceCriar** com INTERFACE **\_ \_ MPR 2** e, em seguida, chame **MprConfigInterfaceCriar** com INTERFACE [**\_ \_ MPR 0**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) ou [**INTERFACE MPR \_ \_ 1.**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_1) Da mesma forma, para fazer alterações persistentes em uma interface discagem por demanda, chame **MprAdminInterfaceSetInfo** com **\_ INTERFACE \_ MPR 2** e, em seguida, chame **MprConfigInterfaceSetInfo** com INTERFACE **\_ \_ MPR 0** ou **INTERFACE \_ \_ MPR 1**.

## <a name="using-router-administration-and-configuration-functions-remotely"></a>Usando funções de administração e configuração de roteador remotamente

A maioria das funções de administração e configuração do roteador pode ser chamada em um computador diferente do que está sendo administrado. Essas funções levam como parâmetro, um handle para o serviço de roteador ou a configuração a ser administrada. As funções de administração usam RPC (Chamada de Procedimento Remoto) para se comunicar com o serviço de roteamento especificado pelo handle. As funções de configuração são escritas e lidas no registro do computador especificado pelo handle.

Para administrar o serviço de roteamento em um computador remoto, primeiro chame [**MprAdminIsServiceRunning**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning) para verificar se o serviço está em execução. Em seguida, [**chame MprAdminServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect) para obter o handle. Se o serviço de roteador não estiver em execução no computador remoto, todas as chamadas de administração de roteador (MprAdmin) falharão.

Para fazer alterações na configuração do roteador em um computador remoto, obtenha um handle chamando a [**função MprConfigServerConnect.**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigserverconnect)

 

 