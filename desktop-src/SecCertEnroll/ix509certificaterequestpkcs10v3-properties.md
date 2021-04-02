---
description: A interface IX509CertificateRequestPkcs10V3 expõe as propriedades a seguir.
ms.assetid: 96FCB9C4-7DDB-4B6B-A776-5A33E07B0BD3
title: Propriedades de IX509CertificateRequestPkcs10V3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db4967b10e49ed015b22ffcab19726f5662937d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922735"
---
# <a name="ix509certificaterequestpkcs10v3-properties"></a>Propriedades de IX509CertificateRequestPkcs10V3

A interface [**IX509CertificateRequestPkcs10V3**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v3) expõe as propriedades a seguir.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                                            | Descrição                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Propriedade AttestationEncryptionCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestationencryptioncertificate)<br/> | O certificado usado para criptografar os valores de EKPUB e EKCERT do cliente. Essa propriedade deve ser definida como um certificado válido que se encadeia a uma raiz de máquina confiável.<br/>                                                                                                                                                                                |
| [**Propriedade AttestPrivateKey**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestprivatekey)<br/>                                 | True se a chave privada criada precisar ser atestada; caso contrário, false. Se for true, espera-se que a propriedade [**AttestationEncryptionCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestationencryptioncertificate) tenha sido definida. <br/>                                                                                                        |
| [**Propriedade ChallengePassword**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_challengepassword)<br/>                               | A senha a ser usada ao criar uma solicitação com um desafio. Para criar uma solicitação sem um desafio, não defina a propriedade [**ChallengePassword**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_challengepassword) .<br/>                                                                                                                                      |
| [**Propriedade EncryptionAlgorithm**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionalgorithm)<br/>                           | O algoritmo de criptografia usado para criptografar os valores de EKPUB e EKCERT do cliente.<br/>                                                                                                                                                                                                                                                               |
| [**Propriedade EncryptionStrength**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionstrength)<br/>                             | Identifica o comprimento de bits para o [**EncryptionAlgorithm**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionalgorithm) usar para criptografia. Se o **EncryptionAlgorithm** der suporte apenas a um comprimento de bit, você não precisará especificar um valor para a propriedade [**EncryptionStrength**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionstrength) .<br/> |
| [**Propriedade NameValuePairs**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_namevaluepairs)<br/>                                     | Uma coleção de pares de nome/valor de valores de propriedade de certificado adicionais.<br/>                                                                                                                                                                                                                                                                         |



 

 

 




