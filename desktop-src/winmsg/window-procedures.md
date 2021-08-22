---
description: Esta seção aborda os procedimentos de janela. Cada janela tem um procedimento de janela associado que processa todas as mensagens enviadas ou postadas em todas as janelas da classe.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\windowprocedures.htm
title: Procedimentos de janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b7892c1547d7f5ed1bf5d70a9242e3bb5bc6a3c8e93121470d27ecbd64fb912
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548456"
---
# <a name="window-procedures"></a>Procedimentos de janela

Cada janela tem um procedimento de janela associado – uma função que processa todas as mensagens enviadas ou postadas em todas as janelas da classe. Todos os aspectos da aparência e do comportamento de uma janela dependem da resposta do procedimento de janela a essas mensagens.

### <a name="in-this-section"></a>Nesta seção



| Nome                                                         | Descrição                                                                                                                                                                                                    |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre procedimentos de janela](about-window-procedures.md)       | Discute procedimentos de janela. Cada janela é membro de uma classe de janela específica. A classe window determina o procedimento de janela padrão que uma janela individual usa para processar suas mensagens.<br/> |
| [Usando procedimentos de janela](using-window-procedures.md)       | Aborda como executar as seguintes tarefas associadas a procedimentos de janela.<br/>                                                                                                                        |
| [Referência de procedimento de janela](window-procedure-reference.md) | Contém a referência de API.<br/>                                                                                                                                                                         |



 

### <a name="functions"></a>Funções



| Nome                                     | Descrição                                                                                                                                                                                                                                                                                                   |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) | Passa informações de mensagem para o procedimento de janela especificado. <br/>                                                                                                                                                                                                                                     |
| [**Defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)   | Chama o procedimento de janela padrão para fornecer processamento padrão para todas as mensagens de janela que um aplicativo não processa. Essa função garante que cada mensagem seja processada. [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) é chamado com os mesmos parâmetros recebidos pelo procedimento de janela. <br/> |
| [*Windowproc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))           | Uma função definida pelo aplicativo que processa mensagens enviadas para uma janela. O **tipo WNDPROC** define um ponteiro para essa função de retorno de chamada. [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) é um espaço reservado para o nome da função definida pelo aplicativo. <br/>                                                            |



 

 

 
