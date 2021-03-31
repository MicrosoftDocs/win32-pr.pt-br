---
title: Como Acessibilidade Ativa funciona
description: O Microsoft Acessibilidade Ativa foi projetado para ajudar os auxílios de acessibilidade, chamados de clientes, a interagir com elementos de interface do usuário padrão e personalizados de outros aplicativos e o sistema operacional.
ms.assetid: 29325f0a-c6ca-42b1-b85d-2671f7041034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdeffcebd96ffba804bfc24672bf867028e9b0c7
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "103823540"
---
# <a name="how-active-accessibility-works"></a>Como Acessibilidade Ativa funciona

O Microsoft Acessibilidade Ativa foi projetado para ajudar os auxílios de acessibilidade, chamados de *clientes*, a interagir com elementos de interface do usuário padrão e personalizados de outros aplicativos e o sistema operacional. Um cliente do Microsoft Acessibilidade Ativa é qualquer programa que usa o Microsoft Acessibilidade Ativa para acessar, identificar ou manipular os elementos da interface do usuário de um aplicativo. Os clientes incluem auxílios de acessibilidade, ferramentas de teste automatizadas e alguns aplicativos de treinamento baseados em computador.

Usando o Microsoft Acessibilidade Ativa, um aplicativo cliente pode:

-   Consultar informações; por exemplo, sobre um elemento de interface do usuário em um local específico.
-   Receber notificações quando as informações forem alteradas; por exemplo, quando um controle torna-se acinzentado ou quando uma cadeia de texto é alterada.
-   Executar ações que afetam o conteúdo da interface do usuário ou do documento; por exemplo, clique em um botão de ação, menu suspenso e escolha um comando de menu.

Os aplicativos que interagem com e fornecem informações para clientes são chamados de *servidores*. Um servidor usa o Microsoft Acessibilidade Ativa para fornecer informações sobre seus elementos de interface do usuário aos clientes. Qualquer controle, módulo ou aplicativo que usa o Microsoft Acessibilidade Ativa para expor informações sobre sua interface do usuário é considerado um Microsoft Acessibilidade Ativa Server. Os servidores se comunicam com clientes enviando notificações de eventos (como chamar [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)) e respondendo a solicitações de clientes para acesso a elementos da interface do usuário (como o tratamento de mensagens do [**WM \_ GetObject**](wm-getobject.md) enviadas do [*OLEACC*](uiauto-glossary.md)). Os servidores expõem informações por meio da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

Usando o Microsoft Acessibilidade Ativa, um aplicativo de servidor pode:

-   Forneça informações sobre seus objetos de interface do usuário personalizados e o conteúdo de suas janelas cliente.
-   Enviar notificações quando a interface do usuário for alterada.

Por exemplo, para permitir que um usuário selecione comandos de forma verbal em uma barra de ferramentas personalizada do processador de texto, um programa de reconhecimento de fala deve ter informações sobre essa barra de ferramentas. Portanto, o processador de texto precisaria disponibilizar essas informações. O Microsoft Acessibilidade Ativa fornece os meios para o processador de texto expor informações sobre sua barra de ferramentas personalizada e para que o programa de reconhecimento de fala obtenha essas informações.

### <a name="client-applications-and-active-accessibility"></a>Aplicativos cliente e Acessibilidade Ativa

Um cliente Microsoft Acessibilidade Ativa deve ser notificado quando a interface do usuário do servidor for alterada para que possa transmitir essas informações ao usuário. Para garantir que o cliente seja informado sobre as alterações da interface do usuário, ele usa um mecanismo chamado eventos de janela, ou WinEvents, para se registrar para receber notificações. Para obter mais informações, consulte [WinEvents](winevents-infrastructure.md).

Para saber mais e manipular um determinado elemento de interface do usuário, os clientes usam a interface COM (Microsoft Acessibilidade Ativa Component Object Model), o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).

Um cliente pode recuperar um objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para um elemento de interface do usuário das quatro maneiras a seguir:

-   Chame [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) e passe o identificador de janela do elemento de interface do usuário.
-   Chame [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) e passe um local de tela que esteja dentro do retângulo delimitador do elemento de interface do usuário.
-   Defina um gancho WinEvent, receba uma notificação e chame [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) para recuperar um ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para o elemento de interface do usuário que gerou o evento.
-   Chame um método [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) como [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) ou [**Get \_ AccParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) para mover para um objeto **IAccessible** diferente.

 

 




