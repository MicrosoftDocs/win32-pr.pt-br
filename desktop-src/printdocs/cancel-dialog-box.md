---
description: Este tópico descreve como exibir o progresso do trabalho de impressão para o usuário e dar a eles a opção de cancelar um trabalho de impressão que está atualmente em andamento.
ms.assetid: 2b7a0ab7-bf7e-473d-ab43-8b79478d4453
title: Como exibir o progresso do trabalho de impressão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9effc778f6affaba5b53cbd96a7a428ea5554d8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789921"
---
# <a name="how-to-display-the-print-job-progress"></a>Como exibir o progresso do trabalho de impressão

Este tópico descreve como exibir o progresso do trabalho de impressão para o usuário e dar a eles a opção de cancelar um trabalho de impressão que está atualmente em andamento.

## <a name="overview"></a>Visão geral

Um procedimento de caixa de diálogo de progresso de impressão normalmente executa as funções a seguir.

-   Exibir o progresso do trabalho de impressão para o usuário.
-   Inicie o thread de processamento de impressão.
-   Exibir um botão de **cancelamento** para que o usuário possa interromper um trabalho de impressão antes de ser concluído.

Estritamente falando, a única coisa que o procedimento da caixa de diálogo de progresso da impressão deve fazer é exibir o progresso do trabalho de impressão para o usuário. No entanto, como as outras duas funções na lista anterior estão fortemente relacionadas, elas também foram incluídas neste módulo.

## <a name="displaying-print-job-progress"></a>Exibindo o progresso do trabalho de impressão

Um procedimento de caixa de diálogo de progresso de impressão manipula as seguintes mensagens de janela.

-   **INITDIALOG do WM \_**

    Inicializa os controles que a caixa de diálogo usa.

-   **WM \_ SETcursor**

    Define o cursor para um ponteiro quando o usuário é capaz de cancelar um trabalho de impressão e para o cursor de espera quando o trabalho de impressão está em um ponto em que não pode ser cancelado.

-   **impressão de \_ início de impressão do usuário \_ \_**

    Define os parâmetros da barra de progresso para o trabalho de impressão e cria o thread de impressão para iniciar o processamento do trabalho de impressão.

    Esta é uma mensagem de janela específica do aplicativo.

-   **comando do WM \_ – IDCANCEL**

    Define o evento de cancelamento para instruir o thread de processamento de impressão a cancelar o trabalho de impressão.

-   **\_atualização do \_ status de impressão do usuário \_**

    Atualiza a barra de progresso e o texto de status para mostrar o estado atual do trabalho de impressão.

    Esta é uma mensagem de janela específica do aplicativo.

-   **\_fechamento de impressão do usuário \_**

    Define o texto de status de fechamento na caixa de diálogo progresso para indicar que o trabalho de impressão está sendo fechado.

    Esta é uma mensagem de janela específica do aplicativo.

-   **impressão do usuário \_ \_ concluída**

    Exibe a mensagem "trabalho de impressão concluído" para o usuário e libera identificadores e eventos que foram usados neste trabalho de impressão.

    Esta é uma mensagem de janela específica do aplicativo.

 

 



