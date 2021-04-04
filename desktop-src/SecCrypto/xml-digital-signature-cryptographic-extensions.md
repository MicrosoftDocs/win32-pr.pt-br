---
description: O CryptXML permite que os desenvolvedores estendam algoritmos de criptografia com suporte nativo registrando uma DLL de extensão de criptografia de todo o sistema.
ms.assetid: b0625481-660a-4fd5-ba15-d532998f95a6
title: Extensões criptográficas de assinatura digital XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8747521913ca1d551f1a2d4fd5b1c79d80065832
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "103837544"
---
# <a name="xml-digital-signature-cryptographic-extensions"></a><span data-ttu-id="4bd63-103">Extensões criptográficas de assinatura digital XML</span><span class="sxs-lookup"><span data-stu-id="4bd63-103">XML Digital Signature Cryptographic Extensions</span></span>

<span data-ttu-id="4bd63-104">O CryptXML permite que os desenvolvedores estendam algoritmos de criptografia com suporte nativo registrando uma DLL de extensão de criptografia de todo o sistema.</span><span class="sxs-lookup"><span data-stu-id="4bd63-104">CryptXML allows developers to extend natively supported cryptographic algorithms by registering a system wide cryptographic extension DLL.</span></span> <span data-ttu-id="4bd63-105">As DLLs de extensão estendem os algoritmos com suporte pelos elementos XML **SignatureMethod** e **DigestMethod** .</span><span class="sxs-lookup"><span data-stu-id="4bd63-105">Extension DLLs extend the algorithms supported by **SignatureMethod** and **DigestMethod** XML elements.</span></span> <span data-ttu-id="4bd63-106">DLLs de extensão podem dar suporte a algoritmos que codificam parâmetros adicionais na assinatura digital XML.</span><span class="sxs-lookup"><span data-stu-id="4bd63-106">Extension DLLs can support algorithms that encode additional parameters into the XML digital signature.</span></span>

<span data-ttu-id="4bd63-107">Todas as DLLs de extensões devem oferecer suporte à função [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface) , que retorna um ponteiro para uma estrutura de [**\_ \_ \_ interface criptográfica XML cript**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_cryptographic_interface) .</span><span class="sxs-lookup"><span data-stu-id="4bd63-107">All extensions DLLs must support the [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface) function, which returns a pointer to a [**CRYPT\_XML\_CRYPTOGRAPHIC\_INTERFACE**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_cryptographic_interface) structure.</span></span> <span data-ttu-id="4bd63-108">Essa estrutura fornece ponteiros de função para implementar funções de extensão criptográfica.</span><span class="sxs-lookup"><span data-stu-id="4bd63-108">This structure provides function pointers to implemented cryptographic extension functions.</span></span> <span data-ttu-id="4bd63-109">As funções com suporte dependem do tipo de algoritmo criptográfico com suporte e se o algoritmo deve codificar parâmetros na assinatura digital XML.</span><span class="sxs-lookup"><span data-stu-id="4bd63-109">The functions supported depend on the type of cryptographic algorithm supported and whether the algorithm must encode parameters into the XML digital signature.</span></span>

<span data-ttu-id="4bd63-110">As funções de extensões criptográficas incluem os seguintes ponteiros de função:</span><span class="sxs-lookup"><span data-stu-id="4bd63-110">Cryptographic extensions functions include the following function pointers:</span></span>

<dl> <dt>

<span data-ttu-id="4bd63-111"><span id="Required_functions"></span><span id="required_functions"></span><span id="REQUIRED_FUNCTIONS"></span>Funções necessárias</span><span class="sxs-lookup"><span data-stu-id="4bd63-111"><span id="Required_functions"></span><span id="required_functions"></span><span id="REQUIRED_FUNCTIONS"></span>Required functions</span></span>
</dt> <dd>

-   [<span data-ttu-id="4bd63-112">**CryptXmlDllGetInterface**</span><span class="sxs-lookup"><span data-stu-id="4bd63-112">**CryptXmlDllGetInterface**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface)
-   [<span data-ttu-id="4bd63-113">**CryptXmlDllGetAlgorithmInfo**</span><span class="sxs-lookup"><span data-stu-id="4bd63-113">**CryptXmlDllGetAlgorithmInfo**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetalgorithminfo)

</dd> <dt>

