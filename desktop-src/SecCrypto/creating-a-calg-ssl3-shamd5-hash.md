---
description: Explica como criar um CALG \_ SSL3 \_ SHAMD5 hash.
ms.assetid: dad6fc7f-8abd-4f90-b3e4-8d0169e95087
title: Criando um hash de CALG_SSL3_SHAMD5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f38b5939dc64467ef813b354f33a90f009619f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754501"
---
# <a name="creating-a-calg_ssl3_shamd5-hash"></a><span data-ttu-id="4170a-103">Criando um \_ \_ hash SHAMD5 do CALG SSL3</span><span class="sxs-lookup"><span data-stu-id="4170a-103">Creating a CALG\_SSL3\_SHAMD5 Hash</span></span>

<span data-ttu-id="4170a-104">**Para criar um CALG \_ SSL3 \_ SHAMD5 hash**</span><span class="sxs-lookup"><span data-stu-id="4170a-104">**To create a CALG\_SSL3\_SHAMD5 hash**</span></span>

1.  <span data-ttu-id="4170a-105">Usando a metodologia CryptoAPI padrão, crie um MD5 e um [](../secgloss/s-gly.md) [*hash*](../secgloss/h-gly.md) Sha dos dados de destino.</span><span class="sxs-lookup"><span data-stu-id="4170a-105">Using standard CryptoAPI methodology, create both a MD5 and a [*SHA*](../secgloss/s-gly.md) [*hash*](../secgloss/h-gly.md) of the target data.</span></span>
2.  <span data-ttu-id="4170a-106">Concatene os dois hashes, com o valor MD5 mais à esquerda e o valor de SHA mais à direita.</span><span class="sxs-lookup"><span data-stu-id="4170a-106">Concatenate the two hashes, with the MD5 value leftmost and the SHA value rightmost.</span></span> <span data-ttu-id="4170a-107">Isso resulta em um valor de 36 bytes (16 bytes + 20 bytes).</span><span class="sxs-lookup"><span data-stu-id="4170a-107">This results in a 36-byte value (16 bytes + 20 bytes).</span></span>
3.  <span data-ttu-id="4170a-108">Obtenha um identificador para um [*objeto de hash*](../secgloss/h-gly.md) chamando [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) com CALG \_ SSL3 \_ SHAMD5 passado no parâmetro *algid* .</span><span class="sxs-lookup"><span data-stu-id="4170a-108">Get a handle to a [*hash object*](../secgloss/h-gly.md) by calling [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) with CALG\_SSL3\_SHAMD5 passed in the *Algid* parameter.</span></span>
4.  <span data-ttu-id="4170a-109">Defina o valor de hash com uma chamada para [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam).</span><span class="sxs-lookup"><span data-stu-id="4170a-109">Set the hash value with a call to [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam).</span></span> <span data-ttu-id="4170a-110">Os valores de hash concatenados são passados como um **byte** \* no parâmetro *pbData* e o valor de HASHVAL da HP \_ deve ser passado no parâmetro *dwParam* .</span><span class="sxs-lookup"><span data-stu-id="4170a-110">The concatenated hash values are passed as a **BYTE**\* in the *pbData* parameter, and the HP\_HASHVAL value must be passed in the *dwParam* parameter.</span></span> <span data-ttu-id="4170a-111">A chamada de [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) usando o identificador retornado por [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) na etapa 3 falhará.</span><span class="sxs-lookup"><span data-stu-id="4170a-111">Calling [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) using the handle returned by [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) in step 3 will fail.</span></span>
5.  <span data-ttu-id="4170a-112">Chame [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) para gerar a assinatura.</span><span class="sxs-lookup"><span data-stu-id="4170a-112">Call [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) to generate the signature.</span></span>
6.  <span data-ttu-id="4170a-113">Chame [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) para destruir o objeto de hash.</span><span class="sxs-lookup"><span data-stu-id="4170a-113">Call [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) to destroy the hash object.</span></span>

 

 
