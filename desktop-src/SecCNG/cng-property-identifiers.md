---
description: Usado com as funções BCryptGetProperty e BCryptSetProperty para identificar uma propriedade.
ms.assetid: ebcc8202-94b4-47ad-9918-e5bc843a258f
title: Identificadores de propriedade primitiva de criptografia (bcrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71f4996a216fbc4fbf63216f99b5f630c4769e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826815"
---
# <a name="cryptography-primitive-property-identifiers"></a><span data-ttu-id="e53eb-103">Identificadores de propriedade primitiva de criptografia</span><span class="sxs-lookup"><span data-stu-id="e53eb-103">Cryptography Primitive Property Identifiers</span></span>

<span data-ttu-id="e53eb-104">Os valores a seguir são usados com as funções [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) e [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) para identificar uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="e53eb-104">The following values are used with the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) and [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) functions to identify a property.</span></span>

<dl> <dt>

<span data-ttu-id="e53eb-105"><span id="BCRYPT_ALGORITHM_NAME"></span><span id="bcrypt_algorithm_name"></span>**\_nome do algoritmo BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="e53eb-105"><span id="BCRYPT_ALGORITHM_NAME"></span><span id="bcrypt_algorithm_name"></span>**BCRYPT\_ALGORITHM\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e53eb-106">L "algorithmName"</span><span class="sxs-lookup"><span data-stu-id="e53eb-106">L"AlgorithmName"</span></span>
</dt> <dt>



<span data-ttu-id="e53eb-107">Uma cadeia de caracteres Unicode terminada em nulo que contém o nome do algoritmo.</span><span class="sxs-lookup"><span data-stu-id="e53eb-107">A null-terminated Unicode string that contains the name of the algorithm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e53eb-108"><span id="BCRYPT_AUTH_TAG_LENGTH"></span><span id="bcrypt_auth_tag_length"></span>**\_comprimento da \_ marca de autenticação BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="e53eb-108"><span id="BCRYPT_AUTH_TAG_LENGTH"></span><span id="bcrypt_auth_tag_length"></span>**BCRYPT\_AUTH\_TAG\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e53eb-109">L "AuthTagLength"</span><span class="sxs-lookup"><span data-stu-id="e53eb-109">L"AuthTagLength"</span></span>
</dt> <dt>



<span data-ttu-id="e53eb-110">Os comprimentos de marca de autenticação que são suportados pelo algoritmo.</span><span class="sxs-lookup"><span data-stu-id="e53eb-110">The authentication tag lengths that are supported by the algorithm.</span></span> <span data-ttu-id="e53eb-111">Essa propriedade é uma estrutura de struct de comprimento de uma [**\_ marca de autenticação \_ \_ \_ BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) .</span><span class="sxs-lookup"><span data-stu-id="e53eb-111">This property is a [**BCRYPT\_AUTH\_TAG\_LENGTHS\_STRUCT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) structure.</span></span> <span data-ttu-id="e53eb-112">Essa propriedade só se aplica a algoritmos.</span><span class="sxs-lookup"><span data-stu-id="e53eb-112">This property only applies to algorithms.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e53eb-113"><span id="BCRYPT_BLOCK_LENGTH"></span><span id="bcrypt_block_length"></span>**\_tamanho do bloco BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="e53eb-113"><span id="BCRYPT_BLOCK_LENGTH"></span><span id="bcrypt_block_length"></span>**BCRYPT\_BLOCK\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e53eb-114">L "BlockLength"</span><span class="sxs-lookup"><span data-stu-id="e53eb-114">L"BlockLength"</span></span>
</dt> <dt>



<span data-ttu-id="e53eb-115">O tamanho, em bytes, de um bloco de codificação para o algoritmo.</span><span class="sxs-lookup"><span data-stu-id="e53eb-115">The size, in bytes, of a cipher block for the algorithm.</span></span> <span data-ttu-id="e53eb-116">Essa propriedade só se aplica a algoritmos de codificação de bloco.</span><span class="sxs-lookup"><span data-stu-id="e53eb-116">This property only applies to block cipher algorithms.</span></span> <span data-ttu-id="e53eb-117">Esse tipo de dados é um **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="e53eb-117">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e53eb-118"><span id="BCRYPT_BLOCK_SIZE_LIST"></span><span id="bcrypt_block_size_list"></span>**\_lista de \_ tamanho de bloco BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="e53eb-118"><span id="BCRYPT_BLOCK_SIZE_LIST"></span><span id="bcrypt_block_size_list"></span>**BCRYPT\_BLOCK\_SIZE\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e53eb-119">L "BlockSizelist"</span><span class="sxs-lookup"><span data-stu-id="e53eb-119">L"BlockSizeList"</span></span>
</dt> <dt>



