---
title: Local e item selecionado
description: Local e item selecionado
ms.assetid: 9556e01f-1f75-4089-9e62-b41a9aa53e93
keywords:
- Lojas online do Windows Media Player, locais
- lojas online, locais
- tipos 1 lojas online, locais
- Lojas online do Windows Media Player, locais de biblioteca
- lojas online, locais de biblioteca
- Digite 1 lojas online, locais de biblioteca
- Lojas online do Windows Media Player, itens selecionados
- lojas online, itens selecionados
- Digite 1 lojas online, itens selecionados
- Biblioteca do Windows Media Player, locais
- Biblioteca do Windows Media Player, itens selecionados
- biblioteca, locais
- biblioteca, itens selecionados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d665b11e7509e369224d3e85db30dddb4a988a14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159726"
---
# <a name="location-and-selected-item"></a>Local e item selecionado

O Windows Media Player usa os cinco itens a seguir para caracterizar sua exibição atual do conteúdo da loja online:

-   task
-   tipo de local da biblioteca
-   ID do local da biblioteca
-   tipo de item selecionado
-   ID do item selecionado

Normalmente, você pode considerar o modo de exibição no Windows Media Player como um contêiner de itens. O contêiner tem um tipo e um item tem um tipo. Todos os itens em um contêiner têm o mesmo tipo. Tipos de localização e tipos de item são especificados pelas [constantes de local de biblioteca](library-location-constants.md). Por exemplo, se a exibição atual estiver mostrando um álbum individual, o tipo de local da biblioteca será CPAlbumID e, como um álbum conterá faixas, o tipo de item selecionado será CPTrackID.

A tabela a seguir mostra os tipos de local e item para vários contêineres.



| Descrição do contêiner                              | Tipo de local da biblioteca | Tipo de item selecionado |
|-------------------------------------------------------|-----------------------|--------------------|
| Um álbum que é um contêiner de faixas                | CPAlbumID             | CPTrackID          |
| Uma lista que é um contêiner de faixas                  | CPListID              | CPTrackID          |
| Uma lista que é um contêiner de álbuns                  | CPListID              | CPAlbumID          |
| Uma estação de rádio que é um contêiner de listas          | CPRadioID             | CPListID           |
| O conjunto de todos os álbuns, que é um contêiner de álbuns | AllCPAlbumIDs         | CPAlbumID          |
| O conjunto de todos os gêneros, que é um contêiner de gêneros | AllCPGenreIDs         | CPGenreID          |



 

As guias no Windows Media Player representam tarefas diferentes. O Player exibe o conteúdo da loja online em três painéis de tarefas diferentes: **biblioteca**, **gravação** e **sincronização**. O painel de tarefas biblioteca também é chamado de painel de tarefas **procurar** . Às vezes, um painel de tarefas é chamado de *recurso*, por isso você pode ver termos como o recurso de *gravação* e o *recurso de sincronização* nesta documentação.

Os exemplos a seguir mostram como o Windows Media Player usa as cinco partes de informações (tarefa, tipo de local da biblioteca, ID do local da biblioteca, tipo de item selecionado, ID do item selecionado) para caracterizar exibições diferentes.

No painel de tarefas **gravar** , o player está exibindo um álbum como um contêiner de faixas. O álbum tem uma ID de 250. Na exibição, o item selecionado é a faixa que tem uma ID de 800. Observe que 800 é a ID da faixa no catálogo da loja online, não o número do controle no álbum.



| Item                  | Valor     |
|-----------------------|-----------|
| task                  | Queima      |
| tipo de local da biblioteca | CPAlbumID |
| ID do local da biblioteca   | 250       |
| tipo de item selecionado    | CPTrackID |
| ID do item selecionado      | 800       |



 

No painel de tarefas **sincronizar** , o player está exibindo o conjunto de todos os álbuns, que é um contêiner de álbuns. Na exibição, o item selecionado é o álbum que tem uma ID de 300. Observe que a ID do local da biblioteca não é aplicável a esta exibição.



| Item                  | Valor         |
|-----------------------|---------------|
| task                  | Sincronizar          |
| tipo de local da biblioteca | AllCPAlbumIDs |
| ID do local da biblioteca   | N/D           |
| tipo de item selecionado    | CPAlbumID     |
| ID do item selecionado      | 300           |



 

No controle de exibição em árvore, o nó raiz do repositório online é selecionado. Nesse caso, não há nenhum contêiner e, consequentemente, não há itens. O painel de tarefas da **biblioteca** inteira está exibindo uma página de descoberta.



| Item                  | Valor           |
|-----------------------|-----------------|
| task                  | Procurar          |
| tipo de local da biblioteca | RootLocation    |
| ID do local da biblioteca   | N/D             |
| tipo de item selecionado    | UnknownLocation |
| ID do item selecionado      | N/D             |



 

No painel de tarefas **sincronizar** , o player está exibindo o ano 2002 como um contêiner de faixas. Na exibição, o item selecionado é a faixa que tem uma ID de 450.



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

 

 




