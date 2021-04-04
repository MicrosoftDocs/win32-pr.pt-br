---
title: Objetos inseridos (COM)
description: Objetos inseridos
ms.assetid: 1f863fd4-fead-4dd3-b855-8820e015b52a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da9938b17130209fec024f94ee99061ad690693
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085069"
---
# <a name="embedded-objects-com"></a>Objetos inseridos (COM)

Um objeto incorporado é armazenado fisicamente no documento composto, juntamente com todas as informações necessárias para gerenciar o objeto. Em outras palavras, o objeto incorporado é, na verdade, uma parte do documento composto no qual ele reside. Essa organização tem algumas desvantagens. Primeiro, um documento composto contendo objetos inseridos será maior que um contendo os mesmos objetos que os links. Em segundo lugar, as alterações feitas na origem de um objeto incorporado não serão replicadas automaticamente na cópia inserida, e as alterações na cópia inserida não serão refletidas na origem, pois elas estão com um link.

Ainda assim, para determinadas finalidades, a incorporação oferece várias vantagens em relação aos links. Primeiro, os usuários podem transferir documentos compostos com objetos incorporados para outros computadores ou outros locais no mesmo computador, sem quebrar um link. Em segundo lugar, os usuários podem editar objetos inseridos sem alterar o conteúdo do original. Às vezes, essa separação é precisamente o que é necessário. Terceiro, os objetos inseridos podem ser ativados em vigor, o que significa que o usuário pode editar ou manipular o objeto sem precisar trabalhar em uma janela separada do contêiner do objeto. Em vez disso, quando o objeto é ativado, a interface do usuário do aplicativo de contêiner é alterada para expor essas ferramentas que são necessárias para gerenciar ou modificar o objeto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando objetos vinculados e incorporados de dados existentes](creating-linked-and-embedded-objects-from-existing-data.md)
</dt> </dl>

 

 




