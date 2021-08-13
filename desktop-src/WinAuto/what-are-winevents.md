---
title: O que são WinEvents
description: Os aplicativos de servidor e o sistema operacional usam o WinEvents para notificar os clientes quando uma alteração ocorre no sistema ou na interface do usuário.
ms.assetid: 43723706-a173-4ddc-b135-824a7a8e8b40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87c177183fa776a6becf52d62b86fe0ae6785c5be19dd287324ba3345b586af5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563507"
---
# <a name="what-are-winevents"></a>O que são WinEvents?

Os aplicativos de servidor e o sistema operacional usam o WinEvents para notificar os clientes quando uma alteração ocorre no sistema ou na interface do usuário.

o suporte a WinEvent é um recurso do sistema operacional Windows que fornece:

-   Uma maneira simples para os clientes se registrarem para notificações de eventos.
-   Um mecanismo para injetar código de cliente em servidores.
-   Roteamento de eventos de servidores para clientes interessados.
-   Geração automática de eventos para a maioria dos controles baseados em **HWND**.

A geração de eventos para controles baseados em **HWND** é especialmente importante para os desenvolvedores de servidor. O tempo de execução da Microsoft Acessibilidade Ativa fornece proxies do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para todos os elementos padrão da interface do usuário. Da mesma forma, o sistema gera automaticamente o WinEvents apropriado sempre que ele cria, destrói, move, redimensiona ou executa qualquer outra ação em um controle baseado em **HWND**.

Alguns WinEvents, incluindo eventos **HWND** gerais, são automaticamente suportados pelo sistema. Outros tipos de WinEvents, como alterações de estado ou eventos de seleção específicos de um controle específico, têm suporte dos servidores Microsoft Acessibilidade Ativa.

Quando ocorre um evento que afeta a interface do usuário, os servidores podem transmitir uma notificação de eventos para todos os clientes interessados chamando a função [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) . A chamada de função inclui informações que identificam o tipo de evento que ocorreu e o elemento de interface do usuário ao qual o evento se aplica. Os clientes podem usar essas informações para recuperar um objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para o elemento de interface do usuário e coletar mais informações.

Por exemplo, para notificar os clientes de que o nome de um controle foi alterado, um servidor chama [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) e passa o [**objeto de evento \_ \_ NAMECHANGE**](event-constants.md) no parâmetro de evento. O sistema responde determinando quais clientes registraram para receber esse evento em particular e chama a função de retorno de chamada registrada. Se nenhum cliente tiver se registrado para o evento, a chamada do servidor para **NotifyWinEvent** será comparável a "nenhuma operação" e o impacto no desempenho será insignificante.

Os servidores chamam [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) para anunciar o evento para o sistema após a ocorrência do evento. Eles nunca devem notificar o sistema de um evento antes que o evento ocorra.

Para ser notificado de eventos, os clientes registram funções de gancho de retorno de chamada usando [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook). Os clientes definem uma função de gancho único para todos os eventos possíveis ou várias funções de gancho para intervalos discretos de eventos. Para obter mais informações, consulte [registrando uma função de gancho](registering-a-hook-function.md).

Quando o Microsoft Acessibilidade Ativa é notificado de um evento, ele chama qualquer função de gancho que foi registrada para esse evento, passando os parâmetros de [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent).

 

 




