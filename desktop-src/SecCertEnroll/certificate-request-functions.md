---
description: A CertEnroll.dll de dados implementa cinco interfaces que podem ser usadas para criar e gerenciar uma solicitação de certificado.
ms.assetid: f4630095-6ba2-46f7-8825-e7a5b1cb185a
title: Funções de solicitação de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e07fb348b335562863f04226a2fb729bfbcbdaba27cb574a04c87075a64653a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902565"
---
# <a name="certificate-request-functions"></a>Funções de solicitação de certificado

A CertEnroll.dll de dados implementa cinco interfaces que podem ser usadas para criar e gerenciar uma solicitação de certificado. Desses, a interface [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) representa um objeto base abstrato que define assinaturas de método herdadas pelas quatro interfaces a seguir.

| Interface                                                                        | Descrição                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) | Permite que você crie um certificado diretamente sem aplicar a uma AC (autoridade [*de certificação).*](/windows/desktop/SecGloss/c-gly)<br/>                                                                                                            |
| [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                 | Representa uma solicitação de certificado do CMC (Gerenciamento de Certificados sobre [*CMS)*](/windows/desktop/SecGloss/c-gly) que pode conter uma solicitação PKCS 10 aninhada ou outro objeto de solicitação \# do CMC.<br/> |
| [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)             | Representa um objeto de solicitação cms (sintaxe de mensagem de certificado) [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) que deve conter uma solicitação PKCS \# 10 aninhada.<br/>                                                                                                         |
| [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)           | Representa uma solicitação de certificado PKCS \# 10. Uma solicitação PKCS 10 pode ser enviada diretamente para uma AC ou pode ser envolvida por uma \# solicitação PKCS \# 7 ou CMC.<br/>                                                                                                                                                            |



 

Você pode usar um objeto de solicitação de certificado para inicializar um objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) para registrar um cliente em uma hierarquia de certificados e instalar a resposta de certificado retornada pela AC.

Cada uma das seções a seguir identifica uma função exportada por Xenroll.dll para criar, enumerar ou excluir solicitações de certificado. Cada seção também discute como usar o CertEnroll.dll para substituir a função ou indica que não existe nenhum mapeamento entre as duas bibliotecas:

