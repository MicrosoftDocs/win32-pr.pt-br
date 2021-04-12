---
description: Há outras circunstâncias em que uma operação de leitura ou gravação pode ser concluída com menos do que o número solicitado de caracteres, mesmo que um tempo limite não tenha ocorrido.
ms.assetid: 05f84661-34ff-4e1f-9ec8-e4682138dfee
title: Erros de comunicação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eeace990620928ce898a3e8a31049a0083cdf07
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457016"
---
# <a name="communications-errors"></a><span data-ttu-id="36256-103">Erros de comunicação</span><span class="sxs-lookup"><span data-stu-id="36256-103">Communications Errors</span></span>

<span data-ttu-id="36256-104">Há outras circunstâncias em que uma operação de leitura ou gravação pode ser concluída com menos do que o número solicitado de caracteres, mesmo que um tempo limite não tenha ocorrido.</span><span class="sxs-lookup"><span data-stu-id="36256-104">There are other circumstances where a read or write operation can be completed with fewer than the requested number of characters, even though a time-out has not occurred.</span></span> <span data-ttu-id="36256-105">A seguir estão alguns exemplos:</span><span class="sxs-lookup"><span data-stu-id="36256-105">Following are some examples:</span></span>

-   <span data-ttu-id="36256-106">Alguns drivers dão suporte ao uso de caracteres especiais, que concluem uma operação de leitura imediatamente com apenas os caracteres que foram lidos até o ponto em que são recebidos.</span><span class="sxs-lookup"><span data-stu-id="36256-106">Some drivers support the use of special characters, which complete a read operation immediately with only the characters that have been read up to the point when they are received.</span></span>
-   <span data-ttu-id="36256-107">A função [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) pode ser chamada para finalizar prematuramente operações de leitura ou gravação pendentes.</span><span class="sxs-lookup"><span data-stu-id="36256-107">The [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) function can be called to prematurely terminate pending read or write operations.</span></span> <span data-ttu-id="36256-108">Essa função também pode excluir o conteúdo dos buffers de saída ou de entrada, ou ambos.</span><span class="sxs-lookup"><span data-stu-id="36256-108">This function can also delete the contents of the output or input buffers, or both.</span></span>
-   <span data-ttu-id="36256-109">Se ocorrer um erro de comunicação durante uma operação de leitura ou gravação, todas as operações de e/s no recurso de comunicações serão encerradas.</span><span class="sxs-lookup"><span data-stu-id="36256-109">If a communications error occurs during a read or write operation, all I/O operations on the communications resource are terminated.</span></span> <span data-ttu-id="36256-110">Condições de interrupção, erros de paridade ou erros de enquadramento são exemplos desses erros.</span><span class="sxs-lookup"><span data-stu-id="36256-110">Break conditions, parity errors, or framing errors are examples of such errors.</span></span> <span data-ttu-id="36256-111">Quando ocorre um erro, o processo deve chamar a função [**ClearCommError**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror) para limpar o sinalizador de erro antes que ele possa iniciar operações de e/s adicionais.</span><span class="sxs-lookup"><span data-stu-id="36256-111">When an error occurs, the process must call the [**ClearCommError**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror) function to clear the error flag before it can begin additional I/O operations.</span></span> <span data-ttu-id="36256-112">**ClearCommError** relata o erro específico que ocorreu e o status atual do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="36256-112">**ClearCommError** reports the specific error that occurred and the current status of the device.</span></span>

 

 



