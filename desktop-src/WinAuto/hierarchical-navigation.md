---
title: Navegação hierárquica
description: Geralmente, os clientes devem se mover entre objetos com base em suas relações pai-filho. Por exemplo, um cliente pode já ter informações sobre um controle de barra de ferramentas, mas não tem informações sobre os botões contidos nele.
ms.assetid: 7adf803c-140a-4f7d-8dc5-71abca706800
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c48ae366f2dd1caba4dfa6ff69aa1f57a23cbf07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159792"
---
# <a name="hierarchical-navigation"></a>Navegação hierárquica

Geralmente, os clientes devem se mover entre objetos com base em suas relações pai-filho. Por exemplo, um cliente pode já ter informações sobre um controle de barra de ferramentas, mas não tem informações sobre os botões contidos nele.

A interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) expõe as relações hierárquicas entre objetos. Os clientes podem navegar de um objeto pai para seus filhos ou de um objeto filho para seu pai chamando [**IAccessible:: get \_ AccParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) ou [**IAccessible:: get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild).

 

 