<span data-ttu-id="4bd63-114"><span id="Digest_Method_functions"></span><span id="digest_method_functions"></span><span id="DIGEST_METHOD_FUNCTIONS"></span>Funções de método Digest</span><span class="sxs-lookup"><span data-stu-id="4bd63-114"><span id="Digest_Method_functions"></span><span id="digest_method_functions"></span><span id="DIGEST_METHOD_FUNCTIONS"></span>Digest Method functions</span></span>
</dt> <dd>

-   [<span data-ttu-id="4bd63-115">**CryptXmlDllCloseDigest**</span><span class="sxs-lookup"><span data-stu-id="4bd63-115">**CryptXmlDllCloseDigest**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllclosedigest)
-   [<span data-ttu-id="4bd63-116">**CryptXmlDllCreateDigest**</span><span class="sxs-lookup"><span data-stu-id="4bd63-116">**CryptXmlDllCreateDigest**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest)
-   [<span data-ttu-id="4bd63-117">**CryptXmlDllDigestData**</span><span class="sxs-lookup"><span data-stu-id="4bd63-117">**CryptXmlDllDigestData**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldlldigestdata)
-   [<span data-ttu-id="4bd63-118">**CryptXmlDllFinalizeDigest**</span><span class="sxs-lookup"><span data-stu-id="4bd63-118">**CryptXmlDllFinalizeDigest**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllfinalizedigest)

</dd> <dt>

<span data-ttu-id="4bd63-119"><span id="Signature_Method_Functions"></span><span id="signature_method_functions"></span><span id="SIGNATURE_METHOD_FUNCTIONS"></span>Funções de método de assinatura</span><span class="sxs-lookup"><span data-stu-id="4bd63-119"><span id="Signature_Method_Functions"></span><span id="signature_method_functions"></span><span id="SIGNATURE_METHOD_FUNCTIONS"></span>Signature Method Functions</span></span>
</dt> <dd>

-   [<span data-ttu-id="4bd63-120">**CryptXmlDllSignData**</span><span class="sxs-lookup"><span data-stu-id="4bd63-120">**CryptXmlDllSignData**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllsigndata)
-   [<span data-ttu-id="4bd63-121">**CryptXmlDllVerifySignature**</span><span class="sxs-lookup"><span data-stu-id="4bd63-121">**CryptXmlDllVerifySignature**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllverifysignature)
-   [<span data-ttu-id="4bd63-122">**CryptXmlDllCreateKey**</span><span class="sxs-lookup"><span data-stu-id="4bd63-122">**CryptXmlDllCreateKey**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatekey)
-   [<span data-ttu-id="4bd63-123">**CryptXmlDllEncodeKeyValue**</span><span class="sxs-lookup"><span data-stu-id="4bd63-123">**CryptXmlDllEncodeKeyValue**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodekeyvalue)

</dd> <dt>

<span data-ttu-id="4bd63-124"><span id="For_algorithms_with_default_encoded_parameters"></span><span id="for_algorithms_with_default_encoded_parameters"></span><span id="FOR_ALGORITHMS_WITH_DEFAULT_ENCODED_PARAMETERS"></span>Para algoritmos com parâmetros codificados padrão</span><span class="sxs-lookup"><span data-stu-id="4bd63-124"><span id="For_algorithms_with_default_encoded_parameters"></span><span id="for_algorithms_with_default_encoded_parameters"></span><span id="FOR_ALGORITHMS_WITH_DEFAULT_ENCODED_PARAMETERS"></span>For algorithms with default encoded parameters</span></span>
</dt> <dd>

-   [<span data-ttu-id="4bd63-125">**CryptXmlDllEncodeAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="4bd63-125">**CryptXmlDllEncodeAlgorithm**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodealgorithm)

</dd> </dl>

<span data-ttu-id="4bd63-126">As DLLs de extensão criptográfica são registradas em todo o sistema.</span><span class="sxs-lookup"><span data-stu-id="4bd63-126">Cryptographic extension DLLs are registered on a system-wide basis.</span></span> <span data-ttu-id="4bd63-127">São necessários privilégios de administrador para registrar uma DLL de extensão criptográfica.</span><span class="sxs-lookup"><span data-stu-id="4bd63-127">Administrator privileges are required to register a cryptographic extension DLL.</span></span>

