---
description: O SDK de Registro de Certificado pode ser usado para criar solicitações de certificado PKCS \# 10, PKCS \# 7, CMC e autoatendados.
ms.assetid: 218eafb9-c9c8-49ff-8288-3909ed708ffc
title: Solicitações de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39125774584d127e40b16dbb2adca563d8c341b79454235163be30edc865b22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902406"
---
# <a name="certificate-requests"></a>Solicitações de certificado

O SDK de Registro de Certificado pode ser usado para criar solicitações de certificado PKCS \# 10, PKCS \# 7, CMC e autoatendados. Cada tipo de solicitação é representado por uma das interfaces listadas na tabela a seguir. Todas as interfaces de solicitação herdam direta ou indiretamente da interface [**IX509CertificateRequest.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) 

| Interface                                                                        | Descrição                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)           | Representa uma solicitação PKCS \# 10. Essa interface herda de [**IX509CertificateRequest.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)                   |
| [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)             | Representa uma solicitação PKCS \# 7. Essa interface herda de [**IX509CertificateRequest.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)                    |
| [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) | Representa um certificado auto-assinado. Essa interface herda de [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10). |
| [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                 | Representa uma solicitação de CMC. Essa interface herda de [**IX509CertificateRequestPkcs7.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)               |



 

A ilustração a seguir mostra a estrutura de herança dos objetos de solicitação com suporte pela API de Registro de Certificado. Um [**objeto IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) serve, direta ou indiretamente, como a classe base para todos os objetos de solicitação disponíveis.

![estrutura de herança para as interfaces de solicitação](images/certificate-request-inheritance.png)

Independentemente do tipo, uma solicitação de certificado contém informações sobre a entidade que está fazendo a solicitação, a chave pública da entidade, um conjunto de atributos, um conjunto de extensões X.509 versão 3 (que podem ser enviadas como parte dos atributos) e uma assinatura. Esses problemas são abordados pelos seguintes tópicos:

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

 

 



