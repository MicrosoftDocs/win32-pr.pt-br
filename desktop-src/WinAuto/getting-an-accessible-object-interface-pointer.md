---
title: Obtendo um ponteiro de interface de objeto acessível
description: Os aplicativos cliente do Microsoft Acessibilidade Ativa recuperam ponteiros de interface para objetos acessíveis usando uma das funções a seguir.
ms.assetid: b82467f0-0d46-482a-8f6d-ad64f236601e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28ea0d7936671a68c140c6d22fdc3afdad0db0899c9c2cbc51637dcf36d9ad55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994196"
---
# <a name="getting-an-accessible-object-interface-pointer"></a>Obtendo um ponteiro de interface de objeto acessível

Os aplicativos cliente do Microsoft Acessibilidade Ativa recuperam ponteiros de interface para objetos acessíveis usando uma das funções a seguir.

**AccessibleObjectFromEvent**

Muitos clientes pesquisam informações sobre objetos acessíveis específicos que geram eventos. Como a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) é o "gateway" para objetos acessíveis, os clientes devem ter uma maneira fácil de associar o [WinEvents](winevents-overview.md) à interface **IAccessible** do objeto que gera os eventos. O Microsoft Acessibilidade Ativa fornece a função [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) especificamente para essa finalidade.

> [!Note]  
> Clientes com [funções de gancho no contexto](in-context-hook-functions.md) devem chamar a função [IsWindow](/windows/win32/api/winuser/nf-winuser-iswindow) antes de chamar [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).

 

A função [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) aceita muitas das mesmas informações que a [*função de Hook*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) de um cliente recebe. Quando uma função de gancho de cliente recebe uma notificação de evento, ela passa os parâmetros apropriados de eventos para **AccessibleObjectFromEvent**.

A função recupera a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) do elemento de interface do usuário que gerou o evento ou a interface do objeto pai do elemento. Se o ponteiro de interface do objeto pai for retornado, o cliente chamará as propriedades e os métodos do pai para obter informações sobre o elemento filho que gerou o evento.

**AccessibleObjectFromPoint**

Para recuperar o endereço da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de um objeto em um ponto especificado na tela, os clientes usam a função [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) .

**AccessibleObjectFromWindow**

Para recuperar a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de um objeto de um identificador de janela, os clientes usam a função [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) .

É possível que os servidores retornem ponteiros de interface distintos para o mesmo elemento de interface do usuário cada vez que a função [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)ou [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) for chamada. Para determinar se dois ponteiros se referem ao mesmo elemento de interface do usuário, os desenvolvedores de cliente devem comparar as propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) do objeto, e não os ponteiros.

 

 