---
title: Noções básicas sobre funções de gerenciamento de roteador
description: As seções a seguir discutem os diferentes tipos de funções de gerenciamento de roteador e o que você deve saber para usá-las com eficiência.
ms.assetid: 2f6831f2-39be-43b1-80bd-9a36c0f8a2af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be4b1891bc55b80a18a6d0dd928044da1e0e9709
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105759600"
---
# <a name="understanding-router-management-functions"></a>Noções básicas sobre funções de gerenciamento de roteador

As seções a seguir discutem os diferentes tipos de funções de gerenciamento de roteador e o que você deve saber para usá-las com eficiência.

Todas as funções de gerenciamento de roteador exigem privilégios de administrador. Um usuário no grupo de usuários avançados não tem privilégios suficientes para usar as funções de gerenciamento de roteador.

## <a name="the-different-classes-of-router-management-functions"></a>As diferentes classes de funções de gerenciamento de roteador

As funções de gerenciamento de roteador podem ser divididas nas funções de administração e nas funções de configuração. As [funções de administração](router-administration-functions.md) têm um prefixo de MprAdmin e as [funções de configuração](router-configuration-functions.md) têm um prefixo de MprConfig. Apesar da nomenclatura, ambos os conjuntos de funções são usados para o gerenciamento de roteador. As funções MprAdmin operam diretamente no roteador em execução. As funções MprConfig têm funcionalidade semelhante, mas operam na configuração do roteador armazenada no registro. Os dois tipos de funções passam por [blocos de informações](router-information-functions.md).

As funções de gerenciamento de roteador também podem ser divididas com base em quais componentes do roteador eles gerenciam: interfaces, gerenciadores de roteadores ou clientes do Gerenciador de roteador.

As [funções de interface do roteador](router-interface-functions.md) têm um prefixo de MprAdminInterface ou MprConfigInterface. Use essas funções para acessar interfaces. As [funções do Gerenciador de roteador](router-manager-transport-functions.md) têm um prefixo de MprAdminTransport ou MprConfigTransport. Use essas funções para acessar os gerenciadores de roteador. Por fim, as [funções de cliente do Gerenciador de roteador](router-manager-client-interfacetransport-functions.md) têm um prefixo de MprAdminInterfaceTransport ou MprConfigInterfaceTransport. Use essas funções para acessar os clientes em execução no roteador.

Um subconjunto de funções MprAdmin são as [funções MprAdminMib](/windows/desktop/RRAS/about-router-management-with-mib). Eles também funcionam apenas na rota em execução. No entanto, essas funções não passam por blocos de informações. Essas funções fornecem flexibilidade adicional ao designer de protocolo, especialmente para recuperar informações que não são de configuração, como estatísticas.

## <a name="ensuring-that-changes-occur-immediately-and-are-persistent"></a>Garantindo que as alterações ocorram imediatamente e sejam persistentes

Um desenvolvedor pode fazer alterações na configuração do roteador diretamente usando as [funções de configuração do roteador](router-configuration-functions.md). No entanto, as alterações feitas na configuração não entram em vigor até que o roteador seja reiniciado, já que essa é a única vez que DIM lê a configuração do registro.

Um desenvolvedor pode fazer alterações no roteador em execução usando as [funções de administração do roteador](router-administration-functions.md). No entanto, essas alterações não são persistentes: como elas não foram gravadas no registro, elas serão perdidas se o roteador for reiniciado.

Para fazer alterações imediatas e persistentes, um desenvolvedor precisa usar ambas as funções de administração de roteador e de configuração de roteador. Se o roteador não estiver em execução, o desenvolvedor precisará chamar apenas as funções de configuração apropriadas do roteador.

Para consultar informações do roteador em execução, use as funções de administração do roteador. Se o roteador não estiver em execução, consulte as informações usando as funções de configuração do roteador.

As funções [**MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) e [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) dão suporte à estrutura [**MPR \_ interface \_ 2**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_2) . No entanto, [**MprConfigInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacecreate) e [**MprConfigInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo) não. Para criar uma interface de discagem por demanda persistente após uma reinicialização, chame **MprAdminInterfaceCreate** com **a \_ interface \_ de MPR 2** e, em seguida, chame **MprConfigInterfaceCreate** com a interface de [**MPR \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) ou a [**interface de MPR \_ \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_1). Da mesma forma, para fazer alterações persistentes em uma interface de discagem por demanda, chame **MprAdminInterfaceSetInfo** com a **interface de MPR \_ \_ 2** e, em seguida, chame **MprConfigInterfaceSetInfo** com a interface de **MPR \_ \_ 0** ou **MPR \_ interface \_ 1**.

## <a name="using-router-administration-and-configuration-functions-remotely"></a>Usando funções de administração e configuração de roteador remotamente

A maioria das funções de administração e configuração do roteador pode ser chamada em um computador diferente daquele que está sendo administrado. Essas funções usam como um parâmetro, um identificador para o serviço de roteador ou a configuração para administrar. As funções de administração usam RPC (chamada de procedimento remoto) para se comunicar com o serviço de roteamento especificado pelo identificador. As funções de configuração gravam e lêem o registro do computador especificado pelo identificador.

Para administrar o serviço de roteamento em uma máquina remota, primeiro chame [**MprAdminIsServiceRunning**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning) para verificar se o serviço está em execução. Em seguida, chame [**MprAdminServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect) para obter o identificador. Se o serviço de roteador não estiver em execução no computador remoto, todas as chamadas de administração de roteador (MprAdmin) falharão.

Para fazer alterações na configuração do roteador em um computador remoto, obtenha um identificador chamando a função [**MprConfigServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigserverconnect) .

 

 