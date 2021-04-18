---
description: Descrição do uso da acessibilidade ativa para expor controles personalizados para o Tablet PC.
ms.assetid: 1557bde2-c382-4259-ae0c-a70902fa91bd
title: Usando Acessibilidade Ativa para expor controles personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d33d4c2b57a881cfbdc15f14e71e339ed7f9e84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810869"
---
# <a name="using-active-accessibility-to-expose-custom-controls"></a>Usando Acessibilidade Ativa para expor controles personalizados

Você pode usar o Microsoft Acessibilidade Ativa como uma maneira eficaz de tornar os controles personalizados compatíveis com os recursos de acessibilidade. Acessibilidade Ativa requer que o aplicativo:

-   Crie objetos COM (Component Object Model) que representem controles personalizados individuais ou grupos de controles que dão suporte adequado à interface **IAccessible** . (O objeto pode ser criado sob demanda quando solicitado por um cliente Acessibilidade Ativa.)
-   Chame [**NotifyWinEvent**](/windows/win32/api/winuser/nf-winuser-notifywinevent) quando os controles forem criados ou destruídos, obter ou perder o foco ou alterar o estado.
-   Manipule a mensagem do WM \_ GetObject quando usada para consultar as propriedades do objeto ou dos objetos.

Para os fins desta discussão, uma janela que contém outros objetos personalizados também precisa ser exposta a Acessibilidade Ativa, permitindo que o cliente descubra e navegue para os objetos filho. Para obter mais informações sobre como tornar os controles personalizados compatíveis com os recursos de acessibilidade, consulte [acessibilidade](../accessibility/accessibility.md).

 

 
