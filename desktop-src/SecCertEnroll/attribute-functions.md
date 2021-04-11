---
description: Os atributos podem ser adicionados a uma solicitação de certificado para fornecer uma autoridade de certificação (CA) com informações adicionais que podem ser usadas ao criar e emitir um certificado.
ms.assetid: 3eba5a2f-eeac-4e38-8705-b12bc183b7eb
title: Funções de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6413da0d43c142373e6f3cabe3d8e31636b82ef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169361"
---
# <a name="attribute-functions"></a>Funções de atributo

Os atributos podem ser adicionados a uma solicitação de certificado para fornecer uma [*autoridade de certificação*](/windows/desktop/SecGloss/c-gly) (CA) com informações adicionais que podem ser usadas ao criar e emitir um certificado.

CertEnroll.dll implementa as seguintes interfaces para definir atributos e coleções de atributos:

-   [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
-   [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
-   [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
-   [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
-   [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)
-   [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)
-   [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)
-   [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)
-   [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)
-   [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)
-   [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate)

As seções a seguir identificam as funções exportadas por Xenroll.dll para associar atributos criptográficos a solicitações de certificado e discutir como usar CertEnroll.dll para substituir a função ou indicar que não existe mapeamento entre as duas bibliotecas:

-   [addAttributeToRequestWStr](#addattributetorequestwstr)
-   [AddAuthenticatedAttributesToPKCS7Request](#addauthenticatedattributestopkcs7request)
-   [addNameValuePairToRequestWStr](#addnamevaluepairtorequestwstr)
-   [AddNameValuePairToSignatureWStr](#addnamevaluepairtosignaturewstr)
-   [ClientId](#clientid)
-   [RenewalCertificate](#renewalcertificate)
-   [redefinirattributes](#resetattributes)
-   [Tópicos relacionados](#related-topics)

## <a name="addattributetorequestwstr"></a>addAttributeToRequestWStr

A função [**addAttributeToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) no Xenroll.dll adiciona um atributo a uma solicitação de certificado.

Em geral, para adicionar um atributo a uma solicitação usando os objetos implementados no CertEnroll.dll, você pode executar as seguintes ações:

1.  Crie um objeto de coleção [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) .
2.  Crie um objeto [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) e chame o método [**Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attribute-initialize) para criar um atributo a partir de um identificador de objeto e um valor de atributo ou use qualquer uma das interfaces listadas anteriormente para definir um dos atributos mais comuns.
3.  Adicione cada novo atributo criado na etapa anterior à coleção [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) usando o método [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-add) .
4.  Crie um objeto [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) e inicialize-o chamando o método [**InitializeFromValues**](/windows/desktop/api/CertEnroll/nf-certenroll-icryptattribute-initializefromvalues) e especificando a coleção [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) na entrada.
5.  Recupere um objeto de coleção [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) chamando a propriedade [**cript**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes) . de um objeto de solicitação [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) ou [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) existente.
6.  Adicione o objeto [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) à coleção [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) .

## <a name="addauthenticatedattributestopkcs7request"></a>AddAuthenticatedAttributesToPKCS7Request

Os atributos autenticados são pares de nome-valor que são assinados e adicionados a uma assinatura. A função [**AddAuthenticatedAttributesToPKCS7Request**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addauthenticatedattributestopkcs7request) no Xenroll.dll adiciona uma matriz de atributos autenticados a uma solicitação [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) .

Conforme discutido acima para a função [**addAttributeToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) , você pode usar CertEnroll.dll para definir e adicionar facilmente uma coleção de atributos a uma solicitação de certificado. No entanto, você não pode escolher se o atributo é autenticado. O processo de registro toma essa decisão automaticamente.

## <a name="addnamevaluepairtorequestwstr"></a>addNameValuePairToRequestWStr

A função [**addNameValuePairToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addnamevaluepairtorequestwstr) no Xenroll.dll adiciona um par de nome-valor não autenticado a uma solicitação.

Você pode usar a interface [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) em CertEnroll.dll para definir um par de nome-valor e pode adicionar uma coleção de pares de nome-valor a um objeto de solicitação CMC executando as seguintes ações:

1.  Crie e inicialize um objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) . O processo de inicialização cria uma coleção [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) vazia.
2.  Chame a propriedade [**NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) em um objeto de solicitação CMC existente para recuperar a coleção.
3.  Crie e inicialize um objeto [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) .
4.  Adicione cada novo par nome-valor à coleção [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) chamando o método [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509namevaluepairs-add) .

O processo de registro coloca a coleção de pares nome-valor na estrutura **taggedattribute** da solicitação CMC.

## <a name="addnamevaluepairtosignaturewstr"></a>AddNameValuePairToSignatureWStr

A função [**AddNameValuePairToSignatureWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addnamevaluepairtosignaturewstr) no Xenroll.dll adiciona um par nome-valor autenticado a uma solicitação. Normalmente, isso é usado para especificar o nome do solicitante em uma solicitação de registro em nome de (EOBO).

Em CertEnroll.dll, use a propriedade [**RequesterName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_requestername) para especificar o nome em uma solicitação EOBO.

## <a name="clientid"></a>ClientId

A função [**ClientID**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_clientid) no Xenroll.dll especifica ou recupera um atributo **ClientID** .

Use a propriedade [**ClientID**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_clientid) em CertEnroll.dll para adicionar esse atributo a uma solicitação CMC ou PKCS \# 10.

## <a name="renewalcertificate"></a>RenewalCertificate

A função [**RenewalCertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_renewalcertificate) em Xenroll.dll especifica ou recupera um atributo **RenewalCertificate** .

No CertEnroll.dll, quando você chama [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) em um \# objeto PKCS 7 ou Pkcs) é criado automaticamente.

## <a name="resetattributes"></a>redefinirattributes

A função [**resetattributes**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-resetattributes) no Xenroll.dll remove a coleção de atributos de uma solicitação.

Para remover um atributo de uma solicitação por índice usando CertEnroll.dll, chame o método [**Remove**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-remove) na coleção [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) . Para remover todos os atributos de uma solicitação, chame o método [**Clear**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-clear) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mapeando Xenroll.dll para CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
</dt> <dt>

[**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
</dt> <dt>

[**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
</dt> <dt>

[**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)
</dt> <dt>

[**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs)
</dt> </dl>

 

 
