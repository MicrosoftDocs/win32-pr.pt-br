---
title: Interface e acessibilidade do IDispatch
description: A interface IDispatch foi inicialmente projetada para dar suporte à Automação.
ms.assetid: 5a95f002-4fd5-43d3-9b50-7b3f7790300a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710fb0bc8142dfa863967114d3841506c220b3c058db042b867607ffe56cd5e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052704"
---
# <a name="idispatch-interface-and-accessibility"></a>Interface e acessibilidade do IDispatch

A [**interface IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) foi inicialmente projetada para dar suporte à Automação. Ele fornece um mecanismo de associação tardia para acessar e recuperar informações sobre os métodos e as propriedades de um objeto. Anteriormente, os desenvolvedores de servidor tinham que implementar as interfaces **IDispatch** e [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para seus objetos acessíveis; ou seja, eles tinham que fornecer uma [interface dupla](dual-interfaces--iaccessible-and-idispatch.md). Com Microsoft Active Accessibility 2.0, os servidores podem retornar **E \_ NOTIMPL** de métodos **IDispatch** e Microsoft Active Accessibility implementará a interface **IAccessible** para eles.

Além dos métodos herdados de [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), os desenvolvedores de servidor devem implementar os seguintes métodos dentro da definição de classe de cada objeto exposto:

-   [**GetTypeInfoCount**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) retorna o número de descrições de tipo para o objeto . Para objetos que suportam [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch), a contagem de informações de tipo é sempre uma.
-   [**GetTypeInfo**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-gettypeinfo) recupera uma descrição da interface programável do objeto.
-   [**GetIDsOfNames**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-getidsofnames) mapeia o nome de um método ou propriedade para um **DISPID,** que é usado posteriormente para invocar o método ou a propriedade .
-   [**Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) chama um dos métodos do objeto ou obtém ou define uma de suas propriedades.

 

 