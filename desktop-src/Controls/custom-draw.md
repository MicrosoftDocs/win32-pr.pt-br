---
title: Desenho personalizado
description: O desenho personalizado não é um controle comum; é um serviço que muitos controles comuns fornecem.
ms.assetid: vs|controls|~\controls\custdraw\custdraw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16271e915a942e21f3f3763237a25c37a8b934fc1a44a016bb7e3938491a3c66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413174"
---
# <a name="custom-draw"></a>Desenho personalizado

O desenho personalizado não é um controle comum; é um serviço que muitos controles comuns fornecem. O serviço de desenho personalizado permite que um aplicativo tenha maior flexibilidade na personalização da aparência de um controle. Seu aplicativo pode aproveitar notificações de desenho personalizadas para alterar facilmente a fonte usada para exibir itens ou desenhar manualmente um item sem precisar fazer um desenho completo do proprietário.

Esta seção contém informações sobre os elementos de programação usados com desenho personalizado.

## <a name="overviews"></a>Visões gerais



| Tópico                                      | Sumário                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre o desenho personalizado](about-custom-draw.md) | Esta seção contém informações gerais sobre a funcionalidade de desenho personalizada e fornece uma visão geral conceitual de como um aplicativo pode dar suporte ao desenho personalizado.<br/> |
| [Usando o desenho personalizado](using-custom-draw.md) | Esta seção contém exemplos que demonstram como implementar o desenho personalizado. <br/>                                                                              |



 

## <a name="notifications"></a>Notificações



| Tópico                               | Sumário                                                                                                                                                                 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ CUSTOMDRAW](nm-customdraw.md) | Notifica a janela pai de um controle sobre operações de desenho personalizadas. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) <br/> |



 

## <a name="structures"></a>Estruturas



| Tópico                                | Sumário                                                                                              |
|--------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**Nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) | Contém informações específicas para um [código de notificação \_ CUSTOMDRAW NM.](nm-customdraw.md)<br/> |



 

 

 





