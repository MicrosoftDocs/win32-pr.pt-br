---
description: Para verificar uma assinatura, crie um objeto de hash usando CryptCreateHash. Esse objeto de hash acumula os dados a serem verificados. Os dados são então adicionados ao objeto de hash com a função CryptHashData.
ms.assetid: 3779f83b-0d87-4f47-949b-9eb39690adfb
title: Verificando uma assinatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9a416dc2c3f7523af781e68fe78b066accbe6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090909"
---
# <a name="verifying-a-signature"></a><span data-ttu-id="d92b0-105">Verificando uma assinatura</span><span class="sxs-lookup"><span data-stu-id="d92b0-105">Verifying a Signature</span></span>

<span data-ttu-id="d92b0-106">Para verificar uma assinatura, crie um [*objeto de hash*](../secgloss/h-gly.md) usando [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span><span class="sxs-lookup"><span data-stu-id="d92b0-106">To verify a signature, create a [*hash object*](../secgloss/h-gly.md) using [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span></span> <span data-ttu-id="d92b0-107">Esse objeto de hash acumula os dados a serem verificados.</span><span class="sxs-lookup"><span data-stu-id="d92b0-107">This hash object accumulates the data to be verified.</span></span> <span data-ttu-id="d92b0-108">Os dados são então adicionados ao objeto de hash com a função [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) .</span><span class="sxs-lookup"><span data-stu-id="d92b0-108">The data is then added to the hash object with the [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) function.</span></span>

<span data-ttu-id="d92b0-109">Depois que o último bloco de dados for adicionado ao hash, use [**CryptVerifySignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) para verificar a assinatura.</span><span class="sxs-lookup"><span data-stu-id="d92b0-109">After the last block of data is added to the hash, use [**CryptVerifySignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) to verify the signature.</span></span> <span data-ttu-id="d92b0-110">O endereço dos dados de assinatura, um identificador para o objeto de hash e o identificador das chaves públicas são passados para **CryptVerifySignature**.</span><span class="sxs-lookup"><span data-stu-id="d92b0-110">The address of the signature data, a handle to the hash object, and the handle of the public keys are passed to **CryptVerifySignature**.</span></span>

<span data-ttu-id="d92b0-111">Depois que a assinatura tiver sido verificada (ou tiver falhado na verificação), destrua o objeto de hash usando a função [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) .</span><span class="sxs-lookup"><span data-stu-id="d92b0-111">After the signature has been verified (or has failed the verification), destroy the hash object using the [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) function.</span></span>

 

 
