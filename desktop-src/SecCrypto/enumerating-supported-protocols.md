---
description: Os protocolos com suporte e os conjuntos de codificação podem ser listados por chamadas para CryptGetProvParam com PP \_ ENUMALGS ou PP \_ ENUMALGS \_ ex.
ms.assetid: 8f0c2129-6841-4793-a404-bb6ee8f41683
title: Enumerando protocolos com suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76976da7e3ab59e299d6ef0a8e9bcabce601c0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811799"
---
# <a name="enumerating-supported-protocols"></a><span data-ttu-id="b78e3-103">Enumerando protocolos com suporte</span><span class="sxs-lookup"><span data-stu-id="b78e3-103">Enumerating Supported Protocols</span></span>

<span data-ttu-id="b78e3-104">Os protocolos com suporte e os conjuntos de codificação podem ser listados por chamadas para [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) com PP \_ ENUMALGS ou PP \_ ENUMALGS \_ ex.</span><span class="sxs-lookup"><span data-stu-id="b78e3-104">Supported protocols and cipher suites can be listed by calls to [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) with PP\_ENUMALGS or PP\_ENUMALGS\_EX.</span></span> <span data-ttu-id="b78e3-105">O \_ valor PP ENUMALGS \_ ex funciona como PP \_ ENUMALGS, mas retorna uma estrutura [**Prov \_ ENUMALGS \_ ex**](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex) que contém informações mais abrangentes sobre os algoritmos suportados pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="b78e3-105">The PP\_ENUMALGS\_EX value works like PP\_ENUMALGS but returns a [**PROV\_ENUMALGS\_EX**](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex) structure that holds more extensive information on the algorithms supported by the provider.</span></span>

<span data-ttu-id="b78e3-106">Para obter mais informações sobre sinalizadores de protocolo definidos e seus valores, consulte [sinalizadores de protocolo](protocol-flags.md).</span><span class="sxs-lookup"><span data-stu-id="b78e3-106">For more information about defined protocol flags and their values, see [Protocol Flags](protocol-flags.md).</span></span>

<span data-ttu-id="b78e3-107">Considerando que o membro **HCRYPTPROV** é o [*identificador*](../secgloss/h-gly.md) de um [*contexto*](../secgloss/c-gly.md) de criptografia aberto adquirido usando [**CRYPTACQUIRECONTEXT**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) com seu parâmetro *dwProvType* definido como Prov \_ RSA \_ Schannel, o exemplo a seguir lista os nomes de todos os algoritmos disponíveis no CSP.</span><span class="sxs-lookup"><span data-stu-id="b78e3-107">Given that the **hCryptProv** member is the [*handle*](../secgloss/h-gly.md) of an open cryptographic [*context*](../secgloss/c-gly.md) acquired by using [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) with its *dwProvType* parameter set to PROV\_RSA\_SCHANNEL, the following example lists the names of all algorithms available in the CSP.</span></span>


```C++
PROV_ENUMALGS_EX EnumAlgs;     //   Structure to hold information on 
                               //   a supported algorithm
DWORD dFlag = CRYPT_FIRST;     //   Flag indicating that the first
                               //   supported algorithm is to be
                               //   enumerated. Changed to 0 after the
                               //   first call to the function.
cbData = sizeof(PROV_ENUMALGS_EX);

while( CryptGetProvParam(
    hCryptProv,          // handle to an open cryptographic provider
    PP_ENUMALGS_EX, 
    (BYTE *)&EnumAlgs,  // information on the next algorithm
    &cbData,            // number of bytes in the PROV_ENUMALGS_EX
    dFlag))             // flag to indicate whether this is a first or
                        // subsequent algorithm supported by the
                        // CSP.
{
    printf("Supported Algorithm name %s\n", EnumAlgs.szName);
    dFlag = CRYPT_NEXT;          // Set to CRYPT_NEXT after the first call,
} //  end of while loop. When all of the supported algorithms have
  //  been enumerated, the function returns FALSE.
```



<span data-ttu-id="b78e3-108">A tabela a seguir lista alguns algoritmos retornados por um \_ CSP de SChannel RSA de Prov doméstico típico \_ .</span><span class="sxs-lookup"><span data-stu-id="b78e3-108">The following table lists some algorithms returned by a typical domestic PROV\_RSA\_SCHANNEL CSP.</span></span> <span data-ttu-id="b78e3-109">Observe que não há suporte para a criptografia DES SSL2 SHA MACs nem SSL2 para o CSP neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="b78e3-109">Notice that neither SSL2 SHA MACs nor SSL2 DES encryption is supported by the CSP in this example.</span></span>



