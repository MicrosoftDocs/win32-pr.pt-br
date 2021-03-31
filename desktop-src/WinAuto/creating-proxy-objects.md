---
title: Criando objetos de proxy
description: Além de criar classes que implementam Propriedades e métodos do IAccessible, os desenvolvedores de servidores também podem precisar criar objetos de proxy que monitorem a vida útil de objetos acessíveis.
ms.assetid: d140206a-9918-438b-96bd-df141da2f04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e005af4f02430376bc013a45c68cdecef8c0feba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635253"
---
# <a name="creating-proxy-objects"></a>Criando objetos de proxy

Além de criar classes que implementam Propriedades e métodos do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , os desenvolvedores de servidores também podem precisar criar objetos de *proxy* que monitorem a vida útil de objetos acessíveis. Se um objeto acessível em um aplicativo estiver disponível todo o tempo em que o aplicativo está sendo executado, você não precisará criar um objeto proxy. Se for possível destruir o objeto acessível enquanto o aplicativo estiver em execução, você deverá criar um objeto proxy.

## <a name="in-this-section"></a>Nesta seção

-   [O que são objetos proxy?](what-are-proxy-objects.md)
-   [Por que os objetos proxy são necessários](why-proxy-objects-are-needed.md)
-   [Considerações de design para objetos de proxy](design-considerations-for-proxy-objects.md)

 

 




