---
description: A API CNG fornece um conjunto de funções que executam operações de criptografia básicas, como a criação de hashes ou a criptografia e a descriptografia de dados. Para obter mais informações sobre essas funções, consulte funções primitivas de criptografia CNG.
ms.assetid: 925848ae-9f4f-444a-81ff-14a1997434b2
title: Primitivos criptográficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0f390b36bc500bf80b5b2ef0065651cf99f5e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501260"
---
# <a name="cryptographic-primitives"></a><span data-ttu-id="dffca-104">Primitivos criptográficos</span><span class="sxs-lookup"><span data-stu-id="dffca-104">Cryptographic Primitives</span></span>

<span data-ttu-id="dffca-105">A API CNG fornece um conjunto de funções que executam operações de criptografia básicas, como a criação de hashes ou a criptografia e a descriptografia de dados.</span><span class="sxs-lookup"><span data-stu-id="dffca-105">The CNG API provides a set of functions that perform basic cryptographic operations such as creating hashes or encrypting and decrypting data.</span></span> <span data-ttu-id="dffca-106">Para obter mais informações sobre essas funções, consulte [funções primitivas de criptografia CNG](cng-cryptographic-primitive-functions.md).</span><span class="sxs-lookup"><span data-stu-id="dffca-106">For more information about these functions, see [CNG Cryptographic Primitive Functions](cng-cryptographic-primitive-functions.md).</span></span>

<span data-ttu-id="dffca-107">A CNG implementa vários algoritmos criptográficos.</span><span class="sxs-lookup"><span data-stu-id="dffca-107">CNG implements numerous cryptographic algorithms.</span></span> <span data-ttu-id="dffca-108">Cada algoritmo ou classe de algoritmos expõe sua própria API primitiva.</span><span class="sxs-lookup"><span data-stu-id="dffca-108">Each algorithm or class of algorithms exposes its own primitive API.</span></span> <span data-ttu-id="dffca-109">Várias implementações de um determinado algoritmo podem ser instaladas ao mesmo tempo; no entanto, apenas uma implementação será o padrão em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="dffca-109">Multiple implementations of a given algorithm can be installed at the same time; however, only one implementation will be the default at any given time.</span></span>

<span data-ttu-id="dffca-110">Cada classe de algoritmo na CNG é representada por um roteador primitivo.</span><span class="sxs-lookup"><span data-stu-id="dffca-110">Each algorithm class in CNG is represented by a primitive router.</span></span> <span data-ttu-id="dffca-111">Os aplicativos que usam as funções do CNG primitiva serão vinculados ao arquivo binário do roteador Bcrypt.dll no modo de usuário ou Ksecdd.sys no modo kernel antes de chamar as funções.</span><span class="sxs-lookup"><span data-stu-id="dffca-111">Applications using the CNG primitive functions will link to the router binary file Bcrypt.dll in user mode, or Ksecdd.sys in kernel mode before calling the functions.</span></span> <span data-ttu-id="dffca-112">Várias rotinas de roteador gerenciam todos os primitivos de algoritmo.</span><span class="sxs-lookup"><span data-stu-id="dffca-112">Various router routines manage all of the algorithm primitives.</span></span> <span data-ttu-id="dffca-113">Esses roteadores rastreiam cada implementação de algoritmo instalada no sistema e roteiam cada chamada de função para o módulo de provedor primitivo apropriado.</span><span class="sxs-lookup"><span data-stu-id="dffca-113">These routers track each algorithm implementation installed on the system and route each function call to the appropriate primitive provider module.</span></span>

<span data-ttu-id="dffca-114">A CNG fornece primitivos para as seguintes classes de algoritmos.</span><span class="sxs-lookup"><span data-stu-id="dffca-114">CNG provides primitives for the following classes of algorithms.</span></span>



