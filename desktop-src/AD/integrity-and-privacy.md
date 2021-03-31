---
title: Integridade e privacidade
description: As comunicações de cliente/serviço que exigem autenticação mútua devem proteger o tráfego que eles trocam após a autenticação bem-sucedida.
ms.assetid: 5ae3ede3-6eed-4532-9b02-448d2f4ca674
ms.tgt_platform: multiple
keywords:
- AD de integridade e privacidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88ed167c3796aec2b0717b1207ff56565ec94afa
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103917119"
---
# <a name="integrity-and-privacy"></a>Integridade e privacidade

As comunicações de cliente/serviço que exigem autenticação mútua devem proteger o tráfego que eles trocam após a autenticação bem-sucedida. Não é recomendável autenticar mutuamente no momento da conexão inicial com o serviço se o tráfego for posteriormente sujeito a modificações por um usuário não autorizado. SSPI, RPC e COM todos fornecem utilitários para assinar digitalmente e criptografar mensagens. A aplicação de assinaturas digitais impede que o tráfego modificado não seja detectado e desanime a espionagem. O tráfego pode ser interceptado, mas a descriptografia do tráfego é suficientemente difícil de deter a maioria dos usuários não autorizados.

A menos que os requisitos de desempenho sejam graves, o uso de assinatura e criptografia é recomendado, especialmente para funções administrativas. Mesmo quando o desempenho é um problema, alguns clientes escolhem uma segurança mais rígida com um melhor desempenho. Nesses casos, torne as opções configuráveis de integridade e privacidade com maior segurança o desempenho padrão e superior da opção.

Os clientes RPC podem especificar o nível de integridade e privacidade quando chamam a função [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) para definir os dados de autenticação para a associação RPC. Use **a \_ \_ integridade do \_ PCT do \_ nível \_ de autenticação RPC c** para assinatura e a **\_ \_ \_ \_ \_ privacidade do PCT do nível de autenticação RPC c** para criptografia. Para obter mais informações, consulte [autenticação mútua em aplicativos RPC](mutual-authentication-in-rpc-applications.md).

Os serviços que usam um pacote SSPI para autenticação mútua podem consultar o pacote para determinar se ele dá suporte às funções [**MakeSignature**](/windows/desktop/api/sspi/nf-sspi-makesignature), [**VerifySignature**](/windows/desktop/api/sspi/nf-sspi-verifysignature), [**EncryptMessage**](../SecAuthN/encryptmessage--general.md)e [**DecryptMessage**](../SecAuthN/decryptmessage--general.md) para assinar e criptografar mensagens. Para obter mais informações e um exemplo de código, consulte [garantindo a integridade da comunicação durante a troca de mensagens](/windows/desktop/SecAuthN/ensuring-communication-integrity-during-message-exchange).

 

 