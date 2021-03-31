---
title: DLL de administração de RAS
description: A DLL exporta as funções que o servidor RAS chama sempre que um usuário tenta se conectar ou se desconectar.
ms.assetid: 014ab85d-8924-4c7a-89ed-f83e75318ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0908032e0916f0937e964408b1551d3f1515dea
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104293606"
---
# <a name="ras-administration-dll"></a>DLL de administração de RAS

A DLL exporta as funções que o servidor RAS chama sempre que um usuário tenta se conectar ou se desconectar. Você pode usar a DLL para executar as seguintes funções administrativas:

-   Decida se deseja permitir que um usuário se conecte ao servidor. Isso pode fornecer uma verificação de segurança além da autenticação de usuário RAS padrão.
-   Registre a hora em que cada usuário se conecta e se desconecta do servidor. Isso pode ser útil para fins de cobrança ou auditoria.
-   Atribua um endereço IP a cada usuário. Isso pode ser útil para fins de segurança para mapear a conexão de um usuário para um computador específico.

Implemente as funções a seguir ao desenvolver uma DLL de administração do servidor RAS.

-   [**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
-   [**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md)
-   [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md)
-   [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md)

Uma DLL de administração de RAS deve implementar e exportar todas as funções acima. Se qualquer uma das funções não for implementada, o serviço de acesso remoto não será iniciado.

As funções [**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md) e [**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md) permitem que a dll faça auditoria de conexões de usuário com o servidor. Um servidor RAS do Windows NT/Windows 2000 chama a função **RasAdminAcceptNewConnection** sempre que um usuário tenta se conectar. A função pode impedir que o usuário se conecte. Você também pode usar a função para gerar uma entrada em um log para cobrança ou auditoria. Quando o usuário se desconecta, o servidor RAS chama a função **RasAdminConnectionHangupNotification** , que pode registrar a hora em que o usuário se desconectou.

Depois que o servidor RAS tiver autenticado um chamador, ele chamará a função [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) para obter um endereço IP para o cliente remoto. A DLL pode usar essa função para fornecer um esquema alternativo para o mapeamento de um endereço IP para um usuário de conexão discada. Se o **RasAdminGetIpAddressForUser** não for implementado, um servidor RAS conectará um usuário remoto a um endereço IP selecionado de um pool estático de endereços IP ou um selecionado por um servidor DHCP (protocolo de configuração dinâmica de hosts). A função **RasAdminGetIpAddressForUser** permite que a dll Substitua esse endereço IP padrão e especifique um endereço IP específico para cada usuário. A função **RasAdminGetIpAddressForUser** pode definir um sinalizador que faz com que o RAS chame a função [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md) quando o usuário se desconecta. A DLL pode usar [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md) para atualizar seu mapa de endereço de usuário para IP.

O RAS serializa chamadas para a DLL de administração. Uma chamada em uma das funções da DLL para um determinado cliente RAS nunca será admitida por uma chamada para essa função para um cliente RAS diferente; a chamada inicial é garantida para ser concluída antes que o RAS chame a função para o outro cliente. Além disso, a serialização se estende a determinados grupos de funções. As funções de endereço IP são serializadas como um grupo; uma chamada para [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) ou [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md) bloqueará chamadas em ambos até que a chamada inicial seja concluída. [**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md) e [**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md) também são serializados como um grupo.

O RAS executa as funções para atribuir endereços IP em um processo e executa as funções de notificações de conexão e desconexão em outro processo. Consequentemente, a DLL não deve depender de dados compartilhados entre os dois conjuntos de funções.

O servidor RAS registra um erro no log de eventos do sistema se ocorrer um erro ao tentar carregar uma DLL de administração de RAS ou ao chamar uma das funções da DLL. Isso pode acontecer, por exemplo, se a DLL especificou o nome errado para uma função exportada ou se ela não incluía o nome da função no arquivo. def. A entrada no log de eventos indica o motivo da falha.

**Windows 2000 Server e posterior:** As DLLs de administração de RAS que implementam essa interface de função não funcionam mais. Em vez disso, use a interface de função MprAdmin fornecida com as versões mais recentes do Windows. Para obter mais informações, consulte a [referência de administração de Ras](remote-access-service-administration-reference.md) na documentação de roteamento e RAS.

 

 




