---
title: Menus de contexto
description: Menus de contexto
ms.assetid: d1ea899a-9087-4502-8825-5cef1a87ef03
keywords:
- Windows Media Player lojas online, menus de contexto
- lojas online, menus de contexto
- tipos 1 lojas online, menus de contexto
- Windows Media Player lojas online, menus de contexto personalizados
- lojas online, menus de contexto personalizados
- tipos 1 lojas online, menus de contexto personalizados
- menus de contexto
- menus de contexto personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6ad3bba5863f83b5f324821ec0904e7ef4c5881c7f10b9214eebde1081b217d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119345"
---
# <a name="context-menus"></a>Menus de contexto

As lojas online podem fornecer menus de contexto personalizados. Para fazer isso, o plug-in da loja online implementa o método [IWMPContentPartner:: GetCommands](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands) . Windows Media Player chama esse método para fornecer informações sobre o local na interface do usuário em que o menu de contexto é exibido (onde o usuário clicou com o botão direito do mouse). O plug-in retorna uma matriz de estruturas [WMPContextMenuInfo](/previous-versions/windows/desktop/api/contentpartner/ns-contentpartner-wmpcontextmenuinfo) que descrevem cada item de menu de contexto, incluindo uma ID de comando para cada.

depois que Windows Media Player tiver recuperado a matriz, o Player usará a matriz para criar o menu de contexto que o usuário vê. Quando o usuário clica em um item no menu de contexto, o Player chama [IWMPContentPartner:: InvokeCommand](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand), passando a ID de comando associada ao item de menu por meio do parâmetro *dwCommandID* . O Player também passa um valor de local de biblioteca e uma matriz de IDs que representa os itens sobre os quais o menu foi invocado, como uma matriz de IDs de faixa. Usando essas informações, o plug-in pode iniciar qualquer processo apropriado em resposta ao clique do mouse do usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o tipo 1 lojas online**](about-type-1-online-stores.md)
</dt> </dl>

 

 




