---
description: O Telefone objeto é a entidade que representa o dispositivo de telefone real e todos os seus controles.
ms.assetid: 5bc2f595-8e2b-4938-b813-1574a9390084
title: Telefone Interfaces de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e146910b8184f35057843f20ad663e2be21d2c4844852e7cca3939e1e979d00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873266"
---
# <a name="phone-object-interfaces"></a>Telefone Interfaces de objeto

O Telefone objeto é a entidade que representa o dispositivo de telefone real e todos os seus controles.

As interfaces [**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent) e [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone) não são expostas diretamente no objeto Telefone, mas estão fortemente relacionadas a ele e são listadas aqui para conveniência de referência.



| Interface                                                  | Descrição                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone)                                 | Permite o acesso ao dispositivo de telefone em um nível comparável ao disponível com a TAPI 2. *API x* C.                                      |
| [**ITAutomatedPhoneControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol) | Fornece métodos para controle automatizado dos toques e anéis de um telefone e para manipulação de chamadas automatizadas com base no estado de gancho de um telefone. |
| [**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent)                       | Recupera a descrição dos eventos de telefone.                                                                                                |
| [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone)                           | Enumera [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone).                                                                                                    |



 

 

 



