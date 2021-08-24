---
description: Funções exportadas por Xenroll.dll que podem ser usadas para gerenciar um provedor criptográfico.
ms.assetid: 4f6f353d-6b06-45b4-8808-56998d3727a4
title: Funções do provedor de serviços de criptografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 947d9c4f2529071b28052ae5ca34f811d4657c3fd4cede23285999cbaa13a72c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883076"
---
# <a name="cryptographic-service-provider-functions"></a>Funções do provedor de serviços de criptografia

Cada uma das seções a seguir identifica uma função exportada por Xenroll.dll que pode ser usada para gerenciar um provedor criptográfico. Cada tópico também discute como usar CertEnroll.dll para substituir a função ou indica que não existe nenhum mapeamento entre as duas bibliotecas:

-   [EnumAlgs](#enumalgs)
-   [enumContainersWStr](#enumcontainerswstr)
-   [enumProvidersWStr](#enumproviderswstr)
-   [GetAlgNameWStr](#getalgnamewstr)
-   [getProviderTypeWStr](#getprovidertypewstr)
-   [HashAlgID](#hashalgid)
-   [HashAlgorithmWStr](#hashalgorithmwstr)
-   [ProviderFlags](#providerflags)
-   [ProviderNameWStr](#providernamewstr)
-   [ProviderType](#getprovidertypewstr)
-   [Tópicos relacionados](#related-topics)

## <a name="enumalgs"></a>EnumAlgs

A função [**EnumAlgs**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-enumalgs) no Xenroll.dll recupera uma coleção de algoritmos criptográficos.

Ao usar CertEnroll.dll, você pode executar as seguintes ações para recuperar informações sobre os algoritmos suportados por um CSP ( [*provedor de serviços de criptografia*](/windows/desktop/SecGloss/c-gly) ):

1.  Chame a propriedade [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) em um objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) existente.
2.  Chame o método [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) na solicitação retornada da etapa 1 para recuperar a solicitação mais interna.
3.  Chame **QueryInterface** no objeto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) retornado da etapa 2 para converter em um objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Chame a propriedade [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) na solicitação PKCS \# 10.
5.  Chame a propriedade [**CspInformations**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_cspinformations) no objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) recuperado da etapa 4.
6.  Chame a propriedade [**CspAlgorithms**](/windows/desktop/api/CertEnroll/nf-certenroll-icspinformation-get_cspalgorithms) em um objeto [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) específico na coleção [**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) recuperada na etapa 5.

## <a name="enumcontainerswstr"></a>enumContainersWStr

A função [**enumContainersWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-enumcontainerswstr) no Xenroll.dll recupera um contêiner de chave da coleção por índice.

A biblioteca de CertEnroll.dll não implementa essa funcionalidade diretamente.

## <a name="enumproviderswstr"></a>enumProvidersWStr

A função [**enumProvidersWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-enumproviderswstr) no Xenroll.dll recupera um CSP da coleção por índice.

Ao usar CertEnroll.dll, você pode executar as seguintes ações para recuperar a coleção de contêineres criptográficos:

1.  Chame a propriedade [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) em um objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) existente.
2.  Chame o método [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) na solicitação retornada da etapa 1 para recuperar a solicitação mais interna.
3.  Chame **QueryInterface** no objeto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) retornado da etapa 2 para converter em um objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Chame a propriedade [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) na solicitação PKCS \# 10.
5.  Chame a propriedade [**CspInformations**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_cspinformations) no objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) recuperado da etapa 4.

## <a name="getalgnamewstr"></a>GetAlgNameWStr

A função [**GetAlgNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getalgnamewstr) no Xenroll.dll recupera o nome de um [*algoritmo criptográfico*](/windows/desktop/SecGloss/c-gly).

Ao usar CertEnroll.dll, você pode executar as seguintes ações para recuperar o nome do algoritmo:

1.  Chame a propriedade [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) em um objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) existente.
2.  Chame o método [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) na solicitação retornada da etapa 1 para recuperar a solicitação mais interna.
3.  Chame **QueryInterface** no objeto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) retornado da etapa 2 para converter em um objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Chame a propriedade [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) na solicitação PKCS \# 10.
5.  Chame a propriedade [**Algorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_algorithm) no objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) para recuperar o identificador de objeto de algoritmo.
6.  Chame a propriedade [**FriendlyName**](/windows/desktop/api/CertEnroll/nf-certenroll-iobjectid-get_friendlyname) na interface [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) para recuperar o nome de exibição do algoritmo.

## <a name="getprovidertypewstr"></a>getProviderTypeWStr

A função [**getProviderTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getprovidertypewstr) no Xenroll.dll recupera o tipo de provedor criptográfico.

Ao usar CertEnroll.dll, você pode executar as seguintes ações para recuperar o tipo de provedor:

1.  Chame a propriedade [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) em um objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) existente.
2.  Chame o método [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) na solicitação retornada da etapa 1 para recuperar a solicitação mais interna.
3.  Chame **QueryInterface** no objeto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) retornado da etapa 2 para converter em um objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Chame a propriedade [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) na solicitação PKCS \# 10.
5.  Chame a propriedade [**ProviderType**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providertype) no objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) recuperado da etapa 4.

