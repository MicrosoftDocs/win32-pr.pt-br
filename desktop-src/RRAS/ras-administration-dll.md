---
title: Sobre DLLs de administração de RAS
description: A DLL de administração de RAS exporta as funções que o servidor RAS chama sempre que um usuário tenta se conectar ou se desconectar.
ms.assetid: c15c6e2d-3bb6-4583-9ac3-19528feb863f
keywords:
- Administração de RAS RRAS, DLL de administração de RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb170e8cfa331ab9591aa509772c6f6a743fa49
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104498958"
---
# <a name="about-ras-administration-dlls"></a>Sobre DLLs de administração de RAS

A DLL de administração de RAS exporta as funções que o servidor RAS chama sempre que um usuário tenta se conectar ou se desconectar. Aqui estão alguns dos usos possíveis para uma DLL de administração de RAS:

-   Decida se deseja permitir que um usuário se conecte ao servidor. A DLL de administração pode fornecer uma verificação de segurança além da autenticação de usuário RAS padrão.
-   Registre a hora em que cada usuário se conecta e se desconecta do servidor. Isso pode ser útil para fins de cobrança ou auditoria.
-   Atribua um endereço IP a cada usuário. Isso é útil para segurança, pois esse recurso é usado para mapear a conexão de um usuário para um computador específico.

O local da DLL de administração de RAS é especificado no registro; consulte [configuração do registro da DLL de administração do RAS](ras-administration-dll-registry-setup.md).

O RAS dá suporte a várias DLLs de administração. O registro dá suporte a vários locais de DLL. O RAS chama as funções nas DLLs na ordem em que as DLLs são listadas no registro; consulte [configuração do registro da DLL de administração do RAS](ras-administration-dll-registry-setup.md).

**Servidor do Windows 2000:** O RAS não dá suporte a várias DLLs.

Uma DLL de administração de RAS deve implementar e exportar todas as seguintes funções:

[**MprAdminAcceptNewLink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)

[**MprAdminInitializeDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininitializedll)

[**MprAdminLinkHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)

[**MprAdminTerminateDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminterminatedll)

Além disso, a DLL de administração de RAS deve implementar e exportar qualquer um

[**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) e

[**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification)

ou

[**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) e

[**MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)

Se todas as funções necessárias não forem implementadas, o RAS falhará ao iniciar.

**Servidor do Windows 2000:** Uma DLL de administração deve implementar as funções [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) e [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) . Se a DLL implementar uma dessas funções, ela também deverá implementar a outra.

O RAS chama a função [**MprAdminInitializeDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininitializedll) quando o serviço de roteamento e acesso remoto é iniciado pela primeira vez. A função **MprAdminInitializeDll** fornece uma oportunidade para que a DLL de administração faça qualquer inicialização necessária. Da mesma forma, o RAS chama o serviço [**MprAdminTerminateDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminterminatedll) quando o serviço de roteamento e acesso remoto é desligado. Essa função permite que a DLL de administração execute qualquer limpeza necessária antes de sair.

As funções [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) e [**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification) permitem que a dll faça auditoria de conexões de usuário com o servidor. Um servidor RAS chama a função **MprAdminAcceptNewConnection** sempre que um usuário tenta se conectar. Essa função torna possível impedir que o usuário se conecte. A função **MprAdminAcceptNewConnection** também pode gerar entradas de log para cobrança ou auditoria. Quando o usuário se desconecta, o servidor RAS chama a função **MprAdminConnectionHangupNotification** , que pode registrar a hora em que o usuário se desconectou.

As funções [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) e [**MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2) são semelhantes a **MprAdminAcceptNewConnection** e [**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification). No entanto, quando o RAS chama as funções **MprAdminAcceptNewConnection2** e **MPRADMINCONNECTIONHANGUPNOTIFICATION2** , o RAS passa em um parâmetro adicional do tipo [**\_ conexão RAS \_ 2**](/windows/desktop/api/Mprapi/ns-mprapi-ras_connection_2).

