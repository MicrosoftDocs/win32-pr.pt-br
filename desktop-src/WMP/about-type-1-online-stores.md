---
title: Sobre o tipo 1 lojas online
description: Sobre o tipo 1 lojas online
ms.assetid: 754b0097-5d28-4c1f-9847-a19cf23beaea
keywords:
- Lojas online do Windows Media Player, tipo 1 lojas online
- lojas online, tipo 1 lojas online
- Digite 1 lojas online, sobre
- Windows Media Player, tipo 1 lojas online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ecd939a03734fed121dcaa22c0d7ae89127476
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105813393"
---
# <a name="about-type-1-online-stores"></a>Sobre o tipo 1 lojas online

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O Microsoft Windows Media Player 11 dá suporte a dois tipos de lojas online: tipo 1 e tipo 2. Os armazenamentos do tipo 1 são mais profundamente integrados ao Windows Media Player do que os repositórios do tipo 2. Uma loja online tipo 1 fornece um catálogo de música baixável para que o Windows Media Player possa disponibilizar o conteúdo da loja para o usuário como se o conteúdo estivesse na biblioteca de mídia local do usuário.

Um repositório online tipo 1 deve fornecer um plug-in que implementa a interface [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) . À medida que o usuário navega na interface do usuário do Windows Media Player, o Player chama o plug-in para que a loja online possa aprimorar a experiência do usuário fornecendo páginas da Web que são exibidas no Player.

Os recursos de repositórios online do tipo 1 que os distinguem dos repositórios do tipo 2 incluem o seguinte:

-   **Facilidade de uso.** Os usuários podem procurar música do catálogo de loja online usando a mesma interface do usuário familiar do Windows Media Player que eles usam atualmente para gerenciar sua biblioteca pessoal. Os usuários podem exibir apenas um único catálogo de loja online no recurso de procura em qualquer momento específico.
-   **Necessidade.** Os usuários podem obter amostras ou comprar música sem alternar do recurso procurar para outra parte da interface do usuário do Windows Media Player.
-   **Recursos avançados.** Como o catálogo de loja online é armazenado de maneira semelhante à biblioteca do usuário, muitos dos recursos da biblioteca do Windows Media Player podem ser aplicados ao catálogo. Por exemplo, os usuários podem usar a roda de palavras do recurso procurar para filtrar o catálogo de loja online.

Para um provedor de loja online, as vantagens de fornecer um repositório tipo 1 em vez de um repositório tipo 2 incluem o seguinte:

-   Um nó personalizado altamente visível na árvore de biblioteca do Windows Media Player.
-   Um sistema projetado para compras de música.
-   Conexões aprimoradas para processos do Player.
-   Um Gerenciador de download melhor e mais fácil de usar.
-   A capacidade de navegar entre vários recursos no Player (incluindo a abertura de nós específicos da árvore de biblioteca).
-   Notificações sobre a expiração da licença para o conteúdo da assinatura.
-   Notificações para trabalhar com players de música portáteis conectados.

As seções a seguir fornecem informações gerais sobre as lojas online do tipo 1.



| Seção                                                                                              | Descrição                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Catálogo de música](music-catalog.md)                                                                   | Descreve o catálogo de música fornecido pela loja online. Descreve o compilador de catálogo fornecido pela Microsoft.                                                                     |
| [Contêineres de conteúdo](content-containers.md)                                                         | Descreve a[IWMPContentContainer](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)(interface de contêiner de conteúdo), que é usada para representar uma coleção de itens de mídia a serem comprados ou baixados. |
| [Integração de biblioteca](library-integration.md)                                                       | Descreve como o catálogo de música do repositório online é integrado à exibição de biblioteca do Player.                                                                                        |
| [Páginas de descoberta](discovery-pages.md)                                                               | Descreve a interação entre o Windows Media Player e as páginas da Web fornecidas pela loja online.                                                                                   |
| [Menus de contexto](context-menus.md)                                                                   | Descreve como o armazenamento online pode fornecer menus de contexto à medida que o usuário navega pela interface do usuário do jogador.                                                                         |
| [Fluxos de áudio](audio-streams.md)                                                                   | Descreve como a loja online fornece ao Windows Media Player a URL para o conteúdo de streaming de áudio.                                                                              |
| [Documento do serviceInfo para uma loja online tipo 1](serviceinfo-document-for-a-type-1-online-store.md) | Descreve o documento XML do serviceInfo fornecido por um repositório online tipo 1.                                                                                                           |
| [Tipo 1 plug-in de loja online](type-1-online-store-plug-in.md)                                       | Descreve o plug-in que um repositório online tipo 1 deve fornecer.                                                                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Tipos 1 lojas online**](type-1-online-stores.md)
</dt> </dl>

 

 




