---
title: Integração de compra para lojas online do tipo 2
description: Integração de compra para lojas online do tipo 2
ms.assetid: aedaa6a0-d559-44b7-9c14-2abf44478b1c
keywords:
- Windows Media Player online, integração de compra
- lojas online, integração de compra
- tipo 2 lojas online, integração de compra
- Windows Media Player online, integrando compras
- lojas online, integrando compras
- tipo 2 lojas online, integrando compras
- Windows Media Player, integração de compra
- Windows Media Player, integrando compras
- integração de compra
- integrando compras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d854ecfd91cd0a887c242ad743874a6ec1a469ebcca3aa788bf57c2c59041d6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746690"
---
# <a name="purchase-integration-for-type-2-online-stores"></a>Integração de compra para lojas online do tipo 2

Quando Windows Media Player reproduz conteúdo de mídia digital ou o usuário escolhe Encontrar Informações do Álbum **,** o Player oferece ao usuário um link para comprar o CD ou DVD do qual o conteúdo originou se esse link estiver disponível. Quando o usuário clica no link, Windows Media Player 10 ou posteriores chamadas na loja de música atual para lidar com a solicitação de compra. Quando isso acontece, o Player navega para o primeiro painel de tarefas de serviço (no Windows Media Player 10) ou a guia Lojas Online (no Windows Media Player 11) e exibe a página da Web especificada pelo atributo **MediaPlayerURL** do elemento **BuyCD** do documento ServiceInfo. (Os atributos **MediaCenterURL** e **BrowserURL** são usados de maneira semelhante para lidar com chamadas do Windows XP Media Center Edition 2004 e Windows XP Service Pack 2).

Windows Media Player anexa uma cadeia de consulta à URL para fornecer informações à loja online sobre o conteúdo que o usuário escolheu comprar. A cadeia de caracteres de consulta inclui atributos como **Title**, **Album** e **Artist,** que a loja online pode usar para determinar o álbum correto a ser vendido. A documentação de referência **para o elemento BuyCD** fornece a lista completa de atributos de cadeia de caracteres de consulta e suas descrições.

## <a name="guidelines-for-the-buycd-page"></a>Diretrizes para a página BuyCD

Ao criar sua página da Web do BuyCD, use as seguintes diretrizes:

-   A página deve identificar claramente a loja online que fornece as informações. Você pode fazer isso exibindo o logotipo em destaque, por exemplo.
-   A página deve incluir um link para a política de privacidade da sua empresa.
-   É melhor fornecer informações iniciais de compra sem exigir que o usuário instale programas ou faça logoff em sua loja online.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre as Lojas Online do Tipo 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Elemento BuyCD**](buycd-element.md)
</dt> </dl>

 

 




