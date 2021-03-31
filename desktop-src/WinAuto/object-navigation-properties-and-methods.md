---
title: Propriedades e métodos de navegação de objeto
description: Os clientes navegam de um objeto para outro usando métodos como IAccessible accNavigate e IAccessible accHitTest.
ms.assetid: c6bcd044-bf70-4eec-92ae-66f9bd836c33
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e7645d5179015280fd40f6618722191e588c74a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916169"
---
# <a name="object-navigation-properties-and-methods"></a>Propriedades e métodos de navegação de objeto

Os clientes *navegam* de um objeto para outro usando métodos como [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) e [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest). Esses métodos permitem que os clientes recuperem uma ID filho ou o endereço da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de outro objeto. A navegação permite que os clientes explorem como os objetos estão relacionados entre si. Observe que navegar para outro objeto não altera a seleção ou o foco.

A interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) fornece propriedades e métodos que dão suporte aos seguintes tipos de navegação:

-   [Navegação hierárquica](hierarchical-navigation.md)
-   [Navegação espacial e lógica](spatial-and-logical-navigation.md)
-   [Navegação por meio de teste de clique e local da tela](navigation-through-hit-testing-and-screen-location.md)

 

 




