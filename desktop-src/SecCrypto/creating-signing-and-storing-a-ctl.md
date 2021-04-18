---
description: Crie uma CTL (lista de certificados confiáveis) assinada e salve-a em um repositório de certificados.
ms.assetid: 82d75d60-2343-413c-ba53-ccee02d1ad41
title: Criando, assinando e armazenando uma CTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2da66ce5acb882d36451118700178519455a4ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760203"
---
# <a name="creating-signing-and-storing-a-ctl"></a><span data-ttu-id="64675-103">Criando, assinando e armazenando uma CTL</span><span class="sxs-lookup"><span data-stu-id="64675-103">Creating, Signing, and Storing a CTL</span></span>

<span data-ttu-id="64675-104">Os procedimentos a seguir criam uma CTL ( [*lista de certificados confiáveis*](../secgloss/c-gly.md) ) assinada e salvam-a em um [*repositório de certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="64675-104">The following procedures create a signed [*certificate trust list*](../secgloss/c-gly.md) (CTL) and save it to a [*certificate store*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="64675-105">**Para criar e assinar uma CTL**</span><span class="sxs-lookup"><span data-stu-id="64675-105">**To create and sign a CTL**</span></span>

1.  <span data-ttu-id="64675-106">Crie uma matriz de itens a serem armazenados na [*CTL*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="64675-106">Create an array of items to be stored in the [*CTL*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="64675-107">No caso de certificados confiáveis, esses devem ser os hashes SHA1 ou MD5 dos certificados confiáveis.</span><span class="sxs-lookup"><span data-stu-id="64675-107">In the case of trusted certificates, this must be the SHA1 or MD5 hashes of the trusted certificates.</span></span>
2.  <span data-ttu-id="64675-108">Inicialize uma estrutura de [**\_ informações de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_info) que inclua a matriz de itens que acabou de ser criada.</span><span class="sxs-lookup"><span data-stu-id="64675-108">Initialize a [**CTL\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_info) structure that includes the array of items just created.</span></span>
3.  <span data-ttu-id="64675-109">Inicializar uma estrutura de [**\_ \_ \_ informações de codificação assinada CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) .</span><span class="sxs-lookup"><span data-stu-id="64675-109">Initialize a [**CMSG\_SIGNED\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) structure.</span></span>
4.  <span data-ttu-id="64675-110">Chame [**CryptMsgEncodeAndSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl).</span><span class="sxs-lookup"><span data-stu-id="64675-110">Call [**CryptMsgEncodeAndSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl).</span></span> <span data-ttu-id="64675-111">Essa chamada de função retorna um ponteiro para uma CTL assinada e codificada (no \# formato PKCS 7) que contém a lista de itens criados na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="64675-111">This function call returns a pointer to a signed, encoded CTL (in PKCS \#7 format) that contains the list of items created in step 1.</span></span>

<span data-ttu-id="64675-112">**Para adicionar uma CTL a um repositório de certificados**</span><span class="sxs-lookup"><span data-stu-id="64675-112">**To add a CTL to a certificate store**</span></span>

1.  <span data-ttu-id="64675-113">Obtenha um ponteiro para uma CTL assinada e codificada.</span><span class="sxs-lookup"><span data-stu-id="64675-113">Get a pointer to a signed and encoded CTL.</span></span>
2.  <span data-ttu-id="64675-114">Abra o repositório de certificados de destino com uma chamada para [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).</span><span class="sxs-lookup"><span data-stu-id="64675-114">Open the target certificate store with a call to [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).</span></span>
3.  <span data-ttu-id="64675-115">Chame [**CertAddEncodedCTLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore).</span><span class="sxs-lookup"><span data-stu-id="64675-115">Call [**CertAddEncodedCTLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore).</span></span>

 

 