-   [createFilePKCS10WStr](#createfilepkcs10wstr)
-   [createFileRequestWStr](#createfilerequestwstr)
-   [createPKCS10WStr](#createpkcs10wstr)
-   [CreatePKCS7RequestFromRequest](#createpkcs7requestfromrequest)
-   [createRequestWStr](#createrequestwstr)
-   [DeleteRequestCert](#deleterequestcert)
-   [enumPendingRequestWStr](#enumpendingrequestwstr)
-   [removePendingRequestWStr](#removependingrequestwstr)
-   [Redefinir](#reset)
-   [setPendingRequestInfoWStr](#setpendingrequestinfowstr)
-   [Tópicos relacionados](#related-topics)

## <a name="createfilepkcs10wstr"></a>createFilePKCS10WStr

A [**função createFilePKCS10WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createfilepkcs10wstr) no Xenroll.dll cria uma solicitação de certificado PKCS 10 codificada em base64 e a salva em \# um arquivo.

A CertEnroll.dll não implementa diretamente a funcionalidade para gravar uma solicitação em um arquivo. No entanto, você pode recuperar uma solicitação de certificado chamando a propriedade [**RawData**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_rawdata) no objeto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) e criando uma função personalizada para copiar o valor para um arquivo.

## <a name="createfilerequestwstr"></a>createFileRequestWStr

A [**função createFileRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilerequestwstr) no Xenroll.dll cria uma solicitação de certificado PKCS \# 7, PKCS 10 ou CMC e a salva em \# um arquivo.

A CertEnroll.dll não implementa diretamente a funcionalidade para gravar uma solicitação em um arquivo. No entanto, você pode recuperar uma solicitação de certificado chamando a propriedade [**RawData**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_rawdata) no objeto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) e criando uma função personalizada para copiar o valor para um arquivo.

## <a name="createpkcs10wstr"></a>createPKCS10WStr

A [**função createPKCS10WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs10wstr) no Xenroll.dll cria uma solicitação de certificado PKCS 10 e a copia \# para uma matriz de byte.

Você pode usar um objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) para inicializar uma solicitação PKCS 10 de uma solicitação existente, um certificado existente, uma chave privada, uma chave pública ou \# um modelo. [](/windows/desktop/SecGloss/p-gly) [](/windows/desktop/SecGloss/p-gly)

## <a name="createpkcs7requestfromrequest"></a>CreatePKCS7RequestFromRequest

A [**função CreatePKCS7RequestFromRequest**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs7requestfromrequest) no Xenroll.dll cria uma solicitação de certificado PKCS 7 e a copia para uma matriz \# de byte.

Você pode usar um objeto [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) para inicializar uma solicitação PKCS 7 de uma solicitação existente, um certificado existente, um objeto de solicitação interna ou \# um modelo.

## <a name="createrequestwstr"></a>createRequestWStr

A [**função createRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createrequestwstr) no Xenroll.dll cria uma solicitação de certificado PKCS \# 7, PKCS 10 ou CMC e a copia para uma matriz \# de byte.

Para usar a biblioteca CertEnroll.dll para criar solicitações PKCS 7, PKCS 10 ou CMC, você pode criar e inicializar instâncias dos objetos \# \# [**IX509CertificateRequestPkcs7,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)ou [**IX509CertificateRequestCmc.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)

## <a name="deleterequestcert"></a>DeleteRequestCert

A [**função DeleteRequestCert**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_deleterequestcert) no Xenroll.dll especifica ou recupera um valor booliano que indica se um certificado fictício é removido após a instalação de uma resposta de certificado.

O [**objeto IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) no CertEnroll.dll cria automaticamente certificados fictícios no armazenamento de solicitações para salvar temporariamente várias propriedades de certificado inicializadas durante o processo de registro. Depois que um certificado é emitido por uma AC, as propriedades são copiadas para o novo certificado e o certificado fictício é excluído. A CertEnroll.dll não permite que você force a permanecer um certificado fictício após a instalação da resposta do certificado.

## <a name="enumpendingrequestwstr"></a>enumPendingRequestWStr

A [**função enumPendingRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-enumpendingrequestwstr) Xenroll.dll recupera um valor de propriedade especificado para uma solicitação pendente.

A CertEnroll.dll não implementa diretamente a funcionalidade para remover uma solicitação de certificado pendente.

## <a name="removependingrequestwstr"></a>removePendingRequestWStr

A [**função removePendingRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-removependingrequestwstr) no Xenroll.dll remove uma solicitação pendente do armazenamento de solicitações.

A CertEnroll.dll não implementa diretamente a funcionalidade para remover uma solicitação de certificado pendente.

## <a name="reset"></a>Redefinir

A [**função Reset**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-reset) no Xenroll.dll retorna o Controle de Registro de Certificado para um estado inicial.

Você pode obter o mesmo resultado usando Certenroll.dll para criar um novo objeto de solicitação do tipo necessário.

## <a name="setpendingrequestinfowstr"></a>setPendingRequestInfoWStr

A [**função setPendingRequestInfoWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setpendingrequestinfowstr) Xenroll.dll especifica propriedades para a solicitação pendente.

A CertEnroll.dll não implementa diretamente a funcionalidade para remover uma solicitação de certificado pendente. Você pode chamar a [**propriedade CAConfigString**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_caconfigstring) no objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) para recuperar uma cadeia de caracteres de configuração, mas apenas para um objeto de registro ativo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mapeamento Xenroll.dll para CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)
</dt> <dt>

[**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)
</dt> <dt>

[**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)
</dt> <dt>

[**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
</dt> <dt>

[**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
</dt> <dt>

[**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

