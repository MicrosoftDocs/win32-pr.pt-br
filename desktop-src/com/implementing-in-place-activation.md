---
title: Implementando a ativação In-Place sistema
description: Implementando a ativação In-Place sistema
ms.assetid: 5fd67d1c-1dc5-4d83-a41e-b64d84cbf212
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 037fea98524b70f1d9d43dcef5909376ac136c5ea077bcbea06a663898ced354
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070816"
---
# <a name="implementing-in-place-activation"></a>Implementando a ativação In-Place sistema

A ativação in-locar permite que um usuário interaja com um objeto inserido sem sair do documento de contêiner. Quando um usuário ativa o objeto , uma barra de *menus* composta que inclui elementos das barras de menu do aplicativo de contêiner e do aplicativo de servidor substitui a barra de menus principal do contêiner. Comandos e recursos de ambos os aplicativos estão, portanto, disponíveis para o usuário, incluindo ajuda contextativa para o objeto ativo. Quando um usuário começa a trabalhar com alguma parte não objeto do documento, o objeto é desativado, fazendo com que o menu original do documento de contêiner substitua o menu composto.

Essa funcionalidade originalmente passou pelo nome de *edição in-in-place.* O nome foi alterado porque a edição é apenas uma maneira de um usuário interagir com um objeto em execução. Clipes de som, por exemplo, podem ser ouvido em vez de editar. Os clipes de vídeo podem ser exibidos em vez de editar. A ativação in-loca é particularmente apt no caso de clipes de vídeo porque permite que eles executem no local, sem chamar uma janela separada. Isso poderá ser crítico se o vídeo for exibido, digamos, em conjunto com os dados de texto adjacentes no documento de contêiner.

Implementar a ativação in-place é estritamente opcional para aplicativos de contêiner e servidor. O OLE ainda dá suporte ao modelo no qual ativar um objeto faz com que o aplicativo de servidor abra uma janela separada. Objetos vinculados sempre são abertos em uma janela separada para enfatizar que residem em um documento separado.

A ativação in-loco começa com o objeto em resposta a [**uma chamada IOleObject::D oVerb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb) de seu contêiner. Essa chamada geralmente ocorre em resposta a um usuário clicando duas vezes no objeto ou selecionando um comando (verbo) no menu Editar do aplicativo de contêiner.

A janela in-loco recebe a entrada do teclado e do mouse enquanto o objeto inserido está ativo. Quando um usuário seleciona comandos na barra de menus composta, o comando e as mensagens de menu associadas são enviadas para o contêiner ou aplicativo de objeto, dependendo de qual possui o menu suspenso específico selecionado. A entrada por meio de réguas, barras de ferramentas ou adornos de quadro de um objeto vai diretamente para o objeto inserido, que possui essas janelas.

Um objeto inserido ativado no local permanece ativo até que o contêiner o desative em resposta à entrada do usuário ou o objeto voluntariamente entrega o estado ativo, como um clipe de vídeo pode fazer, por exemplo. Um usuário pode desativar um objeto clicando dentro do documento de contêiner, mas fora da janela de ativação in-locar do objeto ou simplesmente clicando em outro objeto. Um objeto ativado no local permanecerá ativo, no entanto, se o usuário clicar na barra de título do contêiner, na barra de rolagem ou, em particular, na barra de menus.

Você pode implementar um servidor in-locar-activation-object como um servidor em processo (DLL) ou um servidor local (EXE). Em ambos os casos, a barra de menus composta contém itens (normalmente menus suspensos) dos processos de servidor e contêiner. No caso de um servidor em processo, a janela de ativação in-loco é simplesmente outra janela filho na hierarquia de janelas do contêiner, recebendo sua entrada por meio da bomba de mensagens do aplicativo de contêiner.

No caso de um servidor local, a janela de ativação in-loco pertence ao processo de aplicativo do servidor do objeto inserido, mas sua janela pai pertence ao contêiner. A entrada para a janela de ativação in-place aparece na fila de mensagens do servidor e é expedida pelo loop de mensagens do servidor. As bibliotecas OLE são responsáveis por fazer com que os comandos de menu e as mensagens sejam expedidos corretamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Documentos compostos](compound-documents.md)
</dt> </dl>

 

 




