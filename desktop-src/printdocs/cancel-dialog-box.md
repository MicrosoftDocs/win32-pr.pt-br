---
description: Este tópico descreve como exibir o progresso do trabalho de impressão para o usuário e dar a ele a opção de cancelar um trabalho de impressão que está em andamento no momento.
ms.assetid: 2b7a0ab7-bf7e-473d-ab43-8b79478d4453
title: Como exibir o progresso do trabalho de impressão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec61c07844262b258fb052d08d8d20e9285a8f7e9bb83808ea61eddaf32f3a88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950606"
---
# <a name="how-to-display-the-print-job-progress"></a>Como exibir o progresso do trabalho de impressão

Este tópico descreve como exibir o progresso do trabalho de impressão para o usuário e dar a ele a opção de cancelar um trabalho de impressão que está em andamento no momento.

## <a name="overview"></a>Visão geral

Um procedimento de caixa de diálogo de progresso de impressão normalmente executa as funções a seguir.

-   Exibir o progresso do trabalho de impressão para o usuário.
-   Inicie o thread de processamento de impressão.
-   Exibir um **botão Cancelar** para que o usuário possa interromper um trabalho de impressão antes de concluir.

Estritamente falando, a única coisa que o procedimento da caixa de diálogo progresso de impressão deve fazer é exibir o progresso do trabalho de impressão para o usuário. No entanto, como as outras duas funções na lista anterior estão intimamente relacionadas, elas também foram incluídas neste módulo.

## <a name="displaying-print-job-progress"></a>Exibindo o progresso do trabalho de impressão

Um procedimento de caixa de diálogo de progresso de impressão lida com as mensagens da janela a seguir.

-   **WM \_ INITDIALOG**

    Inicializa os controles que a caixa de diálogo usa.

-   **WM \_ SETCURSOR**

    Define o cursor como um ponteiro quando o usuário é capaz de cancelar um trabalho de impressão e para o cursor de espera quando o trabalho de impressão está em um ponto em que ele não pode ser cancelado.

-   **IMPRESSÃO \_ DO USUÁRIO INICIAR \_ \_ IMPRESSÃO**

    Define os parâmetros da barra de progresso para o trabalho de impressão e cria o thread de impressão para iniciar o processamento do trabalho de impressão.

    Essa é uma mensagem de janela específica do aplicativo.

-   **COMANDO WM \_ – IDCANCEL**

    Define o evento cancel para dizer ao thread de processamento de impressão para cancelar o trabalho de impressão.

-   **ATUALIZAÇÃO DE \_ STATUS DE IMPRESSÃO DO \_ \_ USUÁRIO**

    Atualiza a barra de progresso e o texto de status para mostrar o estado atual do trabalho de impressão.

    Essa é uma mensagem de janela específica do aplicativo.

-   **FECHAMENTO DE \_ IMPRESSÃO \_ DO USUÁRIO**

    Define o texto de status de fechamento na caixa de diálogo progresso para indicar que o trabalho de impressão está sendo fechado.

    Essa é uma mensagem de janela específica do aplicativo.

-   **IMPRESSÃO \_ DO \_ USUÁRIO CONCLUÍDA**

    Exibe a mensagem "Imprimir trabalho concluído" para o usuário e libera os handles e os eventos que foram usados nesse trabalho de impressão.

    Essa é uma mensagem de janela específica do aplicativo.

 

 



