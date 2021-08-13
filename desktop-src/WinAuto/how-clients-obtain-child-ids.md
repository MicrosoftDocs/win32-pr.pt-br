---
title: Como os clientes obtêm IDs filho
description: Como os clientes obtêm IDs filho
ms.assetid: 8e5786fe-5123-4262-b0b8-5c9aff4787bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78a12dc3f40c2aaa776c1fa8e61713c52ffbdcde554c9f6a1cbca7093998780c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119388596"
---
# <a name="how-clients-obtain-child-ids"></a>Como os clientes obtêm IDs filho

Os desenvolvedores de cliente podem obter a ID filho de um objeto das seguintes maneiras:

-   Chame [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren). Essa função recupera uma matriz de estruturas [**Variant**](variant-structure.md) .
-   Consulte o objeto para ver se ele dá suporte à interface [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) . Se estiver presente, use [**IEnumVARIANT:: Next**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ienumvariant-next) obter IDs filho.
-   Colete as IDs filho chamando o método [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) do objeto pai.

> [!Note]  
> É responsabilidade do cliente liberar a memória usada para as estruturas de [**variante**](variant-structure.md) . Os clientes também devem chamar [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em qualquer interface [**IDispatch**](idispatch-interface.md) retornada.

 

 

 