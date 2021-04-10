---
description: Descreve as tarefas que devem ser realizadas para criar uma mensagem assinada.
ms.assetid: 61896022-28c2-4f70-977a-c990b4b23c55
title: Criando uma mensagem assinada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f68511c41a10fc0f690574e71c1dfe8a354efbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170203"
---
# <a name="creating-a-signed-message"></a><span data-ttu-id="027ae-103">Criando uma mensagem assinada</span><span class="sxs-lookup"><span data-stu-id="027ae-103">Creating a Signed Message</span></span>

<span data-ttu-id="027ae-104">A ilustração a seguir descreve as tarefas que devem ser realizadas para criar uma mensagem assinada.</span><span class="sxs-lookup"><span data-stu-id="027ae-104">The following illustration depicts the tasks that must be accomplished to create a signed message.</span></span> <span data-ttu-id="027ae-105">As etapas são listadas após a ilustração.</span><span class="sxs-lookup"><span data-stu-id="027ae-105">The steps are listed following the illustration.</span></span>

![assinando uma mensagem](images/signdmsg.png)

<span data-ttu-id="027ae-107">**Para criar uma mensagem assinada**</span><span class="sxs-lookup"><span data-stu-id="027ae-107">**To create a signed message**</span></span>

1.  <span data-ttu-id="027ae-108">Crie os dados (se necessário) e obtenha um ponteiro para ele.</span><span class="sxs-lookup"><span data-stu-id="027ae-108">Create the data (if necessary) and get a pointer to it.</span></span>
2.  <span data-ttu-id="027ae-109">Abra um [*repositório de certificados*](../secgloss/c-gly.md) que contenha o certificado do signatário.</span><span class="sxs-lookup"><span data-stu-id="027ae-109">Open a [*certificate store*](../secgloss/c-gly.md) that contains the signer's certificate.</span></span>
3.  <span data-ttu-id="027ae-110">Obtenha a [*chave privada*](../secgloss/p-gly.md) para o certificado.</span><span class="sxs-lookup"><span data-stu-id="027ae-110">Get the [*private key*](../secgloss/p-gly.md) for the certificate.</span></span> <span data-ttu-id="027ae-111">Uma propriedade deve ser definida no certificado antes de ser usada, para vincular um certificado a um [*CSP*](../secgloss/c-gly.md)específico e, dentro desse CSP, a uma chave privada específica.</span><span class="sxs-lookup"><span data-stu-id="027ae-111">A property must be set on the certificate before using it, to tie a certificate to a particular [*CSP*](../secgloss/c-gly.md), and, within that CSP, to a particular private key.</span></span> <span data-ttu-id="027ae-112">Isso precisa ser definido uma vez.</span><span class="sxs-lookup"><span data-stu-id="027ae-112">This needs to be set once.</span></span>
4.  <span data-ttu-id="027ae-113">Escolha um algoritmo de hash para a operação de resumo.</span><span class="sxs-lookup"><span data-stu-id="027ae-113">Choose a hashing algorithm for the digest operation.</span></span> <span data-ttu-id="027ae-114">É recomendável que o algoritmo de hash seja selecionado de um local configurável que possa ser atualizado posteriormente sem a necessidade de alterações no código.</span><span class="sxs-lookup"><span data-stu-id="027ae-114">We recommend that the hashing algorithm be selected from a configurable location that can be subsequently updated without requiring changes to code.</span></span>
5.  <span data-ttu-id="027ae-115">Envie os dados por meio da função de hash usando o algoritmo de hash, criando assim um [*hash*](../secgloss/h-gly.md) (Digest) dos dados.</span><span class="sxs-lookup"><span data-stu-id="027ae-115">Send the data through the hashing function by using the hashing algorithm, thus creating a [*hash*](../secgloss/h-gly.md) (digest) of the data.</span></span>
6.  <span data-ttu-id="027ae-116">Usando a [*chave privada*](../secgloss/p-gly.md) obtida por meio da propriedade no certificado, criptografe o resumo, criando a assinatura.</span><span class="sxs-lookup"><span data-stu-id="027ae-116">Using the [*private key*](../secgloss/p-gly.md) obtained through the property on the certificate, encrypt the digest, creating the signature.</span></span>
7.  <span data-ttu-id="027ae-117">Inclua o seguinte na mensagem assinada:</span><span class="sxs-lookup"><span data-stu-id="027ae-117">Include the following in the signed message:</span></span>

    -   <span data-ttu-id="027ae-118">Os dados assinados</span><span class="sxs-lookup"><span data-stu-id="027ae-118">The signed data</span></span>
    -   <span data-ttu-id="027ae-119">O algoritmo de hash</span><span class="sxs-lookup"><span data-stu-id="027ae-119">The hash algorithm</span></span>
    -   <span data-ttu-id="027ae-120">A assinatura</span><span class="sxs-lookup"><span data-stu-id="027ae-120">The signature</span></span>
    -   <span data-ttu-id="027ae-121">O identificador de signatário (emissor do certificado e número de série)</span><span class="sxs-lookup"><span data-stu-id="027ae-121">The signer identifier (certificate issuer and serial number)</span></span>
    -   <span data-ttu-id="027ae-122">O certificado do signatário (opcional)</span><span class="sxs-lookup"><span data-stu-id="027ae-122">The signer's certificate (optional)</span></span>

<span data-ttu-id="027ae-123">Para obter um procedimento detalhado e um exemplo, consulte o [procedimento para assinar dados](procedure-for-signing-data.md) e [programa de exemplo C: assinando uma mensagem e verificando uma assinatura de mensagem](example-c-program-signing-a-message-and-verifying-a-message-signature.md).</span><span class="sxs-lookup"><span data-stu-id="027ae-123">For a detailed procedure and example, see [Procedure for Signing Data](procedure-for-signing-data.md) and [Example C Program: Signing a Message and Verifying a Message Signature](example-c-program-signing-a-message-and-verifying-a-message-signature.md).</span></span>

 

 
