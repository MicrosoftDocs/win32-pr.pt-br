---
title: Menus de contexto
description: Menus de contexto
ms.assetid: d1ea899a-9087-4502-8825-5cef1a87ef03
keywords:
- Lojas online do Windows Media Player, menus de contexto
- lojas online, menus de contexto
- tipos 1 lojas online, menus de contexto
- Lojas online do Windows Media Player, menus de contexto personalizados
- lojas online, menus de contexto personalizados
- tipos 1 lojas online, menus de contexto personalizados
- menus de contexto
- menus de contexto personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba3ed52b408651607cb1f6dab1a04f53282d3ef
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365531"
---
# <a name="context-menus"></a>Menus de contexto

As lojas online podem fornecer menus de contexto personalizados. Para fazer isso, o plug-in da loja online implementa o método [IWMPContentPartner:: GetCommands](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands) . O Windows Media Player chama esse método para fornecer informações sobre o local na interface do usuário em que o menu de contexto é exibido (onde o usuário clicou com o botão direito do mouse). O plug-in retorna uma matriz de estruturas [WMPContextMenuInfo](/previous-versions/windows/desktop/api/contentpartner/ns-contentpartner-wmpcontextmenuinfo) que descrevem cada item de menu de contexto, incluindo uma ID de comando para cada.

Depois que o Windows Media Player tiver recuperado a matriz, o Player usará a matriz para criar o menu de contexto que o usuário vê. Quando o usuário clica em um item no menu de contexto, o Player chama [IWMPContentPartner:: InvokeCommand](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand), passando a ID de comando associada ao item de menu por meio do parâmetro *dwCommandID* . O Player também passa um valor de local de biblioteca e uma matriz de IDs que representa os itens sobre os quais o menu foi invocado, como uma matriz de IDs de faixa. Usando essas informações, o plug-in pode iniciar qualquer processo apropriado em resposta ao clique do mouse do usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o tipo 1 lojas online**](about-type-1-online-stores.md)
</dt> </dl>

 

 




