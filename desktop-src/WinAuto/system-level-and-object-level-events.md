---
title: Eventos de System-Level e Object-Level
description: O Microsoft Acessibilidade Ativa usa três classes de nível de sistema WinEvents, nível de objeto e console.
ms.assetid: 3333fe6c-38cd-4e7e-be4b-94c9f824e7e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d14a0469527a7654dd3e323adb47d650866ca9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292039"
---
# <a name="system-level-and-object-level-events"></a>Eventos de System-Level e Object-Level

O Microsoft Acessibilidade Ativa usa três classes de WinEvents: *nível do sistema*, nível de *objeto* e *console*. Cada um tem um dos seguintes valores [constantes de evento](event-constants.md) correspondentes:

-   Constantes de evento que começam com o sistema de eventos \_ identificam eventos no nível do sistema. Esses eventos descrevem situações que afetam todos os aplicativos no sistema.
-   Constantes de evento que começam com o objeto de evento \_ identificam eventos no nível do objeto. Esses eventos pertencem a situações específicas a objetos dentro de um aplicativo.
-   As constantes de evento que começam com o console de eventos \_ identificam eventos no nível do console. Esses eventos indicam alterações nas janelas do console.

As classes de eventos no nível do sistema e do objeto são geradas pelo sistema operacional e pelos aplicativos de servidor. O sistema operacional gera eventos no nível do sistema e do objeto para os seguintes cenários:

-   Notificações em todo o sistema sobre alterações de foco
-   Alterações de ativação
-   Eventos relacionados a objetos fornecidos pelo sistema, como controles comuns

Os aplicativos de servidor geram eventos de nível de sistema para objetos personalizados que replicam objetos do sistema, como menus personalizados e barras de rolagem.

Os aplicativos de servidor normalmente geram eventos de nível de objeto para alterações nos objetos acessíveis que eles contêm, como criação de objeto, destruição e seleção.

Embora o sistema gere eventos de nível de objeto para objetos de [**janela**](window.md) , os servidores também devem enviar eventos de nível de objeto para cada objeto acessível contido em uma janela. Por exemplo, se um aplicativo de servidor registra uma classe de janela definida pelo aplicativo para criar um controle personalizado, o sistema gera eventos de nível de objeto para a janela que contém o controle personalizado; o servidor gera eventos de nível de objeto para o objeto acessível que fornece informações sobre o controle.

Os servidores só geram eventos de nível de objeto para os controles personalizados para os quais implementam a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Para obter mais informações, consulte [elementos personalizados da interface do usuário](custom-user-interface-elements.md).

 

 




