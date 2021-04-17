---
description: Explica como proteger mensagens usando Microsoft Digest.
ms.assetid: 15509d51-80c0-4d5c-aa24-4dc17de3f12c
title: Protegendo mensagens usando Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 573eafcf66e23188546abd3acd316095ec100187
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747301"
---
# <a name="protecting-messages-using-microsoft-digest"></a><span data-ttu-id="4f3b8-103">Protegendo mensagens usando Microsoft Digest</span><span class="sxs-lookup"><span data-stu-id="4f3b8-103">Protecting Messages Using Microsoft Digest</span></span>

## <a name="http-and-sasl"></a><span data-ttu-id="4f3b8-104">HTTP e SASL</span><span class="sxs-lookup"><span data-stu-id="4f3b8-104">HTTP and SASL</span></span>

<span data-ttu-id="4f3b8-105">Como um meio de detectar determinados tipos de violações de segurança, o cliente e o servidor usam as funções de [*integridade*](../secgloss/i-gly.md) de mensagem do SSPI ( [Security Support Provider interface](sspi.md) ) [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) e [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) para proteger as mensagens.</span><span class="sxs-lookup"><span data-stu-id="4f3b8-105">As a means of detecting certain types of security violations, the client and server use the [security support provider interface](sspi.md) (SSPI) message [*integrity*](../secgloss/i-gly.md) functions [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) and [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) to protect messages.</span></span>

<span data-ttu-id="4f3b8-106">Um cliente chama a função [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) para assinar uma mensagem usando seu [*contexto de segurança*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4f3b8-106">A client calls the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) function to sign a message using its [*security context*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="4f3b8-107">O servidor usa a função [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) para verificar a origem da mensagem.</span><span class="sxs-lookup"><span data-stu-id="4f3b8-107">The server uses the [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) function to verify the message's origin.</span></span> <span data-ttu-id="4f3b8-108">Além de verificar a [*assinatura*](../secgloss/d-gly.md) que acompanha a mensagem, a função **VerifySignature** também verifica se a contagem de [*nonce*](../secgloss/n-gly.md) (especificada pela diretiva NC) é uma maior que a última contagem enviada para o nonce.</span><span class="sxs-lookup"><span data-stu-id="4f3b8-108">In addition to verifying the [*signature*](../secgloss/d-gly.md) that accompanies the message, the **VerifySignature** function also checks that the [*nonce*](../secgloss/n-gly.md) count (specified by the nc directive) is one greater than the last count sent for the nonce.</span></span> <span data-ttu-id="4f3b8-109">Se esse não for o caso, a função **VerifySignature** retornará uma SEC \_ fora \_ do \_ código de erro de sequência.</span><span class="sxs-lookup"><span data-stu-id="4f3b8-109">If this is not the case, the **VerifySignature** function returns an SEC\_OUT\_OF\_SEQUENCE error code.</span></span>

## <a name="sasl-only"></a><span data-ttu-id="4f3b8-110">SASL somente</span><span class="sxs-lookup"><span data-stu-id="4f3b8-110">SASL Only</span></span>

<span data-ttu-id="4f3b8-111">As funções [**EncryptMessage (geral)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) e [**DecryptMessage (geral)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) fornecem confidencialidade para mensagens de pós-autenticação trocadas entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="4f3b8-111">The [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) and [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) functions supply confidentiality for post-authentication messages exchanged between client and server.</span></span>

<span data-ttu-id="4f3b8-112">Para usar as funções de confidencialidade da mensagem, o servidor e o cliente devem ter estabelecido um [*contexto de segurança*](../secgloss/s-gly.md) com os seguintes atributos:</span><span class="sxs-lookup"><span data-stu-id="4f3b8-112">In order to use the message confidentiality functions, the server and client must have established a [*security context*](../secgloss/s-gly.md) with the following attributes:</span></span>

-   <span data-ttu-id="4f3b8-113">A qualidade de proteção, especificada pela diretiva QoP, deve ser "auth-conf".</span><span class="sxs-lookup"><span data-stu-id="4f3b8-113">Quality of protection, specified by the qop directive, must be "auth-conf".</span></span>
-   <span data-ttu-id="4f3b8-114">Um mecanismo de criptografia deve ter sido especificado por meio da diretiva de codificação.</span><span class="sxs-lookup"><span data-stu-id="4f3b8-114">An encryption mechanism must have been specified by means of the cipher directive.</span></span>

 

 
