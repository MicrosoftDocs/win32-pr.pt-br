---
title: Como os clientes obtêm IDs filho
description: Como os clientes obtêm IDs filho
ms.assetid: 8e5786fe-5123-4262-b0b8-5c9aff4787bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a67322a80a00c7cc65463ef50e5d1b470fc0b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641205"
---
# <a name="how-clients-obtain-child-ids"></a>Como os clientes obtêm IDs filho

Os desenvolvedores de cliente podem obter a ID filho de um objeto das seguintes maneiras:

-   Chame [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren). Essa função recupera uma matriz de estruturas [**Variant**](variant-structure.md) .
-   Consulte o objeto para ver se ele dá suporte à interface [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) . Se estiver presente, use [**IEnumVARIANT:: Next**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ienumvariant-next) obter IDs filho.
-   Colete as IDs filho chamando o método [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) do objeto pai.

> [!Note]  
> É responsabilidade do cliente liberar a memória usada para as estruturas de [**variante**](variant-structure.md) . Os clientes também devem chamar [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em qualquer interface [**IDispatch**](idispatch-interface.md) retornada.

 

 

 