---
title: Contêineres de conteúdo
description: Contêineres de conteúdo
ms.assetid: bed0293b-4765-4d1b-861c-f0c0a064df5f
keywords:
- Windows Media Player lojas online, contêineres de conteúdo
- lojas online, contêineres de conteúdo
- Digite 1 lojas online, contêineres de conteúdo
- Windows Media Player lojas online, interface IWMPContentContainer
- lojas online, interface IWMPContentContainer
- Digite 1 lojas online, interface IWMPContentContainer
- Windows Media Player, contêineres de conteúdo
- Windows Media Player, interface IWMPContentContainer
- contêineres de conteúdo
- IWMPContentContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c582a04bd37e54a40f952402343c09fb7243fc07377ef7f507cc76f11390357c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123676"
---
# <a name="content-containers"></a>Contêineres de conteúdo

Windows Media Player usa contêineres de conteúdo para representar o conteúdo de mídia digital em um download de assinatura ou transação de compra. Um contêiner de conteúdo é representado pela interface **IWMPContentContainer** . Um contêiner de conteúdo pode conter uma lista de conteúdo relacionado, como um álbum ou um conjunto de itens de conteúdo não relacionados ou *faixas*. Você pode usar a interface **IWMPContentContainer** para enumerar as faixas do contêiner de conteúdo e recuperar o preço de cada faixa. Você também pode recuperar informações sobre o próprio contêiner de conteúdo, como a ID do contêiner, o tipo de conteúdo no contêiner e o preço total para as faixas no contêiner (que podem ser diferentes da soma dos preços das faixas individuais, como no caso de uma compra de álbum).

para fornecer um mecanismo para empacotar vários contêineres de conteúdo em um único objeto, Windows Media Player dá suporte à interface **IWMPContentContainerList** . **IWMPContentContainerList** fornece métodos para enumerar e recuperar os contêineres de conteúdo na lista. Para descobrir se a lista de contêineres de conteúdo representa uma compra ou um download de assinatura, chame [IWMPContentContainerList:: Gettransactiontype](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainerlist-gettransactiontype) para recuperar um valor de [WMPTransactionType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptransactiontype) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o tipo 1 lojas online**](about-type-1-online-stores.md)
</dt> <dt>

[**Interface IWMPContentContainer**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)
</dt> <dt>

[**Interface IWMPContentContainerList**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainerlist)
</dt> </dl>

 

 




