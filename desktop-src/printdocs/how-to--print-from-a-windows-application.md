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
# <a name="how-to-print-from-a-windows-program"></a><span data-ttu-id="701b3-103">Como: imprimir a partir de um programa do Windows</span><span class="sxs-lookup"><span data-stu-id="701b3-103">How To: Print from a Windows Program</span></span>

<span data-ttu-id="701b3-104">Esta seção descreve como imprimir a partir de um programa nativo do Windows.</span><span class="sxs-lookup"><span data-stu-id="701b3-104">This section describes how to print from a native Windows program.</span></span>

## <a name="overview"></a><span data-ttu-id="701b3-105">Visão geral</span><span class="sxs-lookup"><span data-stu-id="701b3-105">Overview</span></span>

<span data-ttu-id="701b3-106">A impressão geralmente é parte integrante de um programa nativo do Windows.</span><span class="sxs-lookup"><span data-stu-id="701b3-106">Printing is usually an integral part of a native Windows program.</span></span> <span data-ttu-id="701b3-107">Portanto, não é um recurso que você pode adicionar facilmente depois de escrever o programa.</span><span class="sxs-lookup"><span data-stu-id="701b3-107">Therefore, it is not a feature that you can add easily after you have written the program.</span></span> <span data-ttu-id="701b3-108">Dito isso, se o programa for projetado para usar documentos XPS, não será necessário muito, se houver, código adicional para renderizar o conteúdo do documento para impressão.</span><span class="sxs-lookup"><span data-stu-id="701b3-108">That being said, if the program is designed to use XPS documents it will not need much, if any, additional code to render the document content for printing.</span></span> <span data-ttu-id="701b3-109">Os documentos XPS do aplicativo podem ser enviados diretamente para uma impressora que tem um driver de impressora XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="701b3-109">The XPS documents of the application can be sent directly to a printer that has an XPSDrv printer driver.</span></span>

<span data-ttu-id="701b3-110">Use a [API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) para criar o conteúdo do documento e a [API de impressão XPS](xps-printing.md) para enviar o conteúdo do documento para a impressora.</span><span class="sxs-lookup"><span data-stu-id="701b3-110">Use the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)) to create the document content and the [XPS Print API](xps-printing.md) to send the document content to the printer.</span></span> <span data-ttu-id="701b3-111">A API de impressão XPS processa o conteúdo do documento para a impressora de destino.</span><span class="sxs-lookup"><span data-stu-id="701b3-111">The XPS Print API processes the document content for the destination printer.</span></span> <span data-ttu-id="701b3-112">Se a impressora selecionada tiver um driver de impressora XPSDrv, o documento será enviado para a impressora sem nenhuma conversão adicional.</span><span class="sxs-lookup"><span data-stu-id="701b3-112">If the selected printer has an XPSDrv printer driver, the document will be sent to the printer without any additional conversion.</span></span> <span data-ttu-id="701b3-113">Se a impressora selecionada tiver um driver de impressora baseado em GDI, o programa também poderá enviar o conteúdo para a impressora e a API de impressão XPS converterá o conteúdo do documento para que ele seja compatível com o driver de impressora baseado em GDI.</span><span class="sxs-lookup"><span data-stu-id="701b3-113">If the selected printer has a GDI-based printer driver, the program can also send the content to the printer, and the XPS Print API converts the document content so that it will be compatible with the GDI-based printer driver.</span></span> <span data-ttu-id="701b3-114">Em ambos os casos, o processamento que o aplicativo executa é o mesmo.</span><span class="sxs-lookup"><span data-stu-id="701b3-114">In either case, the processing that the application performs is the same.</span></span>

## <a name="printing-tasks"></a><span data-ttu-id="701b3-115">Tarefas de impressão</span><span class="sxs-lookup"><span data-stu-id="701b3-115">Printing tasks</span></span>

<span data-ttu-id="701b3-116">Os tópicos a seguir descrevem as etapas básicas de impressão do conteúdo do programa.</span><span class="sxs-lookup"><span data-stu-id="701b3-116">The following topics describe the basic steps of printing program content.</span></span>

1.  <span data-ttu-id="701b3-117">**Coletar informações do trabalho de impressão do usuário.**</span><span class="sxs-lookup"><span data-stu-id="701b3-117">**Collect print job information from user.**</span></span>

    <span data-ttu-id="701b3-118">Normalmente, um usuário inicia um trabalho de impressão quando seleciona a opção imprimir em um menu e o programa exibe uma caixa de diálogo Imprimir para coletar os detalhes do trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="701b3-118">Typically, a user initiates a print job when they select the print option from a menu and the program displays a print dialog box to collect the details of the print job.</span></span> <span data-ttu-id="701b3-119">O usuário normalmente seleciona a impressora, o número de cópias e os detalhes de configuração da impressora, como impressão e grampeamento em dois lados.</span><span class="sxs-lookup"><span data-stu-id="701b3-119">The user typically selects the printer, the number of copies, and printer configuration details such as two-sided printing and stapling.</span></span>

    <span data-ttu-id="701b3-120">Para obter informações sobre como fazer isso, consulte [como coletar informações do trabalho de impressão do usuário](preparing-to-print.md).</span><span class="sxs-lookup"><span data-stu-id="701b3-120">For information about how to do this, see [How To: Collect Print Job Information from the User](preparing-to-print.md).</span></span>