## <a name="hashalgid"></a>HashAlgID

A função [**HashAlgID**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_hashalgid) no Xenroll.dll recupera um valor inteiro que contém a ID do algoritmo usado para assinar uma solicitação.

Ao usar CertEnroll.dll, você pode executar as seguintes ações para recuperar o algoritmo de hash:

-   Recupere uma interface [**IX509SignatureInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) chamando a propriedade [**SignatureInformation**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_signatureinformation) em uma solicitação PKCS \# 10 ou CMC ou a propriedade [**SignerCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_signercertificate) em uma solicitação [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) .
-   Chame a propriedade [**HashAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509signatureinformation-get_hashalgorithm) no objeto de informações de assinatura para recuperar o identificador de objeto de algoritmo de hash.

## <a name="hashalgorithmwstr"></a>HashAlgorithmWStr

A função [**HashAlgorithmWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_hashalgorithmwstr) em Xenroll.dll especifica ou recupera um valor de cadeia de caracteres que identifica o algoritmo de hash usado para assinar uma solicitação.

Ao usar CertEnroll.dll, você pode executar as seguintes ações para recuperar o algoritmo de hash:

-   Recupere uma interface [**IX509SignatureInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) chamando a propriedade [**SignatureInformation**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_signatureinformation) em uma solicitação PKCS \# 10 ou CMC ou a propriedade [**SignerCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_signercertificate) em uma solicitação PKCS \# 7.
-   Chame a propriedade [**HashAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509signatureinformation-get_hashalgorithm) no objeto de informações de assinatura para recuperar o identificador de objeto de algoritmo de hash.
-   Chame a propriedade [**FriendlyName**](/windows/desktop/api/CertEnroll/nf-certenroll-iobjectid-get_friendlyname) na interface [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) retornada na etapa 2 para recuperar o nome de exibição do algoritmo.

## <a name="providerflags"></a>ProviderFlags

A função [**ProviderFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providerflags) em Xenroll.dll especifica ou recupera os sinalizadores usados ao adquirir um identificador para um CSP.

A biblioteca de CertEnroll.dll não mapeia essa função perfeitamente, mas você pode obter informações de propriedade sofisticadas do objeto de registro e da [*chave privada*](/windows/desktop/SecGloss/p-gly). Para obter mais informações, examine as propriedades expostas pelas interfaces [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) e [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) .

## <a name="providernamewstr"></a>ProviderNameWStr

A função [**ProviderNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providernamewstr) em Xenroll.dll especifica ou recupera o nome de um CSP.

Ao usar CertEnroll.dll, você pode executar as seguintes ações para recuperar o nome do provedor:

1.  Chame a propriedade [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) em um objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) existente.
2.  Chame o método [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) na solicitação retornada da etapa 1 para recuperar a solicitação mais interna.
3.  Chame **QueryInterface** no objeto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) retornado da etapa 2 para converter em um objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Chame a propriedade [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) na solicitação PKCS \# 10.
5.  Chame a propriedade [**ProviderName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providername) no objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) recuperado da etapa 4.

## <a name="providertype"></a>ProviderType

A função [**ProviderType**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providertype) em Xenroll.dll especifica ou recupera um valor inteiro que identifica o tipo do CSP.

Ao usar CertEnroll.dll, você pode executar as seguintes ações para recuperar o tipo de provedor:

1.  Chame a propriedade [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) em um objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) existente.
2.  Chame o método [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) na solicitação retornada da etapa 1 para recuperar a solicitação mais interna.
3.  Chame **QueryInterface** no objeto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) retornado da etapa 2 para converter em um objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Chame a propriedade [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) na solicitação PKCS \# 10.
5.  Chame a propriedade [**ProviderType**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providertype) no objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) recuperado da etapa 4.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mapeando Xenroll.dll para CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm)
</dt> <dt>

[**ICspAlgorithms**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithms)
</dt> <dt>

[**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation)
</dt> <dt>

[**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> <dt>

[**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)
</dt> </dl>

 

 