<span data-ttu-id="e53eb-120">Uma lista de comprimentos de bloco com suporte por um algoritmo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="e53eb-120">A list of the block lengths supported by an encryption algorithm.</span></span> <span data-ttu-id="e53eb-121">Esse tipo de dados é uma matriz de **DWORDs**.</span><span class="sxs-lookup"><span data-stu-id="e53eb-121">This data type is an array of **DWORDs**.</span></span> <span data-ttu-id="e53eb-122">O número de elementos na matriz pode ser determinado pela divisão do número de bytes recuperados pelo tamanho de uma única **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="e53eb-122">The number of elements in the array can be determined by dividing the number of bytes retrieved by the size of a single **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e53eb-123"><span id="BCRYPT_CHAINING_MODE"></span><span id="bcrypt_chaining_mode"></span>**\_modo de ENCADEAMENTO \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="e53eb-123"><span id="BCRYPT_CHAINING_MODE"></span><span id="bcrypt_chaining_mode"></span>**BCRYPT\_CHAINING\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e53eb-124">L "ChainingMode"</span><span class="sxs-lookup"><span data-stu-id="e53eb-124">L"ChainingMode"</span></span>
</dt> <dt>



<span data-ttu-id="e53eb-125">Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que representa o modo de encadeamento do algoritmo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="e53eb-125">A pointer to a null-terminated Unicode string that represents the chaining mode of the encryption algorithm.</span></span> <span data-ttu-id="e53eb-126">Essa propriedade pode ser definida em um identificador de algoritmo ou um identificador de chave para um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e53eb-126">This property can be set on an algorithm handle or a key handle to one of the following values.</span></span>



| <span data-ttu-id="e53eb-127">Identificador</span><span class="sxs-lookup"><span data-stu-id="e53eb-127">Identifier</span></span>                   | <span data-ttu-id="e53eb-128">Valor</span><span class="sxs-lookup"><span data-stu-id="e53eb-128">Value</span></span>                         | <span data-ttu-id="e53eb-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="e53eb-129">Description</span></span>                                                                                                                                                                    |
|------------------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e53eb-130">**\_CBC do \_ modo de cadeia BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="e53eb-130">**BCRYPT\_CHAIN\_MODE\_CBC**</span></span> | <span data-ttu-id="e53eb-131">L "ChainingModeCBC"</span><span class="sxs-lookup"><span data-stu-id="e53eb-131">L"ChainingModeCBC"</span></span><br/> | <span data-ttu-id="e53eb-132">Define o modo de encadeamento do algoritmo para [*encadeamento de blocos de codificação*](/windows/desktop/SecGloss/c-gly).</span><span class="sxs-lookup"><span data-stu-id="e53eb-132">Sets the algorithm's chaining mode to [*cipher block chaining*](/windows/desktop/SecGloss/c-gly).</span></span><br/>            |
| <span data-ttu-id="e53eb-133">**\_CCM de \_ modo de cadeia BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="e53eb-133">**BCRYPT\_CHAIN\_MODE\_CCM**</span></span> | <span data-ttu-id="e53eb-134">L "ChainingModeCCM"</span><span class="sxs-lookup"><span data-stu-id="e53eb-134">L"ChainingModeCCM"</span></span><br/> | <span data-ttu-id="e53eb-135">Define o modo de encadeamento do algoritmo como Counter com o modo CBC-MAC (CCM). **Windows Vista:** Esse valor tem suporte a partir do Windows Vista com SP1.</span><span class="sxs-lookup"><span data-stu-id="e53eb-135">Sets the algorithm's chaining mode to counter with CBC-MAC mode (CCM).**Windows Vista:** This value is supported beginning with Windows Vista with SP1.</span></span><br/> <br/> |
| <span data-ttu-id="e53eb-136">**\_modo de cadeia BCRYPT \_ \_ CFB**</span><span class="sxs-lookup"><span data-stu-id="e53eb-136">**BCRYPT\_CHAIN\_MODE\_CFB**</span></span> | <span data-ttu-id="e53eb-137">L "ChainingModeCFB"</span><span class="sxs-lookup"><span data-stu-id="e53eb-137">L"ChainingModeCFB"</span></span><br/> | <span data-ttu-id="e53eb-138">Define o modo de encadeamento do algoritmo como [*comentários de codificação*](/windows/desktop/SecGloss/c-gly).</span><span class="sxs-lookup"><span data-stu-id="e53eb-138">Sets the algorithm's chaining mode to [*cipher feedback*](/windows/desktop/SecGloss/c-gly).</span></span><br/>                              |
| <span data-ttu-id="e53eb-139">**\_ \_ ECB modo de cadeia de BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="e53eb-139">**BCRYPT\_CHAIN\_MODE\_ECB**</span></span> | <span data-ttu-id="e53eb-140">L "ChainingModeECB"</span><span class="sxs-lookup"><span data-stu-id="e53eb-140">L"ChainingModeECB"</span></span><br/> | <span data-ttu-id="e53eb-141">Define o modo de encadeamento do algoritmo como [*Electronic Codebook*](/windows/desktop/SecGloss/e-gly).</span><span class="sxs-lookup"><span data-stu-id="e53eb-141">Sets the algorithm's chaining mode to [*electronic codebook*](/windows/desktop/SecGloss/e-gly).</span></span><br/>                  |
| <span data-ttu-id="e53eb-142">**\_modo de cadeia BCRYPT \_ \_ GCM**</span><span class="sxs-lookup"><span data-stu-id="e53eb-142">**BCRYPT\_CHAIN\_MODE\_GCM**</span></span> | <span data-ttu-id="e53eb-143">L "ChainingModeGCM"</span><span class="sxs-lookup"><span data-stu-id="e53eb-143">L"ChainingModeGCM"</span></span><br/> | <span data-ttu-id="e53eb-144">Define o modo de encadeamento do algoritmo para o modo Galois/Counter (GCM). **Windows Vista:** Esse valor tem suporte a partir do Windows Vista com SP1.</span><span class="sxs-lookup"><span data-stu-id="e53eb-144">Sets the algorithm's chaining mode to Galois/counter mode (GCM).**Windows Vista:** This value is supported beginning with Windows Vista with SP1.</span></span><br/> <br/>       |
| <span data-ttu-id="e53eb-145">**\_modo de cadeia BCRYPT \_ \_ na**</span><span class="sxs-lookup"><span data-stu-id="e53eb-145">**BCRYPT\_CHAIN\_MODE\_NA**</span></span>  | <span data-ttu-id="e53eb-146">L "ChainingModeN/A"</span><span class="sxs-lookup"><span data-stu-id="e53eb-146">L"ChainingModeN/A"</span></span><br/> | <span data-ttu-id="e53eb-147">O algoritmo não dá suporte ao encadeamento.</span><span class="sxs-lookup"><span data-stu-id="e53eb-147">The algorithm does not support chaining.</span></span><br/>                                                                                                                            |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="e53eb-148"><span id="BCRYPT_DH_PARAMETERS"></span><span id="bcrypt_dh_parameters"></span>**parâmetros da BCRYPT \_ DH \_**</span><span class="sxs-lookup"><span data-stu-id="e53eb-148"><span id="BCRYPT_DH_PARAMETERS"></span><span id="bcrypt_dh_parameters"></span>**BCRYPT\_DH\_PARAMETERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e53eb-149">L "DHParameters"</span><span class="sxs-lookup"><span data-stu-id="e53eb-149">L"DHParameters"</span></span>
</dt> <dt>



