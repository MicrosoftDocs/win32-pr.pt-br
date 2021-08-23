---
title: Diretrizes do servidor
description: Para Microsoft Active Accessibility funcionar como projetado, os servidores devem fornecer informações de acessibilidade aos clientes.
ms.assetid: 88be4bae-fdeb-467c-b5b1-19f2adc0575d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b92d70a33dc8d397ff84fc3b9901dba044741d3044f6a7b7f6d1226aa5b683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614546"
---
# <a name="server-guidelines"></a>Diretrizes do servidor

Para Microsoft Active Accessibility funcionar como projetado, os servidores devem fornecer informações de acessibilidade aos clientes.

Para implementar [**o IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)os desenvolvedores de servidor devem seguir esse processo básico.

1.  Crie objetos acessíveis implementando as propriedades e métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para seus elementos de interface do usuário personalizados e para o cliente do aplicativo. Forneça uma interface dupla que dê suporte a **IAccessible** e [**IDispatch**](idispatch-interface.md) para que os clientes escritos no Microsoft Visual Basic e em várias linguagens de script possam obter informações sobre os objetos.
2.  Chame [**NotifyWinEvent para**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) notificar os clientes sobre alterações nos elementos de interface do usuário personalizados.
3.  Manipular [**WM \_ GETOBJECT**](wm-getobject.md) para fornecer acesso aos seus objetos acessíveis.

Para sugestões e diretrizes para a criação de objetos acessíveis, consulte Guia do desenvolvedor [para Acessibilidade Ativa Servidores](developer-s-guide-for-active-accessibility-servers.md).

## <a name="in-this-section"></a>Nesta seção

-   [Como os servidores implementam IDs filho](how-servers-implement-child-ids.md)

 

 