<span data-ttu-id="4bd63-128">Todas as extensões criptográficas CryptXML são registradas pelo valor de URI definido no campo **SignatureMethod** ou atributo de algoritmo do elemento **DigestMethod** .</span><span class="sxs-lookup"><span data-stu-id="4bd63-128">All CryptXML cryptographic extensions are registered by the URI value set in the **SignatureMethod** or the algorithm attribute field of the **DigestMethod** element.</span></span>

<span data-ttu-id="4bd63-129">Os caminhos de registro para as DLLs de extensão são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="4bd63-129">The registry paths for the extension DLLs are as follows:</span></span>

<dl> <dt>

<span data-ttu-id="4bd63-130"><span id="32-bit"></span><span id="32-BIT"></span>32 bits</span><span class="sxs-lookup"><span data-stu-id="4bd63-130"><span id="32-bit"></span><span id="32-BIT"></span>32-bit</span></span>
</dt> <dd>

<span data-ttu-id="4bd63-131">**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{URI}*</span><span class="sxs-lookup"><span data-stu-id="4bd63-131">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Cryptography**\\**CryptXML**\\**URI**\\ *{uri}*</span></span>

</dd> <dt>

<span data-ttu-id="4bd63-132"><span id="64-bit"></span><span id="64-BIT"></span>64 bits</span><span class="sxs-lookup"><span data-stu-id="4bd63-132"><span id="64-bit"></span><span id="64-BIT"></span>64-bit</span></span>
</dt> <dd>

<span data-ttu-id="4bd63-133">**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{URI}*</span><span class="sxs-lookup"><span data-stu-id="4bd63-133">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Cryptography**\\**CryptXML**\\**URI**\\ *{uri}*</span></span>

<span data-ttu-id="4bd63-134">**HKEY \_ \_Computador local** \\ **software** \\ **WOW6432NODE** \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{URI}*</span><span class="sxs-lookup"><span data-stu-id="4bd63-134">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**WOW6432NODE**\\**Microsoft**\\**Cryptography**\\**CryptXML**\\**URI**\\ *{uri}*</span></span>

</dd> </dl>

