---
description: Depois que um contexto de segurança é estabelecido, o aplicativo pode usar as funções de suporte a mensagens para transmitir mensagens resistentes a adulterações.
ms.assetid: 43d7b940-1816-429f-be6e-40978efed278
title: Garantindo a integridade da comunicação durante a Exchange de mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 394f78fcc1e5becf4bdfc7c67db52e1af177a7f3aa427d1c6182a080f0ae87bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008254"
---
# <a name="ensuring-communication-integrity-during-message-exchange"></a>Garantindo a integridade da comunicação durante a Exchange de mensagens

Depois que um [*contexto de segurança*](/windows/desktop/SecGloss/s-gly) é estabelecido, o aplicativo pode usar as funções de suporte a [mensagens](authentication-functions.md) para transmitir mensagens resistentes a adulterações.

O cliente ou servidor passa o contexto de segurança e uma mensagem para a função [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) para gerar uma assinatura segura que impede que a mensagem seja modificada durante o trânsito. O receptor da mensagem chama a função [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) . O **VerifySignature** usa as informações na assinatura para verificar se a mensagem recebida não foi modificada durante a transmissão. O cliente e o servidor também podem trocar mensagens criptografadas usando [**EncryptMessage (geral)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) e [**DecryptMessage (geral)**](/windows/win32/api/sspi/nf-sspi-decryptmessage).

O servidor em uma conexão autenticada também pode fazer conexões com outros computadores remotos no nome do cliente depois de chamar [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext).

 

 
