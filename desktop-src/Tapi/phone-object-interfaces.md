---
description: O objeto de telefone é a entidade que representa o dispositivo de telefone real e todos os seus controles.
ms.assetid: 5bc2f595-8e2b-4938-b813-1574a9390084
title: Interfaces de objeto de telefone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f39b163e895a512e7adc7be5c2fb848c5849361
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788047"
---
# <a name="phone-object-interfaces"></a>Interfaces de objeto de telefone

O objeto de telefone é a entidade que representa o dispositivo de telefone real e todos os seus controles.

As interfaces [**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent) e [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone) não são diretamente expostas no objeto de telefone, mas estão estreitamente relacionadas a ela e estão listadas aqui para sua conveniência de referência.



| Interface                                                  | Descrição                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone)                                 | Permite o acesso ao dispositivo de telefone em um nível comparável ao que está disponível com a TAPI 2. API *x* C.                                      |
| [**ITAutomatedPhoneControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol) | Fornece métodos para o controle automatizado de toques e anéis de um telefone e para tratamento automatizado de chamadas com base no estado Hookswitch de um telefone. |
| [**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent)                       | Recupera a descrição de eventos do telefone.                                                                                                |
| [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone)                           | Enumera [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone).                                                                                                    |



 

 

 



