---
description: Implementa a interface IX509Enrollment.
ms.assetid: bcf5c2f0-b99f-4de5-83f4-44f17dc31cd4
title: Funções de resposta de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15eec71d0493fa4961988b86db0397d0fd516508
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760397"
---
# <a name="certificate-response-functions"></a>Funções de resposta de certificado

CertEnroll.dll implementa a interface [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) para enviar uma solicitação de certificado de cliente e instalar a resposta de uma [*autoridade de certificação*](/windows/desktop/SecGloss/c-gly) (CA).

O processo de registro pode acomodar os três cenários a seguir:

<dl> Registro fora de banda

1.  Chame qualquer método de inicialização implementado pelo objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) .
2.  Chame o método [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) para recuperar a solicitação.
3.  Envie a solicitação fora de banda (manualmente ou usando algum outro processo).
4.  Receber a resposta de uma AC.
5.  Chame o método [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) .

  
Registro automático

1.  Chame qualquer método de inicialização implementado pelo objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) .
2.  Chame o método de [**registro**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) .

  
Registro atrasado

1.  Chame qualquer método de inicialização implementado pelo objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) .
2.  Chame o método [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) para recuperar a solicitação.
3.  Armazene a solicitação até que você esteja pronto para enviá-la.
4.  Quando você estiver pronto para se registrar, chame o método [**Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-initialize) para reinicializar o objeto de registro.
5.  Chame o método [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) quando a autoridade de certificação retornar um certificado.

  
</dl>

Durante o processo de registro, você pode chamar a propriedade [**status**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_status) no objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) para recuperar um valor de enumeração [**EnrollmentEnrollStatus**](/windows/desktop/api/CertEnroll/ne-certenroll-enrollmentenrollstatus) que identifica se o registro foi bem-sucedido, está pendente, foi ignorado, gerou um erro ou foi negado.

Cada uma das seções a seguir identifica uma função exportada pelo Xenroll.dll para instalar uma resposta de certificado de uma autoridade de certificação. Cada seção também aborda como usar CertEnroll.dll para substituir a função ou indica que não existe nenhum mapeamento entre as duas bibliotecas:

