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
# <a name="enrollcommon"></a>enrollCommon

A pasta enrollCommon contém as seguintes funções auxiliares e macros usadas pelos exemplos fornecidos com o SDK de registro de certificado. Ele é instalado por padrão na pasta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ vc \\ enrollCommon.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Função</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>_JumpIfError</td>
<td>Macro que aceita um valor <strong>HRESULT</strong> , um rótulo e uma cadeia de caracteres de erro, imprime a cadeia de caracteres e transfere o controle do programa para a primeira instrução após o rótulo.</td>
</tr>
<tr class="even">
<td>_JumpError</td>
<td>O mesmo que a macro _JumpIfError.</td>
</tr>
<tr class="odd">
<td>_PrintIfError</td>
<td>Não usado no momento.</td>
</tr>
<tr class="even">
<td>_PrintError</td>
<td>Macro que imprime uma mensagem de erro e um valor <strong>HRESULT</strong> .</td>
</tr>
<tr class="odd">
<td>convertWszToSz</td>
<td>Converte uma cadeia de caracteres largos em uma cadeia de caracteres ASCII usando a função <strong>WideCharToMultiByte</strong> e o identificador de página de código ANSI atual para o sistema. Essa função é usada pelas funções decConvertFromUnicode e findOIDFromTemplateName definidas em enrollCommon. cpp.</td>
</tr>
<tr class="even">
<td>convertSzToWsz</td>
<td>Converte uma cadeia de caracteres ASCII em uma cadeia de caracteres largos usando a função <strong>MultiByteToWideChar</strong> e o identificador de página de código ANSI atual para o sistema. Essa função é usada pela função findCertByTemplate definida em enrollCommon. cpp.</td>
</tr>
<tr class="odd">
<td>convertSzToBstr</td>
<td>Converte uma cadeia de caracteres ASCII em um <strong>BSTR</strong> usando a função <strong>MultiByteToWideChar</strong> . Essa função não é usada no momento.</td>
</tr>
<tr class="even">
<td>convertWszToBstr</td>
<td>Converte uma cadeia de caracteres largos em um <strong>BSTR</strong>. Essa função é usada pelo exemplo installResponseFromPFX.</td>
</tr>
<tr class="odd">
<td>checkEnrollStatus</td>
<td>Verifica o status do processo de registro de certificado usando as interfaces <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> e <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus</strong></a> . Essa função é usada pelos exemplos enrollEOBOCMC, enrollPKCS7, enrollRenewalPKCS7, enrollSimpleMachineCert e enrollSimpleUserCert.</td>
</tr>
<tr class="even">
<td>findCertByKeyUsage</td>
<td>Enumera o repositório de certificados pessoal do usuário atual para localizar o primeiro certificado para o qual o uso pretendido da chave pública corresponde a um valor especificado. O valor especificado pode ser uma combinação de bits de bit abaixo dos seguintes sinalizadores:
<ul>
<li>CERT_DATA_ENCIPHERMENT_KEY_USAGE</li>
<li>CERT_DIGITAL_SIGNATURE_KEY_USAGE</li>
<li>CERT_KEY_AGREEMENT_KEY_USAGE</li>
<li>CERT_KEY_CERT_SIGN_KEY_USAGE</li>
<li>CERT_KEY_ENCIPHERMENT_KEY_USAGE</li>
<li>CERT_NON_REPUDIATION_KEY_USAGE</li>
<li>CERT_OFFLINE_CRL_SIGN_KEY_USAGE</li>
</ul>
Essa função é usada pelo exemplo enrollFromPublicKey.<br/></td>
</tr>
<tr class="odd">
<td>findCertByEKU</td>
<td>Enumera o repositório de certificados pessoal do usuário atual para localizar o primeiro certificado para o qual a extensão EKU (uso avançado de chave) corresponde à especificada na entrada. Para obter mais informações sobre a extensão EKU, consulte a interface <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>IX509ExtensionEnhancedKeyUsage</strong></a> . Essa função é usada pelo exemplo enrollEOBOCMC.</td>
</tr>
<tr class="even">
<td>findCertByTemplate</td>
<td>Enumera o repositório de certificados pessoal do usuário atual para localizar o primeiro certificado para o qual o modelo corresponde ao especificado, por nome, na entrada. Essa função é usada pelos exemplos de enrollPKCS7 e enrollRenewalPKCS7.</td>
</tr>
<tr class="odd">
<td>enrollCertByTemplate</td>
<td>Inicializa um objeto <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> usando um modelo, tenta registrar a solicitação de certificado criada implicitamente e monitora o status do processo de registro. Essa função é usada pelos exemplos enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 e enrollRenewalPKCS7.</td>
</tr>
<tr class="even">
<td>verifyCertContext</td>
<td>Verifica a conformidade da cadeia de certificados com a política especificada (base) e, opcionalmente, em relação a uma extensão EKU (uso avançado de chave) especificado. Para obter mais informações, consulte a função <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>CertVerifyCertificateChainPolicy</strong></a> e as estruturas <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>CERT_CHAIN_POLICY_PARA</strong></a> e <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA</strong></a> . Essa função é usada pelos exemplos enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 e enrollRenewalPKCS7.</td>
</tr>
<tr class="odd">
<td>decConvertFromUnicode</td>
<td>Converte uma cadeia de caracteres Unicode de byte duplo em uma cadeia de caracteres ANSI de byte único. Essa função é usada pela função DecodeFileW definida em enrollCommon. cpp.</td>
</tr>
<tr class="even">
<td>DecodeFileW</td>
<td>Decodifica um certificado codificado ou um arquivo de solicitação de certificado para uma matriz de bytes. Essa função é usada pelo exemplo installResponseFromPFX.</td>
</tr>
<tr class="odd">
<td>EncodeToFileW</td>
<td>Codifica uma solicitação de certificado ou certificado e a salva em um arquivo. Essa função é usada pelos exemplos createCNGCustomCMC, enrollEOBOCMC e enrollFromPublicKey.</td>
</tr>
<tr class="even">
<td>findOIDFromTemplateName</td>
<td>Recupera o identificador de objeto para um modelo especificado por nome. Essa função é usada pela função findCertByTemplate definida em enrollCommon. cpp.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando os exemplos incluídos](using-the-included-samples.md)
</dt> </dl>

 

