---
title: Controle de captura preciso
description: Controle de captura preciso
ms.assetid: 497c9d77-f392-4cbb-88f3-8418e1e9fc6b
keywords:
- Funções de retorno de chamada AVICap, controle de captura preciso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0749d420d7a1999d074546a0cf577fdaceb72483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498681"
---
# <a name="precise-capture-control"></a><span data-ttu-id="d3179-104">Controle de captura preciso</span><span class="sxs-lookup"><span data-stu-id="d3179-104">Precise Capture Control</span></span>

<span data-ttu-id="d3179-105">Uma janela de captura pode fornecer a função de retorno de chamada de controle de captura com controle preciso ao longo do tempo em que a captura de streaming começa e termina.</span><span class="sxs-lookup"><span data-stu-id="d3179-105">A capture window can provide the capture-control callback function with precise control over the moments that streaming capture begin and end.</span></span> <span data-ttu-id="d3179-106">A primeira mensagem enviada do driver de captura para o procedimento de retorno de chamada define o parâmetro *nState* para CONTROLCALLBACK \_ Prevert após a alocação de todos os buffers e todas as outras preparações de captura são concluídas.</span><span class="sxs-lookup"><span data-stu-id="d3179-106">The first message sent from the capture driver to the callback procedure sets the *nState* parameter to CONTROLCALLBACK\_PREROLL after allocating all buffers and all other capture preparations are complete.</span></span> <span data-ttu-id="d3179-107">Essa mensagem fornece ao aplicativo a capacidade de fazer o registro das fontes de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d3179-107">This message gives the application the ability to preroll the video sources.</span></span> <span data-ttu-id="d3179-108">(A função de retorno de chamada especifica *nState* como seu segundo parâmetro.) A função de retorno de chamada retorna na gravação exata do momento para começar.</span><span class="sxs-lookup"><span data-stu-id="d3179-108">(The callback function specifies *nState* as its second parameter.) The callback function then returns at the exact moment recording is to begin.</span></span> <span data-ttu-id="d3179-109">Um valor de retorno de **true** da função de retorno de chamada continua a captura.</span><span class="sxs-lookup"><span data-stu-id="d3179-109">A return value of **TRUE** from the callback function continues capture.</span></span> <span data-ttu-id="d3179-110">Um valor de retorno de **false** anula A captura.</span><span class="sxs-lookup"><span data-stu-id="d3179-110">A return value of **FALSE** aborts capture.</span></span> <span data-ttu-id="d3179-111">Depois que a captura começa, a função de retorno de chamada é chamada com frequência com *nState* definido como CONTROLCALLBACK \_ Capture para permitir que o aplicativo encerre a captura retornando **false**.</span><span class="sxs-lookup"><span data-stu-id="d3179-111">Once capture begins, the callback function is called frequently with *nState* set to CONTROLCALLBACK\_CAPTURING to allow the application to end capture by returning **FALSE**.</span></span>

 

 