-   [acceptFilePKCS7WStr](#acceptfilepkcs7wstr)
-   [acceptFileResponseWStr](#acceptfileresponsewstr)
-   [acceptPKCS7Blob](#acceptpkcs7blob)
-   [acceptResponseBlob](#acceptresponseblob)
-   [getCertContextFromFileResponseWStr](#getcertcontextfromfileresponsewstr)
-   [getCertContextFromPKCS7](#getcertcontextfrompkcs7)
-   [getCertContextFromResponseBlob](#getcertcontextfromresponseblob)
-   [InstallPKCS7Blob](#installpkcs7blobex)
-   [InstallPKCS7BlobEx](#installpkcs7blobex)
-   [SPCFileNameWStr](#spcfilenamewstr)
-   [WriteCertToCSP](#writecerttocsp)
-   [WriteCertToUserDS](#writecerttouserds)
-   [Tópicos relacionados](#related-topics)

## <a name="acceptfilepkcs7wstr"></a>acceptFilePKCS7WStr

A função [**acceptFilePKCS7WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptfilepkcs7wstr) no Xenroll.dll instala uma resposta [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) de um arquivo.

A biblioteca de CertEnroll.dll não implementa diretamente a funcionalidade para instalar uma \# resposta de certificado PKCS 7 de um arquivo. No entanto, você pode criar uma função personalizada para ler os dados do arquivo em uma matriz de bytes e chamar [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) para instalar a resposta.

Se você especificar o valor de **AllowNoOutstandingRequest** da enumeração [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) para o primeiro parâmetro de [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), um certificado fictício não precisará existir, permitindo assim que você instale um certificado sem primeiro chamar o [**registro**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) ou [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). No entanto, se você estiver instalando um certificado usando um script da Web, um certificado fictício deverá existir no repositório de solicitações. Portanto, você deve especificar **AllowNone** para o primeiro parâmetro.

## <a name="acceptfileresponsewstr"></a>acceptFileResponseWStr

A função [**acceptFileResponseWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-acceptfileresponsewstr) no Xenroll.dll instala uma \# resposta de certificado PKCS 7 ou CMC de um arquivo.

A biblioteca de CertEnroll.dll não implementa diretamente a funcionalidade para instalar uma resposta de certificado de um arquivo. No entanto, você pode criar uma função personalizada para ler os dados do arquivo em uma matriz de bytes e chamar [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) para instalar a \# resposta PKCS 7 ou CMC.

Se você especificar o valor de **AllowNoOutstandingRequest** da enumeração [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) para o primeiro parâmetro de [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), um certificado fictício não precisará existir, permitindo assim que você instale um certificado sem primeiro chamar o [**registro**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) ou [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). No entanto, se você estiver instalando um certificado usando um script da Web, um certificado fictício deverá existir no repositório de solicitações. Portanto, você deve especificar **AllowNone** para o primeiro parâmetro.

## <a name="acceptpkcs7blob"></a>acceptPKCS7Blob

A função [**acceptPKCS7Blob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptpkcs7blob) no Xenroll.dll instala uma \# resposta PKCS 7 contida em uma matriz de bytes.

Você pode chamar [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) para instalar uma \# mensagem PKCS 7. Se você especificar o valor **AllowNoOutstandingRequest** da enumeração [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) para o primeiro parâmetro de [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), um certificado fictício não precisará existir, permitindo assim que você instale a \# resposta PKCS 7 sem primeiro chamar o [**registro**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) ou [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). No entanto, se você estiver instalando um certificado usando um script da Web, um certificado fictício deverá existir no repositório de solicitações. Portanto, você deve especificar **AllowNone** para o primeiro parâmetro.

## <a name="acceptresponseblob"></a>acceptResponseBlob

A função [**acceptResponseBlob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-acceptresponseblob) no Xenroll.dll instala uma \# resposta de certificado PKCS 7 ou CMC contida em uma matriz de bytes.

Você pode chamar [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) para instalar uma \# resposta PKCS 7 ou CMC. Se você especificar o valor de **AllowNoOutstandingRequest** da enumeração [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) para o primeiro parâmetro de [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), um certificado fictício não precisará existir, permitindo assim que você instale a resposta sem primeiro chamar o [**registro**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) ou [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). No entanto, se você estiver instalando um certificado usando um script da Web, um certificado fictício deverá existir no repositório de solicitações. Portanto, você deve especificar **AllowNone** para o primeiro parâmetro.

## <a name="getcertcontextfromfileresponsewstr"></a>getCertContextFromFileResponseWStr

A função [**getCertContextFromFileResponseWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getcertcontextfromfileresponsewstr) no Xenroll.dll recupera o certificado do cliente de um arquivo.

A biblioteca de CertEnroll.dll não implementa diretamente a funcionalidade para recuperar um certificado de uma resposta de autoridade de certificação salva em um arquivo. No entanto, você pode criar uma função personalizada para ler os dados do arquivo em uma matriz de bytes e chamar [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) para instalar a \# resposta PKCS 7 ou CMC e chamar a propriedade do [**certificado**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificate) para recuperar o certificado.

Se você especificar o valor de **AllowNoOutstandingRequest** da enumeração [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) para o primeiro parâmetro de [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), um certificado fictício não precisará existir, permitindo assim que você instale um certificado sem primeiro chamar o [**registro**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) ou [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). No entanto, se você estiver instalando um certificado usando um script da Web, um certificado fictício deverá existir no repositório de solicitações. Portanto, você deve especificar **AllowNone** para o primeiro parâmetro.

## <a name="getcertcontextfrompkcs7"></a>getCertContextFromPKCS7

A função [**getCertContextFromPKCS7**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-getcertcontextfrompkcs7) no Xenroll.dll recupera o certificado do cliente de uma \# resposta PKCS 7.

Você pode chamar a propriedade de [**certificado**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificate) no objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) para recuperar um certificado depois de chamar o método de [**inscrição**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) ou [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) .

## <a name="getcertcontextfromresponseblob"></a>getCertContextFromResponseBlob

A função [**getCertContextFromResponseBlob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getcertcontextfromresponseblob) no Xenroll.dll recupera um certificado de cliente de uma \# resposta PKCS 7 ou CMC.

Você pode chamar a propriedade de [**certificado**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificate) no objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) para recuperar um certificado depois de chamar o método de [**inscrição**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) ou [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) .

## <a name="installpkcs7blob"></a>InstallPKCS7Blob

A função [**InstallPKCS7Blob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-installpkcs7blob) no Xenroll.dll instala uma \# resposta PKCS 7.

Você pode chamar [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) para instalar uma \# resposta PKCS 7 ou CMC. Se você especificar o valor de **AllowNoOutstandingRequest** da enumeração [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) para o primeiro parâmetro de [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), um certificado fictício não precisará existir, permitindo assim que você instale a resposta sem primeiro chamar o [**registro**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) ou [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). No entanto, se você estiver instalando um certificado usando um script da Web, um certificado fictício deverá existir no repositório de solicitações. Portanto, você deve especificar **AllowNone** para o primeiro parâmetro.

## <a name="installpkcs7blobex"></a>InstallPKCS7BlobEx

A função [**InstallPKCS7BlobEx**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-installpkcs7blobex) no Xenroll.dll instala uma \# resposta PKCS 7 e retorna o número de certificados instalados.

Você pode chamar [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) para instalar uma \# resposta PKCS 7 ou CMC. Se você especificar o valor de **AllowNoOutstandingRequest** da enumeração [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) para o primeiro parâmetro de [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), um certificado fictício não precisará existir, permitindo assim que você instale a resposta sem primeiro chamar o [**registro**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) ou [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). No entanto, se você estiver instalando um certificado usando um script da Web, um certificado fictício deverá existir no repositório de solicitações. Portanto, você deve especificar **AllowNone** para o primeiro parâmetro.

## <a name="spcfilenamewstr"></a>SPCFileNameWStr

A função [**SPCFileNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_spcfilenamewstr) em Xenroll.dll especifica ou recupera o nome do arquivo no qual salvar a resposta do certificado. A biblioteca de CertEnroll.dll não implementa a funcionalidade que permite copiar um certificado para um arquivo específico. O processo de registro instala automaticamente a cadeia de certificados em arquivos nos armazenamentos apropriados.

## <a name="writecerttocsp"></a>WriteCertToCSP

A função [**WriteCertToCSP**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_writecerttocsp) em Xenroll.dll especifica ou recupera um valor booliano que indica se um certificado deve ser gravado em um CSP ( [*provedor de serviços de criptografia*](/windows/desktop/SecGloss/c-gly) ). Normalmente, se essa função for chamada, o provedor será um [*cartão inteligente*](/windows/desktop/SecGloss/s-gly).

Em CertEnroll.dll, quando um cliente chama o método de [**registro**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) para enviar uma solicitação para um certificado de cartão inteligente e um certificado é emitido, o [**registro**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) instala automaticamente o certificado no cartão inteligente, supondo que o cartão esteja instalado no leitor. O método [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) também grava automaticamente o certificado no cartão inteligente.

## <a name="writecerttouserds"></a>WriteCertToUserDS

A função [**WriteCertToUserDS**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_writecerttouserds) em Xenroll.dll especifica ou recupera um valor booliano que indica se um certificado deve ser salvo no repositório de Active Directory. A biblioteca de CertEnroll.dll não implementa a funcionalidade que permite especificar um repositório para o qual copiar um certificado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mapeando Xenroll.dll para CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

 
