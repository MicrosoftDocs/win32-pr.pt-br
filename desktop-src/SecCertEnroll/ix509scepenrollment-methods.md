---
description: A interface IX509SCEPEnrollment expõe os métodos a seguir.
ms.assetid: B45B68D2-A14D-4D14-AF5F-1A1BB9921A0D
title: Métodos IX509SCEPEnrollment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a33c3bdee14b865211b53649075dec6d4617a4c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105779957"
---
# <a name="ix509scepenrollment-methods"></a>Métodos IX509SCEPEnrollment

A interface [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) expõe os métodos a seguir.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                              | Descrição                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Método CreateRequestMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createrequestmessage)<br/>                         | Crie uma mensagem de solicitação PKCS10 com uma senha de desafio. A mensagem de solicitação está em um PKCS7 envelopado criptografado com o certificado de criptografia do servidor SCEP e assinado pelo certificado de autenticação do servidor.<br/> |
| [**Método CreateRetrieveCertificateMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievecertificatemessage)<br/> | Recupere um certificado emitido anteriormente.<br/>                                                                                                                                                                   |
| [**Método CreateRetrievePendingMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievependingmessage)<br/>         | Crie uma mensagem para sondagem de certificado (registro manual).<br/>                                                                                                                                               |
| [**Método DeleteRequest**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-deleterequest)<br/>                                       | Exclua quaisquer certificados ou chaves criadas para a solicitação.<br/>                                                                                                                                                    |
| [**Método Initialize**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initialize)<br/>                                             | Inicialize a instância em preparação para uma nova solicitação.<br/>                                                                                                                                                   |
| [**Método InitializeForPending**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initializeforpending)<br/>                         | Inicialize a instância para se preparar para gerar uma mensagem para recuperar um certificado emitido ou instalar uma resposta para uma solicitação anterior pelo emissor.<br/>                                              |
| [**Método ProcessResponseMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage)<br/>                     | Processar uma mensagem de resposta e retornar a disposição da mensagem.<br/>                                                                                                                                       |



 

 

 