| <span data-ttu-id="b78e3-110">Identificador de algoritmo</span><span class="sxs-lookup"><span data-stu-id="b78e3-110">Algorithm identifier</span></span>                                                                        | <span data-ttu-id="b78e3-111">Comprimento mínimo da chave</span><span class="sxs-lookup"><span data-stu-id="b78e3-111">Minimum key length</span></span> | <span data-ttu-id="b78e3-112">Comprimento máximo da chave</span><span class="sxs-lookup"><span data-stu-id="b78e3-112">Maximum key length</span></span> | <span data-ttu-id="b78e3-113">Protocolos</span><span class="sxs-lookup"><span data-stu-id="b78e3-113">Protocols</span></span> | <span data-ttu-id="b78e3-114">Nome do algoritmo</span><span class="sxs-lookup"><span data-stu-id="b78e3-114">Algorithm name</span></span> |
|---------------------------------------------------------------------------------------------|--------------------|--------------------|-----------|----------------|
| [<span data-ttu-id="b78e3-115">*CALG \_ RSA \_ KEYX*</span><span class="sxs-lookup"><span data-stu-id="b78e3-115">*CALG\_RSA\_KEYX*</span></span>](../secgloss/c-gly.md) | <span data-ttu-id="b78e3-116">512</span><span class="sxs-lookup"><span data-stu-id="b78e3-116">512</span></span>                | <span data-ttu-id="b78e3-117">2.048</span><span class="sxs-lookup"><span data-stu-id="b78e3-117">2048</span></span>               | <span data-ttu-id="b78e3-118">0x0007</span><span class="sxs-lookup"><span data-stu-id="b78e3-118">0x0007</span></span>    | <span data-ttu-id="b78e3-119">"RSA \_ KEYX"</span><span class="sxs-lookup"><span data-stu-id="b78e3-119">"RSA\_KEYX"</span></span>    |
| [<span data-ttu-id="b78e3-120">*CALG \_ MD5*</span><span class="sxs-lookup"><span data-stu-id="b78e3-120">*CALG\_MD5*</span></span>](../secgloss/c-gly.md)                 | <span data-ttu-id="b78e3-121">128</span><span class="sxs-lookup"><span data-stu-id="b78e3-121">128</span></span>                | <span data-ttu-id="b78e3-122">128</span><span class="sxs-lookup"><span data-stu-id="b78e3-122">128</span></span>                | <span data-ttu-id="b78e3-123">0x0007</span><span class="sxs-lookup"><span data-stu-id="b78e3-123">0x0007</span></span>    | <span data-ttu-id="b78e3-124">MD5</span><span class="sxs-lookup"><span data-stu-id="b78e3-124">"MD5"</span></span>          |
| [<span data-ttu-id="b78e3-125">*CALG \_ Sha*</span><span class="sxs-lookup"><span data-stu-id="b78e3-125">*CALG\_SHA*</span></span>](../secgloss/c-gly.md)                 | <span data-ttu-id="b78e3-126">160</span><span class="sxs-lookup"><span data-stu-id="b78e3-126">160</span></span>                | <span data-ttu-id="b78e3-127">160</span><span class="sxs-lookup"><span data-stu-id="b78e3-127">160</span></span>                | <span data-ttu-id="b78e3-128">0x0005</span><span class="sxs-lookup"><span data-stu-id="b78e3-128">0x0005</span></span>    | <span data-ttu-id="b78e3-129">Sha</span><span class="sxs-lookup"><span data-stu-id="b78e3-129">"SHA"</span></span>          |
| [<span data-ttu-id="b78e3-130">*CALG \_ RC4*</span><span class="sxs-lookup"><span data-stu-id="b78e3-130">*CALG\_RC4*</span></span>](../secgloss/c-gly.md)                 | <span data-ttu-id="b78e3-131">40</span><span class="sxs-lookup"><span data-stu-id="b78e3-131">40</span></span>                 | <span data-ttu-id="b78e3-132">128</span><span class="sxs-lookup"><span data-stu-id="b78e3-132">128</span></span>                | <span data-ttu-id="b78e3-133">0x0007</span><span class="sxs-lookup"><span data-stu-id="b78e3-133">0x0007</span></span>    | <span data-ttu-id="b78e3-134">RC4</span><span class="sxs-lookup"><span data-stu-id="b78e3-134">"RC4"</span></span>          |
| <span data-ttu-id="b78e3-135">CALG \_ des</span><span class="sxs-lookup"><span data-stu-id="b78e3-135">CALG\_DES</span></span>                                                                                   | <span data-ttu-id="b78e3-136">56</span><span class="sxs-lookup"><span data-stu-id="b78e3-136">56</span></span>                 | <span data-ttu-id="b78e3-137">56</span><span class="sxs-lookup"><span data-stu-id="b78e3-137">56</span></span>                 | <span data-ttu-id="b78e3-138">0x0005</span><span class="sxs-lookup"><span data-stu-id="b78e3-138">0x0005</span></span>    | <span data-ttu-id="b78e3-139">DES</span><span class="sxs-lookup"><span data-stu-id="b78e3-139">"DES"</span></span>          |



 

<span data-ttu-id="b78e3-140">Para se preparar para enviar mensagens ClientHello ou ServerHello, o mecanismo de protocolo [*Schannel*](../secgloss/s-gly.md) enumera os algoritmos e os tamanhos de chave suportados pelo CSP e cria uma lista interna de pacotes de criptografia com suporte.</span><span class="sxs-lookup"><span data-stu-id="b78e3-140">To prepare to send ClientHello or ServerHello messages, the [*Schannel*](../secgloss/s-gly.md) protocol engine enumerates the algorithms and key sizes supported by the CSP and builds a list internally of supported cipher suites.</span></span>

 

 
