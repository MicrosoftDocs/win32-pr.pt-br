---
description: As interfaces a seguir podem ser usadas para gerenciar assinaturas de certificado e chaves públicas e privadas.
ms.assetid: 628d6629-3ec3-447e-8b60-a2db5b23e780
title: Assinatura de certificado e interfaces de chave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e35d2f3b1404397b1e6f2e436ef27fb740bbb594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829165"
---
# <a name="certificate-signature-and-key-interfaces"></a>Assinatura de certificado e interfaces de chave

As interfaces a seguir podem ser usadas para gerenciar assinaturas de certificado e chaves públicas e privadas.



| Interface                                                      | Descrição                                                                                       |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)               | Representa um certificado de assinatura que permite assinar uma solicitação de certificado.                  |
| [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates)             | Gerencia uma coleção de objetos [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) .                 |
| [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)                     | Representa uma chave privada assimétrica que pode ser usada para criptografia, assinatura e contrato de chave. |
| [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey)                       | Representa uma chave pública em um par de chaves pública/privada.                                             |
| [**IX509SignatureInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) | Representa informações usadas para assinar uma solicitação de certificado.                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interfaces CertEnroll](certenroll-interfaces.md)
</dt> </dl>

 

 



