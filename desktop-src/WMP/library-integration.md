---
title: Integração de biblioteca
description: Integração de biblioteca
ms.assetid: 6ff1b379-983b-4cd7-8142-27523a7a03e7
keywords:
- Repositórios online do Windows Media Player, integração da biblioteca
- lojas online, integração de biblioteca
- tipos 1 lojas online, integração de biblioteca
- Repositórios online do Windows Media Player, painéis de tarefas
- lojas online, painéis de tarefas
- Digite 1 lojas online, painéis de tarefas
- Windows Media Player, painéis de tarefas
- Biblioteca do Windows Media Player, integrando
- biblioteca, integração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5353aba7099acd2dfd08596be7ffd43503bdad91
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365584"
---
# <a name="library-integration"></a>Integração de biblioteca

A interface do usuário do Windows Media Player é organizada em áreas de recursos, chamadas de *painéis de tarefas*, que encapsulam os vários recursos de alto nível do programa. Isso inclui os painéis de tarefas **biblioteca**, **sincronização** e **gravação** (entre outros). O painel de tarefas **biblioteca** permite que os usuários trabalhem com a biblioteca; o painel de tarefas **sincronizar** permite que os usuários sincronizem arquivos de mídia digital para um dispositivo portátil; e o painel de tarefas **gravar** permite que os usuários gravem arquivos de mídia digital em um CD ou DVD.

> [!Note]  
> O painel de tarefas da **biblioteca** é, às vezes, chamado de painel de tarefas **procurar** .

 

Cada um desses painéis de tarefas tem algum nível de integração com a biblioteca. Por exemplo, se o usuário quiser gravar música em um CD, faz sentido permitir que o usuário escolha a música a ser gravada navegando na biblioteca e simplesmente arrastando e soltando itens de mídia em uma lista. Isso significa que os usuários podem exibir e usar um catálogo de loja online totalmente integrado à biblioteca ao trabalhar nos painéis de tarefas **biblioteca**, **sincronização** e **gravação** . A enumeração [WMPTaskType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptasktype) contém valores que representam esses três painéis de tarefas para que possam ser identificados programaticamente.

Cada um desses três painéis de tarefas é organizado em três partes principais. A primeira parte é o controle de exibição de árvore de biblioteca. Esse controle fornece ao usuário uma exibição hierárquica da biblioteca do Windows Media Player, incluindo recursos de categorização por música, artista, álbum e assim por diante. A segunda parte do painel de tarefas é o painel detalhes. Este painel fornece informações detalhadas organizadas de acordo com a categoria selecionada atualmente no controle de exibição de árvore de biblioteca. Por exemplo, se o usuário tiver clicado em **músicas** no modo de exibição de árvore, o painel detalhes mostrará os títulos de música atualmente na biblioteca, juntamente com outras informações, como comprimento e título do álbum. A terceira parte é o painel de lista, ou *carrinho*. Os usuários podem arrastar e soltar itens de mídia na cesta para criar listas, como listas de reprodução, lista de sincronização e listas de gravação.

Quando um catálogo de loja online é integrado à biblioteca, a loja online aparece como uma categoria de nível superior, ou *nó*, no controle de exibição de árvore de biblioteca. (Somente um catálogo de loja online fica visível para o usuário de cada vez.) Quando um usuário opta por exibir o catálogo de loja online clicando no nó, o painel de detalhes mostra informações sobre a música no catálogo da loja online. Isso inclui música que o usuário comprou ou aluga e também música que o usuário ainda não adquiriu.

O nó de armazenamento online de nível superior tem um conjunto de nós filho fornecidos pelo Windows Media Player. Por exemplo, o nó de armazenamento online de nível superior tem nós filho de rádio, artista e álbum, entre outros. O nó de armazenamento online de nível superior também pode ter até oito nós filho personalizados fornecidos pela loja online. O Windows Media Player cria um nó filho personalizado para qualquer lista que tenha um identificador de lista no intervalo de 0 a 7. A loja online especifica o identificador de uma lista no arquivo de [list.csv](list-csv.md) que faz parte do catálogo do repositório.

O Windows Media Player recupera um ícone para cada um dos nós de árvore personalizada do repositório online chamando [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), passando CPListIDIcon no parâmetro *bstrInfoName* .

À medida que o usuário navega pelo catálogo, o Windows Media Player faz chamadas para **IWMPContentPartner:: GetItemInfo** para recuperar metadados do plug-in de parceiro de conteúdo sobre os itens de música que o usuário seleciona. Esses metadados fornecem informações ao Player para que o Player possa exibir detalhes sobre os itens do catálogo. Por exemplo, se o usuário selecionar um álbum, o Windows Media Player recuperará a URL de arte do álbum para que o usuário possa ver a arte da capa do álbum.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o tipo 1 lojas online**](about-type-1-online-stores.md)
</dt> </dl>

 

 




