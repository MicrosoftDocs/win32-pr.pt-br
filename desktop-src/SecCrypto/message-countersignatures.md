---
description: Às vezes, uma mensagem assinada requer uma referenda.
ms.assetid: de83a9ad-4e88-4477-8c9e-6dd7d5ec9e8f
title: Referendas de mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8dff2920217dd9a79f917f7b625da3919747d7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647306"
---
# <a name="message-countersignatures"></a><span data-ttu-id="8a1a7-103">Referendas de mensagem</span><span class="sxs-lookup"><span data-stu-id="8a1a7-103">Message Countersignatures</span></span>

<span data-ttu-id="8a1a7-104">Às vezes, uma mensagem assinada requer uma [*referenda*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8a1a7-104">Sometimes a signed message requires a [*countersignature*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="8a1a7-105">Por exemplo, o usuário A pode enviar uma mensagem de dados assinados para o usuário B, esperando que B confirme o contrato com os termos contidos no documento.</span><span class="sxs-lookup"><span data-stu-id="8a1a7-105">For example, user A may send a signed-data message to user B, expecting B to confirm agreement with the terms contained in the document.</span></span> <span data-ttu-id="8a1a7-106">O usuário B decodifica a mensagem, lê os termos e, se estiver no contrato, faz a assinatura da mensagem.</span><span class="sxs-lookup"><span data-stu-id="8a1a7-106">User B decodes the message, reads the terms and, if in agreement, countersigns the message.</span></span> <span data-ttu-id="8a1a7-107">A mensagem de assinatura é enviada de volta para o usuário A. o usuário A agora sabe, e pode provar que o usuário B concordou com os termos.</span><span class="sxs-lookup"><span data-stu-id="8a1a7-107">The countersigned message is then sent back to user A. User A now knows, and can prove, that user B agreed to the terms.</span></span>

<span data-ttu-id="8a1a7-108">A tabela a seguir lista as seções que contêm descrições de procedimento ou exemplos de programa C de assinatura de mensagem.</span><span class="sxs-lookup"><span data-stu-id="8a1a7-108">The following table lists sections that contain procedure descriptions or C program examples of message countersigning.</span></span>



| <span data-ttu-id="8a1a7-109">Seção</span><span class="sxs-lookup"><span data-stu-id="8a1a7-109">Section</span></span>                                                                                                                                 | <span data-ttu-id="8a1a7-110">Sumário</span><span class="sxs-lookup"><span data-stu-id="8a1a7-110">Contents</span></span>                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="8a1a7-111">Funções de mensagem</span><span class="sxs-lookup"><span data-stu-id="8a1a7-111">Message Functions</span></span>](cryptography-functions.md)                                                                       | <span data-ttu-id="8a1a7-112">Lista as funções de assinatura do contador.</span><span class="sxs-lookup"><span data-stu-id="8a1a7-112">Lists the counter signature functions.</span></span>                             |
| [<span data-ttu-id="8a1a7-113">Como assinar uma mensagem</span><span class="sxs-lookup"><span data-stu-id="8a1a7-113">Countersigning a Message</span></span>](countersigning-a-message.md)                                                                                | <span data-ttu-id="8a1a7-114">Detalha o processo de assinatura de contador de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="8a1a7-114">Details the process of counter signing a message.</span></span>                  |
| [<span data-ttu-id="8a1a7-115">Verificando uma referenda</span><span class="sxs-lookup"><span data-stu-id="8a1a7-115">Verifying a Countersignature</span></span>](verifying-a-countersignature.md)                                                                        | <span data-ttu-id="8a1a7-116">Detalha o procedimento para verificar uma assinatura de contador.</span><span class="sxs-lookup"><span data-stu-id="8a1a7-116">Details the procedure for verifying a counter signature.</span></span>           |
| [<span data-ttu-id="8a1a7-117">Verificando uma mensagem assinada</span><span class="sxs-lookup"><span data-stu-id="8a1a7-117">Verifying a Signed Message</span></span>](verifying-a-signed-message.md)                                                                            | <span data-ttu-id="8a1a7-118">Detalha um processo para verificar a assinatura em uma mensagem assinada.</span><span class="sxs-lookup"><span data-stu-id="8a1a7-118">Details a process for verifying the signature on a signed message.</span></span> |
| [<span data-ttu-id="8a1a7-119">Programa C de exemplo: codificando e decodificando uma mensagem de assinatura</span><span class="sxs-lookup"><span data-stu-id="8a1a7-119">Example C Program: Encoding and Decoding a CounterSigned Message</span></span>](example-c-program-encoding-and-decoding-a-countersigned-message.md) | <span data-ttu-id="8a1a7-120">Programa C de exemplo que codifica e decodifica uma mensagem de assinatura.</span><span class="sxs-lookup"><span data-stu-id="8a1a7-120">Sample C program that encodes and decodes a countersigned message.</span></span> |



 

 

 
