---
title: Tipos de suporte de IAccessible
description: Tipos de suporte de IAccessible
ms.assetid: 4a61d9a4-3c05-4f12-bdf1-426223b679b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fb38ed0b5f7a306f2551085c77f77a3793efec3bc9281cd44d1d7277abe81fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993976"
---
# <a name="types-of-iaccessible-support"></a>Tipos de suporte de IAccessible

Microsoft Active Accessibility servidores têm dois tipos de [**suporte de IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativo e protegido. Os elementos de interface do usuário usados em um aplicativo determinam qual tipo de suporte é apropriado. Muitos servidores que estão sendo escritos hoje aproveitam ao máximo os proxies **IAccessible** e implementam somente **IAccessible** para esses controles que não são protegidos pelo Oleacc.dll, como controles sem janela ou controles com um nome de classe de janela personalizado.

## <a name="in-this-section"></a>Nesta seção

-   [Implementação Acessibilidade Ativa nativa](native-active-accessibility-implementation.md)
-   [IAccessible Proxies](iaccessible-proxies.md)

 

 