O RAS dá suporte a várias DLLs de administração. O usuário de acesso remoto tem permissão para se conectar somente se a implementação da função [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) ou [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) em cada uma das DLLs aceitar a conexão. Em outras palavras, cada DLL deve aceitar a conexão para que o usuário tenha permissão para se conectar.

É possível que uma única conexão RAS use vários links ao se conectar a um servidor RAS. As funções [**MprAdminAcceptNewLink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink) e [**MprAdminLinkHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification) POSSIBILITAm que a DLL de administração gerencie links individuais em uma conexão. O RAS chama **MprAdminAcceptNewLink** sempre que um novo link é estabelecido para uma conexão. Como todas as conexões envolvem pelo menos um link, o RAS sempre chama **MprAdminAcceptNewLink** uma vez imediatamente após o retorno de [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) ou [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) , desde que [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) ou [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) aceitem a conexão. O RAS chama **MprAdminLinkHangupNotification** sempre que um link para uma conexão é desligado.

Como o RAS dá suporte a várias DLLs de administração, o usuário de acesso remoto tem permissão para se conectar somente se a implementação da função [**MprAdminAcceptNewLink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink) em cada uma das DLLs aceitar a conexão. Em outras palavras, cada DLL deve aceitar o link para que o link seja estabelecido.

Depois que o servidor RAS tiver autenticado um usuário, ele chamará a função [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) para obter um endereço IP para o cliente remoto. Essa função fornece um esquema alternativo para mapear um endereço IP para um usuário de conexão discada. Se **MprAdminGetIpAddressForUser** não for implementado, um servidor RAS associará o usuário remoto a um endereço IP que é selecionado de um pool estático de endereços IP ou um selecionado por um servidor DHCP (protocolo de configuração dinâmica de hosts). A função **MprAdminGetIpAddressForUser** permite que a dll Substitua esse endereço IP padrão e especifique um endereço IP específico para cada usuário. A função **MprAdminGetIpAddressForUser** pode definir um sinalizador que faz com que o RAS chame a função [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) quando o usuário se desconecta. Em seguida, a DLL pode usar **MprAdminReleaseIpAddress** para atualizar seu mapeamento de endereço de usuário para IP.

O RAS dá suporte a várias DLLs de administração, mas chama as funções [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) e [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) somente na primeira dll que implementa e exporta. O RAS ignora implementações dessas funções em outras DLLs. O RAS verifica as DLLs para essas funções na ordem em que estão listadas no [registro](ras-administration-dll-registry-setup.md).

O RAS serializa chamadas para a DLL de administração. Uma chamada em uma das funções da DLL para um determinado cliente RAS não antecipa uma chamada para essa função para um cliente RAS diferente; O RAS não chama a função para o outro cliente até que a chamada inicial seja concluída. Além disso, a serialização se estende a determinados grupos de funções. As funções de endereço IP são serializadas como um grupo; uma chamada para [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) ou [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) bloqueia chamadas em ambas as funções até que a chamada inicial seja retornada. [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) e [**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification) também são serializados como um grupo.

O RAS executa as funções que atribuem endereços IP em um único processo; as funções para conexão e notificações de desconexão são executadas em outro processo. Consequentemente, a DLL não depende de dados compartilhados entre esses dois conjuntos de funções.

Não chame nenhuma das funções de [Administração de Ras](ras-administration-functions.md) ou [funções de administração de usuário de Ras](ras-user-administration-functions.md) de dentro de uma função de texto explicativo. As chamadas para essas funções não serão retornadas quando feitas de dentro de uma função de texto explicativo.

O servidor RAS registra um erro no log de eventos do sistema se ocorrer um erro ao tentar carregar uma DLL de administração de RAS ou ao chamar uma das funções da DLL. Isso pode acontecer, por exemplo, se a DLL especificou o nome errado para uma função exportada ou se ela não incluía o nome da função no arquivo DEF. A entrada no log de eventos indica o motivo da falha.

**Windows 2000/NT:** Não há suporte para várias DLLs de administração.

 

 




