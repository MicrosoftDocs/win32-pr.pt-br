---
description: Um &\# 0034;contexto de entrada&0034; é uma estrutura interna \# mantida pelo IMM.
ms.assetid: 2b639e30-5368-45bb-943d-db1ab6b62582
title: Contexto de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2927d3f573704aadb1ef72bdb26a35d37d90c1f90ab58d3a947ee84f8f38f7c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145895"
---
# <a name="input-context"></a>Contexto de entrada

Um "contexto de entrada" é uma estrutura interna mantida pelo IMM. Ele contém informações sobre o status do IME e é usado pelas janelas do IME. Por padrão, o sistema operacional cria e atribui um contexto de entrada a cada thread. Dentro do thread, esse contexto de entrada padrão é um recurso compartilhado e está associado a cada janela recém-criada.

Para recuperar ou definir informações no IME, um aplicativo com IME deve primeiro recuperar um alçado para o contexto de entrada associado a uma janela especificada. O aplicativo recupera o handle usando a [**função ImmGetContext.**](/windows/desktop/api/Imm/nf-imm-immgetcontext) Ele pode usar o alça recuperado em chamadas subsequentes para as funções do IMM para recuperar e definir valores de IME, como o estilo da janela de composição, o estilo de composição e a posição da janela de status. Depois que o aplicativo terminar de usar o contexto, ele deverá liberar o contexto usando a [**função ImmReleaseContext.**](/windows/desktop/api/Imm/nf-imm-immreleasecontext)

Como o contexto de entrada padrão é um recurso compartilhado, todas as alterações feitas pelo aplicativo a ele se aplicam a todas as janelas no thread. No entanto, o aplicativo pode substituir esse comportamento padrão criando seu próprio contexto de entrada e associando-o a uma ou mais janelas do thread. As alterações feitas em um contexto de entrada específico do aplicativo se aplicam somente às janelas associadas ao contexto.

Seu aplicativo pode criar um contexto de entrada usando a [**função ImmCreateContext.**](/windows/desktop/api/Imm/nf-imm-immcreatecontext) Para atribuir o contexto a uma janela, o aplicativo chama a [**função ImmAssociateContext.**](/windows/desktop/api/Imm/nf-imm-immassociatecontext) Essa função retorna um alça para o contexto de entrada associado anteriormente. Se o aplicativo ainda não tiver associado um contexto de entrada à janela, o handle retornado será para o contexto de entrada padrão. Normalmente, o aplicativo salva esse lidar e, posteriormente, o reassocia com a janela quando o contexto de entrada personalizado não é mais necessário.

Depois que um contexto de entrada é associado a uma janela, o sistema operacional seleciona automaticamente esse contexto quando a janela é ativada e recebe o foco de entrada. O estilo e outras informações no contexto de entrada afetam a entrada subsequente do teclado para essa janela, determinando como o IME opera.

Seu aplicativo deve destruir qualquer contexto de entrada personalizado antes de ser encerrado. Primeiro, o aplicativo remove o contexto de entrada de qualquer associação feita com janelas no thread usando a [**função ImmAssociateContext.**](/windows/desktop/api/Imm/nf-imm-immassociatecontext) Em seguida, ele chama a [**função ImmDestroyContext.**](/windows/desktop/api/Imm/nf-imm-immdestroycontext)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Gerenciador de Métodos de Entrada](about-input-method-manager.md)
</dt> </dl>

 

 



