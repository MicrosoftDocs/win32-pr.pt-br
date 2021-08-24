---
title: Visão geral de WinEvents e Acessibilidade Ativa
description: Os servidores do Microsoft Acessibilidade Ativa geram WinEvents para notificar os clientes quando um objeto acessível é alterado.
ms.assetid: a2d486ee-84ef-4c44-a832-dbc0dae81542
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95507ff1b6cd56451dd7f9acc04014c6013a7179d536565b3518bccb9137e689
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052174"
---
# <a name="winevents-and-active-accessibility"></a>WinEvents e Acessibilidade Ativa

Os servidores do Microsoft Acessibilidade Ativa geram *WinEvents* para notificar os clientes quando um objeto acessível é alterado. Há várias condições em que um servidor notifica um cliente sobre uma alteração. Cada [constante de evento](event-constants.md) definida pelo Microsoft acessibilidade ativa descreve uma condição sobre a qual um cliente é notificado. Por exemplo, WinEvents pode sinalizar:

- Quando um objeto é criado ou destruído.
- Quando um objeto recebe ou perde o foco.
- Quando o estado ou o local de um objeto é alterado.
- Quando qualquer propriedade de um objeto é alterada.

Os aplicativos cliente não recebem notificações de eventos automaticamente; Eles devem especificar quais eventos eles desejam receber chamando a função [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) . Com o **SetWinEventHook**, um cliente registra para receber um ou mais eventos e define uma função de Hook para manipular os eventos especificados. Os clientes podem usar a mesma função de gancho para lidar com vários tipos de eventos ou podem usar funções de gancho multipe. Os clientes chamam o **SetWinEventHook** uma vez para cada função de gancho que precisa registrar.

As funções de gancho estão localizadas no corpo do código do cliente, em uma DLL mapeada no processo do cliente ou em uma DLL mapeada no processo do servidor. Cada um desses métodos tem vantagens e desvantagens. Para obter mais informações, consulte [funções de gancho em contexto e fora de contexto](in-context-and-out-of-context-hook-functions.md).

Para notificar os clientes sobre uma ocorrência de evento, os servidores chamam [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent). O sistema verifica se algum aplicativo cliente definiu funções de gancho para o evento e chama as funções de gancho apropriadas conforme necessário.

Quando a função de gancho do cliente é chamada, ela recebe um número de parâmetros que descrevem o evento e o objeto que gerou o evento. Para obter acesso ao objeto que gerou o evento, a função de gancho do cliente chama [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).

> [!NOTE]
> Se nenhum cliente tiver se registrado para receber WinEvents, o impacto no desempenho em um servidor para chamar [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) será insignificante.
>
> Os servidores chamam [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) para alterações somente em seus próprios objetos acessíveis; Eles não chamam **NotifyWinEvent** para alterações nos elementos da interface do usuário fornecidos pelo sistema.

## <a name="event-driven-communication"></a>Event-Driven comunicação

Os clientes devem registrar um gancho de WinEvent antes que possam receber notificações de WinEvent. Para evitar retornos de chamada desnecessários e melhorar o desempenho, os clientes são aconselhados a registrar somente os eventos que precisam receber.

Dentro do procedimento de gancho, o cliente pode chamar [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) para recuperar um objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para o elemento ao qual o evento se aplica. Com esse objeto, o cliente pode começar a chamar métodos de **IAccessible** para recuperar informações ou interagir com o elemento de interface do usuário.

## <a name="related-topics"></a>Tópicos relacionados

[WinEvents](winevents-infrastructure.md)
