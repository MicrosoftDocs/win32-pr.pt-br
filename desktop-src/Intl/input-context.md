---
description: Um &\# 0034; contexto de entrada&\# 0034; é uma estrutura interna mantida pelo IMM.
ms.assetid: 2b639e30-5368-45bb-943d-db1ab6b62582
title: Contexto de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16f1f83a397373e17a7d637b61a3232a3d72acde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828270"
---
# <a name="input-context"></a>Contexto de entrada

Um "contexto de entrada" é uma estrutura interna mantida pelo IMM. Ele contém informações sobre o status do IME e é usado pelas janelas do IME. Por padrão, o sistema operacional cria e atribui um contexto de entrada para cada thread. Dentro do thread, esse contexto de entrada padrão é um recurso compartilhado e é associado a cada janela recém-criada.

Para recuperar ou definir informações no IME, um aplicativo com reconhecimento de IME deve primeiro recuperar um identificador para o contexto de entrada associado a uma janela especificada. O aplicativo recupera o identificador usando a função [**ImmGetContext**](/windows/desktop/api/Imm/nf-imm-immgetcontext) . Ele pode usar o identificador recuperado em chamadas subsequentes para as funções do IMM para recuperar e definir valores do IME, como o estilo da janela de composição, o estilo de composição e a posição da janela de status. Depois que o aplicativo terminar de usar o contexto, ele deverá liberar o contexto usando a função [**ImmReleaseContext**](/windows/desktop/api/Imm/nf-imm-immreleasecontext) .

Como o contexto de entrada padrão é um recurso compartilhado, todas as alterações que o aplicativo faz para ele se aplicam a todas as janelas no thread. No entanto, o aplicativo pode substituir esse comportamento padrão criando seu próprio contexto de entrada e associando-o a uma ou mais janelas do thread. As alterações feitas em um contexto de entrada específico do aplicativo aplicam-se somente ao Windows associado ao contexto.

Seu aplicativo pode criar um contexto de entrada usando a função [**ImmCreateContext**](/windows/desktop/api/Imm/nf-imm-immcreatecontext) . Para atribuir o contexto a uma janela, o aplicativo chama a função [**ImmAssociateContext**](/windows/desktop/api/Imm/nf-imm-immassociatecontext) . Essa função retorna um identificador para o contexto de entrada associado anteriormente. Se o aplicativo ainda não tiver associado um contexto de entrada com a janela, o identificador retornado será para o contexto de entrada padrão. Normalmente, o aplicativo salva esse identificador e depois o reassocia com a janela quando o contexto de entrada personalizado não é mais necessário.

Depois que um contexto de entrada é associado a uma janela, o sistema operacional seleciona automaticamente esse contexto quando a janela é ativada e recebe o foco de entrada. O estilo e outras informações no contexto de entrada afetam a entrada de teclado subsequente para essa janela, determinando como o IME Opera.

Seu aplicativo deve destruir qualquer contexto de entrada personalizado antes de ser encerrado. Primeiro, o aplicativo remove o contexto de entrada de qualquer associação feita com o Windows no thread usando a função [**ImmAssociateContext**](/windows/desktop/api/Imm/nf-imm-immassociatecontext) . Em seguida, ele chama a função [**ImmDestroyContext**](/windows/desktop/api/Imm/nf-imm-immdestroycontext) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Gerenciador de métodos de entrada](about-input-method-manager.md)
</dt> </dl>

 

 



