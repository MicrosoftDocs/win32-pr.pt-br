---
title: Snego
description: Snego, cujo identificador de serviço de autenticação é RPC \_ C \_ Authn \_ GSS \_ Negotiate, não fornece realmente os próprios serviços de autenticação.
ms.assetid: 2087a84c-d302-4511-9f02-2d20ee9e0d8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a82f8da58cc77ebfd4debd0763ad4af6e1c96d3e88d9ede69ff82a28e3d8a5ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129808"
---
# <a name="snego"></a>Snego

Snego, cujo identificador de serviço de autenticação é RPC \_ C \_ Authn \_ GSS \_ Negotiate, não fornece realmente os próprios serviços de autenticação. Em vez disso, ele usa uma lista de serviços de autenticação e negocia um serviço que funcionará entre o cliente e o servidor. Os parâmetros de autenticação não são usados por Snego, mas são passados para o serviço de autenticação escolhido, que faz a autenticação real. O Snego foi padronizado pela IETF (Internet Engineering Task Force) em dezembro de 1998, no documento [RFC 2478](https://www.ietf.org/rfc/rfc2478.txt).

Snego é útil quando você não sabe quais serviços de autenticação o computador remoto pode fornecer.

Para usar o Snego, o cliente e o servidor devem especificar Snego como o serviço de autenticação. O servidor especifica o RPC \_ C \_ Authn \_ GSS \_ Negotiate como o membro **dwAuthnSvc** de uma das estruturas de [**\_ \_ serviço de autenticação exclusivas**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) no parâmetro de matriz *asAuthSvc* que é passado para [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). O cliente pode especificar Snego chamando [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) e passando RPC \_ C \_ Authn \_ GSS \_ Negotiate como o parâmetro *dwAuthnSvc* . O cliente também deve fornecer uma lista de possíveis serviços de autenticação para Snego por meio do membro **PackageList** da estrutura da [**\_ \_ \_ identidade \_ de autenticação WinNT do s**](/windows/desktop/api/sspi/ns-sspi-_sec_winnt_auth_identity_exa) , que é passada para o parâmetro *pAuthInfo* na chamada para **CoSetProxyBlanket**. Se *pAuthInfo* for **nulo**, Snego comporá uma lista de serviços de autenticação dos pacotes de segurança instalados no computador. Em seguida, Snego envia a lista de serviços de autenticação para o servidor, compara a lista com os serviços de autenticação disponíveis do servidor e escolhe um serviço de autenticação a ser usado para a conexão.

> [!Note]  
> O Schannel não pode estar na lista de serviços de autenticação que o Snego usa.

 

Os clientes também podem especificar Snego ao chamar [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Os parâmetros *dwAuthnSvc* e *pAuthInfo* de [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) tornam-se membros de uma única estrutura de [**\_ \_ informações de autenticação**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) que é passada para **CoInitializeSecurity** por meio de seu parâmetro *pAuthList* . Os detalhes dos valores desses membros são os mesmos descritos no parágrafo anterior.

Se Snego for usado, as chamadas para [**CoQueryProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket) ou [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket) retornarão Snego como o serviço de autenticação, em vez do serviço de autenticação real que Snego escolhido para estabelecer a conexão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pacotes de segurança e COM](com-and-security-packages.md)
</dt> </dl>

 

 