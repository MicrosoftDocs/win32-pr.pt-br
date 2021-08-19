---
title: O que são objetos proxy
description: Um objeto proxy atua como um intermediário entre o cliente e um objeto acessível. A finalidade do objeto proxy é monitorar o período de vida do objeto acessível e encaminhar chamadas para o objeto acessível somente se ele não for destruído.
ms.assetid: fdd5d44a-1797-47e6-8044-37dde926c18a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caf3625bf048241e4ef28163ed3b8ca7916ccc35cccc12e7eac05b2b9b9c96d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052184"
---
# <a name="what-are-proxy-objects"></a>O que são objetos proxy?

Um objeto *proxy* atua como um intermediário entre o cliente e um objeto acessível. A finalidade do objeto proxy é monitorar o período de vida do objeto acessível e encaminhar chamadas para o objeto acessível somente se ele não for destruído.

Quando um cliente chama uma propriedade [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para obter informações sobre um objeto, o objeto proxy deve verificar se o objeto acessível ainda está disponível. Se for, o objeto proxy passará a solicitação do cliente para o objeto acessível. Se o objeto acessível for destruído (por exemplo, quando uma caixa de diálogo com controles personalizados for fechada), o objeto proxy retornará um erro. Para indicar que o objeto foi destruído, é recomendável que os servidores retornem o código de erro **co \_ E \_ OBJNOTCONNECTED** , pois esse erro é RETORNADO por Component Object Model (com) depois que um servidor chama o [CoDisconnectObject](/windows/win32/api/combaseapi/nf-combaseapi-codisconnectobject).

O objeto proxy é transparente para o cliente. Quando o cliente chama [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)ou [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), ele recebe um ponteiro de volta para uma interface do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . No entanto, quando o cliente usa esse ponteiro para chamar qualquer uma das propriedades ou métodos do **IAccessible** , o código executado está dentro do objeto proxy.

 

 