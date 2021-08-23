---
title: Páginas de descoberta
description: Páginas de descoberta
ms.assetid: deb0cbf9-b7e1-4ce6-8241-b9199129515a
keywords:
- Windows Media Player online, páginas de descoberta
- lojas online, páginas de descoberta
- tipo 1 lojas online, páginas de descoberta
- Windows Media Player, páginas de descoberta
- biblioteca, páginas de descoberta
- páginas de descoberta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe29ed5d3948bbdcd6f36239938e3a4e552362318b6ec48658e85895cb58d163
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997336"
---
# <a name="discovery-pages"></a>Páginas de descoberta

Se o armazenamento online ativo for um armazenamento do tipo 1, Windows Media Player exibirá o conteúdo da loja em sua interface do usuário. O controle de exibição de árvore da biblioteca tem um nó para o armazenamento online. Quando o usuário clica nesse nó ou em qualquer um de seus subnónodos, Windows Media Player exibe o conteúdo da loja online no painel de detalhes.

Conforme o usuário interage com o conteúdo da loja online no controle de exibição de árvore ou no painel de detalhes, o Windows Media Player exibe páginas da Web, chamadas páginas de *descoberta,* fornecidas pela loja online. As páginas de descoberta fornecem informações adicionais sobre a música à medida que o usuário navega no catálogo da loja online. As páginas de descoberta se comunicam com Windows Media Player por meio das propriedades, métodos e eventos do [objeto Externo](external-object-for-type-1-online-stores.md).

Sempre Windows Media Player altera sua exibição do conteúdo da loja online, ele chama [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate), implementado pelo plug-in da loja online, para obter a URL da página de descoberta a ser exibida com a nova exibição.

A exibição do conteúdo da loja online no Windows Media Player é caracterizada por cinco informações: tarefa, tipo de local, ID de local, tipo de item selecionado e ID do item selecionado. Windows Media Player fornece esses cinco itens para o método **GetTemplate** nos parâmetros task *,* *location*, *pContext*, *clickLocation* e *pClickContext.* Windows Media Player disponibiliza esses cinco itens para páginas de descoberta na tarefa *,* *libraryLocationType*, *libraryLocationID*, *selectedItemType* e *selectedItemID* propriedades **do objeto Externo.** Para obter mais informações sobre como Windows Media Player especifica sua exibição do conteúdo da loja online, consulte [Local e Item Selecionado.](location-and-selected-item.md)

Além de habilitar uma página de descoberta para  se comunicar com Windows Media Player, o objeto Externo permite que uma página de descoberta se comunique com o plug-in da loja online. Quando isso acontece, Windows Media Player atua como uma ponte entre a página de descoberta e o plug-in. Por exemplo, a página de descoberta pode chamar [External.sendMessage](external-sendmessage.md) para enviar uma mensagem personalizada para o plug-in. Windows Media Player recebe essa chamada de método e, por sua vez, chama [IWMPContentPartner::SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage) para passar a mensagem para o plug-in. Quando o plug-in terminar de processar a mensagem, ele [chamará IWMPContentPartnerCallback::SendMessageComplete.](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete) Windows Media Player notifica a página de descoberta ificando o [evento External.OnSendMessageComplete.](external-onsendmessagecomplete-event.md)

O **objeto** Externo também fornece uma maneira para uma página de descoberta se comunicar com outra página de descoberta. Quando o script em uma página de descoberta [chama External.changeView](external-changeview.md), o script pode fornecer uma cadeia de caracteres no *parâmetro ViewParams.* Windows Media Player não interpreta a cadeia de *caracteres ViewParams,* mas disponibiliza a cadeia de caracteres para a próxima página de descoberta na [propriedade External.viewParameters.](external-viewparameters.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre as Lojas Online do Tipo 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Local e Item Selecionado**](location-and-selected-item.md)
</dt> </dl>

 

 




