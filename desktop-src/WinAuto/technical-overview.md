---
title: Visão geral técnica
description: O Microsoft Acessibilidade Ativa melhora a maneira como os recursos de acessibilidade (programas especializados que ajudam as pessoas com deficiências a usar computadores com mais eficiência) funcionam com aplicativos em execução no Microsoft Windows.
ms.assetid: d71ef40e-4c58-4ee6-8909-04ff4f8d20d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4e2bfd984dce863a2bdcdbd41d7b3d72b521861177bc4086a93eb578eb71c5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118325144"
---
# <a name="technical-overview"></a>Visão geral técnica

O Microsoft Acessibilidade Ativa melhora a maneira como os recursos de acessibilidade (programas especializados que ajudam as pessoas com deficiências a usar computadores com mais eficiência) funcionam com aplicativos em execução no Microsoft Windows.

O Microsoft Acessibilidade Ativa é baseado no Component Object Model (COM), que foi desenvolvido pela Microsoft e é um padrão da indústria que define uma maneira comum para que aplicativos e sistemas operacionais se comuniquem. O Microsoft Acessibilidade Ativa consiste nos seguintes componentes:

-   O [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)da interface com, que expõe informações sobre elementos da interface do usuário. O **IAccessible** também tem propriedades e métodos para obter informações sobre e manipular esse elemento de interface do usuário.
-   WinEvents, um sistema de eventos que permite que os servidores Notifiquem os clientes quando um objeto acessível é alterado.
-   Oleacc.dll, uma DLL de suporte ou de tempo de execução.

A DLL do Microsoft Acessibilidade Ativa, Oleacc.dll, consiste nos seguintes componentes:

-   Funções que permitem que os clientes solicitem um ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (por exemplo, [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)).
-   Funções que permitem que os servidores retornem um ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para um cliente (por exemplo, [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)).
-   Funções para obter texto localizado para os códigos de função e de estado (por exemplo, [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) e [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta)).
-   Algumas funções auxiliares ([**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)).
-   Código que fornece a implementação padrão do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para controles de usuário e COMCTL padrão. Como eles implementam o **IAccessible** em nome dos controles do sistema, eles são conhecidos como *proxies*.

## <a name="in-this-section"></a>Nesta seção

-   [Como Acessibilidade Ativa funciona](how-active-accessibility-works.md)
-   [Noções básicas do Acessibilidade Ativa](active-accessibility-basics.md)
-   [Diretrizes do servidor](server-guidelines.md)
-   [Diretrizes do cliente](client-guidelines.md)
-   [Diretrizes de COM e Unicode](com-and-unicode-guidelines.md)

 

 




