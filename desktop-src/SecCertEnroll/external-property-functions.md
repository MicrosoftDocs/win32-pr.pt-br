---
description: As propriedades são usadas para associar um valor a um certificado.
ms.assetid: a6433416-fe77-4bb0-bd8e-9410a49ab861
title: Funções de propriedade externa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40196f4f42823ad44debeccc0fa85dc4615d58d1a0ccf521b2dd796e72574db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117779626"
---
# <a name="external-property-functions"></a>Funções de propriedade externa

As propriedades são usadas para associar um valor a um certificado. As propriedades nunca são enviadas ou processadas por uma [*autoridade de certificação*](/windows/desktop/SecGloss/c-gly) (CA) e não são armazenadas dentro de um certificado. Normalmente, eles são associados a um certificado depois que o certificado é recebido da CA e antes de ser salvo em um repositório. As propriedades são salvas no armazenamento junto com o certificado. CertEnroll.dll implementa a interface [**ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) e as seguintes interfaces derivadas de **ICertProperty**:

-   [**ICertPropertyArchived**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchived)
-   [**ICertPropertyArchivedKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchivedkeyhash)
-   [**ICertPropertyAutoEnroll**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyautoenroll)
-   [**ICertPropertyBackedUp**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertybackedup)
-   [**ICertPropertyDescription**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertydescription)
-   [**ICertPropertyEnrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyenrollment)
-   [**ICertPropertyFriendlyName**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyfriendlyname)
-   [**ICertPropertyKeyProvInfo**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertykeyprovinfo)
-   [**ICertPropertyRenewal**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrenewal)
-   [**ICertPropertyRequestOriginator**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrequestoriginator)
-   [**ICertPropertySHA1Hash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertysha1hash)

Cada uma das seções a seguir identifica uma função exportada pelo Xenroll.dll para gerenciar Propriedades de certificado externo. Cada seção também aborda como usar CertEnroll.dll para substituir a função ou indica que não existe nenhum mapeamento entre as duas bibliotecas:

-   [addBlobPropertyToCertificateWStr](#addblobpropertytocertificatewstr)
-   [GetPrivateKeyArchiveCertificate](#getprivatekeyarchivecertificate)
-   [resetBlobProperties](#resetblobproperties)
-   [SetPrivateKeyArchiveCertificate](#setprivatekeyarchivecertificate)
-   [SetSignerCertificate](#setsignercertificate)
-   [ThumbPrintWStr](#thumbprintwstr)
-   [Tópicos relacionados](#related-topics)

## <a name="addblobpropertytocertificatewstr"></a>addBlobPropertyToCertificateWStr

A função [**addBlobPropertyToCertificateWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addblobpropertytocertificatewstr) no Xenroll.dll adiciona uma propriedade ao certificado.

Em CertEnroll.dll, todos os objetos derivados de [**ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) implementam um método [**SetValueOnCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-icertproperty-setvalueoncertificate) que você pode usar para associar uma propriedade a um certificado. Além disso, o objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) implementa diretamente as propriedades [**CertificateFriendlyName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificatefriendlyname) e [**CertificateDescription**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificatedescription) .

## <a name="getprivatekeyarchivecertificate"></a>GetPrivateKeyArchiveCertificate

A função [**GetPrivateKeyArchiveCertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getprivatekeyarchivecertificate) no Xenroll.dll recupera o certificado do Exchange usado para arquivar uma [*chave privada*](/windows/desktop/SecGloss/p-gly).

Você pode usar o objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) em CertEnroll.dll para criar uma solicitação de uma autoridade de certificação para arquivar sua chave privada. Você deve recuperar um certificado do Exchange da AC e usar a [*chave pública*](/windows/desktop/SecGloss/p-gly) contida nesse certificado para criptografar a chave privada que você está enviando para arquivamento. Para especificar ou recuperar um certificado de troca de AC, chame a propriedade [**KeyArchivalCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_keyarchivalcertificate) nesse objeto.

## <a name="resetblobproperties"></a>resetBlobProperties

A função [**resetBlobProperties**](/windows/desktop/api/xenroll/nf-xenroll-icenroll4-resetblobproperties) no Xenroll.dll remove a coleção de propriedades do certificado.

Em CertEnroll.dll, todos os objetos de propriedade derivados de [**ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) implementam a propriedade [**RemoveFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-icertproperty-removefromcertificate) que você pode usar para desassociar uma propriedade de um certificado.

## <a name="setprivatekeyarchivecertificate"></a>SetPrivateKeyArchiveCertificate

A função [**SetPrivateKeyArchiveCertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setprivatekeyarchivecertificate) no Xenroll.dll especifica um certificado do Exchange usado para arquivar uma chave privada.

Você pode usar o objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) em CertEnroll.dll para criar uma solicitação de uma autoridade de certificação para arquivar sua chave privada. Você deve recuperar um certificado do Exchange da AC e usar a chave pública contida nesse certificado para criptografar a chave privada que você está enviando para arquivamento. Para especificar ou recuperar um certificado de troca de AC, chame a propriedade [**KeyArchivalCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_keyarchivalcertificate) nesse objeto.

## <a name="setsignercertificate"></a>SetSignerCertificate

A função [**SetSignerCertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setsignercertificate) no Xenroll.dll especifica um certificado de signatário.

O objeto [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) no CertEnroll.dll pode ser usado para assinar uma [*solicitação de certificado*](/windows/desktop/SecGloss/c-gly) [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly), CMC ou autoassinado. Você pode inicializar o objeto usando um certificado de autenticação existente e associá-lo a uma solicitação chamando uma das seguintes propriedades:

-   [**SignerCertificates**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_signercertificates) em [ **IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
-   [**SignerCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_signercertificate) em [ **IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
-   [**SignerCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcertificate-get_signercertificate) em [ **IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)

Além disso, se você inicializar uma solicitação CMC de uma solicitação interna e um modelo ou inicializar uma \# solicitação PKCS 7 de uma solicitação existente, o certificado de autenticação poderá ser definido.

## <a name="thumbprintwstr"></a>ThumbPrintWStr

A função [**ThumbPrintWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_thumbprintwstr) em Xenroll.dll especifica ou recupera o valor do hash de certificado.

No CertEnroll.dll, você pode usar o objeto [**ICertPropertySHA1Hash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertysha1hash) para recuperar um valor de [*hash*](/windows/desktop/SecGloss/h-gly) ([*impressão digital*](/windows/desktop/SecGloss/t-gly)) criado chamando o método [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mapeando Xenroll.dll para CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> </dl>

 

 
