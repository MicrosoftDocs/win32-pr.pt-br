---
title: IAccessible Proxies
description: Proxies IAccessible fornecem informações de acessibilidade padrão para elementos de interface do usuário padrão Controles de USUÁRIO, menus USER e controles comuns de COMCTL e COMCTL32.
ms.assetid: 236c2064-de44-4021-8825-f1519312dbfc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7a416c29021aca0dd99356792ae96f6a77e137e8c0ca0c884ba941229dd4b83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566051"
---
# <a name="iaccessible-proxies"></a>IAccessible Proxies

[**Proxies IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) fornecem informações de acessibilidade padrão para elementos de interface do usuário padrão: controles USER, menus USER e controles comuns de COMCTL e COMCTL32. Esse suporte padrão é exposto por meio de **objetos IAccessible** criados pelo Oleacc.dll e oferece suporte Microsoft Active Accessibility sem trabalho adicional de desenvolvimento de servidor. Em seguida, o servidor pode usar a API de [Anotação](dynamic-annotation-api.md) Dinâmica para modificar grande parte das informações expostas pelo Oleacc.dll, mas não tem controle total.

## <a name="creating-a-proxy"></a>Criando um proxy

Para determinar se um elemento de interface do usuário dá suporte nativo à interface [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Oleacc.dll envia uma mensagem [**WM \_ GETOBJECT.**](wm-getobject.md) Um valor de retorno diferente de zero significa que o elemento dá suporte nativo Microsoft Active Accessibility e fornece seu próprio suporte **a IAccessible.** No entanto, se o valor de retorno for zero, Oleacc.dll fornece um objeto proxy para o elemento de interface do usuário e tenta retornar informações significativas em seu nome. Para obter mais informações sobre **o WM \_ GETOBJECT,** consulte [Como o WM \_ GETOBJECT funciona.](how-wm-getobject-works.md)

## <a name="what-information-is-exposed"></a>Quais informações são expostas

Oleacc.dll usa o nome de classe Windows do elemento de interface do usuário para determinar quais informações devem ser expostas para cada uma de suas propriedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e como coletar essas informações. Por exemplo, Oleacc.dll chama a [**função GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) para recuperar a propriedade [**Name**](name-property.md) de um botão de push padrão, mas chama essa mesma função para recuperar a propriedade [**Value**](value-property.md) para um controle de edição padrão. Na verdade, Oleacc.dll está mapeando cada **método IAccessible** para um Microsoft Win32 apropriado ou chamada de função ou mensagem específica de controle. Usando essa caixa de uso especial baseada em nome de classe, ela pode retornar informações significativas por meio de proxies **IAccessible** sem Microsoft Active Accessibility suporte no servidor.

Os aplicativos construídos com elementos de interface do usuário padrão normalmente têm suporte completo Microsoft Active Accessibility sem trabalho de desenvolvimento adicional. As exceções a essa regra são controles que foram subclasses, que não armazenam suas próprias cadeias de caracteres (ausência do estilo **HASSTRINGS)** ou que são desenhados pelo proprietário. Nesses casos, o Oleacc.dll pode coletar as informações necessárias porque as informações são armazenadas fora do controle. No entanto, em muitos desses cenários, soluções alternativas estabelecidas ou o uso da Anotação Dinâmica permitem que o servidor coopera com os proxies fornecidos pelo Oleacc.dll.

## <a name="generic-proxy-objects"></a>Objetos de proxy genéricos

Se Oleacc.dll reconhece o nome de classe do elemento de interface do usuário, ele cria um proxy genérico que expõe o máximo de informações possível. No máximo, isso inclui o retângulo delimitado do objeto, o objeto pai, o nome (do [**WM \_ GETTEXT)**](/windows/desktop/winmsg/wm-gettext)e todos os filhos na hierarquia da janela.

 

 