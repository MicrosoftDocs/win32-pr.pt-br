---
title: Implementando a ativação do In-Place
description: Implementando a ativação do In-Place
ms.assetid: 5fd67d1c-1dc5-4d83-a41e-b64d84cbf212
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c075f143c772fe34de0c494664227e892b998387
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105770058"
---
# <a name="implementing-in-place-activation"></a>Implementando a ativação do In-Place

A ativação in-loco permite que um usuário interaja com um objeto inserido sem sair do documento de contêiner. Quando um usuário ativa o objeto, uma *barra de menus compostas* que inclui elementos das barras de menus do aplicativo de contêiner e do aplicativo do servidor substitui a barra de menus principal do contêiner. Os comandos e recursos de ambos os aplicativos estão, portanto, disponíveis para o usuário, incluindo a ajuda contextual para o objeto ativo. Quando um usuário começa a trabalhar com alguma parte não objeto do documento, o objeto é desativado, fazendo com que o menu original do documento de contêiner substitua o menu composto.

Esse recurso foi originalmente criado pelo nome da *edição in-loco*. O nome foi alterado porque a edição é apenas uma maneira de um usuário interagir com um objeto em execução. Os clipes de som, por exemplo, podem ser ouvidos em vez de editar. Os clipes de vídeo podem ser exibidos em vez de editar. A ativação in-loco é particularmente apta no caso de clipes de vídeo porque permite que eles sejam executados no local, sem chamar uma janela separada. Isso pode ser crítico se o vídeo fosse exibido, digamos, em conjunto com os dados de texto adjacentes no documento de contêiner.

A implementação da ativação in-loco é estritamente opcional para os aplicativos de contêiner e de servidor. O OLE ainda dá suporte ao modelo no qual a ativação de um objeto faz com que o aplicativo de servidor abra uma janela separada. Os objetos vinculados sempre são abertos em uma janela separada para enfatizar que eles residem em um documento separado.

A ativação in-loco começa com o objeto em resposta a uma chamada [**IOleObject::D overb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb) de seu contêiner. Essa chamada geralmente acontece em resposta a um usuário clicando duas vezes no objeto ou selecionando um comando (verbo) no menu Editar do aplicativo contêiner.

A janela in-loco recebe a entrada do teclado e do mouse enquanto o objeto incorporado está ativo. Quando um usuário seleciona comandos na barra de menus de composição, o comando e as mensagens de menu associadas são enviadas para o aplicativo de contêiner ou objeto, dependendo de quem possui o menu suspenso específico selecionado. A entrada por meio de réguas, barras de ferramentas ou adornos de quadros de um objeto vai diretamente para o objeto inserido, que possui essas janelas.

Um objeto incorporado ativado no local permanece ativo até que o contêiner o desative em resposta à entrada do usuário ou o objeto seja voluntariamente formado pelo estado ativo, como um clipe de vídeo pode, por exemplo. Um usuário pode desativar um objeto clicando dentro do documento do contêiner, mas fora da janela de ativação in-loco do objeto, ou simplesmente clicando em outro objeto. Um objeto ativado no local permanece ativo, no entanto, se o usuário clicar na barra de título do contêiner, na barra de rolagem ou, em particular, na barra de menus.

Você pode implementar um servidor in-loco-Activation-Object como um servidor em processo (DLL) ou um servidor local (EXE). Em ambos os casos, a barra de menu composto contém itens (normalmente menus suspensos) dos processos de servidor e contêiner. No caso de um servidor em processo, a janela de ativação in-loco é simplesmente outra janela filho na hierarquia de janela do contêiner, recebendo sua entrada por meio da bomba de mensagem do aplicativo de contêiner.

No caso de um servidor local, a janela de ativação in-loco pertence ao processo do aplicativo de servidor do objeto incorporado, mas sua janela pai pertence ao contêiner. A entrada para a janela de ativação in-loco é exibida na fila de mensagens do servidor e é expedida pelo loop de mensagem do servidor. As bibliotecas OLE são responsáveis por ver que os comandos de menu e as mensagens são expedidas corretamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Documentos compostos](compound-documents.md)
</dt> </dl>

 

 




