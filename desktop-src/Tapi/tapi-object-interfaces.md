---
description: O objeto TAPI é o objeto principal para a TAPI 3.
ms.assetid: 046f2646-6043-4d68-a42a-8750c016b3c8
title: Interfaces de objeto TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada1e49fe83a75c802b06ded953f309a157365d482d22d06c6bbedf97a5b8ac7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139848"
---
# <a name="tapi-object-interfaces"></a>Interfaces de objeto TAPI

O [objeto TAPI](tapi-object.md) é o objeto principal para a TAPI 3.

A interface [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent) não é exposta diretamente no objeto TAPI, mas está intimamente relacionada a ela e está listada aqui para conveniência de referência.



| Interfaces                                                 | Descrição                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITTAPI**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi)                                   | Interface primária da TAPI 3.                                                                                                                              |
| [**ITTAPI2**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi2)                                 | Deriva de [**ITTAPI**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi); fornece métodos adicionais que dão suporte a dispositivos telefônicos.                                                         |
| [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) | Interface de saída usada para receber informações assíncronas sobre eventos TAPI 3.                                                                       |
| [**ITTAPICallCenter**](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter)               | Fornece uma interface de entrada para controles de Call Center.                                                                                                 |
| [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent)             | Fornece métodos para recuperar informações relacionadas a eventos de objeto TAPI.                                                                                |
| [**ITTAPIObjectEvent2**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent2)           | Estende [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent); fornece um método para recuperar um ponteiro para o objeto de telefone que causou o evento de objeto TAPI. |



 

 

 
