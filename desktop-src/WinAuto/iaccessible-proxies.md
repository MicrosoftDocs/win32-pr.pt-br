---
title: Proxies do IAccessible
description: Os proxies do IAccessible fornecem informações de acessibilidade padrão para elementos de interface do usuário padrão, menus de usuário e controles comuns de COMCTL e COMCTL32.
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
# <a name="iaccessible-proxies"></a>Proxies do IAccessible

Os proxies do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) fornecem informações de acessibilidade padrão para elementos da interface do usuário padrão: controles de usuários, menus de usuário e controles comuns de COMCTL e Comctl32. Esse suporte padrão é exposto por meio de objetos do **IAccessible** criados por Oleacc.dll e fornece suporte ao Microsoft acessibilidade ativa sem trabalho adicional de desenvolvimento do servidor. O servidor pode usar a [API de anotação dinâmica](dynamic-annotation-api.md) para modificar grande parte das informações expostas por Oleacc.dll, mas não tem controle total.

## <a name="creating-a-proxy"></a>Criando um proxy

Para determinar se um elemento de interface do usuário dá suporte nativo à interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , Oleacc.dll envia a ela uma mensagem do [**WM \_ GetObject**](wm-getobject.md) . Um valor de retorno diferente de zero significa que o elemento suporta nativamente o Microsoft Acessibilidade Ativa e fornece seu próprio suporte de **IAccessible** . No entanto, se o valor de retorno for zero, Oleacc.dll fornecerá um objeto proxy para o elemento de interface do usuário e tentará retornar informações significativas em seu nome. Para obter mais informações sobre o **WM \_ GetObject**, consulte [como o WM \_ GetObject funciona](how-wm-getobject-works.md).

## <a name="what-information-is-exposed"></a>Quais informações são expostas

Oleacc.dll usa o nome da classe Windows do elemento de interface do usuário para determinar quais informações devem ser expostas para cada uma de suas propriedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e como coletar essas informações. Por exemplo, Oleacc.dll chama a função [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) para recuperar a propriedade [**Name**](name-property.md) para um botão Push padrão, mas chama essa mesma função para recuperar a propriedade [**Value**](value-property.md) de um controle de edição padrão. Na verdade, Oleacc.dll está mapeando cada método **IAccessible** para um Microsoft Win32 ou uma mensagem específica de controle ou chamada de função. Usando esse uso especial com base no nome de classe, ele pode retornar informações significativas por meio de proxies do **IAccessible** sem qualquer suporte de acessibilidade ativa da Microsoft no servidor.

Aplicativos criados com elementos de interface do usuário padrão normalmente recebem suporte completo do Microsoft Acessibilidade Ativa sem trabalho de desenvolvimento adicional. As exceções a essa regra são controles que foram subclasses, que não armazenam suas próprias cadeias de caracteres (ausência do estilo **HASSTRINGS** ) ou que são desenhadas pelo proprietário. Nesses casos, Oleacc.dll não pode coletar as informações necessárias porque as informações são armazenadas fora do controle. No entanto, em muitos desses cenários, soluções alternativas estabelecidas ou o uso de anotação dinâmica, permita que o servidor cooperasse com os proxies fornecidos pelo Oleacc.dll.

## <a name="generic-proxy-objects"></a>Objetos de proxy genéricos

Se Oleacc.dll não reconhecer o nome de classe do elemento de interface do usuário, ele criará um proxy genérico que expõe o máximo de informações possível. No máximo, isso inclui o retângulo delimitador do objeto, o objeto pai, o nome (do [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext)) e quaisquer filhos na hierarquia da janela.

 

 