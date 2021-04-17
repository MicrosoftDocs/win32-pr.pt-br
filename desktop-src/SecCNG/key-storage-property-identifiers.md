---
description: Usado para identificar uma propriedade de armazenamento de chave.
ms.assetid: 407f0e42-07c8-4ec6-81c6-f8bde005adb0
title: Identificadores de propriedade de armazenamento de chave (NCrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 813a15ba106989cb558eba181bc893d75c6d1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783246"
---
# <a name="key-storage-property-identifiers"></a><span data-ttu-id="b7b10-103">Identificadores de propriedade de armazenamento de chave</span><span class="sxs-lookup"><span data-stu-id="b7b10-103">Key Storage Property Identifiers</span></span>

<span data-ttu-id="b7b10-104">Os valores a seguir são usados para identificar uma propriedade de armazenamento de chave.</span><span class="sxs-lookup"><span data-stu-id="b7b10-104">The following values are used to identify a key storage property.</span></span>

<dl> <dt>

<span data-ttu-id="b7b10-105"><span id="NCRYPT_ALGORITHM_GROUP_PROPERTY"></span><span id="ncrypt_algorithm_group_property"></span>**\_Propriedade do grupo de algoritmos NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-105"><span id="NCRYPT_ALGORITHM_GROUP_PROPERTY"></span><span id="ncrypt_algorithm_group_property"></span>**NCRYPT\_ALGORITHM\_GROUP\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-106">L "grupo de algoritmos"</span><span class="sxs-lookup"><span data-stu-id="b7b10-106">L"Algorithm Group"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-107">Uma cadeia de caracteres Unicode terminada em nulo que contém o nome do grupo de algoritmos do objeto.</span><span class="sxs-lookup"><span data-stu-id="b7b10-107">A null-terminated Unicode string that contains the name of the object's algorithm group.</span></span> <span data-ttu-id="b7b10-108">Essa propriedade só se aplica a chaves.</span><span class="sxs-lookup"><span data-stu-id="b7b10-108">This property only applies to keys.</span></span> <span data-ttu-id="b7b10-109">Os identificadores a seguir são retornados pelo provedor de armazenamento de chaves da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b7b10-109">The following identifiers are returned by the Microsoft key storage provider.</span></span>



| <span data-ttu-id="b7b10-110">Identificador</span><span class="sxs-lookup"><span data-stu-id="b7b10-110">Identifier</span></span>                                     | <span data-ttu-id="b7b10-111">Valor</span><span class="sxs-lookup"><span data-stu-id="b7b10-111">Value</span></span>              | <span data-ttu-id="b7b10-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7b10-112">Description</span></span>                                                   |
|------------------------------------------------|--------------------|---------------------------------------------------------------|
| <span data-ttu-id="b7b10-113">**\_grupo de \_ algoritmos do RSA NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-113">**NCRYPT\_RSA\_ALGORITHM\_GROUP**</span></span><br/>   | <span data-ttu-id="b7b10-114">RSA</span><span class="sxs-lookup"><span data-stu-id="b7b10-114">"RSA"</span></span><br/>   | <span data-ttu-id="b7b10-115">O grupo de algoritmos RSA.</span><span class="sxs-lookup"><span data-stu-id="b7b10-115">The RSA algorithm group.</span></span><br/>                           |
| <span data-ttu-id="b7b10-116">**\_grupo de \_ algoritmos DH NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-116">**NCRYPT\_DH\_ALGORITHM\_GROUP**</span></span><br/>    | <span data-ttu-id="b7b10-117">FEITA</span><span class="sxs-lookup"><span data-stu-id="b7b10-117">"DH"</span></span><br/>    | <span data-ttu-id="b7b10-118">O grupo de algoritmos Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="b7b10-118">The Diffie-Hellman algorithm group.</span></span><br/>                |
| <span data-ttu-id="b7b10-119">**\_grupo de \_ algoritmos DSA NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-119">**NCRYPT\_DSA\_ALGORITHM\_GROUP**</span></span><br/>   | <span data-ttu-id="b7b10-120">DSA</span><span class="sxs-lookup"><span data-stu-id="b7b10-120">"DSA"</span></span><br/>   | <span data-ttu-id="b7b10-121">O grupo de algoritmos DSA.</span><span class="sxs-lookup"><span data-stu-id="b7b10-121">The DSA algorithm group.</span></span><br/>                           |
| <span data-ttu-id="b7b10-122">**\_grupo de \_ algoritmos de ECDSA NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-122">**NCRYPT\_ECDSA\_ALGORITHM\_GROUP**</span></span><br/> | <span data-ttu-id="b7b10-123">ECDSA</span><span class="sxs-lookup"><span data-stu-id="b7b10-123">"ECDSA"</span></span><br/> | <span data-ttu-id="b7b10-124">O grupo de algoritmos DSA de curva elíptica.</span><span class="sxs-lookup"><span data-stu-id="b7b10-124">The elliptic curve DSA algorithm group.</span></span><br/>            |
| <span data-ttu-id="b7b10-125">**\_grupo de \_ algoritmos de ECDH NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-125">**NCRYPT\_ECDH\_ALGORITHM\_GROUP**</span></span><br/>  | <span data-ttu-id="b7b10-126">ECDH</span><span class="sxs-lookup"><span data-stu-id="b7b10-126">"ECDH"</span></span><br/>  | <span data-ttu-id="b7b10-127">O grupo de algoritmos Diffie-Hellman de curva elíptica.</span><span class="sxs-lookup"><span data-stu-id="b7b10-127">The elliptic curve Diffie-Hellman algorithm group.</span></span><br/> |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-128"><span id="NCRYPT_ALGORITHM_PROPERTY"></span><span id="ncrypt_algorithm_property"></span>**\_propriedade de algoritmo NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-128"><span id="NCRYPT_ALGORITHM_PROPERTY"></span><span id="ncrypt_algorithm_property"></span>**NCRYPT\_ALGORITHM\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-129">L "nome do algoritmo"</span><span class="sxs-lookup"><span data-stu-id="b7b10-129">L"Algorithm Name"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-130">Uma cadeia de caracteres Unicode terminada em nulo que contém o nome do algoritmo do objeto.</span><span class="sxs-lookup"><span data-stu-id="b7b10-130">A null-terminated Unicode string that contains the name of the object's algorithm.</span></span> <span data-ttu-id="b7b10-131">Pode ser um dos [**identificadores de algoritmo CNG**](cng-algorithm-identifiers.md) predefinidos ou outro identificador de algoritmo registrado.</span><span class="sxs-lookup"><span data-stu-id="b7b10-131">This can be one of the predefined [**CNG Algorithm Identifiers**](cng-algorithm-identifiers.md) or another registered algorithm identifier.</span></span> <span data-ttu-id="b7b10-132">Essa propriedade só se aplica a chaves.</span><span class="sxs-lookup"><span data-stu-id="b7b10-132">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-133"><span id="NCRYPT_ASSOCIATED_ECDH_KEY"></span><span id="ncrypt_associated_ecdh_key"></span>**\_ \_ chave ECDH associada de NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-133"><span id="NCRYPT_ASSOCIATED_ECDH_KEY"></span><span id="ncrypt_associated_ecdh_key"></span>**NCRYPT\_ASSOCIATED\_ECDH\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-134">L "SmartCardAssociatedECDHKey"</span><span class="sxs-lookup"><span data-stu-id="b7b10-134">L"SmartCardAssociatedECDHKey"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-135">Um valor de **LPWSTR** que indica o nome do contêiner da chave de Diffie-Hellman de curva elíptica (ECDH) a ser usada durante o logon de um determinado identificador para uma chave de ECDSA (algoritmo de assinatura digital de curva elíptica).</span><span class="sxs-lookup"><span data-stu-id="b7b10-135">An **LPWSTR** value that indicates the container name of the Elliptic Curve Diffie-Hellman (ECDH) key to use during logon for a given handle to an Elliptic Curve Digital Signature Algorithm (ECDSA) key.</span></span> <span data-ttu-id="b7b10-136">Se não houver nenhuma chave ECDH no cartão, o KSP ( [*provedor de armazenamento de chaves*](/windows/desktop/SecGloss/k-gly) ) retornará o **nte \_ não \_ encontrado**.</span><span class="sxs-lookup"><span data-stu-id="b7b10-136">If there are no ECDH keys on the card, the [*key storage provider*](/windows/desktop/SecGloss/k-gly) (KSP) returns **NTE\_NOT\_FOUND**.</span></span> <span data-ttu-id="b7b10-137">Essa propriedade se aplica a chaves ECDSA para logon com cartões inteligentes.</span><span class="sxs-lookup"><span data-stu-id="b7b10-137">This property applies to ECDSA keys for logon with smart cards.</span></span> <span data-ttu-id="b7b10-138">A propriedade é suportada pelo provedor de armazenamento de chaves de cartão inteligente da Microsoft e não pelo provedor de armazenamento de chaves de software da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b7b10-138">The property is supported by the Microsoft Smart Card key storage provider and not by the Microsoft Software key storage provider.</span></span>

<span data-ttu-id="b7b10-139">**Windows Server 2008 e Windows Vista:** Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="b7b10-139">**Windows Server 2008 and Windows Vista:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-140"><span id="NCRYPT_BLOCK_LENGTH_PROPERTY"></span><span id="ncrypt_block_length_property"></span>**\_propriedade de \_ comprimento de bloco NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-140"><span id="NCRYPT_BLOCK_LENGTH_PROPERTY"></span><span id="ncrypt_block_length_property"></span>**NCRYPT\_BLOCK\_LENGTH\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-141">L "comprimento do bloco"</span><span class="sxs-lookup"><span data-stu-id="b7b10-141">L"Block Length"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-142">Um **DWORD** que contém o comprimento, em bytes, do bloco de criptografia.</span><span class="sxs-lookup"><span data-stu-id="b7b10-142">A **DWORD** that contains the length, in bytes, of the encryption block.</span></span> <span data-ttu-id="b7b10-143">Essa propriedade só se aplica a chaves que dão suporte à criptografia.</span><span class="sxs-lookup"><span data-stu-id="b7b10-143">This property only applies to keys that support encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-144"><span id="NCRYPT_CERTIFICATE_PROPERTY"></span><span id="ncrypt_certificate_property"></span>**\_propriedade de certificado NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-144"><span id="NCRYPT_CERTIFICATE_PROPERTY"></span><span id="ncrypt_certificate_property"></span>**NCRYPT\_CERTIFICATE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-145">L "SmartCardKeyCertificate"</span><span class="sxs-lookup"><span data-stu-id="b7b10-145">L"SmartCardKeyCertificate"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-146">Um [*blob*](/windows/desktop/SecGloss/b-gly) que contém um certificado X. 509 que está associado à chave.</span><span class="sxs-lookup"><span data-stu-id="b7b10-146">A [*BLOB*](/windows/desktop/SecGloss/b-gly) that contains an X.509 certificate that is associated with the key.</span></span>

<span data-ttu-id="b7b10-147">**Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Um [*blob*](/windows/desktop/SecGloss/b-gly) que contém o [*certificado*](/windows/desktop/SecGloss/c-gly)de chave do [*cartão inteligente*](/windows/desktop/SecGloss/s-gly) .</span><span class="sxs-lookup"><span data-stu-id="b7b10-147">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** A [*BLOB*](/windows/desktop/SecGloss/b-gly) that contains the [*smart card*](/windows/desktop/SecGloss/s-gly) key [*certificate*](/windows/desktop/SecGloss/c-gly).</span></span> <span data-ttu-id="b7b10-148">Não há suporte para essa propriedade no provedor de armazenamento de chaves de software da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b7b10-148">This property is not supported by the Microsoft Software Key Storage Provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-149"><span id="NCRYPT_DH_PARAMETERS_PROPERTY"></span><span id="ncrypt_dh_parameters_property"></span>**Propriedade NCRYPT de \_ \_ parâmetros DH \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-149"><span id="NCRYPT_DH_PARAMETERS_PROPERTY"></span><span id="ncrypt_dh_parameters_property"></span>**NCRYPT\_DH\_PARAMETERS\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-150">L "DHParameters"</span><span class="sxs-lookup"><span data-stu-id="b7b10-150">L"DHParameters"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-151">Especifica os parâmetros a serem usados com uma chave de Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="b7b10-151">Specifies parameters to use with a Diffie-Hellman key.</span></span> <span data-ttu-id="b7b10-152">Esse tipo de dados é um ponteiro para uma estrutura de [**\_ cabeçalho de \_ parâmetro \_ BCRYPT DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) .</span><span class="sxs-lookup"><span data-stu-id="b7b10-152">This data type is a pointer to a [**BCRYPT\_DH\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) structure.</span></span> <span data-ttu-id="b7b10-153">Essa propriedade só pode ser definida e deve ser definida para a chave antes de a chave ser concluída.</span><span class="sxs-lookup"><span data-stu-id="b7b10-153">This property can only be set and must be set for the key before the key is completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-154"><span id="NCRYPT_EXPORT_POLICY_PROPERTY"></span><span id="ncrypt_export_policy_property"></span>**\_propriedade de \_ política de exportação NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-154"><span id="NCRYPT_EXPORT_POLICY_PROPERTY"></span><span id="ncrypt_export_policy_property"></span>**NCRYPT\_EXPORT\_POLICY\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-155">L "exportar política"</span><span class="sxs-lookup"><span data-stu-id="b7b10-155">L"Export Policy"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-156">Um **DWORD** que contém um conjunto de sinalizadores que especificam a política de exportação para uma chave persistente.</span><span class="sxs-lookup"><span data-stu-id="b7b10-156">A **DWORD** that contains a set of flags that specify the export policy for a persisted key.</span></span> <span data-ttu-id="b7b10-157">Essa propriedade só se aplica a chaves.</span><span class="sxs-lookup"><span data-stu-id="b7b10-157">This property only applies to keys.</span></span> <span data-ttu-id="b7b10-158">Isso pode conter zero ou uma combinação de um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b7b10-158">This can contain zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="b7b10-159">Identificador</span><span class="sxs-lookup"><span data-stu-id="b7b10-159">Identifier</span></span>                                    | <span data-ttu-id="b7b10-160">Valor</span><span class="sxs-lookup"><span data-stu-id="b7b10-160">Value</span></span>      | <span data-ttu-id="b7b10-161">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7b10-161">Description</span></span>                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7b10-162">**NCRYPT \_ permitir \_ sinalizador de exportação \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-162">**NCRYPT\_ALLOW\_EXPORT\_FLAG**</span></span>               | <span data-ttu-id="b7b10-163">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b7b10-163">0x00000001</span></span> | <span data-ttu-id="b7b10-164">A chave privada pode ser exportada.</span><span class="sxs-lookup"><span data-stu-id="b7b10-164">The private key can be exported.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="b7b10-165">**NCRYPT \_ permitir \_ \_ sinalizador de exportação de texto não criptografado \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-165">**NCRYPT\_ALLOW\_PLAINTEXT\_EXPORT\_FLAG**</span></span>    | <span data-ttu-id="b7b10-166">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b7b10-166">0x00000002</span></span> | <span data-ttu-id="b7b10-167">A chave privada pode ser exportada em formato de texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="b7b10-167">The private key can be exported in plaintext form.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="b7b10-168">**NCRYPT \_ permitir \_ sinalizador de arquivamento \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-168">**NCRYPT\_ALLOW\_ARCHIVING\_FLAG**</span></span>            | <span data-ttu-id="b7b10-169">0x00000004</span><span class="sxs-lookup"><span data-stu-id="b7b10-169">0x00000004</span></span> | <span data-ttu-id="b7b10-170">A chave privada pode ser exportada uma vez para fins de arquivamento.</span><span class="sxs-lookup"><span data-stu-id="b7b10-170">The private key can be exported once for archiving purposes.</span></span> <span data-ttu-id="b7b10-171">Esse sinalizador se aplica somente ao identificador de chave original no qual ele está definido.</span><span class="sxs-lookup"><span data-stu-id="b7b10-171">This flag only applies to the original key handle on which it is set.</span></span> <span data-ttu-id="b7b10-172">Essa política só pode ser aplicada ao identificador de chave original.</span><span class="sxs-lookup"><span data-stu-id="b7b10-172">This policy can only be applied to the original key handle.</span></span> <span data-ttu-id="b7b10-173">Depois que o identificador de chave for fechado, a chave não poderá mais ser exportada para fins de arquivamento.</span><span class="sxs-lookup"><span data-stu-id="b7b10-173">After the key handle has been closed, the key can no longer be exported for archiving purposes.</span></span>                   |
| <span data-ttu-id="b7b10-174">**NCRYPT \_ permitir \_ \_ sinalizador de arquivamento de texto não criptografado \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-174">**NCRYPT\_ALLOW\_PLAINTEXT\_ARCHIVING\_FLAG**</span></span> | <span data-ttu-id="b7b10-175">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b7b10-175">0x00000008</span></span> | <span data-ttu-id="b7b10-176">A chave privada pode ser exportada uma vez em formato de texto sem formatação para fins de arquivamento.</span><span class="sxs-lookup"><span data-stu-id="b7b10-176">The private key can be exported once in plaintext form for archiving purposes.</span></span> <span data-ttu-id="b7b10-177">Esse sinalizador se aplica somente ao identificador de chave original no qual ele está definido.</span><span class="sxs-lookup"><span data-stu-id="b7b10-177">This flag only applies to the original key handle on which it is set.</span></span> <span data-ttu-id="b7b10-178">Essa política só pode ser aplicada ao identificador de chave original.</span><span class="sxs-lookup"><span data-stu-id="b7b10-178">This policy can only be applied to the original key handle.</span></span> <span data-ttu-id="b7b10-179">Depois que o identificador de chave for fechado, a chave não poderá mais ser exportada para fins de arquivamento.</span><span class="sxs-lookup"><span data-stu-id="b7b10-179">After the key handle has been closed, the key can no longer be exported for archiving purposes.</span></span> |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-180"><span id="NCRYPT_IMPL_TYPE_PROPERTY"></span><span id="ncrypt_impl_type_property"></span>**\_Propriedade do \_ tipo NCRYPT impl \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-180"><span id="NCRYPT_IMPL_TYPE_PROPERTY"></span><span id="ncrypt_impl_type_property"></span>**NCRYPT\_IMPL\_TYPE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-181">L "tipo de impl"</span><span class="sxs-lookup"><span data-stu-id="b7b10-181">L"Impl Type"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-182">Um **DWORD** que contém um conjunto de sinalizadores que definem os detalhes de implementação do provedor.</span><span class="sxs-lookup"><span data-stu-id="b7b10-182">A **DWORD** that contains a set of flags that define implementation details of the provider.</span></span> <span data-ttu-id="b7b10-183">Essa propriedade só se aplica a provedores de armazenamento de chaves.</span><span class="sxs-lookup"><span data-stu-id="b7b10-183">This property only applies to key storage providers.</span></span> <span data-ttu-id="b7b10-184">Isso pode conter zero ou uma combinação de um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b7b10-184">This can contain zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="b7b10-185">Identificador</span><span class="sxs-lookup"><span data-stu-id="b7b10-185">Identifier</span></span>                            | <span data-ttu-id="b7b10-186">Valor</span><span class="sxs-lookup"><span data-stu-id="b7b10-186">Value</span></span>      | <span data-ttu-id="b7b10-187">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7b10-187">Description</span></span>                                               |
|---------------------------------------|------------|-----------------------------------------------------------|
| <span data-ttu-id="b7b10-188">**\_sinalizador de \_ hardware NCRYPT impl \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-188">**NCRYPT\_IMPL\_HARDWARE\_FLAG**</span></span>      | <span data-ttu-id="b7b10-189">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b7b10-189">0x00000001</span></span> | <span data-ttu-id="b7b10-190">O provedor é baseado em hardware.</span><span class="sxs-lookup"><span data-stu-id="b7b10-190">The provider is hardware based.</span></span>                           |
| <span data-ttu-id="b7b10-191">**\_sinalizador de \_ software NCRYPT impl \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-191">**NCRYPT\_IMPL\_SOFTWARE\_FLAG**</span></span>      | <span data-ttu-id="b7b10-192">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b7b10-192">0x00000002</span></span> | <span data-ttu-id="b7b10-193">O provedor é baseado em software.</span><span class="sxs-lookup"><span data-stu-id="b7b10-193">The provider is software based.</span></span>                           |
| <span data-ttu-id="b7b10-194">**sinalizador de removível de NCRYPT \_ impl \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-194">**NCRYPT\_IMPL\_REMOVABLE\_FLAG**</span></span>     | <span data-ttu-id="b7b10-195">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b7b10-195">0x00000008</span></span> | <span data-ttu-id="b7b10-196">O provedor é removível.</span><span class="sxs-lookup"><span data-stu-id="b7b10-196">The provider is removable.</span></span>                                |
| <span data-ttu-id="b7b10-197">**\_sinalizador de \_ RNG de hardware NCRYPT impl \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-197">**NCRYPT\_IMPL\_HARDWARE\_RNG\_FLAG**</span></span> | <span data-ttu-id="b7b10-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7b10-198">0x00000010</span></span> | <span data-ttu-id="b7b10-199">O provedor é um gerador de números aleatórios com base em hardware.</span><span class="sxs-lookup"><span data-stu-id="b7b10-199">The provider is a hardware based random number generator.</span></span> |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-200"><span id="NCRYPT_KEY_TYPE_PROPERTY"></span><span id="ncrypt_key_type_property"></span>**\_propriedade de \_ tipo de chave NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-200"><span id="NCRYPT_KEY_TYPE_PROPERTY"></span><span id="ncrypt_key_type_property"></span>**NCRYPT\_KEY\_TYPE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-201">L "tipo de chave"</span><span class="sxs-lookup"><span data-stu-id="b7b10-201">L"Key Type"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-202">Um **DWORD** que contém um conjunto de sinalizadores que definem o tipo de chave.</span><span class="sxs-lookup"><span data-stu-id="b7b10-202">A **DWORD** that contains a set of flags that define the key type.</span></span> <span data-ttu-id="b7b10-203">Essa propriedade só se aplica a chaves.</span><span class="sxs-lookup"><span data-stu-id="b7b10-203">This property only applies to keys.</span></span> <span data-ttu-id="b7b10-204">Isso pode conter zero ou o valor a seguir.</span><span class="sxs-lookup"><span data-stu-id="b7b10-204">This can contain zero or the following value.</span></span>



| <span data-ttu-id="b7b10-205">Identificador</span><span class="sxs-lookup"><span data-stu-id="b7b10-205">Identifier</span></span>                     | <span data-ttu-id="b7b10-206">Valor</span><span class="sxs-lookup"><span data-stu-id="b7b10-206">Value</span></span>      | <span data-ttu-id="b7b10-207">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7b10-207">Description</span></span>                                                                                              |
|--------------------------------|------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7b10-208">**\_sinalizador de \_ chave de máquina NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-208">**NCRYPT\_MACHINE\_KEY\_FLAG**</span></span> | <span data-ttu-id="b7b10-209">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b7b10-209">0x00000001</span></span> | <span data-ttu-id="b7b10-210">A chave se aplica ao computador local.</span><span class="sxs-lookup"><span data-stu-id="b7b10-210">The key applies to the local computer.</span></span> <span data-ttu-id="b7b10-211">Se esse sinalizador não estiver presente, a chave se aplicará ao usuário atual.</span><span class="sxs-lookup"><span data-stu-id="b7b10-211">If this flag is not present, the key applies to the current user.</span></span> |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-212"><span id="NCRYPT_KEY_USAGE_PROPERTY"></span><span id="ncrypt_key_usage_property"></span>**\_propriedade de \_ uso de chave NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-212"><span id="NCRYPT_KEY_USAGE_PROPERTY"></span><span id="ncrypt_key_usage_property"></span>**NCRYPT\_KEY\_USAGE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-213">L "uso da chave"</span><span class="sxs-lookup"><span data-stu-id="b7b10-213">L"Key Usage"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-214">Um **DWORD** que contém um conjunto de sinalizadores que definem os detalhes de uso de uma chave.</span><span class="sxs-lookup"><span data-stu-id="b7b10-214">A **DWORD** that contains a set of flags that define the usage details for a key.</span></span> <span data-ttu-id="b7b10-215">Essa propriedade só se aplica a chaves.</span><span class="sxs-lookup"><span data-stu-id="b7b10-215">This property only applies to keys.</span></span> <span data-ttu-id="b7b10-216">Isso pode conter zero ou uma combinação de um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b7b10-216">This can contain zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="b7b10-217">Identificador</span><span class="sxs-lookup"><span data-stu-id="b7b10-217">Identifier</span></span>                              | <span data-ttu-id="b7b10-218">Valor</span><span class="sxs-lookup"><span data-stu-id="b7b10-218">Value</span></span>      | <span data-ttu-id="b7b10-219">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7b10-219">Description</span></span>                                          |
|-----------------------------------------|------------|------------------------------------------------------|
| <span data-ttu-id="b7b10-220">**NCRYPT \_ permitir \_ sinalizador de descriptografia \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-220">**NCRYPT\_ALLOW\_DECRYPT\_FLAG**</span></span>        | <span data-ttu-id="b7b10-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b7b10-221">0x00000001</span></span> | <span data-ttu-id="b7b10-222">A chave pode ser usada para descriptografia.</span><span class="sxs-lookup"><span data-stu-id="b7b10-222">The key can be used for decryption.</span></span>                  |
| <span data-ttu-id="b7b10-223">**NCRYPT \_ permitir \_ sinalizador de assinatura \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-223">**NCRYPT\_ALLOW\_SIGNING\_FLAG**</span></span>        | <span data-ttu-id="b7b10-224">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b7b10-224">0x00000002</span></span> | <span data-ttu-id="b7b10-225">A chave pode ser usada para assinatura.</span><span class="sxs-lookup"><span data-stu-id="b7b10-225">The key can be used for signing.</span></span>                     |
| <span data-ttu-id="b7b10-226">**NCRYPT \_ permitir \_ \_ sinalizador de contrato de chave \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-226">**NCRYPT\_ALLOW\_KEY\_AGREEMENT\_FLAG**</span></span> | <span data-ttu-id="b7b10-227">0x00000004</span><span class="sxs-lookup"><span data-stu-id="b7b10-227">0x00000004</span></span> | <span data-ttu-id="b7b10-228">A chave pode ser usada para criptografia de contrato secreto.</span><span class="sxs-lookup"><span data-stu-id="b7b10-228">The key can be used for secret agreement encryption.</span></span> |
| <span data-ttu-id="b7b10-229">**NCRYPT \_ permitir \_ todos os \_ usos**</span><span class="sxs-lookup"><span data-stu-id="b7b10-229">**NCRYPT\_ALLOW\_ALL\_USAGES**</span></span>          | <span data-ttu-id="b7b10-230">0x00ffffff</span><span class="sxs-lookup"><span data-stu-id="b7b10-230">0x00ffffff</span></span> | <span data-ttu-id="b7b10-231">A chave pode ser usada para qualquer finalidade.</span><span class="sxs-lookup"><span data-stu-id="b7b10-231">The key can be used for any purpose.</span></span>                 |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-232"><span id="NCRYPT_LAST_MODIFIED_PROPERTY"></span><span id="ncrypt_last_modified_property"></span>**\_Propriedade NCRYPT última \_ modificação \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-232"><span id="NCRYPT_LAST_MODIFIED_PROPERTY"></span><span id="ncrypt_last_modified_property"></span>**NCRYPT\_LAST\_MODIFIED\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-233">L "Modified"</span><span class="sxs-lookup"><span data-stu-id="b7b10-233">L"Modified"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-234">Indica quando a chave foi modificada pela última vez.</span><span class="sxs-lookup"><span data-stu-id="b7b10-234">Indicates when the key was last modified.</span></span> <span data-ttu-id="b7b10-235">Esse tipo de dados é um ponteiro para uma estrutura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="b7b10-235">This data type is a pointer to a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure.</span></span> <span data-ttu-id="b7b10-236">Essa propriedade só se aplica a chaves persistentes.</span><span class="sxs-lookup"><span data-stu-id="b7b10-236">This property only applies to persisted keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-237"><span id="NCRYPT_LENGTH_PROPERTY"></span><span id="ncrypt_length_property"></span>**\_propriedade de comprimento NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-237"><span id="NCRYPT_LENGTH_PROPERTY"></span><span id="ncrypt_length_property"></span>**NCRYPT\_LENGTH\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-238">L "comprimento"</span><span class="sxs-lookup"><span data-stu-id="b7b10-238">L"Length"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-239">Um **DWORD** que contém o comprimento, em bits, da chave.</span><span class="sxs-lookup"><span data-stu-id="b7b10-239">A **DWORD** that contains the length, in bits, of the key.</span></span> <span data-ttu-id="b7b10-240">Essa propriedade só se aplica a chaves.</span><span class="sxs-lookup"><span data-stu-id="b7b10-240">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-241"><span id="NCRYPT_LENGTHS_PROPERTY"></span><span id="ncrypt_lengths_property"></span>**\_propriedade de comprimentos NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-241"><span id="NCRYPT_LENGTHS_PROPERTY"></span><span id="ncrypt_lengths_property"></span>**NCRYPT\_LENGTHS\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-242">L "comprimentos"</span><span class="sxs-lookup"><span data-stu-id="b7b10-242">L"Lengths"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-243">Indica os tamanhos de chave que são suportados pela chave.</span><span class="sxs-lookup"><span data-stu-id="b7b10-243">Indicates the key sizes that are supported by the key.</span></span> <span data-ttu-id="b7b10-244">Esse tipo de dados é um ponteiro para uma estrutura de [**\_ \_ comprimentos com suporte NCRYPT**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_supported_lengths) que contém essas informações.</span><span class="sxs-lookup"><span data-stu-id="b7b10-244">This data type is a pointer to an [**NCRYPT\_SUPPORTED\_LENGTHS**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_supported_lengths) structure that contains this information.</span></span> <span data-ttu-id="b7b10-245">Essa propriedade só se aplica a chaves.</span><span class="sxs-lookup"><span data-stu-id="b7b10-245">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-246"><span id="NCRYPT_MAX_NAME_LENGTH_PROPERTY"></span><span id="ncrypt_max_name_length_property"></span>**\_propriedade de \_ comprimento de nome Max \_ NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-246"><span id="NCRYPT_MAX_NAME_LENGTH_PROPERTY"></span><span id="ncrypt_max_name_length_property"></span>**NCRYPT\_MAX\_NAME\_LENGTH\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-247">L "comprimento máximo do nome"</span><span class="sxs-lookup"><span data-stu-id="b7b10-247">L"Max Name Length"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-248">Um **DWORD** que contém o comprimento máximo, em caracteres, do nome de uma chave persistente.</span><span class="sxs-lookup"><span data-stu-id="b7b10-248">A **DWORD** that contains the maximum length, in characters, of the name of a persistent key.</span></span> <span data-ttu-id="b7b10-249">Essa propriedade se aplica somente a um provedor.</span><span class="sxs-lookup"><span data-stu-id="b7b10-249">This property only applies to a provider.</span></span>

<span data-ttu-id="b7b10-250">Essa propriedade destina-se principalmente a ser usada por provedores de armazenamento de chaves que armazenam suas chaves em um dispositivo que tem uma quantidade limitada de memória disponível, como um cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="b7b10-250">This property is primarily intended to be used by key storage providers that store their keys on a device that has a limited amount of available memory, such as a smart card.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-251"><span id="NCRYPT_NAME_PROPERTY"></span><span id="ncrypt_name_property"></span>**\_propriedade de nome NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-251"><span id="NCRYPT_NAME_PROPERTY"></span><span id="ncrypt_name_property"></span>**NCRYPT\_NAME\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-252">L "nome"</span><span class="sxs-lookup"><span data-stu-id="b7b10-252">L"Name"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-253">Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que contém o nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="b7b10-253">A pointer to a null-terminated Unicode string that contains the name of the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-254"><span id="NCRYPT_PIN_PROMPT_PROPERTY"></span><span id="ncrypt_pin_prompt_property"></span>**\_propriedade de \_ prompt de PIN NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-254"><span id="NCRYPT_PIN_PROMPT_PROPERTY"></span><span id="ncrypt_pin_prompt_property"></span>**NCRYPT\_PIN\_PROMPT\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-255">L "SmartCardPinPrompt"</span><span class="sxs-lookup"><span data-stu-id="b7b10-255">L"SmartCardPinPrompt"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-256">Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="b7b10-256">This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-257"><span id="NCRYPT_PIN_PROPERTY"></span><span id="ncrypt_pin_property"></span>**\_propriedade de PIN NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-257"><span id="NCRYPT_PIN_PROPERTY"></span><span id="ncrypt_pin_property"></span>**NCRYPT\_PIN\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-258">L "SmartCardPin"</span><span class="sxs-lookup"><span data-stu-id="b7b10-258">L"SmartCardPin"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-259">Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que contém o PIN.</span><span class="sxs-lookup"><span data-stu-id="b7b10-259">A pointer to a null-terminated Unicode string that contains the PIN.</span></span> <span data-ttu-id="b7b10-260">O PIN é usado para uma chave de cartão inteligente ou a senha para uma chave protegida por senha armazenada em um KSP baseado em software.</span><span class="sxs-lookup"><span data-stu-id="b7b10-260">The PIN is used for a smart card key or the password for a password-protected key stored in a software-based KSP.</span></span> <span data-ttu-id="b7b10-261">Esta propriedade só pode ser definida.</span><span class="sxs-lookup"><span data-stu-id="b7b10-261">This property can only be set.</span></span> <span data-ttu-id="b7b10-262">O Microsoft KSPs armazenará esse valor em cache para que o usuário seja solicitado apenas uma vez por processo.</span><span class="sxs-lookup"><span data-stu-id="b7b10-262">Microsoft KSPs will cache this value so that the user is only prompted once per process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-263"><span id="NCRYPT_PROVIDER_HANDLE_PROPERTY"></span><span id="ncrypt_provider_handle_property"></span>**\_propriedade de \_ identificador do provedor NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-263"><span id="NCRYPT_PROVIDER_HANDLE_PROPERTY"></span><span id="ncrypt_provider_handle_property"></span>**NCRYPT\_PROVIDER\_HANDLE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-264">L "identificador do provedor"</span><span class="sxs-lookup"><span data-stu-id="b7b10-264">L"Provider Handle"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-265">Um **\_ \_ identificador de Prov de NCRYPT** que contém o identificador do provedor de armazenamento de chaves CNG.</span><span class="sxs-lookup"><span data-stu-id="b7b10-265">An **NCRYPT\_PROV\_HANDLE** that contains the handle of the CNG key storage provider.</span></span> <span data-ttu-id="b7b10-266">Quando terminar de usar o identificador, você deverá chamar [**NCryptFreeObject**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfreeobject) para liberá-lo.</span><span class="sxs-lookup"><span data-stu-id="b7b10-266">When you are finished using the handle, you must call [**NCryptFreeObject**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfreeobject) to release it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-267"><span id="NCRYPT_READER_PROPERTY"></span><span id="ncrypt_reader_property"></span>**\_propriedade de leitor NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-267"><span id="NCRYPT_READER_PROPERTY"></span><span id="ncrypt_reader_property"></span>**NCRYPT\_READER\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-268">L "SmartCardReader"</span><span class="sxs-lookup"><span data-stu-id="b7b10-268">L"SmartCardReader"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-269">Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que contém o nome do leitor de cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="b7b10-269">A pointer to a null-terminated Unicode string that contains the name of the smart card reader.</span></span> <span data-ttu-id="b7b10-270">Esta propriedade só pode ser definida.</span><span class="sxs-lookup"><span data-stu-id="b7b10-270">This property can only be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-271"><span id="NCRYPT_ROOT_CERTSTORE_PROPERTY"></span><span id="ncrypt_root_certstore_property"></span>**\_ \_ Propriedade CERTSTORE de raiz NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-271"><span id="NCRYPT_ROOT_CERTSTORE_PROPERTY"></span><span id="ncrypt_root_certstore_property"></span>**NCRYPT\_ROOT\_CERTSTORE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-272">L "SmartcardRootCertStore"</span><span class="sxs-lookup"><span data-stu-id="b7b10-272">L"SmartcardRootCertStore"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-273">Um **HCERTSTORE** que representa o repositório de certificados raiz do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="b7b10-273">An **HCERTSTORE** that represents the smart card root certificate store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-274"><span id="_NCRYPT_SCARD_PIN_ID"></span><span id="_ncrypt_scard_pin_id"></span>**NCRYPT \_ \_ \_ ID do PIN do scartar**</span><span class="sxs-lookup"><span data-stu-id="b7b10-274"><span id="_NCRYPT_SCARD_PIN_ID"></span><span id="_ncrypt_scard_pin_id"></span> **NCRYPT\_SCARD\_PIN\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-275">L "SmartCardPinId"</span><span class="sxs-lookup"><span data-stu-id="b7b10-275">L"SmartCardPinId"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-276">Um ponteiro para o valor da **\_ ID de PIN** associado a uma determinada [*chave de criptografia*](/windows/desktop/SecGloss/c-gly) em um [*cartão inteligente*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="b7b10-276">A pointer to the **PIN\_ID** value associated with a given [*cryptographic key*](/windows/desktop/SecGloss/c-gly) on a [*smart card*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="b7b10-277">Trata-se de uma propriedade somente leitura.</span><span class="sxs-lookup"><span data-stu-id="b7b10-277">This is a read-only property.</span></span> <span data-ttu-id="b7b10-278">O tipo de dados **\_ ID do PIN** é definido em cardmod. h.</span><span class="sxs-lookup"><span data-stu-id="b7b10-278">The **PIN\_ID** data type is defined in Cardmod.h.</span></span>

<span data-ttu-id="b7b10-279">**Windows Server 2008 e Windows Vista:** Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="b7b10-279">**Windows Server 2008 and Windows Vista:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-280"><span id="NCRYPT_SCARD_PIN_INFO"></span><span id="ncrypt_scard_pin_info"></span>**informações de PIN de NCRYPT \_ scartar \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-280"><span id="NCRYPT_SCARD_PIN_INFO"></span><span id="ncrypt_scard_pin_info"></span>**NCRYPT\_SCARD\_PIN\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-281">L "SmartCardPinInfo"</span><span class="sxs-lookup"><span data-stu-id="b7b10-281">L"SmartCardPinInfo"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-282">Um ponteiro para [**fixar \_**](/windows/desktop/api/mbnapi/ns-mbnapi-mbn_pin_info) a estrutura de informações do PIN associado a uma determinada chave de criptografia no cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="b7b10-282">A pointer to [**PIN\_INFO**](/windows/desktop/api/mbnapi/ns-mbnapi-mbn_pin_info) structure of the PIN associated with a given cryptographic key on the smart card.</span></span> <span data-ttu-id="b7b10-283">O chamador fornece o identificador de chave.</span><span class="sxs-lookup"><span data-stu-id="b7b10-283">The caller provides the key handle.</span></span> <span data-ttu-id="b7b10-284">Esta propriedade é uma propriedade somente leitura.</span><span class="sxs-lookup"><span data-stu-id="b7b10-284">This property is a read-only property.</span></span> <span data-ttu-id="b7b10-285">A estrutura de **\_ informações de PIN** é definida em cardmod. h.</span><span class="sxs-lookup"><span data-stu-id="b7b10-285">The **PIN\_INFO** structure is defined in Cardmod.h.</span></span>

<span data-ttu-id="b7b10-286">**Windows Server 2008 e Windows Vista:** Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="b7b10-286">**Windows Server 2008 and Windows Vista:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-287"><span id="NCRYPT_SECURE_PIN_PROPERTY"></span><span id="ncrypt_secure_pin_property"></span>**\_Propriedade NCRYPT Secure \_ PIN \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-287"><span id="NCRYPT_SECURE_PIN_PROPERTY"></span><span id="ncrypt_secure_pin_property"></span>**NCRYPT\_SECURE\_PIN\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-288">L "SmartCardSecurePin"</span><span class="sxs-lookup"><span data-stu-id="b7b10-288">L"SmartCardSecurePin"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-289">Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que contém o PIN da sessão de cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="b7b10-289">A pointer to a null-terminated Unicode string that contains the smart card session PIN.</span></span> <span data-ttu-id="b7b10-290">Esta propriedade só pode ser definida.</span><span class="sxs-lookup"><span data-stu-id="b7b10-290">This property can only be set.</span></span>

<span data-ttu-id="b7b10-291">**Windows Vista:** Não há suporte para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="b7b10-291">**Windows Vista:** This property is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-292"><span id="NCRYPT_SECURITY_DESCR_PROPERTY"></span><span id="ncrypt_security_descr_property"></span>**\_propriedade de \_ Descrição de segurança de NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-292"><span id="NCRYPT_SECURITY_DESCR_PROPERTY"></span><span id="ncrypt_security_descr_property"></span>**NCRYPT\_SECURITY\_DESCR\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-293">L "Descrição de segurança"</span><span class="sxs-lookup"><span data-stu-id="b7b10-293">L"Security Descr"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-294">Um ponteiro para uma estrutura de [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) que contém informações de controle de acesso para a chave.</span><span class="sxs-lookup"><span data-stu-id="b7b10-294">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that contains access control information for the key.</span></span> <span data-ttu-id="b7b10-295">Essa propriedade só se aplica a chaves persistentes.</span><span class="sxs-lookup"><span data-stu-id="b7b10-295">This property only applies to persistent keys.</span></span> <span data-ttu-id="b7b10-296">O parâmetro *dwFlags* da função [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) ou [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) identifica a parte do descritor de segurança a ser obtido ou definido.</span><span class="sxs-lookup"><span data-stu-id="b7b10-296">The *dwFlags* parameter of the [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) or [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) function identifies the part of the security descriptor to get or set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-297"><span id="NCRYPT_SECURITY_DESCR_SUPPORT_PROPERTY"></span><span id="ncrypt_security_descr_support_property"></span>**\_propriedade de \_ suporte do descr de segurança NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-297"><span id="NCRYPT_SECURITY_DESCR_SUPPORT_PROPERTY"></span><span id="ncrypt_security_descr_support_property"></span>**NCRYPT\_SECURITY\_DESCR\_SUPPORT\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-298">L "suporte a descr de segurança"</span><span class="sxs-lookup"><span data-stu-id="b7b10-298">L"Security Descr Support"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-299">Indica se o provedor dá suporte a descritores de segurança para chaves.</span><span class="sxs-lookup"><span data-stu-id="b7b10-299">Indicates whether the provider supports security descriptors for keys.</span></span> <span data-ttu-id="b7b10-300">Essa propriedade é uma **DWORD** que contém 1 se o provedor oferece suporte a descritores de segurança para chaves.</span><span class="sxs-lookup"><span data-stu-id="b7b10-300">This property is a **DWORD** that contains 1 if the provider supports security descriptors for keys.</span></span> <span data-ttu-id="b7b10-301">Se essa propriedade contiver qualquer outro valor, ou se a função [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) retornar o **nte \_ sem \_ suporte**, o provedor não oferecerá suporte a descritores de segurança para chaves.</span><span class="sxs-lookup"><span data-stu-id="b7b10-301">If this property contains any other value, or if the [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) function returns **NTE\_NOT\_SUPPORTED**, then the provider does not support security descriptors for keys.</span></span> <span data-ttu-id="b7b10-302">Essa propriedade só se aplica a provedores.</span><span class="sxs-lookup"><span data-stu-id="b7b10-302">This property only applies to providers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-303"><span id="NCRYPT_SMARTCARD_GUID_PROPERTY"></span><span id="ncrypt_smartcard_guid_property"></span>**\_propriedade de GUID de cartão inteligente NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-303"><span id="NCRYPT_SMARTCARD_GUID_PROPERTY"></span><span id="ncrypt_smartcard_guid_property"></span>**NCRYPT\_SMARTCARD\_GUID\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-304">L "SmartCardGuid"</span><span class="sxs-lookup"><span data-stu-id="b7b10-304">L"SmartCardGuid"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-305">Um BLOB que contém o identificador do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="b7b10-305">A BLOB that contains the identifier of the smart card.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-306"><span id="NCRYPT_UI_POLICY_PROPERTY"></span><span id="ncrypt_ui_policy_property"></span>**\_propriedade de \_ política de IU NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-306"><span id="NCRYPT_UI_POLICY_PROPERTY"></span><span id="ncrypt_ui_policy_property"></span>**NCRYPT\_UI\_POLICY\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-307">L "diretiva de interface do usuário"</span><span class="sxs-lookup"><span data-stu-id="b7b10-307">L"UI Policy"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-308">Se usado com a função [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) ou [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) , esse é um ponteiro para uma estrutura de [**\_ \_ diretiva de interface do usuário NCRYPT**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_ui_policy) que contém a diretiva de interface de usuários de chave forte para a chave.</span><span class="sxs-lookup"><span data-stu-id="b7b10-308">If used with the [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) or [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) function, this is a pointer to an [**NCRYPT\_UI\_POLICY**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_ui_policy) structure that contains the strong key user interface policy for the key.</span></span> <span data-ttu-id="b7b10-309">Essa propriedade só se aplica a chaves persistentes.</span><span class="sxs-lookup"><span data-stu-id="b7b10-309">This property only applies to persistent keys.</span></span> <span data-ttu-id="b7b10-310">Essa propriedade só pode ser definida quando a chave está sendo gerada.</span><span class="sxs-lookup"><span data-stu-id="b7b10-310">This property can only be set when the key is being generated.</span></span> <span data-ttu-id="b7b10-311">Depois que a função [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) tiver sido chamada para essa chave, essa propriedade se tornará somente leitura.</span><span class="sxs-lookup"><span data-stu-id="b7b10-311">Once the [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) function has been called for this key, this property becomes read-only.</span></span>

<span data-ttu-id="b7b10-312">Um provedor de armazenamento de chaves pode receber esse parâmetro por meio de uma função de retorno de chamada [**NCryptSetPropertyFn**](https://www.bing.com/search?q=**NCryptSetPropertyFn**) .</span><span class="sxs-lookup"><span data-stu-id="b7b10-312">A key storage provider can receive this parameter through an [**NCryptSetPropertyFn**](https://www.bing.com/search?q=**NCryptSetPropertyFn**) callback function.</span></span> <span data-ttu-id="b7b10-313">O valor do parâmetro é uma \_ estrutura de blob de diretiva de interface do usuário NCRYPT \_ \_ que contém as mesmas informações.</span><span class="sxs-lookup"><span data-stu-id="b7b10-313">The parameter value is an NCRYPT\_UI\_POLICY\_BLOB structure that contains the same information.</span></span> <span data-ttu-id="b7b10-314">Da mesma forma, quando um aplicativo faz uma solicitação por meio de NCryptSetPropertyFn ao provedor para retornar essa propriedade, espera-se que o provedor retorne uma \_ estrutura de blob de política de interface do usuário NCRYPT \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b7b10-314">Similarly, when an application makes a request through NCryptSetPropertyFn to the provider to return this property, the provider is expected to return an NCRYPT\_UI\_POLICY\_BLOB structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-315"><span id="NCRYPT_UNIQUE_NAME_PROPERTY"></span><span id="ncrypt_unique_name_property"></span>**\_propriedade de \_ nome \_ exclusivo NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="b7b10-315"><span id="NCRYPT_UNIQUE_NAME_PROPERTY"></span><span id="ncrypt_unique_name_property"></span>**NCRYPT\_UNIQUE\_NAME\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-316">L "nome exclusivo"</span><span class="sxs-lookup"><span data-stu-id="b7b10-316">L"Unique Name"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-317">Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que contém o nome exclusivo do objeto.</span><span class="sxs-lookup"><span data-stu-id="b7b10-317">A pointer to a null-terminated Unicode string that contains the unique name of the object.</span></span> <span data-ttu-id="b7b10-318">Esse é um nome alternativo que pode ser usado ao acessar a chave.</span><span class="sxs-lookup"><span data-stu-id="b7b10-318">This is an alternate name that can be used when accessing the key.</span></span> <span data-ttu-id="b7b10-319">Essa propriedade é usada quando é pensado que o nome da chave originalmente passado para [**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) não é exclusivo o suficiente para identificar de forma confiável a chave persistente.</span><span class="sxs-lookup"><span data-stu-id="b7b10-319">This property is used when it is thought that the key name originally passed to [**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) is not unique enough to reliably identify the persisted key.</span></span> <span data-ttu-id="b7b10-320">O provedor de armazenamento de chaves da Microsoft retornará o nome do arquivo da chave como essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="b7b10-320">The Microsoft key storage provider will return the file name of the key as this property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-321"><span id="NCRYPT_USE_CONTEXT_PROPERTY"></span><span id="ncrypt_use_context_property"></span>**NCRYPT \_ \_ propriedade de contexto de uso \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-321"><span id="NCRYPT_USE_CONTEXT_PROPERTY"></span><span id="ncrypt_use_context_property"></span>**NCRYPT\_USE\_CONTEXT\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-322">L "usar contexto"</span><span class="sxs-lookup"><span data-stu-id="b7b10-322">L"Use Context"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-323">Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que descreve o contexto da operação.</span><span class="sxs-lookup"><span data-stu-id="b7b10-323">A pointer to a null-terminated Unicode string that describes the context of the operation.</span></span> <span data-ttu-id="b7b10-324">Essa propriedade não é persistente e pode ser definida em um provedor ou em uma chave.</span><span class="sxs-lookup"><span data-stu-id="b7b10-324">This property is not persistent and can be set on either a provider or a key.</span></span> <span data-ttu-id="b7b10-325">Uma chave não tem acesso à propriedade de **\_ propriedade de \_ contexto \_ de uso NCRYPT** do provedor porque a propriedade é específica somente para o identificador para o qual ela está definida.</span><span class="sxs-lookup"><span data-stu-id="b7b10-325">A key does not have access to the **NCRYPT\_USE\_CONTEXT\_PROPERTY** property of the provider because the property is specific only to the handle it is set for.</span></span>

<span data-ttu-id="b7b10-326">Um exemplo em que essa propriedade seria usada no contexto de um provedor é um provedor de armazenamento de chaves que precisa solicitar ao usuário durante uma chamada para [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) (por exemplo, "Insira seu cartão inteligente no leitor.").</span><span class="sxs-lookup"><span data-stu-id="b7b10-326">An example where this property would be used in the context of a provider is a key storage provider that needs to prompt the user during a call to [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) (for example, "Insert your smart card in the reader.").</span></span> <span data-ttu-id="b7b10-327">Como o identificador de chave não está disponível até que **NCryptOpenKey** seja retornado, o aplicativo deve definir essa propriedade no identificador do provedor antes de chamar **NCryptOpenKey**.</span><span class="sxs-lookup"><span data-stu-id="b7b10-327">Because the key handle is not available until after **NCryptOpenKey** returns, the application should set this property on the provider handle prior to calling **NCryptOpenKey**.</span></span>

<span data-ttu-id="b7b10-328">Um exemplo em que essa propriedade seria usada no contexto de um identificador de chave é um provedor de armazenamento de chaves que precisa solicitar ao usuário durante uma operação usando a chave (por exemplo, "este aplicativo precisa usar essa chave para assinar um documento.").</span><span class="sxs-lookup"><span data-stu-id="b7b10-328">An example where this property would be used in the context of a key handle is a key storage provider that needs to prompt the user during an operation using the key (for example, "This application needs to use this key to sign a document.").</span></span> <span data-ttu-id="b7b10-329">Em seguida, o provedor poderia retransmitir essas informações de contexto para o usuário em qualquer interface do usuário mostrada durante a operação.</span><span class="sxs-lookup"><span data-stu-id="b7b10-329">The provider could then relay this context information to the user in any user interface shown during the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-330"><span id="NCRYPT_USE_COUNT_ENABLED_PROPERTY"></span><span id="ncrypt_use_count_enabled_property"></span>**\_propriedade de uso de \_ contagem \_ HABILITAda de NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-330"><span id="NCRYPT_USE_COUNT_ENABLED_PROPERTY"></span><span id="ncrypt_use_count_enabled_property"></span>**NCRYPT\_USE\_COUNT\_ENABLED\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-331">L "contagem de uso habilitada"</span><span class="sxs-lookup"><span data-stu-id="b7b10-331">L"Enabled Use Count"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-332">Indica se o provedor dá suporte à contagem de uso para chaves.</span><span class="sxs-lookup"><span data-stu-id="b7b10-332">Indicates whether the provider supports usage counting for keys.</span></span> <span data-ttu-id="b7b10-333">Essa propriedade é uma **DWORD** que contém 1 se o provedor oferece suporte à contagem de uso para chaves.</span><span class="sxs-lookup"><span data-stu-id="b7b10-333">This property is a **DWORD** that contains 1 if the provider supports usage counting for keys.</span></span> <span data-ttu-id="b7b10-334">Se essa propriedade contiver qualquer outro valor, ou se a função [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) retornar o **nte \_ sem \_ suporte**, o provedor não oferecerá suporte à contagem de uso para chaves.</span><span class="sxs-lookup"><span data-stu-id="b7b10-334">If this property contains any other value, or if the [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) function returns **NTE\_NOT\_SUPPORTED**, then the provider does not support usage counting for keys.</span></span> <span data-ttu-id="b7b10-335">Essa propriedade só se aplica a provedores.</span><span class="sxs-lookup"><span data-stu-id="b7b10-335">This property only applies to providers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-336"><span id="NCRYPT_USE_COUNT_PROPERTY"></span><span id="ncrypt_use_count_property"></span>**\_propriedade de \_ contagem de uso NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-336"><span id="NCRYPT_USE_COUNT_PROPERTY"></span><span id="ncrypt_use_count_property"></span>**NCRYPT\_USE\_COUNT\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-337">L "contagem de uso"</span><span class="sxs-lookup"><span data-stu-id="b7b10-337">L"Use Count"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-338">Uma variável de [**\_ inteiro ULARGE**](https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-ularge_integer~r1) que contém o número de operações que a [*chave privada*](/windows/desktop/SecGloss/p-gly) especificada executou.</span><span class="sxs-lookup"><span data-stu-id="b7b10-338">A [**ULARGE\_INTEGER**](https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-ularge_integer~r1) variable that contains the number of operations that the specified [*private key*](/windows/desktop/SecGloss/p-gly) has performed.</span></span> <span data-ttu-id="b7b10-339">Essa propriedade é opcional e pode não ter suporte de todos os provedores.</span><span class="sxs-lookup"><span data-stu-id="b7b10-339">This property is optional and may not be supported by all providers.</span></span> <span data-ttu-id="b7b10-340">Os provedores que oferecem suporte a essa propriedade nas chaves também devem oferecer suporte à propriedade de **\_ propriedade de uso \_ \_ habilitado \_ da contagem de utilização de NCRYPT** no identificador do provedor.</span><span class="sxs-lookup"><span data-stu-id="b7b10-340">Providers that support this property on keys should also support the **NCRYPT\_USE\_COUNT\_ENABLED\_PROPERTY** property on the provider handle.</span></span> <span data-ttu-id="b7b10-341">O provedor de armazenamento de chaves da Microsoft não oferece suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="b7b10-341">The Microsoft key storage provider does not support this property.</span></span> <span data-ttu-id="b7b10-342">Essa propriedade só se aplica a chaves persistentes.</span><span class="sxs-lookup"><span data-stu-id="b7b10-342">This property only applies to persistent keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-343"><span id="NCRYPT_USER_CERTSTORE_PROPERTY"></span><span id="ncrypt_user_certstore_property"></span>**\_ \_ Propriedade CERTSTORE de usuário NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-343"><span id="NCRYPT_USER_CERTSTORE_PROPERTY"></span><span id="ncrypt_user_certstore_property"></span>**NCRYPT\_USER\_CERTSTORE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-344">L "SmartCardUserCertStore"</span><span class="sxs-lookup"><span data-stu-id="b7b10-344">L"SmartCardUserCertStore"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-345">Um **HCERTSTORE** que representa o repositório de certificados do usuário do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="b7b10-345">An **HCERTSTORE** that represents the smart card user certificate store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-346"><span id="NCRYPT_VERSION_PROPERTY"></span><span id="ncrypt_version_property"></span>**\_propriedade de versão NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-346"><span id="NCRYPT_VERSION_PROPERTY"></span><span id="ncrypt_version_property"></span>**NCRYPT\_VERSION\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-347">L "versão"</span><span class="sxs-lookup"><span data-stu-id="b7b10-347">L"Version"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-348">Um **DWORD** que contém a versão de software do provedor.</span><span class="sxs-lookup"><span data-stu-id="b7b10-348">A **DWORD** that contains the software version of the provider.</span></span> <span data-ttu-id="b7b10-349">A palavra alta contém a versão principal e a palavra inferior contém a versão secundária.</span><span class="sxs-lookup"><span data-stu-id="b7b10-349">The high word contains the major version and the low word contains the minor version.</span></span> <span data-ttu-id="b7b10-350">Por exemplo, 0x00030033 = 3,51.</span><span class="sxs-lookup"><span data-stu-id="b7b10-350">For example, 0x00030033 = 3.51.</span></span> <span data-ttu-id="b7b10-351">Essa propriedade só se aplica a provedores.</span><span class="sxs-lookup"><span data-stu-id="b7b10-351">This property only applies to providers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7b10-352"><span id="NCRYPT_WINDOW_HANDLE_PROPERTY"></span><span id="ncrypt_window_handle_property"></span>**\_propriedade de \_ identificador de janela NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="b7b10-352"><span id="NCRYPT_WINDOW_HANDLE_PROPERTY"></span><span id="ncrypt_window_handle_property"></span>**NCRYPT\_WINDOW\_HANDLE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7b10-353">L "identificador HWND"</span><span class="sxs-lookup"><span data-stu-id="b7b10-353">L"HWND Handle"</span></span>
</dt> <dt>



<span data-ttu-id="b7b10-354">Um ponteiro para o identificador de janela (**HWND**) a ser usado como o pai de qualquer interface do usuário que é exibida.</span><span class="sxs-lookup"><span data-stu-id="b7b10-354">A pointer to the window handle (**HWND**) to be used as the parent of any user interface that is displayed.</span></span>

<span data-ttu-id="b7b10-355">Como um comportamento indesejável pode ocorrer quando uma interface do usuário é mostrada usando um identificador de janela **nulo** para o pai, é altamente recomendável que um provedor de armazenamento de chaves não exiba uma interface do usuário, a menos que essa propriedade esteja definida.</span><span class="sxs-lookup"><span data-stu-id="b7b10-355">Because undesirable behavior can happen when a user interface is shown by using a **NULL** window handle for the parent, we strongly recommend that a key storage provider not display a user interface unless this property is set.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="b7b10-356">Os valores a seguir são usados para definir limites de dados de propriedade.</span><span class="sxs-lookup"><span data-stu-id="b7b10-356">The following values are used to define limits of property data.</span></span>



| <span data-ttu-id="b7b10-357">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="b7b10-357">Constant/value</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="b7b10-358">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7b10-358">Description</span></span>                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="NCRYPT_MAX_PROPERTY_DATA"></span><span id="ncrypt_max_property_data"></span><dl> <span data-ttu-id="b7b10-359"><dt>**NCRYPT \_ 0x100000 \_ de \_ dados de propriedade Max**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b7b10-359"><dt>**NCRYPT\_MAX\_PROPERTY\_DATA**</dt> <dt>0x100000</dt></span></span> </dl> | <span data-ttu-id="b7b10-360">Especifica o tamanho máximo de um valor de propriedade, em bytes.</span><span class="sxs-lookup"><span data-stu-id="b7b10-360">Specifies the maximum size of a property value, in bytes.</span></span><br/>     |
| <span id="NCRYPT_MAX_PROPERTY_NAME"></span><span id="ncrypt_max_property_name"></span><dl> <span data-ttu-id="b7b10-361"><dt>**NCRYPT \_ \_ \_ Nome de propriedade máx**</dt> . <dt>64</dt></span><span class="sxs-lookup"><span data-stu-id="b7b10-361"><dt>**NCRYPT\_MAX\_PROPERTY\_NAME**</dt> <dt>64</dt></span></span> </dl>       | <span data-ttu-id="b7b10-362">Especifica o tamanho máximo de um nome de propriedade, em caracteres.</span><span class="sxs-lookup"><span data-stu-id="b7b10-362">Specifies the maximum size of a property name, in characters.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b7b10-363">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7b10-363">Requirements</span></span>



| <span data-ttu-id="b7b10-364">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7b10-364">Requirement</span></span> | <span data-ttu-id="b7b10-365">Valor</span><span class="sxs-lookup"><span data-stu-id="b7b10-365">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b7b10-366">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7b10-366">Minimum supported client</span></span><br/> | <span data-ttu-id="b7b10-367">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b7b10-367">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b7b10-368">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7b10-368">Minimum supported server</span></span><br/> | <span data-ttu-id="b7b10-369">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b7b10-369">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b7b10-370">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b7b10-370">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7b10-371"><dt>NCrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7b10-371"><dt>Ncrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7b10-372">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7b10-372">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7b10-373">**NCryptGetProperty**</span><span class="sxs-lookup"><span data-stu-id="b7b10-373">**NCryptGetProperty**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty)
</dt> <dt>

[<span data-ttu-id="b7b10-374">**NCryptSetProperty**</span><span class="sxs-lookup"><span data-stu-id="b7b10-374">**NCryptSetProperty**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty)
</dt> </dl>

 

