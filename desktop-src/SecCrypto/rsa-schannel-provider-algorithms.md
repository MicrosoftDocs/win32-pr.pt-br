---
description: Os algoritmos podem ter suporte do provedor criptográfico Microsoft RSA/Schannel.
ms.assetid: 8793f0e8-a368-42be-8351-c60d99c34fb9
title: Algoritmos de provedor RSA/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9dc3293b0938e9c9e89e955b26eac2a40ac198b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778671"
---
# <a name="rsaschannel-provider-algorithms"></a><span data-ttu-id="4a5bd-103">Algoritmos de provedor RSA/Schannel</span><span class="sxs-lookup"><span data-stu-id="4a5bd-103">RSA/Schannel Provider Algorithms</span></span>

<span data-ttu-id="4a5bd-104">Os algoritmos a seguir podem ser suportados pelo provedor Microsoft [*RSA*](../secgloss/r-gly.md) / [*Schannel*](../secgloss/s-gly.md) Cryptographic.</span><span class="sxs-lookup"><span data-stu-id="4a5bd-104">The following algorithms might be supported by the Microsoft [*RSA*](../secgloss/r-gly.md)/[*Schannel*](../secgloss/s-gly.md) Cryptographic Provider.</span></span>



| <span data-ttu-id="4a5bd-105">ID do algoritmo</span><span class="sxs-lookup"><span data-stu-id="4a5bd-105">Algorithm ID</span></span>    | <span data-ttu-id="4a5bd-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="4a5bd-106">Description</span></span>                                                                                                                         | <span data-ttu-id="4a5bd-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a5bd-107">Comments</span></span>                                                                                                        |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a5bd-108">CALG \_ RSA \_ KEYX</span><span class="sxs-lookup"><span data-stu-id="4a5bd-108">CALG\_RSA\_KEYX</span></span> | <span data-ttu-id="4a5bd-109">[ *Algoritmo de troca de chave* de chave pública RSA](../secgloss/k-gly.md)</span><span class="sxs-lookup"><span data-stu-id="4a5bd-109">RSA public key [*key exchange algorithm*](../secgloss/k-gly.md)</span></span> | <span data-ttu-id="4a5bd-110">Comprimento da chave: pode ser definido, 384 bits a 16.384 bits em incrementos de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="4a5bd-110">Key length: Can be set, 384 bits to 16,384 bits in 8 bit increments.</span></span> <span data-ttu-id="4a5bd-111">Comprimento de chave padrão: 1.024 bits.</span><span class="sxs-lookup"><span data-stu-id="4a5bd-111">Default key length: 1,024 bits.</span></span><br/> |
| <span data-ttu-id="4a5bd-112">CALG \_ MD5</span><span class="sxs-lookup"><span data-stu-id="4a5bd-112">CALG\_MD5</span></span>       | <span data-ttu-id="4a5bd-113">Algoritmo de hash MD5.</span><span class="sxs-lookup"><span data-stu-id="4a5bd-113">MD5 hashing algorithm.</span></span>                                                                                                              | <span data-ttu-id="4a5bd-114">Fornecido somente para hash.</span><span class="sxs-lookup"><span data-stu-id="4a5bd-114">Provided only for hashing.</span></span>                                                                                      |
| <span data-ttu-id="4a5bd-115">CALG \_ Sha</span><span class="sxs-lookup"><span data-stu-id="4a5bd-115">CALG\_SHA</span></span>       | <span data-ttu-id="4a5bd-116">Algoritmo de hash SHA.</span><span class="sxs-lookup"><span data-stu-id="4a5bd-116">SHA hashing algorithm.</span></span>                                                                                                              | <span data-ttu-id="4a5bd-117">Deve ser usado para assinaturas DSS.</span><span class="sxs-lookup"><span data-stu-id="4a5bd-117">Must be used for DSS signatures.</span></span>                                                                                |
| <span data-ttu-id="4a5bd-118">CALG \_ RC2</span><span class="sxs-lookup"><span data-stu-id="4a5bd-118">CALG\_RC2</span></span>       | <span data-ttu-id="4a5bd-119">Algoritmo de criptografia de bloco RC2.</span><span class="sxs-lookup"><span data-stu-id="4a5bd-119">RC2 block encryption algorithm.</span></span>                                                                                                     | <span data-ttu-id="4a5bd-120">Comprimento da chave: 40 a 88 bits</span><span class="sxs-lookup"><span data-stu-id="4a5bd-120">Key length: 40 to 88 bits</span></span>                                                                                       |
| <span data-ttu-id="4a5bd-121">CALG \_ RC4</span><span class="sxs-lookup"><span data-stu-id="4a5bd-121">CALG\_RC4</span></span>       | <span data-ttu-id="4a5bd-122">Algoritmo de criptografia de fluxo RC4.</span><span class="sxs-lookup"><span data-stu-id="4a5bd-122">RC4 stream encryption algorithm.</span></span>                                                                                                    | <span data-ttu-id="4a5bd-123">Comprimento da chave: 40 a 88 bits</span><span class="sxs-lookup"><span data-stu-id="4a5bd-123">Key length: 40 to 88 bits</span></span>                                                                                       |



 

 

 