<span data-ttu-id="e53eb-150">Especifica os parâmetros a serem usados com uma chave de Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="e53eb-150">Specifies parameters to use with a Diffie-Hellman key.</span></span> <span data-ttu-id="e53eb-151">Esse tipo de dados é um ponteiro para uma estrutura de [**\_ cabeçalho de \_ parâmetro \_ BCRYPT DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) .</span><span class="sxs-lookup"><span data-stu-id="e53eb-151">This data type is a pointer to a [**BCRYPT\_DH\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) structure.</span></span> <span data-ttu-id="e53eb-152">Essa propriedade só pode ser definida e deve ser definida para a chave antes de a chave ser concluída.</span><span class="sxs-lookup"><span data-stu-id="e53eb-152">This property can only be set and must be set for the key before the key is completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e53eb-153"><span id="BCRYPT_DSA_PARAMETERS"></span><span id="bcrypt_dsa_parameters"></span>**\_parâmetros de DSA de BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="e53eb-153"><span id="BCRYPT_DSA_PARAMETERS"></span><span id="bcrypt_dsa_parameters"></span>**BCRYPT\_DSA\_PARAMETERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e53eb-154">L "DSAParameters"</span><span class="sxs-lookup"><span data-stu-id="e53eb-154">L"DSAParameters"</span></span>
</dt> <dt>



<span data-ttu-id="e53eb-155">Especifica os parâmetros a serem usados com uma chave DSA.</span><span class="sxs-lookup"><span data-stu-id="e53eb-155">Specifies parameters to use with a DSA key.</span></span> <span data-ttu-id="e53eb-156">Esta propriedade é um [**\_ cabeçalho de \_ parâmetro \_ BCrypt DSA**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) ou uma estrutura de cabeçalho de parâmetro de [**BCrypt \_ DSA \_ \_ \_ v2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) .</span><span class="sxs-lookup"><span data-stu-id="e53eb-156">This property is a [**BCRYPT\_DSA\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) or a [**BCRYPT\_DSA\_PARAMETER\_HEADER\_V2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) structure.</span></span> <span data-ttu-id="e53eb-157">Essa propriedade só pode ser definida e deve ser definida para a chave antes de a chave ser concluída.</span><span class="sxs-lookup"><span data-stu-id="e53eb-157">This property can only be set and must be set for the key before the key is completed.</span></span>

