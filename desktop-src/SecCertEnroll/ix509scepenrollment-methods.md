---
description: A interface IX509SCEPEnrollment expõe os métodos a seguir.
ms.assetid: B45B68D2-A14D-4D14-AF5F-1A1BB9921A0D
title: Métodos IX509SCEPEnrollment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a15fc7de6392c49bd38381771956685ba6c8427b3562e7c81c372c1bab61db49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993536"
---
# <a name="ix509scepenrollment-methods"></a>Métodos IX509SCEPEnrollment

A interface [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) expõe os métodos a seguir.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                              | Descrição                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Método CreateRequestMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createrequestmessage)<br/>                         | Crie uma mensagem de solicitação PKCS10 com uma senha de desafio. A mensagem de solicitação está em um PKCS7 enveloped criptografado com o certificado de criptografia do servidor SCEP e assinado pelo certificado de assinatura do servidor.<br/> |
| [**Método CreateRetrieveCertificateMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievecertificatemessage)<br/> | Recuperar um certificado emitido anteriormente.<br/>                                                                                                                                                                   |
| [**Método CreateRetrievePendingMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievependingmessage)<br/>         | Crie uma mensagem para sondagem de certificado (registro manual).<br/>                                                                                                                                               |
| [**Método DeleteRequest**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-deleterequest)<br/>                                       | Exclua todos os certificados ou chaves criados para a solicitação.<br/>                                                                                                                                                    |
| [**Método Initialize**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initialize)<br/>                                             | Inicialize a instância em preparação para uma nova solicitação.<br/>                                                                                                                                                   |
| [**Método InitializeForPending**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initializeforpending)<br/>                         | Inicialize a instância para se preparar para gerar uma mensagem para recuperar um certificado emitido ou instalar uma resposta para uma solicitação anterior pelo emissor.<br/>                                              |
| [**Método ProcessResponseMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage)<br/>                     | Processe uma mensagem de resposta e retorne a disposição da mensagem.<br/>                                                                                                                                       |



 

 

 




