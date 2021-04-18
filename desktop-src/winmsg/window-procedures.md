---
description: Esta seção discute os procedimentos de janela. Cada janela tem um procedimento de janela associado que processa todas as mensagens enviadas ou postadas em todas as janelas da classe.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\windowprocedures.htm
title: Procedimentos de janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ae68ba9b64557a6dc70d5c83788b8337648a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784634"
---
# <a name="window-procedures"></a>Procedimentos de janela

Cada janela tem um procedimento de janela associado — uma função que processa todas as mensagens enviadas ou postadas em todas as janelas da classe. Todos os aspectos da aparência e do comportamento de uma janela dependem da resposta do procedimento da janela para essas mensagens.

### <a name="in-this-section"></a>Nesta seção



| Nome                                                         | Descrição                                                                                                                                                                                                    |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre os procedimentos de janela](about-window-procedures.md)       | Discute os procedimentos de janela. Cada janela é um membro de uma determinada classe de janela. A classe Window determina o procedimento de janela padrão que uma janela individual usa para processar suas mensagens.<br/> |
| [Usando os procedimentos de janela](using-window-procedures.md)       | Aborda como executar as seguintes tarefas associadas a procedimentos de janela.<br/>                                                                                                                        |
| [Referência de procedimento de janela](window-procedure-reference.md) | Contém a referência de API.<br/>                                                                                                                                                                         |



 

### <a name="functions"></a>Funções



| Nome                                     | Descrição                                                                                                                                                                                                                                                                                                   |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) | Passa informações da mensagem para o procedimento de janela especificado. <br/>                                                                                                                                                                                                                                     |
| [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)   | Chama o procedimento de janela padrão para fornecer o processamento padrão para qualquer mensagem de janela que um aplicativo não processar. Essa função garante que cada mensagem seja processada. [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) é chamado com os mesmos parâmetros recebidos pelo procedimento de janela. <br/> |
| [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))           | Uma função definida pelo aplicativo que processa as mensagens enviadas a uma janela. O tipo **WndProc** define um ponteiro para essa função de retorno de chamada. [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) é um espaço reservado para o nome da função definida pelo aplicativo. <br/>                                                            |



 

 

 
