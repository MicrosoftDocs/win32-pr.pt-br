---
description: Para tornar mais difícil para um interloper substituir uma CTL (lista confiável de certificados) falsa para uma existente, verifique a assinatura na CTL sempre que a CTL for usada.
ms.assetid: 24ba6955-f6d1-4123-ab39-50385f6e03a0
title: Verificando uma CTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac88362c96d5b419a7c16731e31456b569079d7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502176"
---
# <a name="verifying-a-ctl"></a><span data-ttu-id="2443d-103">Verificando uma CTL</span><span class="sxs-lookup"><span data-stu-id="2443d-103">Verifying a CTL</span></span>

<span data-ttu-id="2443d-104">Para tornar mais difícil para um interloper substituir uma CTL ( [*lista confiável de certificados*](../secgloss/c-gly.md) ) falsa para uma existente, verifique a assinatura na CTL sempre que a CTL for usada.</span><span class="sxs-lookup"><span data-stu-id="2443d-104">To make it more difficult for an interloper to substitute a bogus [*certificate trust list*](../secgloss/c-gly.md) (CTL) for an existing one, verify the signature on the CTL each time the CTL is used.</span></span> <span data-ttu-id="2443d-105">Não use uma CTL que não contenha uma assinatura confiável.</span><span class="sxs-lookup"><span data-stu-id="2443d-105">Do not use a CTL that does not contain a trusted signature.</span></span>

<span data-ttu-id="2443d-106">**Para verificar uma assinatura de CTL**</span><span class="sxs-lookup"><span data-stu-id="2443d-106">**To verify a CTL signature**</span></span>

1.  <span data-ttu-id="2443d-107">Abra o [*repositório de certificados*](../secgloss/c-gly.md) que contém a CTL desejada.</span><span class="sxs-lookup"><span data-stu-id="2443d-107">Open the [*certificate store*](../secgloss/c-gly.md) containing the desired CTL.</span></span>
2.  <span data-ttu-id="2443d-108">Obtenha um identificador para um [**\_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) para a CTL.</span><span class="sxs-lookup"><span data-stu-id="2443d-108">Get a handle to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) for the CTL.</span></span> <span data-ttu-id="2443d-109">Isso pode ser feito chamando qualquer uma das funções que retornam um identificador para o **\_ contexto de CTL**, como [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span><span class="sxs-lookup"><span data-stu-id="2443d-109">This can be done by calling any of the functions that return a handle to the **CTL\_CONTEXT**, such as [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span></span>
3.  <span data-ttu-id="2443d-110">Chame [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), passando o [**\_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) recuperado na etapa 2 no parâmetro *hCryptMsg* , um identificador para o repositório de certificados que contém o certificado da fonte confiável para CTLs no parâmetro *rghSignerStore* e o sinalizador de \_ signatário confiável CMSG \_ \_ no parâmetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="2443d-110">Call [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), passing the [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) retrieved in step 2 in the *hCryptMsg* parameter, a handle to the certificate store containing the certificate of the trusted source for CTLs in the *rghSignerStore* parameter, and the CMSG\_TRUSTED\_SIGNER\_FLAG in the *dwFlags* parameter.</span></span> <span data-ttu-id="2443d-111">Se a função retornar **true**, a assinatura foi verificada e um ponteiro para o [**\_ contexto PCCERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) do assinante de CTL será retornado no parâmetro *ppSigner* .</span><span class="sxs-lookup"><span data-stu-id="2443d-111">If the function returns **TRUE**, the signature was verified, and a pointer to the CTL signer's [**PCCERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) is returned in the *ppSigner* parameter.</span></span>

 

 
