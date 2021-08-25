---
title: Gerando WinEvents apropriado
description: Os desenvolvedores de servidor precisam garantir que os WinEvents apropriados sejam gerados para todos os elementos da interface do usuário, incluindo elementos da interface do usuário baseados em janela, elementos da interface do usuário sem janelas e elementos da interface do usuário com comportamentos altamente personalizados.
ms.assetid: 253e0162-20e6-4e89-b563-aae9cf7e53a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7e148578f55f59d2827fd13a637baf5139c3f934ddf24059e437185c15349b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860386"
---
# <a name="generating-appropriate-winevents"></a>Gerando WinEvents apropriado

Os desenvolvedores de servidor precisam garantir que os WinEvents apropriados sejam gerados para todos os elementos da interface do usuário, incluindo elementos da interface do usuário baseados em janela, elementos da interface do usuário sem janelas e elementos da interface do usuário com comportamentos altamente personalizados.

O usuário fornece suporte padrão de WinEvent para elementos de interface do usuário padrão, com base em **HWND**. Como o usuário gera esses eventos automaticamente, os servidores precisam gerar eventos somente para controles personalizados, elementos sem janela ou controles cujos eventos ainda não são gerados pelo usuário.

Para enviar um evento, os servidores chamam [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) e passam a constante do evento, uma ID de objeto e o **HWND** para uma janela que pode responder às solicitações do cliente para obter mais informações. Os eventos que precisam ser acionados variam de acordo com o tipo de elemento de interface do usuário. Há eventos gerais que devem ser enviados para todos os controles e eventos específicos que devem ser enviados somente para o elemento de interface do usuário apropriado.

## <a name="general-events"></a>Eventos gerais

WinEvents geral podem ser enviados para todos os elementos da interface do usuário. Elas incluem:

-   [**Evento \_ de \_Criação de objeto**](event-constants.md) (quando um objeto é criado)
-   [**Evento \_ de \_Destruição de objeto**](event-constants.md) (quando um objeto é destruído)
-   [**Evento \_ de \_Exibição de objeto**](event-constants.md) (quando um objeto é mostrado)
-   [**Evento \_ de \_Ocultar objeto**](event-constants.md) (quando um objeto estiver oculto)

## <a name="specific-events"></a>Eventos específicos

Também há WinEvents específicos que podem ser enviados para um tipo específico de elemento de interface do usuário. Por exemplo, use [**a \_ \_ seleção de objeto de evento**](event-constants.md) para controles que permitem ao usuário fazer uma seleção, como uma caixa de listagem.

Para obter mais informações sobre quais eventos são esperados para um tipo específico de elemento de interface do usuário, consulte os seguintes recursos:

-   [Apêndice A: referência de elementos da interface do usuário com suporte](appendix-a--supported-user-interface-elements-reference.md). Este apêndice inclui informações sobre elementos de interface do usuário gerados pelo sistema que são expostos pelo Microsoft Acessibilidade Ativa. A documentação de cada controle inclui informações sobre eventos que podem ser gerados pelo elemento de interface do usuário.
-   [Constantes de evento](event-constants.md). Este tópico inclui informações sobre eventos gerados pelo sistema operacional e pelos aplicativos de servidor.
-   Inspetor de eventos acessível (AccEvent.exe). Essa ferramenta mostra quais eventos o usuário envia para um determinado elemento de interface de usuário. Você pode usar essa ferramenta para saber quais eventos você pode esperar para um elemento de interface do usuário. Para obter mais informações, consulte [Inspetor de eventos acessível](accessible-event-watcher.md).

 

 




