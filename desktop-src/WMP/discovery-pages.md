---
title: Páginas de descoberta
description: Páginas de descoberta
ms.assetid: deb0cbf9-b7e1-4ce6-8241-b9199129515a
keywords:
- Lojas online do Windows Media Player, páginas de descoberta
- lojas online, páginas de descoberta
- Digite 1 lojas online, páginas de descoberta
- Biblioteca do Windows Media Player, páginas de descoberta
- biblioteca, páginas de descoberta
- páginas de descoberta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a349b0e7238aa6d59b56f9035a3c02a5b3ff7b7e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640150"
---
# <a name="discovery-pages"></a>Páginas de descoberta

Se o repositório online ativo for um repositório do tipo 1, o Windows Media Player exibirá o conteúdo da loja em sua interface do usuário. O controle de exibição de árvore de biblioteca tem um nó para a loja online. Quando o usuário clica nesse nó ou em qualquer um de seus subnós, o Windows Media Player exibe o conteúdo da loja online no painel de detalhes.

Como o usuário interage com o conteúdo da loja online no controle de exibição em árvore ou no painel de detalhes, o Windows Media Player exibe páginas da Web, chamadas *páginas de descoberta*, fornecidas pela loja online. As páginas de descoberta fornecem informações adicionais sobre a música à medida que o usuário navega no catálogo da loja online. As páginas de descoberta se comunicam com o Windows Media Player por meio das propriedades, métodos e eventos do [objeto externo](external-object-for-type-1-online-stores.md).

Sempre que o Windows Media Player altera sua exibição do conteúdo da loja online, ele chama [IWMPContentPartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate), implementado pelo plug-in da loja online, para obter a URL da página de descoberta a ser exibida com a nova exibição.

A exibição do conteúdo da loja online no Windows Media Player é caracterizada por cinco partes de informações: tarefa, tipo de local, ID de local, tipo de item selecionado e ID de item selecionado. O Windows Media Player fornece esses cinco itens para o método **GetTemplate** nos parâmetros *Task*, *Location*, *pContext*, *clickLocation* e *pClickContext* . O Windows Media Player disponibiliza esses cinco itens para páginas de descoberta na *tarefa*, *libraryLocationType*, *LibraryLocationID*, *selecteditemtype* e *selecteditemid* Propriedades do objeto **externo** . Para obter mais informações sobre como o Windows Media Player especifica sua exibição do conteúdo da loja online, consulte [local e item selecionado](location-and-selected-item.md).

Além de habilitar uma página de descoberta para se comunicar com o Windows Media Player, o objeto **externo** permite que uma página de descoberta se comunique com o plug-in da loja online. Quando isso acontece, o Windows Media Player atua como uma ponte entre a página de descoberta e o plug-in. Por exemplo, a página de descoberta pode chamar [external. SendMessage](external-sendmessage.md) para enviar uma mensagem personalizada para o plug-in. O Windows Media Player recebe essa chamada de método e, por sua vez, chama [IWMPContentPartner:: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage) para passar a mensagem para o plug-in. Quando o plug-in conclui o processamento da mensagem, ele chama [IWMPContentPartnerCallback:: SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete). Em seguida, o Windows Media Player notifica a página de descoberta gerando o evento [external. OnSendMessageComplete](external-onsendmessagecomplete-event.md) .

O objeto **externo** também fornece uma maneira para uma página de descoberta se comunicar com outra página de descoberta. Quando o script em uma página de descoberta chama [external. changeView](external-changeview.md), o script pode fornecer uma cadeia de caracteres no parâmetro *ViewParams* . O Windows Media Player não interpreta a cadeia de caracteres *ViewParams* , mas disponibiliza a cadeia de caracteres para a próxima página de descoberta na propriedade [external. viewparameters](external-viewparameters.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o tipo 1 lojas online**](about-type-1-online-stores.md)
</dt> <dt>

[**Local e item selecionado**](location-and-selected-item.md)
</dt> </dl>

 

 




