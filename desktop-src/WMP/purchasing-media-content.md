---
title: Comprando conteúdo de mídia
description: Comprando conteúdo de mídia
ms.assetid: df4a3152-f9e3-4a97-b021-6d5e8de9c184
keywords:
- Windows Media Player online, comprando conteúdo de mídia
- lojas online, comprando conteúdo de mídia
- tipo 1 lojas online, comprando conteúdo de mídia
- Windows Media Player online, compras de conteúdo de mídia
- lojas online, compras de conteúdo de mídia
- tipo 1 lojas online, compras de conteúdo de mídia
- conteúdo de mídia, compra
- comprando conteúdo de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc830d4b1351b7649343f1f76f347c89da9a8ed9ceffedc3663c3156be6b7ead
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995636"
---
# <a name="purchasing-media-content"></a>Comprando conteúdo de mídia

Quando Windows Media Player exibe conteúdo de música no exibição de árvore de biblioteca, a interface do usuário inclui elementos que o usuário pode clicar para comprar o conteúdo. Por exemplo, o usuário pode clicar em um botão para comprar uma música individual ou comprar um álbum inteiro.

Se a loja online ativa for uma loja do Tipo 1, Windows Media Player terá acesso aos preços de faixa, álbum e lista no catálogo da loja online. Esses preços no catálogo são cadeias de caracteres que têm um formato compreendido apenas pela loja online. Windows Media Player não interpreta cadeias de caracteres de preço; ele simplesmente os exibe em elementos de interface do usuário, como botões Comprar.

Quando Windows Media Player configura uma compra para um conjunto de itens de mídia, ele passa as IDs e os preços dos itens de mídia para o plug-in do parceiro de conteúdo chamando [IWMPContentPartner::CanBuySilent](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-canbuysilent). Nesse ponto, o plug-in pode inspecionar os preços fornecidos pelo Player. Esses são os preços que o usuário espera pagar; ou seja, os preços que o Player exibiu para o usuário. Com base nas IDs de mídia e nos preços fornecidos pelo Player, o plug-in calcula um preço total, que ele retorna ao Player no parâmetro *bstrTotalPrice.* Os preços que o Player passa para **o CanBuySilent** fornecem ao plug-in informações, mas eles não obligateam o plug-in para retornar um determinado preço total. O plug-in pode calcular o preço total como ele quiser.

Além de calcular o preço total de uma compra, **o CanBuySilent** determina se o purchace pode continuar silenciosamente; ou seja, sem exibir uma caixa de diálogo. Se **CanBuySilent** retornar **True,** Windows Media Player simplesmente altera o texto no botão Comprar para solicitar que o usuário confirme a compra. Se **CanBuySilent** retornar **False,** Windows Media Player exibirá uma caixa de diálogo solicitando que o usuário confirme a compra. A caixa de diálogo fornece ao usuário informações que resumem a compra, como o número de álbums, o número de faixas individuais e o preço total (conforme retornado pelo plug-in).

Depois que o usuário confirmar a compra, o Player [chamará IWMPContentPartner::Buy.](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy) Essa chamada de método fornece o plug-in com a mesma lista de contêineres de conteúdo **que CanBuySilent**. Ao chamar **Comprar**, Windows Media Player também fornece um cookie (simplesmente um valor **DWORD,** exclusivo para a sessão) que o plug-in pode usar para identificar a transação. Quando a transação for concluída, o plug-in deverá chamar [IWMPContentPartnerCallback::BuyComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-buycomplete), passando o valor do cookie original para o parâmetro *dwBuyCookie,* para notificar o Player de que a transação foi concluída.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação para lojas online do tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




