---
title: Como Acessibilidade Ativa expõe elementos da interface do usuário
description: O Microsoft Acessibilidade Ativa cria um objeto proxy para cada elemento da interface do usuário que ele expõe.
ms.assetid: 64aa8fac-cea7-4466-ae34-2760956c296b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b450ebe79aa467100fe9b6fb3bc4cdfb5540b60c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159800"
---
# <a name="how-active-accessibility-exposes-user-interface-elements"></a>Como Acessibilidade Ativa expõe elementos da interface do usuário

O Microsoft Acessibilidade Ativa cria um objeto *proxy* para cada elemento da interface do usuário que ele expõe. Um objeto proxy atua como um intermediário entre o utilitário cliente e o elemento de interface do usuário. A finalidade do objeto de proxy é monitorar o período de vida do elemento de interface do usuário e implementar as propriedades e os métodos do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) em nome do elemento de interface do usuário. Os desenvolvedores de servidores que criam controles personalizados ou outros elementos personalizados da interface do usuário também devem criar objetos proxy. Para obter mais informações, consulte [Creating proxy Objects](creating-proxy-objects.md).

Quando o Microsoft Acessibilidade Ativa cria um objeto para expor um controle predefinido ou comum, ele realmente cria pelo menos dois objetos: um para o controle e outro para a janela que circunda o controle. Na maioria dos casos, essas janelas pai têm a [Propriedade Role](role-property.md) da [**janela do \_ sistema \_ de função**](object-roles.md) e têm a mesma [Propriedade Name](name-property.md) e o nome da classe Window que o controle. As informações sobre o controle que os clientes transmitem para os usuários finais estão contidas no objeto que o Microsoft Acessibilidade Ativa cria para expor o controle, não o objeto pai que expõe a janela que circunda o controle.

Para obter mais informações, consulte os tópicos a seguir.

-   [Triagem de objetos desnecessários](screening-out-unnecessary-objects.md)
-   [Fornecendo a propriedade Name](providing-the-name-property.md)
-   [Garantindo que os elementos da interface do usuário sejam nomeados corretamente](ensure-that-ui-elements-are-named-correctly.md)
-   [Elementos de interface do usuário sem suporte](unsupported-user-interface-elements.md)

 

 




