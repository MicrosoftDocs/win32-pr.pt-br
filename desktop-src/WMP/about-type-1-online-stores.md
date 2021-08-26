---
title: Sobre o tipo 1 lojas online
description: Sobre o tipo 1 lojas online
ms.assetid: 754b0097-5d28-4c1f-9847-a19cf23beaea
keywords:
- Windows Media Player lojas online, digite 1 lojas online
- lojas online, tipo 1 lojas online
- Digite 1 lojas online, sobre
- Windows Media Player, digite 1 lojas online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35bc84311bb61c71fdcaf57b584b5c595a62be5c80d406f71ef36c8d1ad8e655
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903056"
---
# <a name="about-type-1-online-stores"></a>Sobre o tipo 1 lojas online

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

o Microsoft Windows Media Player 11 dá suporte a dois tipos de lojas online: tipo 1 e tipo 2. os armazenamentos do tipo 1 são mais profundamente integrados a Windows Media Player do que os repositórios do tipo 2. uma loja online tipo 1 fornece um catálogo de música baixável para que Windows Media Player possa disponibilizar o conteúdo do repositório para o usuário como se o conteúdo estivesse na biblioteca de mídia local do usuário.

Um repositório online tipo 1 deve fornecer um plug-in que implementa a interface [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) . à medida que o usuário navega na interface do usuário Windows Media Player, o Player chama o plug-in para que a loja online possa aprimorar a experiência do usuário fornecendo páginas da web que são exibidas no Player.

Os recursos de repositórios online do tipo 1 que os distinguem dos repositórios do tipo 2 incluem o seguinte:

-   **Facilidade de uso.** os usuários podem procurar música do catálogo de loja online usando a mesma interface do usuário familiar Windows Media Player que eles usam atualmente para gerenciar sua biblioteca pessoal. Os usuários podem exibir apenas um único catálogo de loja online no recurso de procura em qualquer momento específico.
-   **Necessidade.** os usuários podem obter amostras ou comprar música sem alternar do recurso procurar para outra parte da interface do usuário Windows Media Player.
-   **Recursos avançados.** como o catálogo de loja online é armazenado de forma semelhante à biblioteca do usuário, muitos dos recursos da biblioteca Windows Media Player podem ser aplicados ao catálogo. Por exemplo, os usuários podem usar a roda de palavras do recurso procurar para filtrar o catálogo de loja online.

Para um provedor de loja online, as vantagens de fornecer um repositório tipo 1 em vez de um repositório tipo 2 incluem o seguinte:

-   um nó personalizado altamente visível na árvore de biblioteca de Windows Media Player.
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
| [Páginas de descoberta](discovery-pages.md)                                                               | descreve a interação entre Windows Media Player e páginas da web fornecidas pela loja online.                                                                                   |
| [Menus de contexto](context-menus.md)                                                                   | Descreve como o armazenamento online pode fornecer menus de contexto à medida que o usuário navega pela interface do usuário do jogador.                                                                         |
| [Fluxos de áudio](audio-streams.md)                                                                   | descreve como a loja online fornece Windows Media Player com a URL para o conteúdo de streaming de áudio.                                                                              |
| [Documento do serviceInfo para uma loja online tipo 1](serviceinfo-document-for-a-type-1-online-store.md) | Descreve o documento XML do serviceInfo fornecido por um repositório online tipo 1.                                                                                                           |
| [Tipo 1 plug-in de loja online](type-1-online-store-plug-in.md)                                       | Descreve o plug-in que um repositório online tipo 1 deve fornecer.                                                                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Tipos 1 lojas online**](type-1-online-stores.md)
</dt> </dl>

 

 




