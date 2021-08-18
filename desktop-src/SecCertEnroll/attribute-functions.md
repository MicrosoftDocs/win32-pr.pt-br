---
description: Atributos podem ser adicionados a uma solicitação de certificado para fornecer uma AC (autoridade de certificação) com informações adicionais que podem ser usadas ao criar e emissão de um certificado.
ms.assetid: 3eba5a2f-eeac-4e38-8705-b12bc183b7eb
title: Funções de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a353b5beb5b7da048edf8712c5d82545fd326a7d1720748705ae093aaa2cc44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903108"
---
# <a name="attribute-functions"></a>Funções de atributo

Atributos podem ser adicionados a uma solicitação de certificado para fornecer uma AC [*(autoridade*](/windows/desktop/SecGloss/c-gly) de certificação) com informações adicionais que podem ser usadas ao criar e emissão de um certificado.

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

As seções a seguir identificam as funções exportadas pelo Xenroll.dll para associar atributos criptográficos a solicitações de certificado e discutir como usar o CertEnroll.dll para substituir a função ou indicar que não existe nenhum mapeamento entre as duas bibliotecas:

-   [addAttributeToRequestWStr](#addattributetorequestwstr)
-   [AddAuthenticatedAttributesToPKCS7Request](#addauthenticatedattributestopkcs7request)
-   [addNameValuePairToRequestWStr](#addnamevaluepairtorequestwstr)
-   [AddNameValuePairToSignatureWStr](#addnamevaluepairtosignaturewstr)
-   [Clientid](#clientid)
-   [RenewalCertificate](#renewalcertificate)
-   [resetAttributes](#resetattributes)
-   [Tópicos relacionados](#related-topics)

## <a name="addattributetorequestwstr"></a>addAttributeToRequestWStr

A [**função addAttributeToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) no Xenroll.dll adiciona um atributo a uma solicitação de certificado.

Em geral, para adicionar um atributo a uma solicitação usando os objetos implementados no CertEnroll.dll, você pode executar as seguintes ações:

1.  Crie um [**objeto de coleção IX509Attributes.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
2.  Crie um [**objeto IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) e chame o método [**Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attribute-initialize) para criar um atributo de um valor de atributo e identificador de objeto ou use qualquer uma das interfaces listadas anteriormente para definir um dos atributos mais comuns.
3.  Adicione cada novo atributo criado na etapa anterior à [**coleção IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) usando o [**método**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-add) Add.
4.  Crie um [**objeto ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) e inicialize-o chamando o método [**InitializeFromValues**](/windows/desktop/api/CertEnroll/nf-certenroll-icryptattribute-initializefromvalues) e especificando a coleção [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) na entrada.
5.  Recupere um objeto de coleção [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) chamando a propriedade [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes) em um objeto de solicitação [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) ou [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) existente.
6.  Adicione o [**objeto ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) à [**coleção ICryptAttributes.**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)

## <a name="addauthenticatedattributestopkcs7request"></a>AddAuthenticatedAttributesToPKCS7Request

Atributos autenticados são pares nome-valor que são assinados por e adicionados a uma assinatura. A [**função AddAuthenticatedAttributesToPKCS7Request**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addauthenticatedattributestopkcs7request) no Xenroll.dll adiciona uma matriz de atributos autenticados a uma [*solicitação PKCS \# 7.*](/windows/desktop/SecGloss/p-gly)

Conforme discutido acima para a função [**addAttributeToRequestWStr,**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) você pode usar CertEnroll.dll para definir e adicionar facilmente uma coleção de atributos a uma solicitação de certificado. No entanto, não é possível escolher se o atributo é autenticado. O processo de registro toma essa decisão automaticamente.

## <a name="addnamevaluepairtorequestwstr"></a>addNameValuePairToRequestWStr

A [**função addNameValuePairToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addnamevaluepairtorequestwstr) no Xenroll.dll adiciona um par nome-valor não autenticado a uma solicitação.

Você pode usar a interface [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) no CertEnroll.dll para definir um par nome-valor e adicionar uma coleção de pares nome-valor a um objeto de solicitação do CMC executando as seguintes ações:

1.  Crie e inicialize um [**objeto IX509CertificateRequestCmc.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) O processo de inicialização cria uma [**coleção IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) vazia.
2.  Chame a [**propriedade NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) em um objeto de solicitação do CMC existente para recuperar a coleção.
3.  Crie e inicialize um [**objeto IX509NameValuePair.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)
4.  Adicione cada novo par nome-valor à [**coleção IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) chamando o [**método**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509namevaluepairs-add) Add.

O processo de registro coloca a coleção de pares nome-valor na estrutura **TaggedAttribute** da solicitação do CMC.

## <a name="addnamevaluepairtosignaturewstr"></a>AddNameValuePairToSignatureWStr

A [**função AddNameValuePairToSignatureWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addnamevaluepairtosignaturewstr) no Xenroll.dll adiciona um par nome-valor autenticado a uma solicitação. Normalmente, isso é usado para especificar o nome do solicitante em uma solicitação EOBO (registro em nome de).

No CertEnroll.dll, use a propriedade [**RequesterName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_requestername) para especificar o nome em uma solicitação EOBO.

## <a name="clientid"></a>ClientId

A [**função ClientId**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_clientid) no Xenroll.dll especifica ou recupera um **atributo ClientId.**

Use a [**propriedade ClientId**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_clientid) no CertEnroll.dll para adicionar esse atributo a uma solicitação CMC ou PKCS \# 10.

## <a name="renewalcertificate"></a>RenewalCertificate

A [**função RenewalCertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_renewalcertificate) Xenroll.dll especifica ou recupera um **atributo RenewalCertificate.**

No CertEnroll.dll, quando você chama [**InitializeFromCertificate em**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) um objeto PKCS 7 ou \# PKCS ) é criado automaticamente.

## <a name="resetattributes"></a>resetAttributes

A [**função resetAttributes**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-resetattributes) no Xenroll.dll remove a coleção de atributos de uma solicitação.

Para remover um atributo de uma solicitação por índice usando CertEnroll.dll, chame o [**método Remove**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-remove) na [**coleção IX509Attributes.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) Para remover todos os atributos de uma solicitação, chame o [**método Clear.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-clear)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mapeamento Xenroll.dll para CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
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

 

 
