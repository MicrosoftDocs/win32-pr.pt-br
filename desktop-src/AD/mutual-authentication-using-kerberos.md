---
title: Autenticação mútua usando Kerberos
description: A autenticação mútua é um recurso de segurança no qual um processo de cliente deve provar sua identidade para um serviço, e o serviço deve provar sua identidade para o cliente, antes que qualquer tráfego de aplicativo seja transmitido pela conexão de cliente/serviço.
ms.assetid: 775dd350-5c70-4d97-aa2f-d21e9aecc778
ms.tgt_platform: multiple
keywords:
- Active Directory, usando a autenticação mútua
- Active Directory, usando, segurança, autenticação mútua
- ANÚNCIO de segurança
- segurança do AD, autenticação mútua
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cf2e68c1983dde9221cc3fa89866b5358ee6eb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "105753621"
---
# <a name="mutual-authentication-using-kerberos"></a>Autenticação mútua usando Kerberos

A autenticação mútua é um recurso de segurança no qual um processo de cliente deve provar sua identidade para um serviço, e o serviço deve provar sua identidade para o cliente, antes que qualquer tráfego de aplicativo seja transmitido pela conexão de cliente/serviço.

Active Directory Domain Services e Windows oferecem suporte para SPN (nomes de entidade de serviço), que são um componente-chave no mecanismo Kerberos pelo qual um cliente autentica um serviço. Um SPN é um nome exclusivo que identifica uma instância de um serviço e está associado à conta de logon na qual a instância de serviço é executada. Os componentes de um SPN são de tal forma que um cliente pode compor um SPN para um serviço sem a conta de logon do serviço. Isso permite que o cliente solicite ao serviço que autentique sua conta, mesmo que o cliente não tenha o nome da conta.

Esta seção inclui uma visão geral do:

-   Autenticação mútua usando Kerberos.
-   Compor um SPN exclusivo.
-   Como um instalador de serviço registra SPNs no objeto de conta associado a uma instância de serviço.
-   Como um aplicativo cliente usa um objeto SCP (ponto de conexão de serviço) da instância de serviço no Active Directory Domain Services para recuperar dados dos quais compor um SPN para o serviço.
-   Como um aplicativo cliente usa um SPN de serviço em conjunto com a interface de provedor de suporte de segurança (SSPI) para autenticar o serviço.
-   Um exemplo de código para um aplicativo de serviço/cliente do Windows Sockets que usa um SCP e SSPI para executar a autenticação mútua.
-   Um exemplo de código para um cliente/serviço RPC que executa autenticação mútua usando o serviço de nome RPC e a autenticação RPC.
-   Como um serviço de RnR (registro e resolução do Windows Sockets) usa SPNs para executar a autenticação mútua.

Esta seção aborda o uso do serviço Domínio do Active Directory para autenticação mútua, em particular, a finalidade dos pontos de conexão de serviço e nomes de entidade de serviço na autenticação mútua. Não é uma discussão completa de como usar SSPI para autenticação mútua ou autenticação e suporte de segurança disponíveis para aplicativos RPC e Windows Sockets.

Para obter mais informações, consulte:

-   [Publicando com pontos de conexão de serviço](publishing-with-service-connection-points.md)
-   [SSPI](/windows/desktop/SecAuthN/sspi)
-   [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
-   [RPC](/windows/desktop/Rpc/rpc-start-page)

 

 