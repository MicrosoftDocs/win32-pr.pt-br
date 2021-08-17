---
title: Usando a interface IAccessible
description: A interface IAccessible é uma coleção de métodos que expõem os atributos e comportamentos mais comuns de uma ampla gama de elementos de interface do usuário.
ms.assetid: 82f6e934-58ea-47f2-98a3-2ab1c20f24c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c683e83928db53894c7c2c22976a5cf58c402c241e698dca5248230b1b24177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744891"
---
# <a name="using-the-iaccessible-interface"></a>Usando a interface IAccessible

A interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) é uma coleção de métodos que expõem os atributos e comportamentos mais comuns de uma ampla gama de elementos de interface do usuário. Um elemento de interface do usuário é um controle, como um menu ou botão de ação, que faz parte da interface do usuário. Um objeto acessível é um elemento de interface do usuário que tem uma interface de **IAccessible** significativa.

Algumas das propriedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) não são aplicáveis a todos os tipos de elemento de interface do usuário. Além disso, a implementação do **IAccessible** varia de aplicativo para aplicativo.

Embora os parâmetros e valores de retorno para as propriedades e métodos do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) sejam totalmente especificados, como um cliente deve usar uma propriedade ou como um servidor deve implementar uma propriedade, às vezes, está sujeito à interpretação.

Esta seção fornece sugestões, diretrizes e exemplos para ajudar aplicativos cliente a obter informações sobre elementos de interface do usuário e para ajudar aplicativos de servidor a fornecer informações apropriadas.

## <a name="in-this-section"></a>Nesta seção

-   [Conteúdo de propriedades descritivas](content-of-descriptive-properties.md)
-   [Propriedades e métodos de seleção e foco](selection-and-focus-properties-and-methods.md)
-   [Propriedades e métodos de navegação de objeto](object-navigation-properties-and-methods.md)

 

 




