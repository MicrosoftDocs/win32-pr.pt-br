---
title: Diretrizes do cliente
description: Os desenvolvedores de cliente devem usar a seguinte funcionalidade para obter informações sobre os elementos da interface do usuário
ms.assetid: 0e102e60-4d11-490e-88d5-dfadba620781
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d3cfa9a269d796d7071b2107bba2fde6717f42928b9c9dc8074f94afbdbe15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133939"
---
# <a name="client-guidelines"></a>Diretrizes do cliente

Os desenvolvedores de cliente devem usar a seguinte funcionalidade para obter informações sobre os elementos da interface do usuário:

-   Para obter uma interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para objetos, chame [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)ou [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).
-   Para examinar e manipular objetos acessíveis, use as propriedades e os métodos do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .
-   Para receber [WinEvents](winevents-overview.md), chame [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) para registrar uma função de retorno de chamada WinEvent para os eventos que são relevantes para o aplicativo cliente.

## <a name="in-this-section"></a>Nesta seção

-   [Como os clientes obtêm IDs filho](how-clients-obtain-child-ids.md)

 

 




