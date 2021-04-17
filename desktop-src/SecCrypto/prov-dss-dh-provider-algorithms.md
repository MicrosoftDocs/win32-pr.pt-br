---
description: Algoritmos com suporte no Microsoft Base DSS e no provedor de criptografia Diffie-Hellman.
ms.assetid: 8db1c7cb-41e0-470b-b927-989da4c09324
title: Algoritmos de provedor de PROV_DSS_DH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098625153d4d447d7290827dcad44a6c78f55561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748865"
---
# <a name="prov_dss_dh-provider-algorithms"></a><span data-ttu-id="c6d7e-103">\_Algoritmos de provedor do Prov DSS \_ DH</span><span class="sxs-lookup"><span data-stu-id="c6d7e-103">PROV\_DSS\_DH Provider Algorithms</span></span>

<span data-ttu-id="c6d7e-104">A tabela a seguir lista os algoritmos suportados pelo Microsoft Base DSS e Diffie-Hellman provedor criptográfico.</span><span class="sxs-lookup"><span data-stu-id="c6d7e-104">The following table lists the algorithms supported by the Microsoft Base DSS and Diffie-Hellman Cryptographic Provider.</span></span>



| <span data-ttu-id="c6d7e-105">ID do algoritmo</span><span class="sxs-lookup"><span data-stu-id="c6d7e-105">Algorithm ID</span></span>      | <span data-ttu-id="c6d7e-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="c6d7e-106">Description</span></span>                                 | <span data-ttu-id="c6d7e-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6d7e-107">Comments</span></span>                                                                                                        |
|-------------------|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6d7e-108">CALG \_ MD5</span><span class="sxs-lookup"><span data-stu-id="c6d7e-108">CALG\_MD5</span></span>         | <span data-ttu-id="c6d7e-109">Algoritmo de hash MD5.</span><span class="sxs-lookup"><span data-stu-id="c6d7e-109">MD5 hashing algorithm.</span></span>                      | <span data-ttu-id="c6d7e-110">Fornecido somente para hash.</span><span class="sxs-lookup"><span data-stu-id="c6d7e-110">Provided only for hashing.</span></span>                                                                                      |
| <span data-ttu-id="c6d7e-111">CALG \_ Sha</span><span class="sxs-lookup"><span data-stu-id="c6d7e-111">CALG\_SHA</span></span>         | <span data-ttu-id="c6d7e-112">Algoritmo de hash SHA.</span><span class="sxs-lookup"><span data-stu-id="c6d7e-112">SHA hashing algorithm.</span></span>                      | <span data-ttu-id="c6d7e-113">Deve ser usado para assinaturas DSS.</span><span class="sxs-lookup"><span data-stu-id="c6d7e-113">Must be used for DSS signatures.</span></span>                                                                                |
| <span data-ttu-id="c6d7e-114">CALG \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="c6d7e-114">CALG\_SHA1</span></span>        | <span data-ttu-id="c6d7e-115">O mesmo que CALG \_ Sha.</span><span class="sxs-lookup"><span data-stu-id="c6d7e-115">Same as CALG\_SHA.</span></span>                          | <span data-ttu-id="c6d7e-116">Sem comentários.</span><span class="sxs-lookup"><span data-stu-id="c6d7e-116">No comment.</span></span>                                                                                                     |
| <span data-ttu-id="c6d7e-117">\_sinal DSS \_ CALG</span><span class="sxs-lookup"><span data-stu-id="c6d7e-117">CALG\_DSS\_SIGN</span></span>   | <span data-ttu-id="c6d7e-118">Algoritmo de assinatura de chave pública/privada DSS.</span><span class="sxs-lookup"><span data-stu-id="c6d7e-118">DSS public/private key signature algorithm.</span></span> | <span data-ttu-id="c6d7e-119">Comprimento da chave: pode ser definido, 512 bits a 1.024 bits em incrementos de bits 64.</span><span class="sxs-lookup"><span data-stu-id="c6d7e-119">Key length: can be set, 512 bits to 1,024 bits in 64 bit increments.</span></span> <span data-ttu-id="c6d7e-120">Comprimento de chave padrão: 1.024 bits.</span><span class="sxs-lookup"><span data-stu-id="c6d7e-120">Default key length: 1,024 bits.</span></span><br/> |
| <span data-ttu-id="c6d7e-121">CALG \_ DH \_ it</span><span class="sxs-lookup"><span data-stu-id="c6d7e-121">CALG\_DH\_SF</span></span>      | <span data-ttu-id="c6d7e-122">Armazene e encaminhe a troca de chaves D-H.</span><span class="sxs-lookup"><span data-stu-id="c6d7e-122">Store and Forward D-H key exchange.</span></span>         | <span data-ttu-id="c6d7e-123">Comprimento da chave: pode ser definido, 384 bits a 512 bits em incrementos de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="c6d7e-123">Key length: can be set, 384 bits to 512 bits in 8 bit increments.</span></span> <span data-ttu-id="c6d7e-124">Comprimento de chave padrão: 512 bits.</span><span class="sxs-lookup"><span data-stu-id="c6d7e-124">Default key length: 512 bits.</span></span><br/>      |
| <span data-ttu-id="c6d7e-125">CALG \_ DH \_ EPHEM</span><span class="sxs-lookup"><span data-stu-id="c6d7e-125">CALG\_DH\_EPHEM</span></span>   | <span data-ttu-id="c6d7e-126">Troca de chaves efêmeras D-H.</span><span class="sxs-lookup"><span data-stu-id="c6d7e-126">Ephemeral D-H key exchange.</span></span>                 | <span data-ttu-id="c6d7e-127">Comprimento da chave: pode ser definido, 384 bits a 512 bits em incrementos de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="c6d7e-127">Key length: can be set, 384 bits to 512 bits in 8 bit increments.</span></span> <span data-ttu-id="c6d7e-128">Comprimento de chave padrão: 512 bits.</span><span class="sxs-lookup"><span data-stu-id="c6d7e-128">Default key length: 512 bits.</span></span><br/>      |
| <span data-ttu-id="c6d7e-129">CALG \_ CYLINK \_ MEK</span><span class="sxs-lookup"><span data-stu-id="c6d7e-129">CALG\_CYLINK\_MEK</span></span> | <span data-ttu-id="c6d7e-130">Uma variante de 40 bits de uma chave DES.</span><span class="sxs-lookup"><span data-stu-id="c6d7e-130">A 40-bit variant of a DES key.</span></span>              | <span data-ttu-id="c6d7e-131">Comprimento da chave: 40 bits.</span><span class="sxs-lookup"><span data-stu-id="c6d7e-131">Key Length: 40 bits.</span></span>                                                                                            |



 

 

 




