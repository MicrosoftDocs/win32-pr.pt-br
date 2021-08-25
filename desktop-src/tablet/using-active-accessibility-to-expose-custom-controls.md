---
description: Descrição do uso da acessibilidade ativa para expor controles personalizados para o Tablet PC.
ms.assetid: 1557bde2-c382-4259-ae0c-a70902fa91bd
title: Usando Acessibilidade Ativa para expor controles personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d275b6c5639dddfe60f358427751ad4ff4cd7989923dc4a368b3316b3bfc01e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934316"
---
# <a name="using-active-accessibility-to-expose-custom-controls"></a>Usando Acessibilidade Ativa para expor controles personalizados

Você pode usar Microsoft Active Accessibility como uma maneira eficaz de tornar os controles personalizados compatíveis com os auxílios de acessibilidade. Acessibilidade Ativa requer que o aplicativo:

-   Crie Component Object Model (COM) que representam controles personalizados individuais ou grupos de controles que suportam corretamente a interface **IAccessible.** (O objeto pode ser criado sob demanda quando solicitado por um Acessibilidade Ativa cliente.)
-   Chame [**NotifyWinEvent**](/windows/win32/api/winuser/nf-winuser-notifywinevent) quando os controles são criados ou destruídos, obtenha ou perca o foco ou altere o estado.
-   Manipular a mensagem WM \_ GETOBJECT quando usado para consultar propriedades do objeto ou objetos .

Para os fins desta discussão, uma janela que contém outros objetos personalizados também precisa ser exposta ao Acessibilidade Ativa, permitindo que o cliente descubra e navegue até os objetos filho. Para obter mais informações sobre como tornar controles personalizados compatíveis com auxílios de acessibilidade, consulte [Acessibilidade](../accessibility/accessibility.md).

 

 
