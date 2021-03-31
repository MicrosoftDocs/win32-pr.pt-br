---
description: As funções de mensagem de nível baixo codificam dados para transmissão e decodificação de dados recebidos. Funções de mensagem de nível baixo também descriptografam e verificam as assinaturas de mensagens recebidas.
ms.assetid: 42c19920-c7f7-4a4d-9de3-3de9a34fbe0c
title: Funções de mensagem de nível baixo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22654f19dfe5178dfb98006c17c2d0536f78cd46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647307"
---
# <a name="low-level-message-functions"></a><span data-ttu-id="dca05-104">Funções de mensagem de nível baixo</span><span class="sxs-lookup"><span data-stu-id="dca05-104">Low-level Message Functions</span></span>

<span data-ttu-id="dca05-105">As [*funções de mensagem de nível baixo*](../secgloss/l-gly.md) codificam dados para transmissão e decodificação de dados recebidos.</span><span class="sxs-lookup"><span data-stu-id="dca05-105">The [*low-level message functions*](../secgloss/l-gly.md) encode data for transmission and decode data that has been received.</span></span> <span data-ttu-id="dca05-106">Funções de mensagem de nível baixo também descriptografam e verificam as assinaturas de mensagens recebidas.</span><span class="sxs-lookup"><span data-stu-id="dca05-106">Low-level message functions also decrypt and verify the signatures of received messages.</span></span>

<span data-ttu-id="dca05-107">Quando uma mensagem é aberta usando uma função Open de baixo nível, ela permanece aberta e disponível (mantém seu [*estado*](../secgloss/s-gly.md)) até que seja fechada.</span><span class="sxs-lookup"><span data-stu-id="dca05-107">When a message is opened using a low-level message open function, it remains open and available (maintains its [*state*](../secgloss/s-gly.md)) until it is closed.</span></span> <span data-ttu-id="dca05-108">Isso permite que uma mensagem seja construída gradativamente usando várias chamadas para a função [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) .</span><span class="sxs-lookup"><span data-stu-id="dca05-108">This allows a message to be constructed piecemeal using multiple calls to the [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) function.</span></span>

<span data-ttu-id="dca05-109">O uso de funções de mensagens de nível baixo requer mais chamadas de função do que o uso de funções de mensagens simplificadas (consulte [mensagens simplificadas](simplified-messages.md)).</span><span class="sxs-lookup"><span data-stu-id="dca05-109">Using low-level message functions requires more function calls than using simplified message functions (see [Simplified Messages](simplified-messages.md)).</span></span> <span data-ttu-id="dca05-110">Se as funções de mensagem simplificadas forem usadas, mais trabalho será feito dentro das funções da API.</span><span class="sxs-lookup"><span data-stu-id="dca05-110">If the simplified message functions are used, more of the work is done inside the functions of the API.</span></span>

<span data-ttu-id="dca05-111">O uso de funções de mensagens de nível baixo envolve o trabalho adicional de fazer chamadas para outras funções de certificado ou de criptografia.</span><span class="sxs-lookup"><span data-stu-id="dca05-111">Using low-level message functions involves the additional work of making calls to other certificate or cryptographic functions.</span></span> <span data-ttu-id="dca05-112">Por exemplo, os dados de chamadas para funções de certificado podem ser necessários para inicializar estruturas usadas por essas funções de mensagens de nível baixo.</span><span class="sxs-lookup"><span data-stu-id="dca05-112">For example, data from calls to certificate functions may be needed to initialize structures used by these low-level message functions.</span></span> <span data-ttu-id="dca05-113">As funções de mensagens simplificadas inicializam muitas dessas estruturas internamente.</span><span class="sxs-lookup"><span data-stu-id="dca05-113">Simplified message functions initialize many of these structures internally.</span></span>

<span data-ttu-id="dca05-114">A tabela a seguir lista seções com descrições de procedimento e exemplos de código C de como usar as funções de mensagens de nível baixo.</span><span class="sxs-lookup"><span data-stu-id="dca05-114">The following table lists sections with procedure descriptions and C code examples of using the low-level message functions.</span></span>



| <span data-ttu-id="dca05-115">Seção</span><span class="sxs-lookup"><span data-stu-id="dca05-115">Section</span></span>                                                                               | <span data-ttu-id="dca05-116">Sumário</span><span class="sxs-lookup"><span data-stu-id="dca05-116">Contents</span></span>                                           |
|---------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="dca05-117">Funções de mensagem de nível baixo</span><span class="sxs-lookup"><span data-stu-id="dca05-117">Low-level Message Functions</span></span>](cryptography-functions.md) | <span data-ttu-id="dca05-118">Lista as funções de mensagem de nível baixo.</span><span class="sxs-lookup"><span data-stu-id="dca05-118">Lists the low-level message functions.</span></span>             |
| [<span data-ttu-id="dca05-119">Dados de assinatura</span><span class="sxs-lookup"><span data-stu-id="dca05-119">Signing Data</span></span>](signing-data.md)                                                      | <span data-ttu-id="dca05-120">Detalha as tarefas necessárias para assinar dados.</span><span class="sxs-lookup"><span data-stu-id="dca05-120">Details the tasks needed to sign data.</span></span>             |
| [<span data-ttu-id="dca05-121">Codificando dados Envelopos</span><span class="sxs-lookup"><span data-stu-id="dca05-121">Encoding Enveloped Data</span></span>](encoding-enveloped-data.md)                                | <span data-ttu-id="dca05-122">Detalha as tarefas necessárias para codificar dados de envelope.</span><span class="sxs-lookup"><span data-stu-id="dca05-122">Details the tasks needed to encode enveloped data.</span></span> |
| [<span data-ttu-id="dca05-123">Decodificando dados envelopado</span><span class="sxs-lookup"><span data-stu-id="dca05-123">Decoding Enveloped Data</span></span>](decoding-enveloped-data.md)                                | <span data-ttu-id="dca05-124">Detalha as tarefas necessárias para decodificar dados de envelope.</span><span class="sxs-lookup"><span data-stu-id="dca05-124">Details the tasks needed to decode enveloped data.</span></span> |



 

 

 
