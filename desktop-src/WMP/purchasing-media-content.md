---
title: Comprando conteúdo de mídia
description: Comprando conteúdo de mídia
ms.assetid: df4a3152-f9e3-4a97-b021-6d5e8de9c184
keywords:
- Lojas online do Windows Media Player, comprando conteúdo de mídia
- lojas online, comprando conteúdo de mídia
- Digite 1 lojas online, comprando conteúdo de mídia
- Lojas online do Windows Media Player, compras de conteúdo de mídia
- lojas online, compras de conteúdo de mídia
- Digite 1 lojas online, compras de conteúdo de mídia
- conteúdo de mídia, comprando
- comprando conteúdo de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e420f1dce607e1c596c48490d10bbe8a2a5a5f61
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103916973"
---
# <a name="purchasing-media-content"></a>Comprando conteúdo de mídia

Quando o Windows Media Player exibe o conteúdo de música no modo de exibição de árvore de biblioteca, a interface do usuário inclui elementos que o usuário pode clicar para comprar o conteúdo. Por exemplo, o usuário pode clicar em um botão para comprar uma música individual ou para comprar um álbum inteiro.

Se o repositório online ativo for um repositório do tipo 1, o Windows Media Player terá acesso a preços de acompanhamento, álbum e lista no catálogo da loja online. Esses preços no catálogo são cadeias de caracteres que têm um formato compreendido somente pela loja online. O Windows Media Player não interpreta as cadeias de caracteres de preço; Ele simplesmente as exibe em elementos da interface do usuário, como botões de compra.

Quando o Windows Media Player configura uma compra para um conjunto de itens de mídia, ele passa as IDs e os preços dos itens de mídia para o plug-in de parceiro de conteúdo chamando [IWMPContentPartner:: CanBuySilent](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-canbuysilent). Nesse ponto, o plug-in pode inspecionar os preços fornecidos pelo jogador. Estes são os preços que o usuário espera pagar; ou seja, os preços que o jogador exibiu ao usuário. Com base nas IDs de mídia e nos preços fornecidos pelo Player, o plug-in calcula um preço total, que ele retorna ao Player no parâmetro *bstrTotalPrice* . Os preços que o Player passa para o **CanBuySilent** fornecem o plug-in com informações, mas não obrigam o plug-in a retornar um determinado preço total. O plug-in pode calcular o preço total conforme ele se ajusta.

Além de calcular o preço total de uma compra, o **CanBuySilent** determina se o purchace pode continuar silenciosamente; ou seja, sem exibir uma caixa de diálogo. Se **CanBuySilent** retornar **true**, o Windows Media Player simplesmente altera o texto no botão comprar para solicitar que o usuário confirme a compra. Se **CanBuySilent** retornar **false**, o Windows Media Player exibirá uma caixa de diálogo solicitando que o usuário confirme a compra. A caixa de diálogo fornece ao usuário informações que resumem a compra, como o número de álbuns, o número de faixas individuais e o preço total (conforme retornado pelo plug-in).

Depois que o usuário confirmar a compra, o jogador chamará [IWMPContentPartner:: Buy](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy). Essa chamada de método fornece o plug-in com a mesma lista de contêineres de conteúdo que **CanBuySilent**. Ao chamar **comprar**, o Windows Media Player também fornece um cookie (simplesmente um valor **DWORD** , exclusivo para a sessão) que o plug-in pode usar para identificar a transação. Quando a transação é concluída, o plug-in deve chamar [IWMPContentPartnerCallback:: BuyComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-buycomplete), passando o valor do cookie original para o parâmetro *dwBuyCookie* , para notificar o player de que a transação foi concluída.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação para lojas online do tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




