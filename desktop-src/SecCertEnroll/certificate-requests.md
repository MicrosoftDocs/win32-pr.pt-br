---
description: O SDK de registro de certificado pode ser usado para criar \# solicitações de certificado PKCS 10, PKCS \# 7, CMC e autoassinados.
ms.assetid: 218eafb9-c9c8-49ff-8288-3909ed708ffc
title: Solicitações de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9690f3a5117abfa0ae262f0a8fa38f68528abf02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758027"
---
# <a name="certificate-requests"></a>Solicitações de certificado

O SDK de registro de certificado pode ser usado para criar \# solicitações de certificado PKCS 10, PKCS \# 7, CMC e autoassinados. Cada tipo de solicitação é representado por uma das interfaces listadas na tabela a seguir. Todas as interfaces de solicitação herdam direta ou indiretamente da interface [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) . 

| Interface                                                                        | Descrição                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)           | Representa uma \# solicitação PKCS 10. Essa interface herda de [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).                   |
| [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)             | Representa uma \# solicitação PKCS 7. Essa interface herda de [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).                    |
| [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) | Representa um certificado autoassinado. Essa interface herda de [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10). |
| [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                 | Representa uma solicitação CMC. Essa interface herda de [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7).               |



 

A ilustração a seguir mostra a estrutura de herança dos objetos de solicitação com suporte pela API de registro de certificado. Um objeto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) serve, direta ou indiretamente, como a classe base para todos os objetos de solicitação disponíveis.

![estrutura de herança para as interfaces de solicitação](images/certificate-request-inheritance.png)

Independentemente do tipo, uma solicitação de certificado contém informações sobre o assunto que faz a solicitação, a chave pública da entidade, um conjunto de atributos, um conjunto de extensões X. 509 versão 3 (que podem ser enviadas como parte dos atributos) e uma assinatura. Esses problemas são abordados pelos seguintes tópicos:

-   [Nomes de Entidades](subject-names.md)
-   [Atributos](attributes.md)
-   [Extensões](extensions.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)
</dt> <dt>

[**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
</dt> <dt>

[**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
</dt> <dt>

[**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
</dt> </dl>

 

 



