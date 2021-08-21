---
title: Como lidar com WM_GETOBJECT
description: Quando ele recebe uma mensagem WM GETOBJECT que contém OBJID CLIENT, o servidor deve retornar um ponteiro para o objeto que implementa \_ \_ IAccessible.
ms.assetid: 455398b7-f748-4ab0-8953-3f74439e44f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f066ee42ffaeee2d585ac5480e5af31acf14c87ba9994d3d338b65e6cf427a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052715"
---
# <a name="how-to-handle-wm_getobject"></a>Como lidar com WM \_ GETOBJECT

Quando ele recebe uma mensagem [**WM \_ GETOBJECT**](wm-getobject.md) que contém [**OBJID \_ CLIENT**](object-identifiers.md), o servidor deve retornar um ponteiro para o objeto que [**implementa IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). Esse ponteiro é um LRESULT obtido chamando [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject). Microsoft Active Accessibility, em conjunto com a biblioteca Component Object Model (COM), executa o marshaling apropriado e passa o ponteiro de interface **IAccessible** do servidor para o cliente.

Os servidores devem lidar corretamente com a contagem de referência no objeto acessível. Lembre-se de que, quando você cria um objeto COM, a contagem de referência é 1. [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) incrementa ainda mais a contagem de referência várias vezes. Todas as referências criadas por **LresultFromObject** são liberadas automaticamente quando o objeto não é mais necessário, mas o servidor é responsável por liberar a referência inicial e, a menos que isso seja feito, o objeto nunca será destruído. Os exemplos nas seções a seguir mostram como liberar referências a objetos acessíveis.

Os servidores normalmente [**lidam com WM \_ GETOBJECT**](wm-getobject.md) de uma das seguintes maneiras:

-   [Criar novos objetos acessíveis](create-new-accessible-objects.md)
-   [Reutilizar ponteiros existentes para objetos](reuse-existing-pointers-to-objects.md)
-   [Criar novas interfaces para o mesmo objeto](create-new-interfaces-to-the-same-object.md)

> [!Note]  
> Nesta seção, como no restante da documentação, quando um ponteiro para uma interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) é discutido, esse ponteiro pode, na verdade, ser um ponteiro para um objeto proxy que envolve a interface **IAccessible.** Para obter mais informações sobre objetos de proxy, consulte [Criando objetos de proxy](creating-proxy-objects.md).

 

Para obter uma visão [**geral do WM \_ GETOBJECT,**](wm-getobject.md)consulte [Como o WM \_ GETOBJECT funciona.](how-wm-getobject-works.md)

 

 




