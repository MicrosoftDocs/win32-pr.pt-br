---
description: Implementa as interfaces IX509PrivateKey e IX509PublicKey.
ms.assetid: 1358053e-ed4e-4482-b160-5b9b1024c771
title: Funções de chave pública e privada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c1d8ec481c87337e7d7e56cffee47f1f483b84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784156"
---
# <a name="private-and-public-key-functions"></a>Funções de chave pública e privada

CertEnroll.dll implementa as interfaces [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) e [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey) . Você pode, por exemplo, usar a interface [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) para executar as seguintes ações em uma [*chave privada*](/windows/desktop/SecGloss/p-gly):

-   Criar, abrir, fechar, importar, exportar e excluir a chave.
-   Especifique ou recupere o [*algoritmo de chave pública*](/windows/desktop/SecGloss/p-gly).
-   Especifique ou recupere informações sobre o CSP ( [*provedor de serviços de criptografia*](/windows/desktop/SecGloss/c-gly) ) disponível que oferece suporte ao algoritmo de chave pública.
-   Especifique ou recupere o [*certificado*](/windows/desktop/SecGloss/c-gly) associado à [*chave privada*](/windows/desktop/SecGloss/p-gly).
-   Especifique ou recupere o nome do [*contêiner de chave*](/windows/desktop/SecGloss/k-gly).
-   Especifique ou recupere uma descrição de e um nome de exibição para a chave.
-   Especifique ou recupere os locais de restrições de exportação em uma chave privada.
-   Especifique ou recupere um valor booliano que indica se a chave existe.
-   Especifique ou recupere um valor que indica como a chave é protegida antes do uso.
-   Especifique ou recupere um valor que indique se a chave pode ser usada para assinatura, criptografia ou ambos.
-   Especifique ou recupere um valor que identifique a finalidade específica para a qual a chave pode ser usada.
-   Especifique ou recupere o comprimento da chave.
-   Especifique ou recupere um valor que indique se a chave é usada ou salva no contexto de um computador ou usuário.
-   Recupere um valor booliano que especifica se a chave foi aberta.
-   Especifique um número de identificação pessoal para acessar uma chave privada em um [*cartão inteligente*](/windows/desktop/SecGloss/s-gly).
-   Especifique ou recupere o nome do CSP associado à chave.
-   Especifique ou recupere o [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) para a chave.

Cada uma das seções a seguir identifica uma função exportada por Xenroll.dll que pode ser usada para gerenciar uma [*chave de criptografia*](/windows/desktop/SecGloss/c-gly). Cada tópico também discute como usar CertEnroll.dll para substituir a função ou indica que não existe nenhum mapeamento entre as duas bibliotecas:

