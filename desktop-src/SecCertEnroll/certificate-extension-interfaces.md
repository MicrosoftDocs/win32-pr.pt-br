---
description: As interfaces a seguir podem ser usadas para criar extensões de certificado.
ms.assetid: 52750a0a-0cd9-40cc-8c23-839e4e20fd77
title: Interfaces de extensão de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c192ff7bc661c36ded8611628a1cd82dddca1697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501749"
---
# <a name="certificate-extension-interfaces"></a>Interfaces de extensão de certificado

As interfaces a seguir podem ser usadas para criar extensões de certificado.



| Interface                                                                            | Descrição                                                                                                                                    |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename)                                         | Representa uma instância de uma extensão **alternativonames** .                                                                                   |
| [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames)                                       | Gerencia uma coleção de objetos [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) .                                                                  |
| [**ICertificatePolicy**](/windows/desktop/api/CertEnroll/nn-certenroll-icertificatepolicy)                                     | Especifica uma política de certificado que identifica a finalidade para a qual o certificado pode ser usado.                                              |
| [**ICertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-icertificatepolicies)                                 | Gerencia uma coleção de objetos [**ICertificatePolicy**](/windows/desktop/api/CertEnroll/nn-certenroll-icertificatepolicy) .                                                              |
| [**IPolicyQualifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ipolicyqualifier)                                         | Representa um qualificador que pode ser associado a uma política de certificado.                                                                       |
| [**IPolicyQualifiers**](/windows/desktop/api/CertEnroll/nn-certenroll-ipolicyqualifiers)                                       | Gerencia uma coleção de objetos [**IPolicyQualifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ipolicyqualifier) .                                                                  |
| [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)                                             | Define uma extensão para uma solicitação de certificado.                                                                                                |
| [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)             | Especifica um ou mais formulários de nome alternativo para o assunto de um certificado.                                                                 |
| [**IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier) | Representa uma extensão **AuthorityKeyIdentifier** .                                                                                            |
| [**IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)             | Especifica se a entidade do certificado é uma autoridade de certificação e, nesse caso, a profundidade da cadeia de autoridade de certificação subordinada. |
| [**IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)       | Representa uma coleção de termos de informações de política.                                                                                           |
| [**IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)   | Representa uma coleção de identificadores de objeto que indicam como um certificado pode ser usado por um aplicativo.                                   |
| [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)             | Representa uma coleção de identificadores de objeto que identificam os usos pretendidos da chave pública contida em um certificado.                    |
| [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)                             | Representa restrições nas operações que podem ser executadas pela chave pública contida no certificado.                                |
| [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)                                           | Gerencia uma coleção de objetos [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) .                                                                      |
| [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)           | Representa uma coleção que relata os recursos de descriptografia de um destinatário de email para um remetente de email.                                     |
| [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)     | Representa uma extensão **SubjectKeyIdentifier** usada para identificar um certificado de autenticação.                                                        |
| [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)                             | Representa uma extensão **certificatetemplate** que contém um modelo versão 2.                                                             |
| [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)                     | Representa uma extensão **CertificateTemplateName** que contém um modelo de versão 1.                                                         |
| [**ISmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ismimecapabilities)                                     | Gerencia uma coleção de objetos [**ISmimeCapability**](/windows/desktop/api/CertEnroll/nn-certenroll-ismimecapability) .                                                                  |
| [**ISmimeCapability**](/windows/desktop/api/CertEnroll/nn-certenroll-ismimecapability)                                         | Representa uma extensão **SMIMECapabilities** que identifica os recursos de descriptografia de um destinatário de email.                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interfaces CertEnroll](certenroll-interfaces.md)
</dt> </dl>

 

 



