---
title: Integridade e privacidade
description: As comunicações de cliente/serviço que exigem autenticação mútua devem proteger o tráfego que trocam após a autenticação bem-sucedida.
ms.assetid: 5ae3ede3-6eed-4532-9b02-448d2f4ca674
ms.tgt_platform: multiple
keywords:
- AD de integridade e privacidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7c287956fcebc250d5324a15f88fb6a47e087fca40f68f793dd695b47e6719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187100"
---
# <a name="integrity-and-privacy"></a>Integridade e privacidade

As comunicações de cliente/serviço que exigem autenticação mútua devem proteger o tráfego que trocam após a autenticação bem-sucedida. Não é inteligente autenticar mutuamente no momento da conexão inicial com o serviço se o tráfego estiver sujeito posteriormente à modificação por um usuário não autorizado. Todos os SSPI, RPC e COM fornecem utilitários para assinar e criptografar mensagens digitalmente. A aplicação de assinaturas digitais impede que o tráfego modificado não seja detectado e não evita a escuta. O tráfego pode ser interceptado, é claro, mas descriptografar o tráfego é suficientemente difícil para impedir a maioria dos usuários não autorizados.

A menos que os requisitos de desempenho sejam graves, o uso de assinatura e criptografia é recomendado, especialmente para funções administrativas. Mesmo quando o desempenho é um problema, alguns clientes escolhem uma segurança mais rígida em vez de um melhor desempenho. Nesses casos, faça com que as opções de integridade e privacidade configuráveis com maior segurança o padrão e o melhor desempenho da opção.

Os clientes RPC podem especificar o nível de integridade e privacidade quando chamam a função [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) para definir os dados de autenticação para a associação RPC. Use **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ INTEGRITY** para assinatura e **RPC C \_ \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY** para criptografia. Para obter mais informações, consulte [Autenticação mútua em aplicativos RPC.](mutual-authentication-in-rpc-applications.md)

Os serviços que usam um pacote SSPI para autenticação mútua podem consultar o pacote para determinar se ele dá suporte às funções [**MakeSignature**](/windows/desktop/api/sspi/nf-sspi-makesignature), [**VerifySignature,**](/windows/desktop/api/sspi/nf-sspi-verifysignature) [**EncryptMessage**](../SecAuthN/encryptmessage--general.md)e [**DecryptMessage**](../SecAuthN/decryptmessage--general.md) para assinatura e criptografia de mensagens. Para obter mais informações e um exemplo de código, consulte [Garantindo a integridade da comunicação durante a mensagem Exchange](/windows/desktop/SecAuthN/ensuring-communication-integrity-during-message-exchange).

 

 