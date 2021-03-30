---
title: API de anotação dinâmica
description: A API de anotação dinâmica é uma extensão do Microsoft Acessibilidade Ativa que permite aos desenvolvedores personalizar o suporte do IAccessible existente sem precisar usar a subclasse ou as técnicas de encapsulamento propensos a erros.
ms.assetid: 2daf0e76-b300-47e7-994b-d1d00d0dca4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7f73c1da79784fdd86652128b572fd81904023c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916646"
---
# <a name="dynamic-annotation-api"></a>API de anotação dinâmica

A API de anotação dinâmica é uma extensão do Microsoft Acessibilidade Ativa que permite aos desenvolvedores personalizar o suporte do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) existente sem precisar usar a subclasse ou as técnicas de encapsulamento propensos a erros. Esse mecanismo também permite que os desenvolvedores transmitam dicas ou outras informações úteis para os proxies de Oleacc.dll.

A anotação dinâmica normalmente é usada para corrigir ou corrigir uma instância imprecisa de um objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) exposto por um proxy de Oleacc.dll existente. Por exemplo, você pode usá-lo para substituir as propriedades de [**nome**](name-property.md) e [**função**](role-property.md) fornecidas pelo proxy padrão e para fornecer as propriedades [**Description**](description-property.md) e [**Help**](help-property.md) (que podem não ser fornecidas pelo proxy padrão).

Com o Windows 7, os desenvolvedores podem usar a API de anotação dinâmica para anotar as propriedades de automação da interface do usuário da Microsoft, bem como as propriedades do Microsoft Acessibilidade Ativa dos objetos de proxy que Oleacc.dll cria para controles padrão do Windows. Os objetos de proxy de Oleacc.dll servem para clientes de automação da interface do usuário e do Microsoft Acessibilidade Ativa.

## <a name="in-this-section"></a>Nesta seção

-   [Informações gerais](background-information.md)
-   [Alternativas para anotação dinâmica](alternatives-to-dynamic-annotation.md)
-   [Tipos de anotação dinâmica](types-of-dynamic-annotation.md)
-   [Anotação direta](direct-annotation.md)
-   [Anotação de mapa de valor](value-map-annotation.md)
-   [Anotação do servidor](server-annotation.md)
-   [Problemas e limitações](issues-and-limitations.md)

 

 




