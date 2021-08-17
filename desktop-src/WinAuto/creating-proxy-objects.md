---
title: Criando objetos de proxy
description: Além de criar classes que implementam métodos e propriedades IAccessible, os desenvolvedores de servidor também podem precisar criar objetos proxy que monitoram o período de vida de objetos acessíveis.
ms.assetid: d140206a-9918-438b-96bd-df141da2f04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49abceb3b38b4495d871605634c8f95353c35b4b6bcd0c54dda374c75572fbea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133889"
---
# <a name="creating-proxy-objects"></a>Criando objetos de proxy

Além de criar classes que implementam métodos e propriedades [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) os desenvolvedores de servidor também podem precisar criar objetos *proxy* que monitoram o período de vida de objetos acessíveis. Se um objeto acessível em um aplicativo estiver disponível o tempo todo em que o aplicativo estiver em execução, você não precisará criar um objeto proxy. Se for possível destruir o objeto acessível enquanto o aplicativo estiver em execução, você deverá criar um objeto proxy.

## <a name="in-this-section"></a>Nesta seção

-   [O que são objetos de proxy?](what-are-proxy-objects.md)
-   [Por que os objetos de proxy são necessários](why-proxy-objects-are-needed.md)
-   [Considerações de design para objetos de proxy](design-considerations-for-proxy-objects.md)

 

 