<span data-ttu-id="4bd63-135">Cada chave contém as configurações a seguir.</span><span class="sxs-lookup"><span data-stu-id="4bd63-135">Each key contains the following settings.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4bd63-136">Nome</span><span class="sxs-lookup"><span data-stu-id="4bd63-136">Name</span></span></th>
<th><span data-ttu-id="4bd63-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="4bd63-137">Type</span></span></th>
<th><span data-ttu-id="4bd63-138">Dados</span><span class="sxs-lookup"><span data-stu-id="4bd63-138">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4bd63-139">DLL</span><span class="sxs-lookup"><span data-stu-id="4bd63-139">DLL</span></span><br/></td>
<td><span data-ttu-id="4bd63-140">Cadeia de caracteres expansível</span><span class="sxs-lookup"><span data-stu-id="4bd63-140">Expandable string</span></span><br/></td>
<td><span data-ttu-id="4bd63-141">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="4bd63-141">Required.</span></span><br/><span data-ttu-id="4bd63-142">O caminho absoluto para a DLL do provedor criptográfico XML.</span><span class="sxs-lookup"><span data-stu-id="4bd63-142">The absolute path to the XML Cryptographic Provider DLL.</span></span>
<blockquote>
<p><span data-ttu-id="4bd63-143"><b>Observação: </b> Recomendamos que as DLLs de extensão criptográficas estejam localizadas em diretórios que só possam ser gravados por aplicativos com privilégio administrativo.</span><span class="sxs-lookup"><span data-stu-id="4bd63-143"><b>Note: </b>We recommend that cryptographic extension DLLs be located in directories that can only be written to by applications with administrative privilege.</span></span></p>
<p><span data-ttu-id="4bd63-144"><a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary</strong></a> é usado para carregar a DLL de extensão criptográfica.</span><span class="sxs-lookup"><span data-stu-id="4bd63-144"><a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary</strong></a> is used to load the cryptographic extension DLL.</span></span><br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4bd63-145">Nome</span><span class="sxs-lookup"><span data-stu-id="4bd63-145">Name</span></span><br/></td>
<td><span data-ttu-id="4bd63-146"><strong>Cadeia de caracteres</strong></span><span class="sxs-lookup"><span data-stu-id="4bd63-146"><strong>String</strong></span></span></td>
<td><span data-ttu-id="4bd63-147">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4bd63-147">Optional.</span></span><br/> <span data-ttu-id="4bd63-148">O nome de exibição associado a esse URI.</span><span class="sxs-lookup"><span data-stu-id="4bd63-148">The display name associated with this URI.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4bd63-149">GroupId</span><span class="sxs-lookup"><span data-stu-id="4bd63-149">GroupId</span></span><br/></td>
<td><span data-ttu-id="4bd63-150"><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="4bd63-150"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="4bd63-151">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="4bd63-151">Required.</span></span><br/> <span data-ttu-id="4bd63-152">O identificador de grupo associado a este algoritmo criptográfico.</span><span class="sxs-lookup"><span data-stu-id="4bd63-152">The group identifier associated with this cryptographic algorithm.</span></span> <span data-ttu-id="4bd63-153">Os valores possíveis incluem o seguinte:<strong>CRYPT_XML_GROUP_ID_HASH</strong> \ <strong></strong> = 1</span><span class="sxs-lookup"><span data-stu-id="4bd63-153">Possible values include the following:<strong>CRYPT_XML_GROUP_ID_HASH</strong>\<strong></strong> = 1</span></span><br/><span data-ttu-id="4bd63-154"><strong></strong> \ CRYPT_XML_GROUP_ID_SIGN <strong></strong> = 2</span><span class="sxs-lookup"><span data-stu-id="4bd63-154"><strong>CRYPT_XML_GROUP_ID_SIGN</strong>\<strong></strong> = 2</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4bd63-155">CNGAlgid</span><span class="sxs-lookup"><span data-stu-id="4bd63-155">CNGAlgid</span></span><br/></td>
<td><span data-ttu-id="4bd63-156"><strong>Cadeia de caracteres</strong></span><span class="sxs-lookup"><span data-stu-id="4bd63-156"><strong>String</strong></span></span></td>
<td><span data-ttu-id="4bd63-157">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="4bd63-157">Required.</span></span><br/> <span data-ttu-id="4bd63-158">O nome do algoritmo CNG a ser passado para as funções BCrypt ou NCrypt.</span><span class="sxs-lookup"><span data-stu-id="4bd63-158">The CNG algorithm name to be passed to BCrypt or NCrypt functions.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4bd63-159">CNGExtraAlgid</span><span class="sxs-lookup"><span data-stu-id="4bd63-159">CNGExtraAlgid</span></span><br/></td>
<td><span data-ttu-id="4bd63-160"><strong>Cadeia de caracteres</strong></span><span class="sxs-lookup"><span data-stu-id="4bd63-160"><strong>String</strong></span></span></td>
<td><span data-ttu-id="4bd63-161">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4bd63-161">Optional.</span></span><br/> <span data-ttu-id="4bd63-162">Uma cadeia de caracteres de algoritmo extra, diferente da cadeia de caracteres no membro CNGAlgid, que pode ser passada para as funções CNG.</span><span class="sxs-lookup"><span data-stu-id="4bd63-162">An extra algorithm string, other than the string in the CNGAlgid member, that can be passed to the CNG functions.</span></span><br/> <span data-ttu-id="4bd63-163">Para os algoritmos de assinatura (CRYPT_XML_GROUP_ID_SIGN), esse membro é a cadeia de caracteres de algoritmo de chave pública a ser passada para as funções CNG.</span><span class="sxs-lookup"><span data-stu-id="4bd63-163">For the signature algorithms (CRYPT_XML_GROUP_ID_SIGN), this member is the public key algorithm string to pass to the CNG functions.</span></span><br/> <span data-ttu-id="4bd63-164">Para os outros valores de GroupId, defina o membro <strong>pwszCNGExtraAlgid</strong> como a cadeia de caracteres vazia, L &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="4bd63-164">For the other values of GroupId, set the <strong>pwszCNGExtraAlgid</strong> member to the empty string, L&quot;&quot;.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="4bd63-165">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4bd63-165">Related topics</span></span>

<dl> <span data-ttu-id="4bd63-166"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="4bd63-166"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="4bd63-167">Algoritmos criptográficos de assinatura digital XML</span><span class="sxs-lookup"><span data-stu-id="4bd63-167">XML Digital Signature Cryptographic Algorithms</span></span>](xml-digital-signature-cryptographic-algorithms.md)
</dt> </dl>

 

 
