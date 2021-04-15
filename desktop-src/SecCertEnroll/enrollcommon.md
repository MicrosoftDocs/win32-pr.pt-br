---
description: A pasta enrollCommon contém as seguintes funções auxiliares e macros usadas pelos exemplos fornecidos com o SDK de registro de certificado.
ms.assetid: a9b3532d-9640-4373-a6c6-7828cb6f55c7
title: enrollCommon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384a1f3741fd8bd7762c60da524e2e639c442e41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501971"
---
# <a name="enrollcommon"></a><span data-ttu-id="8bfec-103">enrollCommon</span><span class="sxs-lookup"><span data-stu-id="8bfec-103">enrollCommon</span></span>

<span data-ttu-id="8bfec-104">A pasta enrollCommon contém as seguintes funções auxiliares e macros usadas pelos exemplos fornecidos com o SDK de registro de certificado.</span><span class="sxs-lookup"><span data-stu-id="8bfec-104">The enrollCommon folder contains the following helper functions and macros used by the samples provided with the Certificate Enrollment SDK.</span></span> <span data-ttu-id="8bfec-105">Ele é instalado por padrão na pasta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ vc \\ enrollCommon.</span><span class="sxs-lookup"><span data-stu-id="8bfec-105">It is installed by default in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollCommon folder.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8bfec-106">Função</span><span class="sxs-lookup"><span data-stu-id="8bfec-106">Function</span></span></th>
<th><span data-ttu-id="8bfec-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8bfec-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8bfec-108">_JumpIfError</span><span class="sxs-lookup"><span data-stu-id="8bfec-108">_JumpIfError</span></span></td>
<td><span data-ttu-id="8bfec-109">Macro que aceita um valor <strong>HRESULT</strong> , um rótulo e uma cadeia de caracteres de erro, imprime a cadeia de caracteres e transfere o controle do programa para a primeira instrução após o rótulo.</span><span class="sxs-lookup"><span data-stu-id="8bfec-109">Macro that accepts an <strong>HRESULT</strong> value, a label, and an error string, prints the string, and transfers program control to the first statement following the label.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8bfec-110">_JumpError</span><span class="sxs-lookup"><span data-stu-id="8bfec-110">_JumpError</span></span></td>
<td><span data-ttu-id="8bfec-111">O mesmo que a macro _JumpIfError.</span><span class="sxs-lookup"><span data-stu-id="8bfec-111">Same as the _JumpIfError macro.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8bfec-112">_PrintIfError</span><span class="sxs-lookup"><span data-stu-id="8bfec-112">_PrintIfError</span></span></td>
<td><span data-ttu-id="8bfec-113">Não usado no momento.</span><span class="sxs-lookup"><span data-stu-id="8bfec-113">Not currently used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8bfec-114">_PrintError</span><span class="sxs-lookup"><span data-stu-id="8bfec-114">_PrintError</span></span></td>
<td><span data-ttu-id="8bfec-115">Macro que imprime uma mensagem de erro e um valor <strong>HRESULT</strong> .</span><span class="sxs-lookup"><span data-stu-id="8bfec-115">Macro that prints an error message and an <strong>HRESULT</strong> value.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8bfec-116">convertWszToSz</span><span class="sxs-lookup"><span data-stu-id="8bfec-116">convertWszToSz</span></span></td>
<td><span data-ttu-id="8bfec-117">Converte uma cadeia de caracteres largos em uma cadeia de caracteres ASCII usando a função <strong>WideCharToMultiByte</strong> e o identificador de página de código ANSI atual para o sistema.</span><span class="sxs-lookup"><span data-stu-id="8bfec-117">Converts a wide-character string to an ASCII character string by using the <strong>WideCharToMultiByte</strong> function and the current ANSI code-page identifier for the system.</span></span> <span data-ttu-id="8bfec-118">Essa função é usada pelas funções decConvertFromUnicode e findOIDFromTemplateName definidas em enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="8bfec-118">This function is used by the decConvertFromUnicode and findOIDFromTemplateName functions defined in enrollCommon.cpp.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8bfec-119">convertSzToWsz</span><span class="sxs-lookup"><span data-stu-id="8bfec-119">convertSzToWsz</span></span></td>
<td><span data-ttu-id="8bfec-120">Converte uma cadeia de caracteres ASCII em uma cadeia de caracteres largos usando a função <strong>MultiByteToWideChar</strong> e o identificador de página de código ANSI atual para o sistema.</span><span class="sxs-lookup"><span data-stu-id="8bfec-120">Converts an ASCII string to a wide-character string by using the <strong>MultiByteToWideChar</strong> function and the current ANSI code-page identifier for the system.</span></span> <span data-ttu-id="8bfec-121">Essa função é usada pela função findCertByTemplate definida em enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="8bfec-121">This function is used by the findCertByTemplate function defined in enrollCommon.cpp.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8bfec-122">convertSzToBstr</span><span class="sxs-lookup"><span data-stu-id="8bfec-122">convertSzToBstr</span></span></td>
<td><span data-ttu-id="8bfec-123">Converte uma cadeia de caracteres ASCII em um <strong>BSTR</strong> usando a função <strong>MultiByteToWideChar</strong> .</span><span class="sxs-lookup"><span data-stu-id="8bfec-123">Converts an ASCII string to a <strong>BSTR</strong> by using the <strong>MultiByteToWideChar</strong> function.</span></span> <span data-ttu-id="8bfec-124">Essa função não é usada no momento.</span><span class="sxs-lookup"><span data-stu-id="8bfec-124">This function is not currently used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8bfec-125">convertWszToBstr</span><span class="sxs-lookup"><span data-stu-id="8bfec-125">convertWszToBstr</span></span></td>
<td><span data-ttu-id="8bfec-126">Converte uma cadeia de caracteres largos em um <strong>BSTR</strong>.</span><span class="sxs-lookup"><span data-stu-id="8bfec-126">Converts a wide-character string to a <strong>BSTR</strong>.</span></span> <span data-ttu-id="8bfec-127">Essa função é usada pelo exemplo installResponseFromPFX.</span><span class="sxs-lookup"><span data-stu-id="8bfec-127">This function is used by the installResponseFromPFX sample.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8bfec-128">checkEnrollStatus</span><span class="sxs-lookup"><span data-stu-id="8bfec-128">checkEnrollStatus</span></span></td>
<td><span data-ttu-id="8bfec-129">Verifica o status do processo de registro de certificado usando as interfaces <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> e <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8bfec-129">Checks the status of the certificate enrollment process by using the <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> and <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus</strong></a> interfaces.</span></span> <span data-ttu-id="8bfec-130">Essa função é usada pelos exemplos enrollEOBOCMC, enrollPKCS7, enrollRenewalPKCS7, enrollSimpleMachineCert e enrollSimpleUserCert.</span><span class="sxs-lookup"><span data-stu-id="8bfec-130">This function is used by the enrollEOBOCMC, enrollPKCS7, enrollRenewalPKCS7, enrollSimpleMachineCert, and enrollSimpleUserCert samples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8bfec-131">findCertByKeyUsage</span><span class="sxs-lookup"><span data-stu-id="8bfec-131">findCertByKeyUsage</span></span></td>
<td><span data-ttu-id="8bfec-132">Enumera o repositório de certificados pessoal do usuário atual para localizar o primeiro certificado para o qual o uso pretendido da chave pública corresponde a um valor especificado.</span><span class="sxs-lookup"><span data-stu-id="8bfec-132">Enumerates the personal certificate store of the current user to find the first certificate for which the intended use of the public key matches a specified value.</span></span> <span data-ttu-id="8bfec-133">O valor especificado pode ser uma combinação de bits de bit abaixo dos seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="8bfec-133">The value specified can be a bitwise combination of the following flags:</span></span>
<ul>
<li><span data-ttu-id="8bfec-134">CERT_DATA_ENCIPHERMENT_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="8bfec-134">CERT_DATA_ENCIPHERMENT_KEY_USAGE</span></span></li>
<li><span data-ttu-id="8bfec-135">CERT_DIGITAL_SIGNATURE_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="8bfec-135">CERT_DIGITAL_SIGNATURE_KEY_USAGE</span></span></li>
<li><span data-ttu-id="8bfec-136">CERT_KEY_AGREEMENT_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="8bfec-136">CERT_KEY_AGREEMENT_KEY_USAGE</span></span></li>
<li><span data-ttu-id="8bfec-137">CERT_KEY_CERT_SIGN_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="8bfec-137">CERT_KEY_CERT_SIGN_KEY_USAGE</span></span></li>
<li><span data-ttu-id="8bfec-138">CERT_KEY_ENCIPHERMENT_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="8bfec-138">CERT_KEY_ENCIPHERMENT_KEY_USAGE</span></span></li>
<li><span data-ttu-id="8bfec-139">CERT_NON_REPUDIATION_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="8bfec-139">CERT_NON_REPUDIATION_KEY_USAGE</span></span></li>
<li><span data-ttu-id="8bfec-140">CERT_OFFLINE_CRL_SIGN_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="8bfec-140">CERT_OFFLINE_CRL_SIGN_KEY_USAGE</span></span></li>
</ul>
<span data-ttu-id="8bfec-141">Essa função é usada pelo exemplo enrollFromPublicKey.</span><span class="sxs-lookup"><span data-stu-id="8bfec-141">This function is used by the enrollFromPublicKey sample.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8bfec-142">findCertByEKU</span><span class="sxs-lookup"><span data-stu-id="8bfec-142">findCertByEKU</span></span></td>
<td><span data-ttu-id="8bfec-143">Enumera o repositório de certificados pessoal do usuário atual para localizar o primeiro certificado para o qual a extensão EKU (uso avançado de chave) corresponde à especificada na entrada.</span><span class="sxs-lookup"><span data-stu-id="8bfec-143">Enumerates the personal certificate store of the current user to find the first certificate for which the Enhanced Key Usage (EKU) extension matches that specified on input.</span></span> <span data-ttu-id="8bfec-144">Para obter mais informações sobre a extensão EKU, consulte a interface <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>IX509ExtensionEnhancedKeyUsage</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8bfec-144">For more information about the EKU extension, see the <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>IX509ExtensionEnhancedKeyUsage</strong></a> interface.</span></span> <span data-ttu-id="8bfec-145">Essa função é usada pelo exemplo enrollEOBOCMC.</span><span class="sxs-lookup"><span data-stu-id="8bfec-145">This function is used by the enrollEOBOCMC sample.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8bfec-146">findCertByTemplate</span><span class="sxs-lookup"><span data-stu-id="8bfec-146">findCertByTemplate</span></span></td>
<td><span data-ttu-id="8bfec-147">Enumera o repositório de certificados pessoal do usuário atual para localizar o primeiro certificado para o qual o modelo corresponde ao especificado, por nome, na entrada.</span><span class="sxs-lookup"><span data-stu-id="8bfec-147">Enumerates the personal certificate store of the current user to find the first certificate for which the template matches that specified, by name, on input.</span></span> <span data-ttu-id="8bfec-148">Essa função é usada pelos exemplos de enrollPKCS7 e enrollRenewalPKCS7.</span><span class="sxs-lookup"><span data-stu-id="8bfec-148">This function is used by the enrollPKCS7 and enrollRenewalPKCS7 samples.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8bfec-149">enrollCertByTemplate</span><span class="sxs-lookup"><span data-stu-id="8bfec-149">enrollCertByTemplate</span></span></td>
<td><span data-ttu-id="8bfec-150">Inicializa um objeto <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> usando um modelo, tenta registrar a solicitação de certificado criada implicitamente e monitora o status do processo de registro.</span><span class="sxs-lookup"><span data-stu-id="8bfec-150">Initializes an <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> object by using a template, attempts to enroll the implicitly created certificate request, and monitors the status of the enrollment process.</span></span> <span data-ttu-id="8bfec-151">Essa função é usada pelos exemplos enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 e enrollRenewalPKCS7.</span><span class="sxs-lookup"><span data-stu-id="8bfec-151">This function is used by the enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7, and enrollRenewalPKCS7 samples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8bfec-152">verifyCertContext</span><span class="sxs-lookup"><span data-stu-id="8bfec-152">verifyCertContext</span></span></td>
<td><span data-ttu-id="8bfec-153">Verifica a conformidade da cadeia de certificados com a política especificada (base) e, opcionalmente, em relação a uma extensão EKU (uso avançado de chave) especificado.</span><span class="sxs-lookup"><span data-stu-id="8bfec-153">Verifies compliance of the certificate chain against the specified (base) policy and, optionally, against a specified Enhanced Key Usage (EKU) extension.</span></span> <span data-ttu-id="8bfec-154">Para obter mais informações, consulte a função <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>CertVerifyCertificateChainPolicy</strong></a> e as estruturas <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>CERT_CHAIN_POLICY_PARA</strong></a> e <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8bfec-154">For more information, see the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>CertVerifyCertificateChainPolicy</strong></a> function and the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>CERT_CHAIN_POLICY_PARA</strong></a> and <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA</strong></a> structures.</span></span> <span data-ttu-id="8bfec-155">Essa função é usada pelos exemplos enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 e enrollRenewalPKCS7.</span><span class="sxs-lookup"><span data-stu-id="8bfec-155">This function is used by the enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7, and enrollRenewalPKCS7 samples.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8bfec-156">decConvertFromUnicode</span><span class="sxs-lookup"><span data-stu-id="8bfec-156">decConvertFromUnicode</span></span></td>
<td><span data-ttu-id="8bfec-157">Converte uma cadeia de caracteres Unicode de byte duplo em uma cadeia de caracteres ANSI de byte único.</span><span class="sxs-lookup"><span data-stu-id="8bfec-157">Converts a string of double-byte Unicode characters to a string of single-byte ANSI characters.</span></span> <span data-ttu-id="8bfec-158">Essa função é usada pela função DecodeFileW definida em enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="8bfec-158">This function is used by the DecodeFileW function defined in enrollCommon.cpp.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8bfec-159">DecodeFileW</span><span class="sxs-lookup"><span data-stu-id="8bfec-159">DecodeFileW</span></span></td>
<td><span data-ttu-id="8bfec-160">Decodifica um certificado codificado ou um arquivo de solicitação de certificado para uma matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="8bfec-160">Decodes an encoded certificate or certificate request file to a byte array.</span></span> <span data-ttu-id="8bfec-161">Essa função é usada pelo exemplo installResponseFromPFX.</span><span class="sxs-lookup"><span data-stu-id="8bfec-161">This function is used by the installResponseFromPFX sample.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8bfec-162">EncodeToFileW</span><span class="sxs-lookup"><span data-stu-id="8bfec-162">EncodeToFileW</span></span></td>
<td><span data-ttu-id="8bfec-163">Codifica uma solicitação de certificado ou certificado e a salva em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="8bfec-163">Encodes a certificate or certificate request and saves it to a file.</span></span> <span data-ttu-id="8bfec-164">Essa função é usada pelos exemplos createCNGCustomCMC, enrollEOBOCMC e enrollFromPublicKey.</span><span class="sxs-lookup"><span data-stu-id="8bfec-164">This function is used by the createCNGCustomCMC, enrollEOBOCMC, and enrollFromPublicKey samples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8bfec-165">findOIDFromTemplateName</span><span class="sxs-lookup"><span data-stu-id="8bfec-165">findOIDFromTemplateName</span></span></td>
<td><span data-ttu-id="8bfec-166">Recupera o identificador de objeto para um modelo especificado por nome.</span><span class="sxs-lookup"><span data-stu-id="8bfec-166">Retrieves the object identifier for a template specified by name.</span></span> <span data-ttu-id="8bfec-167">Essa função é usada pela função findCertByTemplate definida em enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="8bfec-167">This function is used by the findCertByTemplate function defined in enrollCommon.cpp.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="8bfec-168">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8bfec-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bfec-169">Usando os exemplos incluídos</span><span class="sxs-lookup"><span data-stu-id="8bfec-169">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

