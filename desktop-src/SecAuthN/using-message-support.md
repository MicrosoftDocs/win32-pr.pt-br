---
description: Explica como usar o suporte a mensagens SSPI.
ms.assetid: 14d4813e-413e-4ef9-85f0-96986c3c1eca
title: Usando o suporte a mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d75a2475609afed1647d99552a3719479d84fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755568"
---
# <a name="using-message-support"></a><span data-ttu-id="93452-103">Usando o suporte a mensagens</span><span class="sxs-lookup"><span data-stu-id="93452-103">Using Message Support</span></span>

<span data-ttu-id="93452-104">Depois que um Handshake for concluído e uma conexão segura tiver sido estabelecida, um aplicativo poderá usar as funções [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), [**EncryptMessage (geral)**](/windows/win32/api/sspi/nf-sspi-encryptmessage), [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature)e [**DecryptMessage (geral)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) para trocar dados de aplicativo assinados ou criptografados com o computador remoto.</span><span class="sxs-lookup"><span data-stu-id="93452-104">After a handshake has been completed and a secure connection has been established, an application can use the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage), [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature), and [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) functions to exchange signed or encrypted application data with the remote computer.</span></span>

<span data-ttu-id="93452-105">Os exemplos que usam essas funções depois que um [*contexto de segurança*](../secgloss/s-gly.md) foi estabelecido são demonstrados nas seções a seguir:</span><span class="sxs-lookup"><span data-stu-id="93452-105">Examples that use these functions after a [*security context*](../secgloss/s-gly.md) has been established are demonstrated in the following sections:</span></span>

-   [<span data-ttu-id="93452-106">Assinando uma mensagem</span><span class="sxs-lookup"><span data-stu-id="93452-106">Signing a Message</span></span>](signing-a-message.md)
-   [<span data-ttu-id="93452-107">Verificando uma mensagem</span><span class="sxs-lookup"><span data-stu-id="93452-107">Verifying a Message</span></span>](verifying-a-message.md)
-   [<span data-ttu-id="93452-108">Criptografando uma mensagem</span><span class="sxs-lookup"><span data-stu-id="93452-108">Encrypting a Message</span></span>](encrypting-a-message.md)
-   [<span data-ttu-id="93452-109">Descriptografando uma mensagem</span><span class="sxs-lookup"><span data-stu-id="93452-109">Decrypting a Message</span></span>](decrypting-a-message.md)

 

 
