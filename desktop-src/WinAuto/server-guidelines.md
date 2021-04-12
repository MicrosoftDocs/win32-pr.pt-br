---
title: Diretrizes do servidor
description: Para que o Microsoft Acessibilidade Ativa funcione como projetado, os servidores devem fornecer informações de acessibilidade aos clientes.
ms.assetid: 88be4bae-fdeb-467c-b5b1-19f2adc0575d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 344721428c94e2ea3d9e9ff78e194851ba9304db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363763"
---
# <a name="server-guidelines"></a>Diretrizes do servidor

Para que o Microsoft Acessibilidade Ativa funcione como projetado, os servidores devem fornecer informações de acessibilidade aos clientes.

Para implementar o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), os desenvolvedores de servidor devem seguir este processo básico.

1.  Crie objetos acessíveis implementando as propriedades e os métodos do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para seus elementos personalizados de interface do usuário e para o cliente do seu aplicativo. Certifique-se de fornecer uma interface dupla que dê suporte a **IAccessible** e [**IDispatch**](idispatch-interface.md) para que os clientes escritos no Microsoft Visual Basic e várias linguagens de script possam obter informações sobre os objetos.
2.  Chame [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) para notificar os clientes sobre alterações em seus elementos personalizados da interface do usuário.
3.  Manipule o [**WM \_ GetObject**](wm-getobject.md) para fornecer acesso aos seus objetos acessíveis.

Para obter sugestões e diretrizes para a criação de objetos acessíveis, consulte o [Guia do desenvolvedor para servidores de acessibilidade ativa](developer-s-guide-for-active-accessibility-servers.md).

## <a name="in-this-section"></a>Nesta seção

-   [Como os servidores implementam IDs filho](how-servers-implement-child-ids.md)

 

 




