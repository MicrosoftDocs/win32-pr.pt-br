---
title: API de Anotação Dinâmica
description: A API de Anotação Dinâmica é uma extensão para Microsoft Active Accessibility que permite que os desenvolvedores personalizem o suporte de IAccessible existente sem precisar usar técnicas de subclasse ou de empacotamento propensas a erros.
ms.assetid: 2daf0e76-b300-47e7-994b-d1d00d0dca4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca8b95d1175d4a6bd894e79c55f6798a73165fab2d6e6da40e3b952e68824d50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115316"
---
# <a name="dynamic-annotation-api"></a>API de Anotação Dinâmica

A API de Anotação Dinâmica é uma extensão para Microsoft Active Accessibility que permite que os desenvolvedores personalizem o suporte [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) existente sem a necessidade de usar técnicas de subclasse ou de empacotamento propensas a erros. Esse mecanismo também permite que os desenvolvedores passem dicas ou outras informações úteis para os Oleacc.dll proxies.

A Anotação Dinâmica normalmente é usada para corrigir ou corrigir uma instância imprecisa de um objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) exposto por um proxy Oleacc.dll existente. Por exemplo, você pode usá-lo [](role-property.md) para substituir as propriedades Nome [](description-property.md) e [](help-property.md) Função fornecidas pelo proxy padrão e para fornecer propriedades de Descrição e Ajuda (que podem não ser fornecidas pelo proxy padrão). [](name-property.md)

Com Windows 7, os desenvolvedores podem usar a API de Anotação Dinâmica para anotar as propriedades do Microsoft Automação da Interface do Usuário, bem como Microsoft Active Accessibility propriedades dos objetos proxy que o Oleacc.dll cria para controles Windows padrão. Os Oleacc.dll proxy de dados atendem Microsoft Active Accessibility e Automação da Interface do Usuário clientes.

## <a name="in-this-section"></a>Nesta seção

-   [Informações gerais](background-information.md)
-   [Alternativas à Anotação Dinâmica](alternatives-to-dynamic-annotation.md)
-   [Tipos de anotação dinâmica](types-of-dynamic-annotation.md)
-   [Anotação direta](direct-annotation.md)
-   [Anotação do mapa de valor](value-map-annotation.md)
-   [Anotação do servidor](server-annotation.md)
-   [Problemas e limitações](issues-and-limitations.md)

 

 




