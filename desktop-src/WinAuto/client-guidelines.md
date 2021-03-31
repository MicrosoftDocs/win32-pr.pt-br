---
title: Diretrizes do cliente
description: Os desenvolvedores de cliente devem usar a seguinte funcionalidade para obter informações sobre os elementos da interface do usuário
ms.assetid: 0e102e60-4d11-490e-88d5-dfadba620781
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ced411c24ed0b7aa3ab97cbe1ce2511d4e6b05
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "103916939"
---
# <a name="client-guidelines"></a>Diretrizes do cliente

Os desenvolvedores de cliente devem usar a seguinte funcionalidade para obter informações sobre os elementos da interface do usuário:

-   Para obter uma interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para objetos, chame [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)ou [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).
-   Para examinar e manipular objetos acessíveis, use as propriedades e os métodos do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .
-   Para receber [WinEvents](winevents-overview.md), chame [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) para registrar uma função de retorno de chamada WinEvent para os eventos que são relevantes para o aplicativo cliente.

## <a name="in-this-section"></a>Nesta seção

-   [Como os clientes obtêm IDs filho](how-clients-obtain-child-ids.md)

 

 




