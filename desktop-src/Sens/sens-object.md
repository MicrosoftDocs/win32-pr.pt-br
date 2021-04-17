---
description: O serviço de notificação de eventos do sistema (SENS) define a coclasse SENS como parte da biblioteca de tipos do SENS.
ms.assetid: b494808c-1116-47ac-8713-0d515b312368
title: Objeto SENS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e9d0d5cd857063d6ac224de66610d2604db619d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754946"
---
# <a name="sens-object"></a>Objeto SENS

O serviço de notificação de eventos do sistema (SENS) define a coclasse SENS como parte da biblioteca de tipos do SENS.

## <a name="implementation"></a>Implementação

A implementação do objeto SENS é fornecida pelo sistema operacional.

## <a name="creationaccess-functions"></a>Funções de criação/acesso



| Função                                      | Descrição                                             |
|-----------------------------------------------|---------------------------------------------------------|
| [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) | Cria uma instância do objeto SENS usando seu CLSID. |



 

## <a name="interfaces"></a>Interfaces



| Interface                            | Descrição                                                                                         |
|--------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**IsensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork) | Padrão. Interface de saída implementada pelo objeto de coletor no aplicativo de assinante.                   |
| [**IsensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)     | Interface de saída implementada pelo objeto de coletor no aplicativo de assinante.                            |
| [**IsensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)     | Interface de saída implementada pelo objeto de coletor no aplicativo de assinante.                            |
| [**IsensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2)   | Interface de saída implementada pelo objeto de coletor no aplicativo de assinante. Disponível com o Windows XP. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)
</dt> <dt>

[**ISensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork)
</dt> <dt>

[**ISensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)
</dt> <dt>

[Sobre o serviço de notificação de eventos do sistema](about-system-event-notification-service.md)
</dt> </dl>

 

 
