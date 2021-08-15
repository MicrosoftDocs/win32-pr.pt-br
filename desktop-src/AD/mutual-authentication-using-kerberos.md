---
title: Autenticação mútua usando Kerberos
description: A autenticação mútua é um recurso de segurança no qual um processo de cliente deve provar sua identidade para um serviço e o serviço deve provar sua identidade para o cliente, antes que qualquer tráfego de aplicativo seja transmitido pela conexão cliente/serviço.
ms.assetid: 775dd350-5c70-4d97-aa2f-d21e9aecc778
ms.tgt_platform: multiple
keywords:
- Active Directory, usando a autenticação mútua
- Active Directory, usando, segurança, autenticação mútua
- AD de segurança
- AD de segurança, autenticação mútua
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e22a9f83712b15f22f9d9b05aee4219f3cbc892d88d0b44ba2d63fb9bbe2b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185946"
---
# <a name="mutual-authentication-using-kerberos"></a>Autenticação mútua usando Kerberos

A autenticação mútua é um recurso de segurança no qual um processo de cliente deve provar sua identidade para um serviço e o serviço deve provar sua identidade para o cliente, antes que qualquer tráfego de aplicativo seja transmitido pela conexão cliente/serviço.

Active Directory Domain Services e Windows dão suporte a SPN (nomes de entidade de serviço), que são um componente fundamental no mecanismo Kerberos pelo qual um cliente autentica um serviço. Um SPN é um nome exclusivo que identifica uma instância de um serviço e está associado à conta de logon na qual a instância de serviço é executado. Os componentes de um SPN são de tal forma que um cliente pode compor um SPN para um serviço sem a conta de logon do serviço. Isso permite que o cliente solicite ao serviço para autenticar sua conta, mesmo que o cliente não tenha o nome da conta.

Esta seção inclui uma visão geral de:

-   Autenticação mútua usando Kerberos.
-   Compondo um SPN exclusivo.
-   Como um instalador de serviço registra SPNs no objeto de conta associado a uma instância de serviço.
-   Como um aplicativo cliente usa um objeto SCP (ponto de conexão de serviço) da instância de serviço no Active Directory Domain Services para recuperar dados dos quais compor um SPN para o serviço.
-   Como um aplicativo cliente usa um SPN de serviço em conjunto com a SSPI (Interface do Provedor de Suporte de Segurança) para autenticar o serviço.
-   Um exemplo de código para um Windows de serviço/cliente soquetes que usa um SCP e um SSPI para executar autenticação mútua.
-   Um exemplo de código para um cliente/serviço RPC que executa autenticação mútua usando o serviço de nome RPC e a autenticação RPC.
-   Como um Windows RnR (registro e resolução de soquetes) usa SPNs para executar autenticação mútua.

Esta seção discute o uso do Domínio do Active Directory para autenticação mútua, em particular, a finalidade dos pontos de conexão de serviço e nomes de entidade de serviço na autenticação mútua. Não é uma discussão completa sobre como usar o SSPI para autenticação mútua ou o suporte de autenticação e segurança disponível para aplicativos RPC e Windows Sockets.

Para obter mais informações, consulte:

-   [Publicação com pontos de conexão de serviço](publishing-with-service-connection-points.md)
-   [SSPI](/windows/desktop/SecAuthN/sspi)
-   [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
-   [RPC](/windows/desktop/Rpc/rpc-start-page)

 

 