-   [ContainerNameWStr](#containernamewstr)
-   [GenKeyFlags](#genkeyflags)
-   [GetKeyLen](#getkeylenex)
-   [GetKeyLenEx](#getkeylenex)
-   [GetSupportedKeySpec](#getsupportedkeyspec)
-   [KeySpec](#getsupportedkeyspec)
-   [LimitExchangeKeyToEncipherment](#limitexchangekeytoencipherment)
-   [PVKFileNameWStr](#pvkfilenamewstr)
-   [ReuseHardwareKeyIfUnableToGenNew](#reusehardwarekeyifunabletogennew)
-   [UseExistingKeySet](#useexistingkeyset)
-   [Tópicos relacionados](#related-topics)

## <a name="containernamewstr"></a>ContainerNameWStr

A função [**ContainerNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_containernamewstr) em Xenroll.dll especifica ou recupera o nome do [*contêiner de chave*](/windows/desktop/SecGloss/k-gly).

Ao usar CertEnroll.dll, você pode executar as seguintes ações para recuperar o nome de um contêiner de chave:

1.  Chame a propriedade [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) em um objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) existente.
2.  Chame o método [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) na solicitação retornada da etapa 1 para recuperar a solicitação mais interna.
3.  Chame **QueryInterface** no objeto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) retornado da etapa 2 para converter em um objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Chame a propriedade [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) na solicitação PKCS \# 10.
5.  Chame a propriedade [**ContainerName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_containername) no objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) recuperado da etapa 4.

## <a name="genkeyflags"></a>GenKeyFlags

A função [**GenKeyFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_genkeyflags) definida em Xenroll.dll especifica ou recupera sinalizadores usados para gerar uma chave privada ou [*par de chaves pública/privada*](/windows/desktop/SecGloss/p-gly).

Ao usar CertEnroll.dll, você pode especificar várias propriedades diferentes que determinarão como uma chave privada é criada. Para obter mais informações, consulte [**criar**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create).

## <a name="getkeylen"></a>GetKeyLen

A função [**GetKeyLen**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getkeylen) definida em Xenroll.dll recupera o tamanho máximo ou mínimo de chave de uma chave de criptografia.

Ao usar CertEnroll.dll, você pode chamar a propriedade [**Length**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_length) em um objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) ou [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey) para recuperar o tamanho da chave em bits.

## <a name="getkeylenex"></a>GetKeyLenEx

A função [**GetKeyLenEx**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getkeylenex) definida em Xenroll.dll recupera o tamanho máximo ou mínimo da chave ou o comprimento de incremento de uma chave de criptografia.

Ao usar CertEnroll.dll, você pode chamar a propriedade [**Length**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_length) em um objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) ou [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey) para recuperar o tamanho da chave em bits. Se um algoritmo oferecer suporte a comprimentos de chave incrementais, você poderá chamar a propriedade [**IncrementLength**](/windows/desktop/api/CertEnroll/nf-certenroll-icspalgorithm-get_incrementlength) no objeto [**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm) para recuperar o valor de incremento. Você também pode chamar as propriedades [**minLength**](/windows/desktop/api/CertEnroll/nf-certenroll-icspalgorithm-get_minlength) e [**MaxLength**](/windows/desktop/api/CertEnroll/nf-certenroll-icspalgorithm-get_maxlength) para recuperar os tamanhos mínimo e máximo de chave.

## <a name="getsupportedkeyspec"></a>GetSupportedKeySpec

A função [**GetSupportedKeySpec**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getsupportedkeyspec) definida em Xenroll.dll recupera um valor que indica se um CSP dá suporte a chaves de troca, chaves de assinatura ou ambas.

Ao usar CertEnroll.dll, você pode chamar a propriedade [**KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) nos objetos [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) ou [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) para recuperar as operações com suporte pela chave.

## <a name="keyspec"></a>KeySpec

A função [**KeySpec**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_keyspec) definida em Xenroll.dll especifica ou recupera o tipo de chave.

Ao usar CertEnroll.dll, você pode chamar a propriedade [**KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) em um objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) para recuperar as operações com suporte pela chave.

## <a name="limitexchangekeytoencipherment"></a>LimitExchangeKeyToEncipherment

A função [**LimitExchangeKeyToEncipherment**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_limitexchangekeytoencipherment) definida em Xenroll.dll especifica ou recupera um valor booliano que indica se uma chave de criptografia pode ser usada somente para dados ou codificação de chave.

CertEnroll.dll não contém um equivalente direto para essa função. No entanto, você pode obter um resultado quase equivalente especificando um objeto [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage) e adicionando-o à solicitação de certificado.

## <a name="pvkfilenamewstr"></a>PVKFileNameWStr

A função [**PVKFileNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_pvkfilenamewstr) definida em Xenroll.dll especifica ou recupera o nome de um arquivo que contém chaves exportadas.

Ao usar CertEnroll.dll, você pode chamar o método [**Export**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-export) em um objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) para exportar uma chave para um **BSTR**. Você pode chamar o método [**ExportPublicKey**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-exportpublickey) para exportar a parte da [*chave pública*](/windows/desktop/SecGloss/p-gly) de um par de chaves assimétricas.

## <a name="reusehardwarekeyifunabletogennew"></a>ReuseHardwareKeyIfUnableToGenNew

A função [**ReuseHardwareKeyIfUnableToGenNew**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_reusehardwarekeyifunabletogennew) definida em Xenroll.dll especifica ou recupera um valor booliano que indica se uma chave existente é reutilizada quando um erro é encontrado ao gerar uma nova chave.

Ao usar CertEnroll.dll, você pode chamar o método [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate) em um objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e especificar um valor do tipo de enumeração [**X509RequestInheritOptions**](/windows/desktop/api/CertEnroll/ne-certenroll-x509requestinheritoptions) para reutilizar uma chave privada existente.

## <a name="useexistingkeyset"></a>UseExistingKeySet

A função [**UseExistingKeySet**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_useexistingkeyset) definida em Xenroll.dll especifica ou recupera um valor booliano que indica se as chaves existentes devem ser usadas.

Ao usar CertEnroll.dll, você pode chamar o método [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate) em um objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e especificar um valor do tipo de enumeração [**X509RequestInheritOptions**](/windows/desktop/api/CertEnroll/ne-certenroll-x509requestinheritoptions) para reutilizar as chaves públicas e privadas existentes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mapeando Xenroll.dll para CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> </dl>

 

 
