---
description: Se um arquivo de configuração automática de proxy não tiver sido implantado na rede local, o WinHttpGetProxyForUrl não poderá localizar um servidor proxy.
ms.assetid: a170e63a-8586-47df-af5e-4ee3621795b2
title: Descoberta sem um arquivo de configuração automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a5ec281c2ef74e2a377cecbd30f16cbc49bd79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105786300"
---
# <a name="discovery-without-an-auto-config-file"></a>Descoberta sem um arquivo de configuração automática

Se um arquivo de configuração automática de proxy não tiver sido implantado na rede local, o [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) não poderá localizar um servidor proxy. Se **WinHttpGetProxyForUrl** falhar, haverá várias estratégias de retirada possíveis para obter uma configuração de proxy viável, dependendo de seu ambiente de tempo de execução. Isso inclui solicitar a configuração de proxy por meio de uma interface do usuário, exigindo que alguém armazene a configuração de proxy no registro usando o utilitário "ProxyCfg.exe" do WinHTTP ou usando [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) para verificar se um servidor proxy está listado nas configurações do Internet Explorer.

É possível que não haja nenhum arquivo de configuração automática de proxy porque o cliente tem uma conexão direta com a Internet, por exemplo, por meio de um ISP, e não precisa de um servidor proxy.

Um servidor proxy pode ser necessário, por outro lado, mas a rede local pode não oferecer suporte a WPAD. Nesse caso, a configuração de proxy deve ser obtida do usuário ou encontrada em algum lugar no computador cliente.

Um aplicativo baseado em WinHTTP em execução em um ambiente de servidor de camada intermediária, como um aplicativo COM+ ou ASP, deve contar com um administrador de servidor definindo uma configuração de proxy padrão no registro usando o utilitário "ProxyCfg.exe". Essas informações de configuração padrão podem então ser recuperadas usando a função [**WinHttpGetDefaultProxyConfiguration**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration) ou simplesmente especificando o sinalizador de **\_ \_ \_ configuração do tipo de acesso WinHTTP** na chamada [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) .

Por outro lado, um aplicativo WinHTTP em execução em um computador desktop cliente pode tentar examinar as configurações de proxy do Internet Explorer. O [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) preenche uma estrutura de [**\_ \_ \_ \_ \_ configuração de proxy do usuário atual do WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) , fornecida pelo chamador, com as configurações de proxy do Internet Explorer do usuário atual para a conexão ativa atual (dial-up, VPN ou LAN). Essa configuração pode indicar que a detecção automática é usada, ou pode especificar uma URL para um arquivo de configuração automática de proxy, ou pode especificar um servidor proxy real a ser usado, ou pode especificar uma combinação dos três. Se essas informações incluírem uma URL PAC ou um servidor proxy, o aplicativo WinHTTP poderá tentar usá-la.

Um exemplo que usa as funções [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) e [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) pode ser encontrado nos exemplos de WinHTTP do SDK (Software Development Kit) da plataforma.

 

 