<span data-ttu-id="e53eb-158">**Windows 8:** A partir do Windows 8, essa propriedade pode ser uma estrutura [**v2 de cabeçalho de parâmetro de BCRYPT \_ DSA \_ \_ \_**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) .</span><span class="sxs-lookup"><span data-stu-id="e53eb-158">**Windows 8:** Beginning with Windows 8, this property can be a [**BCRYPT\_DSA\_PARAMETER\_HEADER\_V2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) structure.</span></span> <span data-ttu-id="e53eb-159">Use esta estrutura se o tamanho da chave exceder 1024 bits e for menor ou igual a 3072 bits.</span><span class="sxs-lookup"><span data-stu-id="e53eb-159">Use this structure if the key size exceeds 1024 bits and is less than or equal to 3072 bits.</span></span> <span data-ttu-id="e53eb-160">Se o tamanho da chave for maior ou igual a 512, mas menor ou igual a 1024 bits, use a estrutura de [**\_ cabeçalho do \_ parâmetro \_ BCRYPT DSA**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) .</span><span class="sxs-lookup"><span data-stu-id="e53eb-160">If the key size is greater than or equal to 512 but less than or equal to 1024 bits, use the [**BCRYPT\_DSA\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e53eb-161"><span id="BCRYPT_EFFECTIVE_KEY_LENGTH"></span><span id="bcrypt_effective_key_length"></span>**tamanho de chave de BCRYPT \_ efetivo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e53eb-161"><span id="BCRYPT_EFFECTIVE_KEY_LENGTH"></span><span id="bcrypt_effective_key_length"></span>**BCRYPT\_EFFECTIVE\_KEY\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e53eb-162">L "EffectiveKeyLength"</span><span class="sxs-lookup"><span data-stu-id="e53eb-162">L"EffectiveKeyLength"</span></span>
</dt> <dt>



<span data-ttu-id="e53eb-163">O tamanho, em bits, do comprimento efetivo de uma chave RC2.</span><span class="sxs-lookup"><span data-stu-id="e53eb-163">The size, in bits, of the effective length of an RC2 key.</span></span> <span data-ttu-id="e53eb-164">Esse tipo de dados é um **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="e53eb-164">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e53eb-165"><span id="BCRYPT_HASH_BLOCK_LENGTH"></span><span id="bcrypt_hash_block_length"></span>**\_tamanho do \_ bloco de hash BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="e53eb-165"><span id="BCRYPT_HASH_BLOCK_LENGTH"></span><span id="bcrypt_hash_block_length"></span>**BCRYPT\_HASH\_BLOCK\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e53eb-166">L "HashBlockLength"</span><span class="sxs-lookup"><span data-stu-id="e53eb-166">L"HashBlockLength"</span></span>
</dt> <dt>



<span data-ttu-id="e53eb-167">O tamanho, em bytes, do bloco para um hash.</span><span class="sxs-lookup"><span data-stu-id="e53eb-167">The size, in bytes, of the block for a hash.</span></span> <span data-ttu-id="e53eb-168">Essa propriedade se aplica somente a algoritmos de hash.</span><span class="sxs-lookup"><span data-stu-id="e53eb-168">This property only applies to hash algorithms.</span></span> <span data-ttu-id="e53eb-169">Esse tipo de dados é um **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="e53eb-169">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e53eb-170"><span id="BCRYPT_HASH_LENGTH"></span><span id="bcrypt_hash_length"></span>**\_tamanho do hash BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="e53eb-170"><span id="BCRYPT_HASH_LENGTH"></span><span id="bcrypt_hash_length"></span>**BCRYPT\_HASH\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e53eb-171">L "HashDigestLength"</span><span class="sxs-lookup"><span data-stu-id="e53eb-171">L"HashDigestLength"</span></span>
</dt> <dt>



<span data-ttu-id="e53eb-172">O tamanho, em bytes, do valor de hash de um provedor de hash.</span><span class="sxs-lookup"><span data-stu-id="e53eb-172">The size, in bytes, of the hash value of a hash provider.</span></span> <span data-ttu-id="e53eb-173">Esse tipo de dados é um **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="e53eb-173">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e53eb-174"><span id="BCRYPT_HASH_OID_LIST"></span><span id="bcrypt_hash_oid_list"></span>**\_lista de \_ OID de hash BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="e53eb-174"><span id="BCRYPT_HASH_OID_LIST"></span><span id="bcrypt_hash_oid_list"></span>**BCRYPT\_HASH\_OID\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e53eb-175">L "HashOIDList"</span><span class="sxs-lookup"><span data-stu-id="e53eb-175">L"HashOIDList"</span></span>
</dt> <dt>



<span data-ttu-id="e53eb-176">A lista de OIDs ( [*identificadores de objeto*](/windows/desktop/SecGloss/o-gly) hash) codificados em [*der*](/windows/desktop/SecGloss/d-gly).</span><span class="sxs-lookup"><span data-stu-id="e53eb-176">The list of [*DER*](/windows/desktop/SecGloss/d-gly)-encoded hashing [*object identifiers*](/windows/desktop/SecGloss/o-gly) (OIDs).</span></span> <span data-ttu-id="e53eb-177">Essa propriedade é uma estrutura de [**\_ \_ lista de OID BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_oid_list) .</span><span class="sxs-lookup"><span data-stu-id="e53eb-177">This property is a [**BCRYPT\_OID\_LIST**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_oid_list) structure.</span></span> <span data-ttu-id="e53eb-178">Esta propriedade só pode ser lida.</span><span class="sxs-lookup"><span data-stu-id="e53eb-178">This property can only be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e53eb-179"><span id="BCRYPT_INITIALIZATION_VECTOR"></span><span id="bcrypt_initialization_vector"></span>**\_vetor de inicialização de BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="e53eb-179"><span id="BCRYPT_INITIALIZATION_VECTOR"></span><span id="bcrypt_initialization_vector"></span>**BCRYPT\_INITIALIZATION\_VECTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e53eb-180">L "IV"</span><span class="sxs-lookup"><span data-stu-id="e53eb-180">L"IV"</span></span>
</dt> <dt>



<span data-ttu-id="e53eb-181">Contém o [*vetor de inicialização*](/windows/desktop/SecGloss/i-gly) (IV) para uma chave.</span><span class="sxs-lookup"><span data-stu-id="e53eb-181">Contains the [*initialization vector*](/windows/desktop/SecGloss/i-gly) (IV) for a key.</span></span> <span data-ttu-id="e53eb-182">Essa propriedade só se aplica a chaves.</span><span class="sxs-lookup"><span data-stu-id="e53eb-182">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e53eb-183"><span id="BCRYPT_KEY_LENGTH"></span><span id="bcrypt_key_length"></span>**\_comprimento da chave BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="e53eb-183"><span id="BCRYPT_KEY_LENGTH"></span><span id="bcrypt_key_length"></span>**BCRYPT\_KEY\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e53eb-184">L "KeyLength"</span><span class="sxs-lookup"><span data-stu-id="e53eb-184">L"KeyLength"</span></span>
</dt> <dt>



<span data-ttu-id="e53eb-185">O tamanho, em bits, do valor de chave de um provedor de chave simétrica.</span><span class="sxs-lookup"><span data-stu-id="e53eb-185">The size, in bits, of the key value of a symmetric key provider.</span></span> <span data-ttu-id="e53eb-186">Esse tipo de dados é um **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="e53eb-186">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e53eb-187"><span id="BCRYPT_KEY_LENGTHS"></span><span id="bcrypt_key_lengths"></span>**\_comprimentos de chave BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="e53eb-187"><span id="BCRYPT_KEY_LENGTHS"></span><span id="bcrypt_key_lengths"></span>**BCRYPT\_KEY\_LENGTHS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e53eb-188">L "keycomprimentos"</span><span class="sxs-lookup"><span data-stu-id="e53eb-188">L"KeyLengths"</span></span>
</dt> <dt>



<span data-ttu-id="e53eb-189">Os comprimentos de chave que são suportados pelo algoritmo.</span><span class="sxs-lookup"><span data-stu-id="e53eb-189">The key lengths that are supported by the algorithm.</span></span> <span data-ttu-id="e53eb-190">Essa propriedade é uma estrutura de [**\_ struct de \_ tamanho \_ de chave BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) .</span><span class="sxs-lookup"><span data-stu-id="e53eb-190">This property is a [**BCRYPT\_KEY\_LENGTHS\_STRUCT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) structure.</span></span> <span data-ttu-id="e53eb-191">Essa propriedade só se aplica a algoritmos.</span><span class="sxs-lookup"><span data-stu-id="e53eb-191">This property only applies to algorithms.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e53eb-192"><span id="BCRYPT_KEY_OBJECT_LENGTH"></span><span id="bcrypt_key_object_length"></span>**\_comprimento do \_ objeto de chave BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="e53eb-192"><span id="BCRYPT_KEY_OBJECT_LENGTH"></span><span id="bcrypt_key_object_length"></span>**BCRYPT\_KEY\_OBJECT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e53eb-193">L "KeyObjectLength"</span><span class="sxs-lookup"><span data-stu-id="e53eb-193">L"KeyObjectLength"</span></span>
</dt> <dt>



<span data-ttu-id="e53eb-194">Essa propriedade não é usada.</span><span class="sxs-lookup"><span data-stu-id="e53eb-194">This property is not used.</span></span> <span data-ttu-id="e53eb-195">A propriedade de **\_ \_ comprimento do objeto BCRYPT** é usada para obter essas informações.</span><span class="sxs-lookup"><span data-stu-id="e53eb-195">The **BCRYPT\_OBJECT\_LENGTH** property is used to obtain this information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e53eb-196"><span id="BCRYPT_KEY_STRENGTH"></span><span id="bcrypt_key_strength"></span>**\_restrição de chave BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="e53eb-196"><span id="BCRYPT_KEY_STRENGTH"></span><span id="bcrypt_key_strength"></span>**BCRYPT\_KEY\_STRENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e53eb-197">L "keyforça"</span><span class="sxs-lookup"><span data-stu-id="e53eb-197">L"KeyStrength"</span></span>
</dt> <dt>



<span data-ttu-id="e53eb-198">O número de bits na chave.</span><span class="sxs-lookup"><span data-stu-id="e53eb-198">The number of bits in the key.</span></span> <span data-ttu-id="e53eb-199">Esse tipo de dados é um **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="e53eb-199">This data type is a **DWORD**.</span></span> <span data-ttu-id="e53eb-200">Essa propriedade só se aplica a chaves.</span><span class="sxs-lookup"><span data-stu-id="e53eb-200">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e53eb-201"><span id="BCRYPT_MESSAGE_BLOCK_LENGTH"></span><span id="bcrypt_message_block_length"></span>**\_comprimento do \_ bloco de mensagens BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="e53eb-201"><span id="BCRYPT_MESSAGE_BLOCK_LENGTH"></span><span id="bcrypt_message_block_length"></span>**BCRYPT\_MESSAGE\_BLOCK\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e53eb-202">L "MessageBlockLength"</span><span class="sxs-lookup"><span data-stu-id="e53eb-202">L"MessageBlockLength"</span></span>
</dt> <dt>



<span data-ttu-id="e53eb-203">Isso pode ser definido em qualquer identificador de chave que tenha o modo de encadeamento de CFB definido.</span><span class="sxs-lookup"><span data-stu-id="e53eb-203">This can be set on any key handle that has the CFB chaining mode set.</span></span> <span data-ttu-id="e53eb-204">Por padrão, essa propriedade é definida como 1 para CFB de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="e53eb-204">By default, this property is set to 1 for 8-bit CFB.</span></span> <span data-ttu-id="e53eb-205">Configurá-lo para o tamanho do bloco em bytes faz com que o CFB de bloco completo seja usado.</span><span class="sxs-lookup"><span data-stu-id="e53eb-205">Setting it to the block size in bytes causes full-block CFB to be used.</span></span> <span data-ttu-id="e53eb-206">Para chaves XTS, ela é usada para definir o tamanho, em bytes, da unidade de dados XTS (geralmente 512 ou 4096).</span><span class="sxs-lookup"><span data-stu-id="e53eb-206">For XTS keys it is used to set the size, in bytes, of the XTS Data Unit (commonly 512 or 4096).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e53eb-207"><span id="BCRYPT_MULTI_OBJECT_LENGTH"></span><span id="bcrypt_multi_object_length"></span>**\_tamanho de vários \_ objetos \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="e53eb-207"><span id="BCRYPT_MULTI_OBJECT_LENGTH"></span><span id="bcrypt_multi_object_length"></span>**BCRYPT\_MULTI\_OBJECT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e53eb-208">L "MultiObjectLength"</span><span class="sxs-lookup"><span data-stu-id="e53eb-208">L"MultiObjectLength"</span></span>
</dt> <dt>



<span data-ttu-id="e53eb-209">Essa propriedade retorna um [**\_ struct de \_ \_ comprimento \_ de vários objetos BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_multi_object_length_struct), que contém as informações necessárias para calcular o tamanho de um buffer de objeto.</span><span class="sxs-lookup"><span data-stu-id="e53eb-209">This property returns a [**BCRYPT\_MULTI\_OBJECT\_LENGTH\_STRUCT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_multi_object_length_struct), which contains information necessary to calculate the size of an object buffer.</span></span> <span data-ttu-id="e53eb-210">Essa propriedade só tem suporte em versões de sistema operacional que dão suporte à função [**BCryptCreateMultiHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatemultihash) .</span><span class="sxs-lookup"><span data-stu-id="e53eb-210">This property is only supported on operating system versions that support the [**BCryptCreateMultiHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatemultihash) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e53eb-211"><span id="BCRYPT_OBJECT_LENGTH"></span><span id="bcrypt_object_length"></span>**\_tamanho do objeto BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="e53eb-211"><span id="BCRYPT_OBJECT_LENGTH"></span><span id="bcrypt_object_length"></span>**BCRYPT\_OBJECT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e53eb-212">L "ObjectLength"</span><span class="sxs-lookup"><span data-stu-id="e53eb-212">L"ObjectLength"</span></span>
</dt> <dt>



<span data-ttu-id="e53eb-213">O tamanho, em bytes, do subobjeto de um provedor.</span><span class="sxs-lookup"><span data-stu-id="e53eb-213">The size, in bytes, of the subobject of a provider.</span></span> <span data-ttu-id="e53eb-214">Esse tipo de dados é um **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="e53eb-214">This data type is a **DWORD**.</span></span> <span data-ttu-id="e53eb-215">Atualmente, os provedores de hash e de algoritmo de criptografia simétrica usam buffers alocados pelo chamador para armazenar seus subobjetos.</span><span class="sxs-lookup"><span data-stu-id="e53eb-215">Currently, the hash and symmetric cipher algorithm providers use caller-allocated buffers to store their subobjects.</span></span> <span data-ttu-id="e53eb-216">Por exemplo, o provedor de hash exige que você aloque memória para o objeto de hash obtido com a função [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) .</span><span class="sxs-lookup"><span data-stu-id="e53eb-216">For example, the hash provider requires you to allocate memory for the hash object obtained with the [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) function.</span></span> <span data-ttu-id="e53eb-217">Essa propriedade fornece o tamanho do buffer para o objeto de um provedor para que você possa alocar memória para o objeto criado pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="e53eb-217">This property provides the buffer size for a provider's object so you can allocate memory for the object created by the provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e53eb-218"><span id="BCRYPT_PADDING_SCHEMES"></span><span id="bcrypt_padding_schemes"></span>**\_esquemas de preenchimento BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="e53eb-218"><span id="BCRYPT_PADDING_SCHEMES"></span><span id="bcrypt_padding_schemes"></span>**BCRYPT\_PADDING\_SCHEMES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e53eb-219">L "PaddingSchemes"</span><span class="sxs-lookup"><span data-stu-id="e53eb-219">L"PaddingSchemes"</span></span>
</dt> <dt>



<span data-ttu-id="e53eb-220">Representa o esquema de preenchimento do provedor de algoritmo RSA.</span><span class="sxs-lookup"><span data-stu-id="e53eb-220">Represents the padding scheme of the RSA algorithm provider.</span></span> <span data-ttu-id="e53eb-221">Esse tipo de dados é um **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="e53eb-221">This data type is a **DWORD**.</span></span> <span data-ttu-id="e53eb-222">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e53eb-222">This can be one of the following values.</span></span>



| <span data-ttu-id="e53eb-223">Identificador</span><span class="sxs-lookup"><span data-stu-id="e53eb-223">Identifier</span></span>                             | <span data-ttu-id="e53eb-224">Valor</span><span class="sxs-lookup"><span data-stu-id="e53eb-224">Value</span></span>      | <span data-ttu-id="e53eb-225">Descrição</span><span class="sxs-lookup"><span data-stu-id="e53eb-225">Description</span></span>                                                |
|----------------------------------------|------------|------------------------------------------------------------|
| <span data-ttu-id="e53eb-226">**\_roteador de \_ teclado com suporte em BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="e53eb-226">**BCRYPT\_SUPPORTED\_PAD\_ROUTER**</span></span>     | <span data-ttu-id="e53eb-227">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e53eb-227">0x00000001</span></span> | <span data-ttu-id="e53eb-228">O provedor dá suporte ao preenchimento adicionado pelo roteador.</span><span class="sxs-lookup"><span data-stu-id="e53eb-228">The provider supports padding added by the router.</span></span>         |
| <span data-ttu-id="e53eb-229">**BCRYPT \_ com suporte do \_ pad \_ PKCS1 \_ ENC**</span><span class="sxs-lookup"><span data-stu-id="e53eb-229">**BCRYPT\_SUPPORTED\_PAD\_PKCS1\_ENC**</span></span> | <span data-ttu-id="e53eb-230">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e53eb-230">0x00000002</span></span> | <span data-ttu-id="e53eb-231">O provedor dá suporte ao esquema de preenchimento de criptografia PKCS1.</span><span class="sxs-lookup"><span data-stu-id="e53eb-231">The provider supports the PKCS1 encryption padding scheme.</span></span> |
| <span data-ttu-id="e53eb-232">**BCRYPT \_ com suporte do \_ pad \_ PKCS1 \_ SIG**</span><span class="sxs-lookup"><span data-stu-id="e53eb-232">**BCRYPT\_SUPPORTED\_PAD\_PKCS1\_SIG**</span></span> | <span data-ttu-id="e53eb-233">0x00000004</span><span class="sxs-lookup"><span data-stu-id="e53eb-233">0x00000004</span></span> | <span data-ttu-id="e53eb-234">O provedor dá suporte ao esquema de preenchimento de assinatura PKCS1.</span><span class="sxs-lookup"><span data-stu-id="e53eb-234">The provider supports the PKCS1 signature padding scheme.</span></span>  |
| <span data-ttu-id="e53eb-235">**BCRYPT \_ \_ OAEP pad com suporte \_**</span><span class="sxs-lookup"><span data-stu-id="e53eb-235">**BCRYPT\_SUPPORTED\_PAD\_OAEP**</span></span>       | <span data-ttu-id="e53eb-236">0x00000008</span><span class="sxs-lookup"><span data-stu-id="e53eb-236">0x00000008</span></span> | <span data-ttu-id="e53eb-237">O provedor dá suporte ao esquema de preenchimento OAEP.</span><span class="sxs-lookup"><span data-stu-id="e53eb-237">The provider supports the OAEP padding scheme.</span></span>             |
| <span data-ttu-id="e53eb-238">**\_teclado compatível com BCRYPT \_ \_ PSS**</span><span class="sxs-lookup"><span data-stu-id="e53eb-238">**BCRYPT\_SUPPORTED\_PAD\_PSS**</span></span>        | <span data-ttu-id="e53eb-239">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e53eb-239">0x00000010</span></span> | <span data-ttu-id="e53eb-240">O provedor oferece suporte ao esquema de preenchimento PSS.</span><span class="sxs-lookup"><span data-stu-id="e53eb-240">The provider supports the PSS padding scheme.</span></span>              |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="e53eb-241"><span id="BCRYPT_PROVIDER_HANDLE"></span><span id="bcrypt_provider_handle"></span>**\_identificador do provedor BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="e53eb-241"><span id="BCRYPT_PROVIDER_HANDLE"></span><span id="bcrypt_provider_handle"></span>**BCRYPT\_PROVIDER\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e53eb-242">L "ProviderHandle"</span><span class="sxs-lookup"><span data-stu-id="e53eb-242">L"ProviderHandle"</span></span>
</dt> <dt>



<span data-ttu-id="e53eb-243">O identificador do provedor CNG que criou o objeto passado no parâmetro *hObject* .</span><span class="sxs-lookup"><span data-stu-id="e53eb-243">The handle of the CNG provider that created the object passed in the *hObject* parameter.</span></span> <span data-ttu-id="e53eb-244">Esse tipo de dados é **um \_ \_ identificador BCRYPT alg**.</span><span class="sxs-lookup"><span data-stu-id="e53eb-244">This data type is a **BCRYPT\_ALG\_HANDLE**.</span></span> <span data-ttu-id="e53eb-245">Esta propriedade só pode ser recuperada; Ele não pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="e53eb-245">This property can only be retrieved; it cannot be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e53eb-246"><span id="BCRYPT_SIGNATURE_LENGTH"></span><span id="bcrypt_signature_length"></span>**\_tamanho da assinatura BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="e53eb-246"><span id="BCRYPT_SIGNATURE_LENGTH"></span><span id="bcrypt_signature_length"></span>**BCRYPT\_SIGNATURE\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e53eb-247">L "SignatureLength"</span><span class="sxs-lookup"><span data-stu-id="e53eb-247">L"SignatureLength"</span></span>
</dt> <dt>



<span data-ttu-id="e53eb-248">O tamanho, em bytes, do comprimento de uma assinatura para uma chave.</span><span class="sxs-lookup"><span data-stu-id="e53eb-248">The size, in bytes, of the length of a signature for a key.</span></span> <span data-ttu-id="e53eb-249">Esse tipo de dados é um **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="e53eb-249">This data type is a **DWORD**.</span></span> <span data-ttu-id="e53eb-250">Essa propriedade só se aplica a chaves.</span><span class="sxs-lookup"><span data-stu-id="e53eb-250">This property only applies to keys.</span></span> <span data-ttu-id="e53eb-251">Esta propriedade só pode ser recuperada; Ele não pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="e53eb-251">This property can only be retrieved; it cannot be set.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e53eb-252">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e53eb-252">Requirements</span></span>



| <span data-ttu-id="e53eb-253">Requisito</span><span class="sxs-lookup"><span data-stu-id="e53eb-253">Requirement</span></span> | <span data-ttu-id="e53eb-254">Valor</span><span class="sxs-lookup"><span data-stu-id="e53eb-254">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e53eb-255">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e53eb-255">Minimum supported client</span></span><br/> | <span data-ttu-id="e53eb-256">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e53eb-256">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e53eb-257">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e53eb-257">Minimum supported server</span></span><br/> | <span data-ttu-id="e53eb-258">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e53eb-258">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e53eb-259">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e53eb-259">Header</span></span><br/>                   | <dl> <span data-ttu-id="e53eb-260"><dt>Bcrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="e53eb-260"><dt>Bcrypt.h</dt></span></span> </dl> |



 