2.  <span data-ttu-id="701b3-121">**Criar indicador de progresso.**</span><span class="sxs-lookup"><span data-stu-id="701b3-121">**Create progress indicator.**</span></span>

    <span data-ttu-id="701b3-122">Um indicador de progresso fornece ao usuário comentários sobre como o trabalho de impressão está progredindo.</span><span class="sxs-lookup"><span data-stu-id="701b3-122">A progress indicator provides the user with feedback about how the print job is progressing.</span></span> <span data-ttu-id="701b3-123">O indicador de progresso pode ser uma barra de progresso que faz parte de uma caixa de diálogo que inclui o botão **Cancelar** para o trabalho ou pode ser uma barra de progresso na barra de status na parte inferior da janela principal.</span><span class="sxs-lookup"><span data-stu-id="701b3-123">The progress indicator can be a progress bar that is part of a dialog box that includes the **Cancel** button for the job, or it can be a progress bar in the status bar at the bottom of the main window.</span></span>

    <span data-ttu-id="701b3-124">Para obter informações sobre o indicador de progresso, consulte [como exibir o progresso do trabalho de impressão](cancel-dialog-box.md).</span><span class="sxs-lookup"><span data-stu-id="701b3-124">For information about the progress indicator works, see [How To: Display the Print Job Progress](cancel-dialog-box.md).</span></span>

    <span data-ttu-id="701b3-125">Para obter mais ideias sobre como exibir o progresso do trabalho de impressão, consulte as informações nas diretrizes de [desenvolvimento da interface do usuário do aplicativo do Windows](/windows/desktop/windows-application-ui-development) .</span><span class="sxs-lookup"><span data-stu-id="701b3-125">For more ideas about how to display the progress of the print job, see the information in the [Windows Application UI Development](/windows/desktop/windows-application-ui-development) guidelines.</span></span>

3.  <span data-ttu-id="701b3-126">**Inicie o thread de impressão.**</span><span class="sxs-lookup"><span data-stu-id="701b3-126">**Start the printing thread.**</span></span>

    <span data-ttu-id="701b3-127">Depois que o programa coletou as informações do trabalho de impressão do usuário, ele pode iniciar o thread de impressão para executar o processamento real do documento para impressão.</span><span class="sxs-lookup"><span data-stu-id="701b3-127">After the program has collected the print job information from the user, it can start the printing thread to perform the actual processing of the document for printing.</span></span>

    <span data-ttu-id="701b3-128">Para obter informações sobre o thread de impressão, consulte [como: Iniciar e parar um thread de impressão](how-to--start-and-stop-a-printing-thread.md).</span><span class="sxs-lookup"><span data-stu-id="701b3-128">For information about the printing thread, see [How To: Start and Stop a Printing Thread](how-to--start-and-stop-a-printing-thread.md).</span></span>

4.  <span data-ttu-id="701b3-129">**Renderizar dados do trabalho de impressão.**</span><span class="sxs-lookup"><span data-stu-id="701b3-129">**Render print job data.**</span></span>

    <span data-ttu-id="701b3-130">O thread de impressão renderiza os dados do documento para impressão.</span><span class="sxs-lookup"><span data-stu-id="701b3-130">The printing thread renders the document data for printing.</span></span> <span data-ttu-id="701b3-131">Você deve dividir esse processamento em etapas de processamento discretos para que o usuário possa interromper o processamento e cancelar o trabalho, bem como não permitir que o thread de processamento bloqueie outros threads e processos.</span><span class="sxs-lookup"><span data-stu-id="701b3-131">You should break down this processing into discrete processing steps so that the user can interrupt the processing and cancel the job as well as to not allow the processing thread to block other threads and processes.</span></span>

    <span data-ttu-id="701b3-132">Para obter informações sobre como o renderiza os dados do trabalho de impressão, consulte [como: renderizar dados do trabalho de impressão](how-to--render-the-print-job-data.md).</span><span class="sxs-lookup"><span data-stu-id="701b3-132">For information about how the renders the print job data, see [How To: Render Print Job Data](how-to--render-the-print-job-data.md).</span></span>

5.  <span data-ttu-id="701b3-133">**Monitorar o andamento do trabalho de impressão.**</span><span class="sxs-lookup"><span data-stu-id="701b3-133">**Monitor print job progress.**</span></span>

    <span data-ttu-id="701b3-134">À medida que cada etapa de processamento é executada, atualize a barra de progresso para informar o uso.</span><span class="sxs-lookup"><span data-stu-id="701b3-134">As each processing step is performed, update the progress bar to inform the use.</span></span> <span data-ttu-id="701b3-135">Compute as etapas de processamento para concluir o trabalho solicitado e, em seguida, atualiza a barra de progresso conforme essas etapas são executadas.</span><span class="sxs-lookup"><span data-stu-id="701b3-135">Compute the processing steps to complete the requested job and then updates the progress bar as those steps are performed.</span></span>

6.  <span data-ttu-id="701b3-136">**Feche o trabalho de impressão e encerre o thread de impressão.**</span><span class="sxs-lookup"><span data-stu-id="701b3-136">**Close print job and terminate printing thread.**</span></span>

    <span data-ttu-id="701b3-137">Depois que o programa enviar o trabalho de impressão para a impressora ou se o usuário tiver cancelado o trabalho de impressão, você deverá fechar o trabalho de impressão e liberar os recursos usados pelo trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="701b3-137">After the program has sent the print job to the printer, or if the user has cancelled the print job, you must close the print job and release the resources used by the print job.</span></span>

## <a name="related-topics"></a><span data-ttu-id="701b3-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="701b3-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="701b3-139">Como coletar informações do trabalho de impressão do usuário</span><span class="sxs-lookup"><span data-stu-id="701b3-139">How To: Collect Print Job Information from the User</span></span>](preparing-to-print.md)
</dt> </dl>

 

 
