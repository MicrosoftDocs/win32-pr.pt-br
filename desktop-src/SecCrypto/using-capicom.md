---
description: Esta seção inclui cenários que usam procedimentos CAPICOM.
ms.assetid: f886e04a-4ea7-4d24-a05f-3e08742fe134
title: Usando CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f81b1a346b6186ead6544b7194259cc52ae2be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502179"
---
# <a name="using-capicom"></a><span data-ttu-id="e23df-103">Usando CAPICOM</span><span class="sxs-lookup"><span data-stu-id="e23df-103">Using CAPICOM</span></span>

<span data-ttu-id="e23df-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e23df-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e23df-105">Em vez disso, use o .NET Framework para implementar recursos de segurança.</span><span class="sxs-lookup"><span data-stu-id="e23df-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="e23df-106">Para obter mais informações, consulte [alternativas ao uso do CApicom](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="e23df-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="e23df-107">Esta seção inclui cenários que usam procedimentos CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="e23df-107">This section includes scenarios that use CAPICOM procedures.</span></span>

> [!Note]  
> <span data-ttu-id="e23df-108">A criação de [*assinaturas digitais*](../secgloss/d-gly.md) e mensagens enveloping com CAPICOM é feita usando a criptografia PKI (infraestrutura de chave pública) e só pode ser feita se o signatário ou o usuário descriptografar uma mensagem envelopada tiver acesso a um certificado com uma chave privada disponível e associada.</span><span class="sxs-lookup"><span data-stu-id="e23df-108">Creating [*digital signatures*](../secgloss/d-gly.md) and un-enveloping messages with CAPICOM is done using Public Key Infrastructure (PKI) cryptography and can only be done if the signer or user decrypting an enveloped message has access to a certificate with an available, associated private key.</span></span> <span data-ttu-id="e23df-109">Para descriptografar uma mensagem envelopada, um certificado com acesso à chave privada deve estar no meu repositório.</span><span class="sxs-lookup"><span data-stu-id="e23df-109">To decrypt an enveloped message, a certificate with access to the private key must be in the MY store.</span></span>

 

<span data-ttu-id="e23df-110">As discussões e os exemplos de cenários baseados em tarefas foram separados nas seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="e23df-110">Task-based scenarios discussions and examples have been separated into the following sections:</span></span>

-   [<span data-ttu-id="e23df-111">Alternativas ao uso de CAPICOM</span><span class="sxs-lookup"><span data-stu-id="e23df-111">Alternatives to Using CAPICOM</span></span>](alternatives-to-using-capicom.md)
-   [<span data-ttu-id="e23df-112">Preparando-se para usar o CAPICOM</span><span class="sxs-lookup"><span data-stu-id="e23df-112">Getting Ready to Use CAPICOM</span></span>](getting-ready-to-use-capicom.md)
-   [<span data-ttu-id="e23df-113">Criptografando e descriptografando dados</span><span class="sxs-lookup"><span data-stu-id="e23df-113">Encrypting and Decrypting Data</span></span>](encrypting-and-decrypting-data.md)
-   [<span data-ttu-id="e23df-114">Assinatura de dados e verificação de assinaturas digitais</span><span class="sxs-lookup"><span data-stu-id="e23df-114">Signing Data and Verifying Digital Signatures</span></span>](signing-data-and-verifying-digital-signatures.md)
-   [<span data-ttu-id="e23df-115">Usando repositórios de certificados</span><span class="sxs-lookup"><span data-stu-id="e23df-115">Using Certificate Stores</span></span>](using-certificate-stores.md)
-   [<span data-ttu-id="e23df-116">Criando e recebendo mensagens de dados envelopadas</span><span class="sxs-lookup"><span data-stu-id="e23df-116">Creating and Receiving Enveloped Data Messages</span></span>](creating-and-receiving-enveloped-data-messages-in-capicom.md)

 

 
