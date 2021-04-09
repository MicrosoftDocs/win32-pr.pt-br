---
description: Depois que um contexto de segurança é estabelecido, o aplicativo pode usar as funções de suporte a mensagens para transmitir mensagens resistentes a adulterações.
ms.assetid: 43d7b940-1816-429f-be6e-40978efed278
title: Garantindo a integridade da comunicação durante a troca de mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70545abf11a933cd3bb6d0c32f3312637fcccbe2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090199"
---
# <a name="ensuring-communication-integrity-during-message-exchange"></a><span data-ttu-id="dc1ea-103">Garantindo a integridade da comunicação durante a troca de mensagens</span><span class="sxs-lookup"><span data-stu-id="dc1ea-103">Ensuring Communication Integrity During Message Exchange</span></span>

<span data-ttu-id="dc1ea-104">Depois que um [*contexto de segurança*](/windows/desktop/SecGloss/s-gly) é estabelecido, o aplicativo pode usar as funções de suporte a [mensagens](authentication-functions.md) para transmitir mensagens resistentes a adulterações.</span><span class="sxs-lookup"><span data-stu-id="dc1ea-104">After a [*security context*](/windows/desktop/SecGloss/s-gly) is established, the application can use the [message support](authentication-functions.md) functions to transmit tamper-resistant messages.</span></span>

<span data-ttu-id="dc1ea-105">O cliente ou servidor passa o contexto de segurança e uma mensagem para a função [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) para gerar uma assinatura segura que impede que a mensagem seja modificada durante o trânsito.</span><span class="sxs-lookup"><span data-stu-id="dc1ea-105">The client or server passes the security context and a message to the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) function to generate a secure signature that prevents the message from being modified while in transit.</span></span> <span data-ttu-id="dc1ea-106">O receptor da mensagem chama a função [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) .</span><span class="sxs-lookup"><span data-stu-id="dc1ea-106">The receiver of the message calls the [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) function.</span></span> <span data-ttu-id="dc1ea-107">O **VerifySignature** usa as informações na assinatura para verificar se a mensagem recebida não foi modificada durante a transmissão.</span><span class="sxs-lookup"><span data-stu-id="dc1ea-107">**VerifySignature** uses the information in the signature to verify that the message received was not modified during transmission.</span></span> <span data-ttu-id="dc1ea-108">O cliente e o servidor também podem trocar mensagens criptografadas usando [**EncryptMessage (geral)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) e [**DecryptMessage (geral)**](/windows/win32/api/sspi/nf-sspi-decryptmessage).</span><span class="sxs-lookup"><span data-stu-id="dc1ea-108">The client and server can also exchange encrypted messages using [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) and [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage).</span></span>

<span data-ttu-id="dc1ea-109">O servidor em uma conexão autenticada também pode fazer conexões com outros computadores remotos no nome do cliente depois de chamar [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext).</span><span class="sxs-lookup"><span data-stu-id="dc1ea-109">The server in an authenticated connection can also make connections with other remote computers in the name of the client after calling [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext).</span></span>

 

 
