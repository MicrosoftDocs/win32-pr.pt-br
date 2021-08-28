---
description: A pasta enrollCommon contém as seguintes funções auxiliares e macros usadas pelos exemplos fornecidos com o SDK de Registro de Certificado.
ms.assetid: a9b3532d-9640-4373-a6c6-7828cb6f55c7
title: enrollCommon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ddc05ad1a143de025abbc875c8280a3f419d0e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476012"
---
# <a name="enrollcommon"></a>enrollCommon

A pasta enrollCommon contém as seguintes funções auxiliares e macros usadas pelos exemplos fornecidos com o SDK de Registro de Certificado. Ele é instalado por padrão na pasta *%ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollCommon.




| Função | Descrição | 
|----------|-------------|
| _JumpIfError | Macro que aceita um valor <strong>HRESULT,</strong> um rótulo e uma cadeia de caracteres de erro, imprime a cadeia de caracteres e transfere o controle do programa para a primeira instrução após o rótulo. | 
| _JumpError | O mesmo que a _JumpIfError macro. | 
| _PrintIfError | Não usado no momento. | 
| _PrintError | Macro que imprime uma mensagem de erro e <strong>um valor HRESULT.</strong> | 
| convertWszToSz | Converte uma cadeia de caracteres largos em uma cadeia de caracteres ASCII usando a função <strong>WideCharToMultiByte</strong> e o identificador de página de código ANSI atual para o sistema. Essa função é usada pelas funções decConvertFromUnicode e findOIDFromTemplateName definidas em enrollCommon.cpp. | 
| convertSzToWsz | Converte uma cadeia de caracteres ASCII em uma cadeia de caracteres largos usando a função <strong>MultiByteToWideChar</strong> e o identificador de página de código ANSI atual para o sistema. Essa função é usada pela função findCertByTemplate definida em enrollCommon.cpp. | 
| convertSzToBstr | Converte uma cadeia de caracteres ASCII em um <strong>BSTR</strong> usando a <strong>função MultiByteToWideChar.</strong> Essa função não é usada no momento. | 
| convertWszToBstr | Converte uma cadeia de caracteres largos em um <strong>BSTR.</strong> Essa função é usada pelo exemplo installResponseFromPFX. | 
| checkEnrollStatus | Verifica o status do processo de registro de certificado usando as interfaces <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> e <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus.</strong></a> Essa função é usada pelos exemplos enrollEOBOCMC, enrollPKCS7, enrollRenewalPKCS7, enrollSimpleMachineCert e enrollSimpleUserCert. | 
| findCertByKeyUsage | Enumera o armazenamento de certificados pessoais do usuário atual para encontrar o primeiro certificado para o qual o uso pretendido da chave pública corresponde a um valor especificado. O valor especificado pode ser uma combinação bit a bit dos seguintes sinalizadores:<ul><li>CERT_DATA_ENCIPHERMENT_KEY_USAGE</li><li>CERT_DIGITAL_SIGNATURE_KEY_USAGE</li><li>CERT_KEY_AGREEMENT_KEY_USAGE</li><li>CERT_KEY_CERT_SIGN_KEY_USAGE</li><li>CERT_KEY_ENCIPHERMENT_KEY_USAGE</li><li>CERT_NON_REPUDIATION_KEY_USAGE</li><li>CERT_OFFLINE_CRL_SIGN_KEY_USAGE</li></ul>Essa função é usada pelo exemplo enrollFromPublicKey.<br /> | 
| findCertByEKU | Enumera o armazenamento de certificados pessoais do usuário atual para encontrar o primeiro certificado para o qual a extensão EKU (Uso Aprimorado de Chave) corresponde ao especificado na entrada. Para obter mais informações sobre a extensão de EKU, consulte a interface <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>IX509ExtensionEnhancedKeyUsage.</strong></a> Essa função é usada pelo exemplo enrollEOBOCMC. | 
| findCertByTemplate | Enumera o armazenamento de certificados pessoais do usuário atual para encontrar o primeiro certificado para o qual o modelo corresponde ao especificado, por nome, na entrada. Essa função é usada pelos exemplos enrollPKCS7 e enrollRenewalPKCS7. | 
| enrollCertByTemplate | Inicializa um objeto <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> usando um modelo, tenta registrar a solicitação de certificado criada implicitamente e monitora o status do processo de registro. Essa função é usada pelos exemplos enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 e enrollRenewalPKCS7. | 
| verifyCertContext | Verifica a conformidade da cadeia de certificados em relação à política (base) especificada e, opcionalmente, em relação a uma extensão EKU (Uso De Chave Aprimorado) especificada. Para obter mais informações, consulte <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>a função CertVerifyCertificateChainPolicy</strong></a> e as <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>estruturas CERT_CHAIN_POLICY_PARA</strong></a> e <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA</strong></a> dados. Essa função é usada pelos exemplos enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 e enrollRenewalPKCS7. | 
| decConvertFromUnicode | Converte uma cadeia de caracteres Unicode de byte duplo em uma cadeia de caracteres ANSI de byte único. Essa função é usada pela função DecodeFileW definida em enrollCommon.cpp. | 
| DecodeFileW | Decodifica um certificado codificado ou um arquivo de solicitação de certificado para uma matriz de byte. Essa função é usada pelo exemplo installResponseFromPFX. | 
| EncodeToFileW | Codifica uma solicitação de certificado ou certificado e salva-a em um arquivo. Essa função é usada pelos exemplos createCNGCustomCMC, enrollEOBOCMC e enrollFromPublicKey. | 
| findOIDFromTemplateName | Recupera o identificador de objeto para um modelo especificado pelo nome. Essa função é usada pela função findCertByTemplate definida em enrollCommon.cpp. | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando os exemplos incluídos](using-the-included-samples.md)
</dt> </dl>

 

