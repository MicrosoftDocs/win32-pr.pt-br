---
description: O formato de certificado X. 509 versão 3 identifica várias extensões que podem ser adicionadas a um certificado para fornecer informações aprimoradas sobre o uso de chave, políticas de certificado e restrições, formulários de nomes alternativos e muito mais.
ms.assetid: d53107b7-a153-41cf-9876-1d28aaf99816
title: Funções de extensão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bc490c8763a00fae9e7fb1e8a702ff87e2c18fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761401"
---
# <a name="extension-functions"></a>Funções de extensão

O formato de certificado [*X. 509*](/windows/desktop/SecGloss/x-gly) versão 3 identifica várias extensões que podem ser adicionadas a um certificado para fornecer informações aprimoradas sobre o uso de chave, políticas de certificado e restrições, formulários de nomes alternativos e muito mais.

CertEnroll.dll implementa as seguintes interfaces para gerenciar as extensões de certificado:

-   [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)
-   [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)
-   [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)
-   [**IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)
-   [**IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)
-   [**IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)
-   [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)
-   [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)
-   [**IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)
-   [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)
-   [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)
-   [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)
-   [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)

Cada uma das seções a seguir discute uma função exportada por Xenroll.dll para gerenciar as extensões de certificado. Cada seção também aborda como usar CertEnroll.dll para substituir a função ou indica que não existe nenhum mapeamento entre as duas bibliotecas:

