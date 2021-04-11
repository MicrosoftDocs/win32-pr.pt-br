---
title: Funções de Sistema de Arquivos Distribuído (DFS)
description: As funções de Sistema de Arquivos Distribuído (DFS) fornecem a capacidade de agrupar logicamente compartilhamentos em vários servidores e vincular de forma transparente compartilhamentos em um único namespace hierárquico. O DFS organiza os recursos compartilhados em uma rede em uma estrutura treelike.
ms.assetid: a29cde3e-483a-4658-94d4-27398f66abfb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73738d4f503d10e7668f0f323583f49604e3a90d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164135"
---
# <a name="distributed-file-system-dfs-functions"></a>Funções de Sistema de Arquivos Distribuído (DFS)

As funções de Sistema de Arquivos Distribuído (DFS) fornecem a capacidade de agrupar logicamente compartilhamentos em vários servidores e vincular de forma transparente compartilhamentos em um único namespace hierárquico. O DFS organiza os recursos compartilhados em uma rede em uma estrutura treelike.

O DFS dá suporte a namespaces de DFS *autônomos* , aqueles com um servidor host e namespaces *baseados em domínio* que têm vários servidores host e alta disponibilidade. Os *dados de topologia* do DFS para Namespaces baseados em domínio são armazenados em Active Directory. Os dados incluem a raiz DFS, os links DFS e os destinos DFS.

Cada estrutura de árvore do DFS tem um ou mais *destinos raiz*. O destino raiz é um servidor host que executa o serviço DFS. Uma estrutura de árvore do DFS pode conter um ou mais *links DFS*. Cada link DFS aponta para uma ou mais pastas compartilhadas na rede. Você pode adicionar, modificar e excluir links DFS de um namespace DFS. Quando você remove o último destino associado a um link do DFS, o DFS exclui o link do DFS no namespace do DFS. (Na documentação anterior, os links do DFS eram chamados de pontos de junção.)

Um link do DFS pode apontar para uma ou mais pastas compartilhadas; as pastas são chamadas de *destinos*. Quando os usuários acessam um link DFS, o servidor DFS seleciona um conjunto de destinos com base nas informações do site de um cliente. O cliente acessa o primeiro destino disponível no conjunto. Isso ajuda a distribuir solicitações de clientes entre os possíveis destinos e pode fornecer acessibilidade contínua para os usuários mesmo quando alguns servidores falham.

Um aplicativo pode usar as funções do DFS para:

- Adicione um link DFS a uma raiz DFS.
- Crie ou remova namespaces do DFS baseados em domínio e autônomos.
- Adicionar destinos a um link do DFS existente.
- Remover um link DFS de uma raiz DFS.
- Remover um destino de um link do DFS.
- Exiba e configure informações sobre raízes e links de DFS.

Para obter uma lista das funções de DFS, consulte [funções de sistema de arquivos distribuído](distributed-file-system-functions.md).

Para obter uma lista das estruturas do DFS, consulte [estruturas de sistema de arquivos distribuído](distributed-file-system-structures.md).

Os destinos em computadores que executam o Microsoft Windows podem ser publicados em um namespace do DFS. Você também pode publicar quaisquer compartilhamentos que não sejam da Microsoft para os quais os redirecionadores de cliente estejam disponíveis em um namespace do DFS. No entanto, ao contrário de um compartilhamento publicado em um servidor que executa o Windows Server, eles não podem hospedar uma raiz DFS ou fornecer referências a outros destinos DFS.

O DFS usa o serviço de replicação de arquivos do Windows Server para copiar alterações entre destinos replicados. Os usuários podem modificar arquivos armazenados em um destino e o serviço de replicação de arquivo propaga as alterações para os outros destinos designados. O serviço preserva a alteração mais recente em um documento ou arquivos.
