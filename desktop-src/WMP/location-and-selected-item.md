---
title: Local e Item Selecionado
description: Local e Item Selecionado
ms.assetid: 9556e01f-1f75-4089-9e62-b41a9aa53e93
keywords:
- Windows Media Player online, locais
- lojas online, locais
- tipo 1 lojas online, locais
- Windows Media Player online, locais de biblioteca
- lojas online, locais de biblioteca
- tipo 1 lojas online, locais de biblioteca
- Windows Media Player online, itens selecionados
- lojas online, itens selecionados
- tipo 1 lojas online, itens selecionados
- Windows Media Player, locais
- Windows Media Player biblioteca, itens selecionados
- biblioteca, locais
- biblioteca, itens selecionados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6532c6417b6e95632aa21fa8d4a3a9ed943ad844eb1324f34eb80191043eeb80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003367"
---
# <a name="location-and-selected-item"></a>Local e Item Selecionado

Windows Media Player usa os cinco itens a seguir para caracterizar sua exibição atual do conteúdo da loja online:

-   task
-   tipo de local da biblioteca
-   ID do local da biblioteca
-   tipo de item selecionado
-   ID do item selecionado

Normalmente, você pode pensar na exibição no Windows Media Player como um contêiner de itens. O contêiner tem um tipo e um item tem um tipo . Todos os itens em um contêiner têm o mesmo tipo. Os tipos de local e os tipos de item são especificados pelas [constantes de local da biblioteca](library-location-constants.md). Por exemplo, se a exibição atual estiver mostrando um álbum individual, o tipo de local da biblioteca será CPAlbumID e, como um álbum contém faixas, o tipo de item selecionado é CPTrackID.

A tabela a seguir mostra o local e os tipos de item para vários contêineres.



| Descrição do contêiner                              | Tipo de local da biblioteca | Tipo de item selecionado |
|-------------------------------------------------------|-----------------------|--------------------|
| Um álbum que é um contêiner de faixas                | CPAlbumID             | CPTrackID          |
| Uma lista que é um contêiner de faixas                  | CPListID              | CPTrackID          |
| Uma lista que é um contêiner de álbums                  | CPListID              | CPAlbumID          |
| Uma estação de rádio que é um contêiner de listas          | CPRadioID             | CPListID           |
| O conjunto de todos os álbums, que é um contêiner de álbums | AllCPAlbumIDs         | CPAlbumID          |
| O conjunto de todos os gêneros, que é um contêiner de gêneros | AllCPGenreIDs         | CPGenreID          |



 

As guias no Windows Media Player representam tarefas diferentes. O Player exibe o conteúdo da loja online em três painéis de tarefas diferentes: **Biblioteca,** **Gravar** e **Sincronizar**. O painel de tarefas Biblioteca também é chamado de **painel de** tarefas Procurar. Às vezes, um painel de tarefas é chamado *de recurso*, portanto, você pode ver termos como Recurso *de* burn e recurso *de sincronização* nesta documentação.

Os exemplos a seguir mostram como o Windows Media Player usa as cinco informações (tarefa, tipo de local da biblioteca, ID do local da biblioteca, tipo de item selecionado, ID do item selecionado) para caracterizar diferentes exibições.

No painel **da tarefa Gravar,** o Player está exibindo um álbum como um contêiner de faixas. O álbum tem uma ID de 250. Na exibição, o item selecionado é a faixa que tem uma ID de 800. Observe que 800 é a ID da faixa no catálogo da loja online, não o número da faixa no álbum.



| Item                  | Valor     |
|-----------------------|-----------|
| task                  | Queimar      |
| tipo de local da biblioteca | CPAlbumID |
| ID do local da biblioteca   | 250       |
| tipo de item selecionado    | CPTrackID |
| ID do item selecionado      | 800       |



 

No painel **da** tarefa Sincronizar, o Player está exibindo o conjunto de todos os álbums, que é um contêiner de álbums. Na exibição, o item selecionado é o álbum que tem uma ID de 300. Observe que a ID do local da biblioteca não é aplicável a essa exibição.



| Item                  | Valor         |
|-----------------------|---------------|
| task                  | Sincronizar          |
| tipo de local da biblioteca | AllCPAlbumIDs |
| ID do local da biblioteca   | N/D           |
| tipo de item selecionado    | CPAlbumID     |
| ID do item selecionado      | 300           |



 

No controle de exibição de árvore, o nó raiz do armazenamento online é selecionado. Nesse caso, não há nenhum contêiner e, consequentemente, não há itens. Todo o **painel de** tarefas Biblioteca está exibindo uma página de descoberta.



| Item                  | Valor           |
|-----------------------|-----------------|
| task                  | Procurar          |
| tipo de local da biblioteca | RootLocation    |
| ID do local da biblioteca   | N/D             |
| tipo de item selecionado    | UnknownLocation |
| ID do item selecionado      | N/D             |



 

No painel **da** tarefa Sincronizar, o Player está exibindo o ano 2002 como um contêiner de faixas. Na exibição, o item selecionado é a faixa que tem uma ID de 450.



| Item                  | Valor           |
|-----------------------|-----------------|
| task                  | Sincronizar            |
| tipo de local da biblioteca | ReleaseDateYear |
| ID do local da biblioteca   | 2002            |
| tipo de item selecionado    | CPTrackID       |
| ID do item selecionado      | 450             |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o tipo 1 lojas online**](about-type-1-online-stores.md)
</dt> <dt>

[**Páginas de descoberta**](discovery-pages.md)
</dt> </dl>

 

 