| <span data-ttu-id="dffca-115">Classe de algoritmo</span><span class="sxs-lookup"><span data-stu-id="dffca-115">Algorithm class</span></span>                                                                                                                                                  | <span data-ttu-id="dffca-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="dffca-116">Description</span></span>                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dffca-117"><span id="Random_number_generator"></span><span id="random_number_generator"></span><span id="RANDOM_NUMBER_GENERATOR"></span>Gerador de número aleatório</span><span class="sxs-lookup"><span data-stu-id="dffca-117"><span id="Random_number_generator"></span><span id="random_number_generator"></span><span id="RANDOM_NUMBER_GENERATOR"></span>Random number generator</span></span><br/> | <span data-ttu-id="dffca-118">Geração de número aleatório conectável (RNG).</span><span class="sxs-lookup"><span data-stu-id="dffca-118">Pluggable random number generation (RNG).</span></span><br/>                                                         |
| <span data-ttu-id="dffca-119"><span id="Hashing"></span><span id="hashing"></span><span id="HASHING"></span>Hash</span><span class="sxs-lookup"><span data-stu-id="dffca-119"><span id="Hashing"></span><span id="hashing"></span><span id="HASHING"></span>Hashing</span></span><br/>                                                                 | <span data-ttu-id="dffca-120">Algoritmos usados para hash, como SHA1 e SHA2.</span><span class="sxs-lookup"><span data-stu-id="dffca-120">Algorithms used for hashing, such as SHA1 and SHA2.</span></span><br/>                                               |
| <span data-ttu-id="dffca-121"><span id="Symmetric_encryption"></span><span id="symmetric_encryption"></span><span id="SYMMETRIC_ENCRYPTION"></span>Criptografia simétrica</span><span class="sxs-lookup"><span data-stu-id="dffca-121"><span id="Symmetric_encryption"></span><span id="symmetric_encryption"></span><span id="SYMMETRIC_ENCRYPTION"></span>Symmetric encryption</span></span><br/>             | <span data-ttu-id="dffca-122">Algoritmos usados para criptografia simétrica, como AES, 3DES e RC4.</span><span class="sxs-lookup"><span data-stu-id="dffca-122">Algorithms used for symmetric encryption, such as AES, 3DES, and RC4.</span></span><br/>                             |
| <span data-ttu-id="dffca-123"><span id="Asymmetric_encryption"></span><span id="asymmetric_encryption"></span><span id="ASYMMETRIC_ENCRYPTION"></span>Criptografia assimétrica</span><span class="sxs-lookup"><span data-stu-id="dffca-123"><span id="Asymmetric_encryption"></span><span id="asymmetric_encryption"></span><span id="ASYMMETRIC_ENCRYPTION"></span>Asymmetric encryption</span></span><br/>         | <span data-ttu-id="dffca-124">Algoritmos assimétricos (chave pública) que dão suporte à criptografia, como RSA.</span><span class="sxs-lookup"><span data-stu-id="dffca-124">Asymmetric (public key) algorithms that support encryption, such as RSA.</span></span><br/>                          |
| <span data-ttu-id="dffca-125"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signature</span><span class="sxs-lookup"><span data-stu-id="dffca-125"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signature</span></span><br/>                                                         | <span data-ttu-id="dffca-126">Algoritmos de assinatura como DSA e ECDSA.</span><span class="sxs-lookup"><span data-stu-id="dffca-126">Signature algorithms such as DSA and ECDSA.</span></span> <span data-ttu-id="dffca-127">Essa classe também pode ser usada com RSA.</span><span class="sxs-lookup"><span data-stu-id="dffca-127">This class can also be used with RSA.</span></span><br/>                 |
| <span data-ttu-id="dffca-128"><span id="Secret_agreement"></span><span id="secret_agreement"></span><span id="SECRET_AGREEMENT"></span>Contrato secreto</span><span class="sxs-lookup"><span data-stu-id="dffca-128"><span id="Secret_agreement"></span><span id="secret_agreement"></span><span id="SECRET_AGREEMENT"></span>Secret agreement</span></span><br/>                             | <span data-ttu-id="dffca-129">Algoritmos de contrato secreto, como Diffie-Hellman (DH) e Diffie-Hellman de curva elíptica (ECDH).</span><span class="sxs-lookup"><span data-stu-id="dffca-129">Secret agreement algorithms such as Diffie-Hellman (DH) and elliptic curve Diffie-Hellman (ECDH).</span></span><br/> |



 

<span data-ttu-id="dffca-130">A ilustração a seguir mostra o design e a função dos primitivos de criptografia CNG.</span><span class="sxs-lookup"><span data-stu-id="dffca-130">The following illustration shows the design and function of the CNG cryptographic primitives.</span></span>

![Design e função de primitivos criptográficos CNG](images/ssdk-cng1c.png)

<span data-ttu-id="dffca-132">O arquivo de cabeçalho bcrypt. h define a constante do **\_ \_ provedor de MS Primitive** como "provedor Microsoft Primitive".</span><span class="sxs-lookup"><span data-stu-id="dffca-132">The header file Bcrypt.h defines the **MS\_PRIMITIVE\_PROVIDER** constant as "Microsoft Primitive Provider".</span></span> <span data-ttu-id="dffca-133">Para usar o provedor Microsoft Primitive, passe esse valor para [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider).</span><span class="sxs-lookup"><span data-stu-id="dffca-133">To use the Microsoft Primitive Provider, pass this value to [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider).</span></span>

 

 




