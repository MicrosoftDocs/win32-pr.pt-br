---
title: Como lidar com WM_GETOBJECT
description: Quando recebe uma \_ mensagem do WM GetObject que contém \_ o cliente OBJID, o servidor deve retornar um ponteiro para o objeto que implementa o IAccessible.
ms.assetid: 455398b7-f748-4ab0-8953-3f74439e44f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6223d75339f537ccf1939f9c9af46a42aa47bfdb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636307"
---
# <a name="how-to-handle-wm_getobject"></a>Como tratar o WM \_ GETobject

Quando recebe uma mensagem do [**WM \_ GetObject**](wm-getobject.md) que contém [**o \_ cliente OBJID**](object-identifiers.md), o servidor deve retornar um ponteiro para o objeto que implementa o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). Esse ponteiro é um LRESULT que é obtido chamando [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject). O Microsoft Acessibilidade Ativa, em conjunto com a biblioteca do Component Object Model (COM), executa o marshaling apropriado e passa o ponteiro da interface **IAccessible** do servidor para o cliente.

Os servidores devem lidar corretamente com a contagem de referência no objeto acessível. Lembre-se de que quando você cria um objeto COM, a contagem de referência é 1. Em seguida, o [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) incrementa a contagem de referência várias vezes. Todas as referências criadas por **LresultFromObject** são liberadas automaticamente quando o objeto não é mais necessário, mas o servidor é responsável por liberar a referência inicial e, a menos que isso seja feito, o objeto nunca será destruído. Os exemplos nas seções a seguir mostram como liberar referências a objetos acessíveis.

Os servidores normalmente tratam do [**WM \_ GetObject**](wm-getobject.md) em uma das seguintes maneiras:

-   [Criar novos objetos acessíveis](create-new-accessible-objects.md)
-   [Reutilizar ponteiros existentes para objetos](reuse-existing-pointers-to-objects.md)
-   [Criar novas interfaces para o mesmo objeto](create-new-interfaces-to-the-same-object.md)

> [!Note]  
> Nesta seção, como no restante da documentação, quando um ponteiro para uma interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) é discutido, esse ponteiro pode, na verdade, ser um ponteiro para um objeto proxy que encapsula a interface **IAccessible** . Para obter mais informações sobre objetos proxy, consulte [Creating proxy Objects](creating-proxy-objects.md).

 

Para obter uma visão geral do [**WM \_ GetObject**](wm-getobject.md), consulte [como o WM \_ GetObject funciona](how-wm-getobject-works.md).

 

 




