---
description: Esta seção descreve como imprimir a partir de um programa nativo do Windows.
ms.assetid: D0AE8FF8-D02D-43D3-80CA-E13EAA894F87
title: 'Como: imprimir a partir de um programa do Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84229823944d7f7104da359b953e579f1b21cdca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785041"
---
# <a name="how-to-print-from-a-windows-program"></a>Como: imprimir a partir de um programa do Windows

Esta seção descreve como imprimir a partir de um programa nativo do Windows.

## <a name="overview"></a>Visão geral

A impressão geralmente é parte integrante de um programa nativo do Windows. Portanto, não é um recurso que você pode adicionar facilmente depois de escrever o programa. Dito isso, se o programa for projetado para usar documentos XPS, não será necessário muito, se houver, código adicional para renderizar o conteúdo do documento para impressão. Os documentos XPS do aplicativo podem ser enviados diretamente para uma impressora que tem um driver de impressora XPSDrv.

Use a [API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) para criar o conteúdo do documento e a [API de impressão XPS](xps-printing.md) para enviar o conteúdo do documento para a impressora. A API de impressão XPS processa o conteúdo do documento para a impressora de destino. Se a impressora selecionada tiver um driver de impressora XPSDrv, o documento será enviado para a impressora sem nenhuma conversão adicional. Se a impressora selecionada tiver um driver de impressora baseado em GDI, o programa também poderá enviar o conteúdo para a impressora e a API de impressão XPS converterá o conteúdo do documento para que ele seja compatível com o driver de impressora baseado em GDI. Em ambos os casos, o processamento que o aplicativo executa é o mesmo.

## <a name="printing-tasks"></a>Tarefas de impressão

Os tópicos a seguir descrevem as etapas básicas de impressão do conteúdo do programa.

1.  **Coletar informações do trabalho de impressão do usuário.**

    Normalmente, um usuário inicia um trabalho de impressão quando seleciona a opção imprimir em um menu e o programa exibe uma caixa de diálogo Imprimir para coletar os detalhes do trabalho de impressão. O usuário normalmente seleciona a impressora, o número de cópias e os detalhes de configuração da impressora, como impressão e grampeamento em dois lados.

    Para obter informações sobre como fazer isso, consulte [como coletar informações do trabalho de impressão do usuário](preparing-to-print.md).

2.  **Criar indicador de progresso.**

    Um indicador de progresso fornece ao usuário comentários sobre como o trabalho de impressão está progredindo. O indicador de progresso pode ser uma barra de progresso que faz parte de uma caixa de diálogo que inclui o botão **Cancelar** para o trabalho ou pode ser uma barra de progresso na barra de status na parte inferior da janela principal.

    Para obter informações sobre o indicador de progresso, consulte [como exibir o progresso do trabalho de impressão](cancel-dialog-box.md).

    Para obter mais ideias sobre como exibir o progresso do trabalho de impressão, consulte as informações nas diretrizes de [desenvolvimento da interface do usuário do aplicativo do Windows](/windows/desktop/windows-application-ui-development) .

3.  **Inicie o thread de impressão.**

    Depois que o programa coletou as informações do trabalho de impressão do usuário, ele pode iniciar o thread de impressão para executar o processamento real do documento para impressão.

    Para obter informações sobre o thread de impressão, consulte [como: Iniciar e parar um thread de impressão](how-to--start-and-stop-a-printing-thread.md).

4.  **Renderizar dados do trabalho de impressão.**

    O thread de impressão renderiza os dados do documento para impressão. Você deve dividir esse processamento em etapas de processamento discretos para que o usuário possa interromper o processamento e cancelar o trabalho, bem como não permitir que o thread de processamento bloqueie outros threads e processos.

    Para obter informações sobre como o renderiza os dados do trabalho de impressão, consulte [como: renderizar dados do trabalho de impressão](how-to--render-the-print-job-data.md).

5.  **Monitorar o andamento do trabalho de impressão.**

    À medida que cada etapa de processamento é executada, atualize a barra de progresso para informar o uso. Compute as etapas de processamento para concluir o trabalho solicitado e, em seguida, atualiza a barra de progresso conforme essas etapas são executadas.

6.  **Feche o trabalho de impressão e encerre o thread de impressão.**

    Depois que o programa enviar o trabalho de impressão para a impressora ou se o usuário tiver cancelado o trabalho de impressão, você deverá fechar o trabalho de impressão e liberar os recursos usados pelo trabalho de impressão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como coletar informações do trabalho de impressão do usuário](preparing-to-print.md)
</dt> </dl>

 

 
