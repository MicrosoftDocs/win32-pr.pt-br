---
title: Visão geral do cenário do SSO EAPHost
description: Contém dois cenários que demonstram as vantagens de um suplicante habilitado para SSO (logon único).
ms.assetid: 2a5cbcae-74fe-4241-9e20-ec1ec5d9ed8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc9be7af26844004073f21154df5ac12cb44d4eaa04fddc457b729ffe5e1083
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042774"
---
# <a name="sso-eaphost-scenario-overview"></a>Visão geral do cenário do SSO EAPHost

O tópico a seguir contém dois cenários que demonstram as vantagens de um suplicante habilitado para SSO (logon único).

## <a name="about-the-scenarios"></a>Sobre os cenários

O SSO fornece a funcionalidade para reter informações de credenciais de usuário adicionais do que é tradicionalmente armazenado no BLOB de usuário EAP. Ao contrário de outros processos de credenciais, os suplicantes habilitados para SSO podem resolver situações de logon como roaming de AP e alteração de senha sem intervenção do usuário.

## <a name="sso-eap-tls-pin-caching-behavior"></a>comportamento de Caching de PIN do SSO EAP-TLS

Um suplicante pode tentar a autenticação de rede usando um método EAP baseado em cartão inteligente, como EAP-TLS (Extensible Authentication Protocol Transport Layer Security). Nesse e em cenários semelhantes, o suplicante Obtém o PIN do cartão inteligente do usuário e recupera um certificado de usuário para autenticação de rede seguido de uma chamada para WinLogin no computador local. Após a autenticação bem-sucedida, o suplicante armazena em cache o BLOB do usuário e não armazena informações de PIN do usuário.

Quando o usuário faz roaming em uma sessão de local diferente, a retomada e a nova autenticação devem ocorrer. Como o certificado não pode ser armazenado antes do logon, a autenticação do usuário falhará e o suplicante liberará o BLOB do usuário. Neste ponto, o PIN do usuário é necessário para recuperar o certificado do usuário do cartão inteligente para autenticação de rede. Como o SSO armazena em cache o PIN, o certificado pode ser recuperado sem a intervenção do usuário. Sem o SSO, o EAP-TLS teria que gerar uma interface do usuário de coleção de PIN novamente.

para obter uma abordagem passo a passo, consulte [comportamento de Caching do PIN do SSO EAP-TLS](sso-eap-tls-pin-caching-behavior-.md).

## <a name="sso-password-change-behavior"></a>Comportamento de alteração de senha de SSO

Um suplicante pode tentar a autenticação de rede usando um método EAP baseado em senha, como o Microsoft Challenge Handshake Authentication Protocol versão 2,0 (MS-CHAPv2), configurado para usar as credenciais do WinLogin. Nesse cenário, o suplicante coleta as credenciais do usuário uma vez e as fornece para o EAPHost para a autenticação de rede. Após a autenticação de rede bem-sucedida, o suplicante usa o mesmo conjunto de credenciais para WinLogin.

No entanto, se as credenciais, como a senha do usuário, forem alteradas durante a autenticação de rede sem um suplicante habilitado para SSO, a chamada WinLogin subsequente resultará em falha. O SSO retém as novas credenciais e permite um WinLogin bem-sucedido sem intervenção adicional do usuário.

Para obter uma abordagem passo a passo, consulte [comportamento de alteração de senha de SSO](sso-password-change-behavior-.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[SSO e PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

 