-   [AddCertTypeToRequestWStr](#addcerttypetorequestwstr)
-   [AddCertTypeToRequestWStrEx](#addcerttypetorequestwstrex)
-   [AddExtensionsToRequest](#addextensionstorequest)
-   [addExtensionToRequestWStr](#addextensiontorequestwstr)
-   [EnableSMIMECapabilities](#enablesmimecapabilities)
-   [IncludeSubjectKeyID](#includesubjectkeyid)
-   [resetExtensions](#resetextensions)
-   [Tópicos relacionados](#related-topics)

## <a name="addcerttypetorequestwstr"></a>AddCertTypeToRequestWStr

A função [**AddCertTypeToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addcerttypetorequestwstr) no Xenroll.dll adiciona um modelo de certificado, por nome, a uma solicitação.

Usando CertEnroll.dll, o método preferencial para incorporar um modelo a uma solicitação de certificado é usar o método [**InitializeFromTemplateName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromtemplatename) em um \# objeto de solicitação PKCS 10 ou [* Pkcs) ou o método [**INITIALIZEFROMINNERREQUESTTEMPLATENAME**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-initializefrominnerrequesttemplatename) em uma solicitação CMC.

Se um modelo específico não estiver disponível no cliente, mas for esperado que seja compreendido pela [*autoridade de certificação*](/windows/desktop/SecGloss/c-gly) (CA), você poderá usar a interface [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) para adicionar um modelo de versão 1 ou pode usar a interface [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate) para adicionar um modelo de versão 2 a uma solicitação de certificado. Por exemplo, para adicionar um modelo de versão 1, execute as seguintes ações:

1.  Crie um objeto [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .
2.  Crie um objeto [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) e chame o método [**InitializeEncode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensiontemplatename-initializeencode) , especificando o nome do modelo.
3.  Adicione a extensão criada à coleção [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) chamando o método [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-add) .
4.  Crie um objeto [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) e chame o método [**InitializeEncode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributeextensions-initializeencode) , especificando a coleção [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) na entrada.
5.  Recupere um objeto de coleção [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) chamando a propriedade [**cript**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes) . de um objeto de solicitação [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) ou [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) existente.

## <a name="addcerttypetorequestwstrex"></a>AddCertTypeToRequestWStrEx

A função [**AddCertTypeToRequestWStrEx**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addcerttypetorequestwstrex) no Xenroll.dll adiciona um modelo de certificado a uma solicitação por nome, identificador de objeto e versão.

Para obter informações sobre como usar CertEnroll.dll para incorporar informações de modelo em uma solicitação, consulte AddCertTypeToRequestWStr.

## <a name="addextensionstorequest"></a>AddExtensionsToRequest

A função [**AddExtensionsToRequest**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addextensionstorequest) no Xenroll.dll adiciona uma coleção de extensões a uma solicitação.

No CertEnroll.dll, as extensões são adicionadas à coleção Attributes de uma solicitação CMC ou PKCS \# 10. Para adicionar extensões, execute as seguintes ações:

1.  Crie um objeto [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .
2.  Crie um objeto [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) e chame o método [**Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extension-initialize) para criar uma extensão a partir de um identificador de objeto e um valor de extensão ou use qualquer uma das interfaces listadas anteriormente para definir uma das extensões mais comuns.
3.  Adicione cada nova extensão criada na etapa anterior à coleção [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) chamando o método [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-add) .

## <a name="addextensiontorequestwstr"></a>addExtensionToRequestWStr

A função [**addExtensionToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addextensiontorequestwstr) no Xenroll.dll adiciona uma extensão específica à solicitação.

No CertEnroll.dll, uma extensão específica deve ser definida e adicionada a uma coleção de extensões antes que a coleção de extensão seja adicionada à coleção de atributos de uma solicitação CMC ou PKCS \# 10. Para obter mais informações, consulte a discussão sobre o AddExtensionsToRequest acima.

## <a name="enablesmimecapabilities"></a>EnableSMIMECapabilities

A função [**EnableSMIMECapabilities**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_enablesmimecapabilities) em Xenroll.dll especifica ou recupera um valor booliano que indica se a extensão **SMIMECapabilities** deve ser adicionada à solicitação.

Você pode chamar a propriedade [**SmimeCapabilities**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_smimecapabilities) no objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) para adicionar automaticamente um objeto [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities) à solicitação antes da codificação.

## <a name="includesubjectkeyid"></a>IncludeSubjectKeyID

A função [**IncludeSubjectKeyID**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_includesubjectkeyid) em Xenroll.dll especifica ou recupera um valor booliano que indica se a extensão **SubjectKeyIdentifier** deve ser adicionada à solicitação.

Por padrão, a extensão **SubjectKeyIdentifier** é criada quando o objeto de solicitação [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) é inicializado. Você pode substituir esse comportamento chamando a propriedade [**SuppressOids**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_suppressoids) .

Se você tiver um [*par de chaves pública/privada*](/windows/desktop/SecGloss/p-gly), também poderá usar a interface [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier) em CertEnroll.dll para adicionar uma extensão **SubjectKeyIdentifier** a uma solicitação de certificado executando as seguintes ações:

1.  Crie um objeto [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .
2.  Crie um objeto [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier) e chame o método [**InitializeEncode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensionsubjectkeyidentifier-initializeencode) , especificando uma cadeia de caracteres que contém o identificador. Normalmente, esse é um hash SHA-1 de 20 bytes da [*chave pública*](/windows/desktop/SecGloss/p-gly) contida no certificado de autenticação da autoridade de certificação.
3.  Adicione a extensão criada à coleção [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) chamando o método [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-add) .
4.  Crie um objeto [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) e chame o método [**InitializeEncode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributeextensions-initializeencode) , especificando a coleção [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) na entrada.
5.  Recupere um objeto de coleção [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) chamando a propriedade [**cript**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes) . de um objeto de solicitação [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) ou [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) existente.

## <a name="resetextensions"></a>resetExtensions

A função [**resetExtensions**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-resetextensions) no Xenroll.dll remove a coleção de extensão da solicitação.

Para remover uma extensão de uma solicitação por número de índice usando CertEnroll.dll, chame o método [**Remove**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-remove) na coleção [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) . Para remover todos os atributos de uma solicitação, chame o método [**Clear**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-clear) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mapeando Xenroll.dll para CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)
</dt> <dt>

[**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)
</dt> </dl>

 

 
