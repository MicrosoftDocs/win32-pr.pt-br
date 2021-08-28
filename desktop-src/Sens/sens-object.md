---
description: O SENS (Serviço de Notificação de Eventos do Sistema) define a coclasse SENS como parte da biblioteca de tipos SENS.
ms.assetid: b494808c-1116-47ac-8713-0d515b312368
title: Objeto SENS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acdf70b5e2229051d569bd1f607ad8db5d3d567b4c0421464757f02bc6a8e4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003944"
---
# <a name="sens-object"></a>Objeto SENS

O SENS (Serviço de Notificação de Eventos do Sistema) define a coclasse SENS como parte da biblioteca de tipos SENS.

## <a name="implementation"></a>Implementação

A implementação do objeto SENS é fornecida pelo sistema operacional.

## <a name="creationaccess-functions"></a>Funções de criação/acesso



| Função                                      | Descrição                                             |
|-----------------------------------------------|---------------------------------------------------------|
| [**Cocreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) | Cria uma instância do objeto SENS usando seu CLSID. |



 

## <a name="interfaces"></a>Interfaces



| Interface                            | Descrição                                                                                         |
|--------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**IsensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork) | Padrão. Interface de saída implementada pelo objeto sink no aplicativo assinante.                   |
| [**IsensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)     | Interface de saída implementada pelo objeto sink no aplicativo assinante.                            |
| [**IsensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)     | Interface de saída implementada pelo objeto sink no aplicativo assinante.                            |
| [**IsensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2)   | Interface de saída implementada pelo objeto sink no aplicativo assinante. Disponível com o Windows XP. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)
</dt> <dt>

[**ISensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork)
</dt> <dt>

[**ISensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)
</dt> <dt>

[Sobre o Serviço de Notificação de Eventos do Sistema](about-system-event-notification-service.md)
</dt> </dl>

 

 
