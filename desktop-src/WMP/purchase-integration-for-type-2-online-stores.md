---
title: Integração de compras para lojas online do tipo 2
description: Integração de compras para lojas online do tipo 2
ms.assetid: aedaa6a0-d559-44b7-9c14-2abf44478b1c
keywords:
- Lojas online do Windows Media Player, integração de compra
- lojas online, integração de compra
- tipo 2 lojas online, integração de compra
- Lojas online do Windows Media Player, integrando compras
- lojas online, integrando compras
- Digite 2 lojas online, integrando compras
- Windows Media Player, integração de compra
- Windows Media Player, integrando compras
- integração de compra
- integrando compras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d8fb56b286b66de12bb59412e7f9077eb398f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105796253"
---
# <a name="purchase-integration-for-type-2-online-stores"></a>Integração de compras para lojas online do tipo 2

Quando o Windows Media Player reproduz conteúdo de mídia digital ou o usuário escolhe **localizar informações do álbum**, o Player oferece ao usuário um link para comprar o CD ou DVD do qual o conteúdo se originou, se esse link estiver disponível. Quando o usuário clica no link, o Windows Media Player 10 ou posterior chama o repositório de música atual para lidar com a solicitação de compra. Quando isso acontece, o Player navega até o primeiro painel de tarefas de serviço (no Windows Media Player 10) ou a guia lojas online (no Windows Media Player 11) e exibe a página da Web especificada pelo atributo **MediaPlayerURL** do elemento **BuyCD** do documento serviceInfo. (Os atributos **MediaCenterURL** e **BrowserURL** são usados de maneira semelhante para lidar com chamadas do Windows xp Media Center Edition 2004 e do Windows XP Service Pack 2).

O Windows Media Player acrescenta uma cadeia de caracteres de consulta à URL para fornecer informações à loja online sobre o conteúdo que o usuário optou por comprar. A cadeia de caracteres de consulta inclui atributos como **título**, **álbum** e **artista**, que o repositório online pode usar para determinar o álbum correto a ser vendido. A documentação de referência para o elemento **BuyCD** fornece a lista completa de atributos de cadeia de caracteres de consulta e suas descrições.

## <a name="guidelines-for-the-buycd-page"></a>Diretrizes para a página BuyCD

Ao criar sua página da Web do BuyCD, use as seguintes diretrizes:

-   A página deve identificar claramente a loja online que fornece as informações. Você pode fazer isso exibindo de forma proeminente seu logotipo, por exemplo.
-   A página deve incluir um link para a política de privacidade da sua empresa.
-   É melhor fornecer informações de compra inicial sem exigir que o usuário instale programas ou faça logon na sua loja online.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre as lojas online do tipo 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Elemento BuyCD**](buycd-element.md)
</dt> </dl>

 

 




