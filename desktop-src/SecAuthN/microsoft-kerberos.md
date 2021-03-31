---
description: O protocolo Kerberos define como os clientes interagem com um \[ SDK (Software Development Kit) da plataforma de serviço de autenticação de rede \] .
ms.assetid: e7870e72-1386-4818-bf6f-73430ae942a8
title: Microsoft Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03787bcc65959838ea02c49958d9ca4e0405649
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920855"
---
# <a name="microsoft-kerberos"></a>Microsoft Kerberos

O [*protocolo Kerberos*](../secgloss/k-gly.md) define como os clientes interagem com um serviço de autenticação de rede. Os clientes obtêm tíquetes do centro de distribuição de chaves do Kerberos (KDC) e apresentam esses tíquetes para servidores quando as conexões são estabelecidas. Os tíquetes Kerberos representam as [*credenciais*](../secgloss/c-gly.md)de rede do cliente.

As informações nesta seção fornecem um plano de fundo teórico sobre o uso do protocolo Kerberos em um processo de autenticação. Essas são informações básicas que podem ser adicionadas ao conhecimento de um desenvolvedor sobre o que está acontecendo nos bastidores em um processo SSPI que usa o protocolo Kerberos versão 5.

O protocolo de autenticação Kerberos fornece um mecanismo para autenticação mútua entre entidades antes de uma conexão de rede segura ser estabelecida. Durante toda a documentação, as duas entidades são chamadas de cliente e servidor, mesmo que conexões de rede seguras possam ser feitas entre servidores. Tanto o cliente quanto o servidor também podem ser chamados de [*entidades de segurança*](../secgloss/s-gly.md).

O protocolo Kerberos assume que as transações entre clientes e servidores ocorrem em uma rede aberta, na qual a maioria dos clientes e muitos servidores não são fisicamente protegidos, e os pacotes que viajam pela rede podem ser monitorados e modificados ao mesmo tempo. O ambiente assumido é como a Internet de hoje, em que um invasor pode facilmente representar como um cliente ou um servidor, e pode rapidamente bisbilhotar ou adulterar as comunicações entre clientes e servidores legítimos.

Esta seção fornece as seguintes informações:

-   [Conceitos básicos de autenticação](basic-authentication-concepts.md)
-   [Subprotocolos Kerberos](kerberos-subprotocols.md)
-   [Modelo Kerberos](kerberos-components.md)
-   [Interoperabilidade de SSPI/Kerberos com GSSAPI](sspi-kerberos-interoperability-with-gssapi.md)

Seu aplicativo não deve acessar o [*pacote de segurança*](../secgloss/s-gly.md) Kerberos diretamente; em vez disso, ele deve usar o pacote de segurança [*Negotiate*](../secgloss/n-gly.md) . Negociar permite que seu aplicativo aproveite os [*protocolos de segurança*](../secgloss/s-gly.md) mais avançados se eles tiverem suporte dos sistemas envolvidos na autenticação. Atualmente, o pacote de segurança Negotiate seleciona entre [*Kerberos*](../secgloss/k-gly.md) e NTLM. Negociar seleciona Kerberos, a menos que não possa ser usado por um dos sistemas envolvidos na autenticação.

 

 
