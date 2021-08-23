---
description: O protocolo Kerberos define como os clientes interagem com um serviço de autenticação de rede \[ SDK (Software Development Kit). \]
ms.assetid: e7870e72-1386-4818-bf6f-73430ae942a8
title: Microsoft Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 680a55581394d9d36da5b54cb2365d07384893069e26f9787163209daf2eabd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921788"
---
# <a name="microsoft-kerberos"></a>Microsoft Kerberos

O [*protocolo Kerberos define*](../secgloss/k-gly.md) como os clientes interagem com um serviço de autenticação de rede. Os clientes obtém tíquetes do KDC (centro de distribuição de chaves Kerberos) e apresentam esses tíquetes para servidores quando as conexões são estabelecidas. Os tíquetes Kerberos representam as credenciais de [*rede do cliente.*](../secgloss/c-gly.md)

As informações nesta seção fornece informações teóricos sobre o uso do protocolo Kerberos em um processo de autenticação. Essas são informações em segundo plano que podem ser acrescentadas ao entendimento de um desenvolvedor sobre o que está acontecendo nos bastidores em um processo SSPI que usa o protocolo Kerberos versão 5.

O protocolo de autenticação Kerberos fornece um mecanismo para autenticação mútua entre entidades antes que uma conexão de rede segura seja estabelecida. Ao longo desta documentação, as duas entidades são chamadas de cliente e servidor, embora conexões de rede seguras possam ser feitas entre servidores. O cliente e o servidor também podem ser chamados de [*entidades de segurança.*](../secgloss/s-gly.md)

O protocolo Kerberos presume que as transações entre clientes e servidores ocorrem em uma rede aberta em que a maioria dos clientes e muitos servidores não são fisicamente seguros e os pacotes que viajam pela rede podem ser monitorados e modificados à vontade. O ambiente assumido é como a Internet de hoje, em que um invasor pode facilmente representar como um cliente ou um servidor e pode prontamente escutar ou adulterar as comunicações entre clientes legítimos e servidores.

Esta seção fornece as seguintes informações:

-   [Conceitos básicos de autenticação](basic-authentication-concepts.md)
-   [Subprotocoles kerberos](kerberos-subprotocols.md)
-   [Modelo Kerberos](kerberos-components.md)
-   [Interoperabilidade de SSPI/Kerberos com GSSAPI](sspi-kerberos-interoperability-with-gssapi.md)

Seu aplicativo não deve acessar [](../secgloss/s-gly.md) o pacote de segurança Kerberos diretamente; Em vez disso, ele deve usar o pacote de segurança [*Negotiate.*](../secgloss/n-gly.md) Negociar permite que seu aplicativo aproveite [*protocolos*](../secgloss/s-gly.md) de segurança mais avançados se eles têm suporte pelos sistemas envolvidos na autenticação. Atualmente, o pacote de segurança Negotiate seleciona entre [*Kerberos*](../secgloss/k-gly.md) e NTLM. Negotiate seleciona Kerberos, a menos que ele não possa ser usado por um dos sistemas envolvidos na autenticação.

 

 
