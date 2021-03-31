---
description: Este tópico descreve como renderizar os dados do programa a serem impressos.
ms.assetid: D1343C53-6F13-49FF-8C7C-25D5A3C31B22
title: 'Como: renderizar dados de trabalho de impressão'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2d9f8cbf68394fd56ebcf31cfb37ee8f337f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837146"
---
# <a name="how-to-render-print-job-data"></a><span data-ttu-id="3ec8b-103">Como: renderizar dados de trabalho de impressão</span><span class="sxs-lookup"><span data-stu-id="3ec8b-103">How To: Render Print Job Data</span></span>

<span data-ttu-id="3ec8b-104">Este tópico descreve como renderizar os dados do programa a serem impressos.</span><span class="sxs-lookup"><span data-stu-id="3ec8b-104">This topic describes how to render the program data to be printed.</span></span> <span data-ttu-id="3ec8b-105">Este tópico não explica em detalhes como renderizar imagens de texto ou gráficos específicos.</span><span class="sxs-lookup"><span data-stu-id="3ec8b-105">This topic does not explain in detail about how to render specific graphics or text images.</span></span> <span data-ttu-id="3ec8b-106">Em vez disso, ele descreve como gerenciar os dados do programa e renderizá-los como um documento XPS, que ele envia para uma impressora usando a [API de impressão XPS](xps-printing.md).</span><span class="sxs-lookup"><span data-stu-id="3ec8b-106">Instead, it describes how to manage the program data and render it as an XPS document, which it sends to a printer by using the [XPS Print API](xps-printing.md).</span></span>

## <a name="overview"></a><span data-ttu-id="3ec8b-107">Visão geral</span><span class="sxs-lookup"><span data-stu-id="3ec8b-107">Overview</span></span>

<span data-ttu-id="3ec8b-108">Renderizar dados de trabalho de impressão para impressão envolve pegar os dados específicos do programa, como texto, imagens e formatação, e convertê-los em um formato compatível com a impressora de destino.</span><span class="sxs-lookup"><span data-stu-id="3ec8b-108">Rendering print job data for printing involves taking the program-specific data, such as text, images, and formatting, and converting them into a format that is compatible with the destination printer.</span></span> <span data-ttu-id="3ec8b-109">O programa que envia os dados para a impressora deve enviá-lo no formato que o driver de impressora requer.</span><span class="sxs-lookup"><span data-stu-id="3ec8b-109">The program that sends the data to the printer must send it in the format that the printer driver requires.</span></span>

<span data-ttu-id="3ec8b-110">Use a [API de impressão XPS](xps-printing.md) para enviar os dados para a impressora e ela exige que os dados sejam formatados como um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="3ec8b-110">Use the [XPS Print API](xps-printing.md) to send the data to the printer and it requires the data to be formatted as an XPS document.</span></span> <span data-ttu-id="3ec8b-111">Para produzir o conteúdo do documento XPS que a API de impressão XPS precisa, o programa de exemplo usa a [API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3ec8b-111">To produce the XPS document content that the XPS Print API needs, the sample program uses the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span></span>

<span data-ttu-id="3ec8b-112">Se o conteúdo do programa estiver em um formato que não seja compatível com uma impressora, ele precisará ser renderizado antes de ser enviado para a impressora.</span><span class="sxs-lookup"><span data-stu-id="3ec8b-112">If the program content is in a format that is not compatible with a printer, it will need to be rendered before it is sent to the printer.</span></span> <span data-ttu-id="3ec8b-113">Se o programa usar a [API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) para gerenciar o conteúdo do programa, o conteúdo do programa estará em um formato que pode ser enviado diretamente para a [API de impressão do XPS](xps-printing.md) e não exigirá nenhuma renderização adicional antes de enviá-lo para a impressora.</span><span class="sxs-lookup"><span data-stu-id="3ec8b-113">If the program uses the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)) to manage its program content, the program content will be in a format that can be sent directly to the [XPS Print API](xps-printing.md) and will not require any additional rendering before you send it to the printer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ec8b-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3ec8b-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3ec8b-115">[API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3ec8b-115">[XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3ec8b-116">API de impressão XPS</span><span class="sxs-lookup"><span data-stu-id="3ec8b-116">XPS Print API</span></span>](xps-printing.md)
</dt> </dl>

 

 
