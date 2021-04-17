---
description: O spooler de impressão monitora os trabalhos de impressão atuais e a impressora de destino para determinar um horário apropriado para imprimir um trabalho.
ms.assetid: c3ce7c63-b72d-4e91-9509-5189f2ccac8a
title: Processador de impressão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bcb7ed062b4e03069201d3ec1faa0ee427f0973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752814"
---
# <a name="print-processor"></a><span data-ttu-id="3b8a6-103">Processador de impressão</span><span class="sxs-lookup"><span data-stu-id="3b8a6-103">Print Processor</span></span>

<span data-ttu-id="3b8a6-104">O spooler de impressão monitora os trabalhos de impressão atuais e a impressora de destino para determinar um horário apropriado para imprimir um trabalho.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-104">The print spooler monitors the current print jobs and the target printer to determine an appropriate time to print a job.</span></span> <span data-ttu-id="3b8a6-105">Depois que o spooler determina que um trabalho deve ser impresso, ele chama o processador de impressão.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-105">Once the spooler determines that a job should be printed, it calls the print processor.</span></span> <span data-ttu-id="3b8a6-106">O processador de impressão é um plug-in que processa os dados do trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-106">The print processor is a plug-in that processes print job data.</span></span>

<span data-ttu-id="3b8a6-107">Use as funções a seguir para trabalhar com processadores de impressão.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-107">Use the following functions to work with print processors.</span></span>



| <span data-ttu-id="3b8a6-108">Função</span><span class="sxs-lookup"><span data-stu-id="3b8a6-108">Function</span></span>                                                           | <span data-ttu-id="3b8a6-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b8a6-109">Description</span></span>                                                          |
|--------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="3b8a6-110">**AddPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="3b8a6-110">**AddPrintProcessor**</span></span>](addprintprocessor.md)                     | <span data-ttu-id="3b8a6-111">Instala um processador de impressão em um servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-111">Installs a print processor on a specified server.</span></span>                    |
| [<span data-ttu-id="3b8a6-112">**DeletePrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="3b8a6-112">**DeletePrintProcessor**</span></span>](deleteprintprocessor.md)               | <span data-ttu-id="3b8a6-113">Remove um processador de impressora de um servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-113">Removes a printer processor from a specified server.</span></span>                 |
| [<span data-ttu-id="3b8a6-114">**EnumPrintProcessorDatatypes**</span><span class="sxs-lookup"><span data-stu-id="3b8a6-114">**EnumPrintProcessorDatatypes**</span></span>](enumprintprocessordatatypes.md) | <span data-ttu-id="3b8a6-115">Enumera os tipos de dados aos quais um processador de impressão especificado dá suporte.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-115">Enumerates the data types that a specified print processor supports.</span></span> |
| [<span data-ttu-id="3b8a6-116">**EnumPrintProcessors**</span><span class="sxs-lookup"><span data-stu-id="3b8a6-116">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)                 | <span data-ttu-id="3b8a6-117">Enumera os processadores de impressão instalados em um servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-117">Enumerates the print processors installed on a specified server.</span></span>     |
| [<span data-ttu-id="3b8a6-118">**GetPrintProcessorDirectory**</span><span class="sxs-lookup"><span data-stu-id="3b8a6-118">**GetPrintProcessorDirectory**</span></span>](getprintprocessordirectory.md)   | <span data-ttu-id="3b8a6-119">Recupera o caminho para o processador de impressão no servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-119">Retrieves the path for the print processor on the specified server.</span></span>  |



 

 

 



