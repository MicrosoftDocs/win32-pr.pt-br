---
description: Você usa a função GetDC para executar o desenho que deve ocorrer instantaneamente em vez de quando uma \_ mensagem do WM Paint está sendo processada.
ms.assetid: 75525e26-72f5-4a58-a663-0bbdc2034759
title: Usando a função GetDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c018228eccbce7b487444341481165e24214b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967856"
---
# <a name="using-the-getdc-function"></a><span data-ttu-id="4791a-103">Usando a função GetDC</span><span class="sxs-lookup"><span data-stu-id="4791a-103">Using the GetDC Function</span></span>

<span data-ttu-id="4791a-104">Você usa a função [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) para executar o desenho que deve ocorrer instantaneamente em vez de quando uma mensagem do [**WM \_ Paint**](wm-paint.md) está sendo processada.</span><span class="sxs-lookup"><span data-stu-id="4791a-104">You use the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) function to carry out drawing that must occur instantly rather than when a [**WM\_PAINT**](wm-paint.md) message is processing.</span></span> <span data-ttu-id="4791a-105">Esse desenho geralmente é em resposta a uma ação pelo usuário, como fazer uma seleção ou um desenho com o mouse.</span><span class="sxs-lookup"><span data-stu-id="4791a-105">Such drawing is usually in response to an action by the user, such as making a selection or drawing with the mouse.</span></span> <span data-ttu-id="4791a-106">Nesses casos, o usuário deve receber comentários instantâneos e não deve ser forçado a parar de selecionar ou desenhar para que o aplicativo exiba o resultado.</span><span class="sxs-lookup"><span data-stu-id="4791a-106">In such cases, the user should receive instant feedback and must not be forced to stop selecting or drawing in order for the application to display the result.</span></span> <span data-ttu-id="4791a-107">As seções a seguir mostram como usar o GetDC para desenhar em uma janela:</span><span class="sxs-lookup"><span data-stu-id="4791a-107">The following sections show how to use GetDC to draw in a window:</span></span>

-   [<span data-ttu-id="4791a-108">Desenho com o mouse</span><span class="sxs-lookup"><span data-stu-id="4791a-108">Drawing with the Mouse</span></span>](drawing-with-the-mouse.md)
-   [<span data-ttu-id="4791a-109">Desenhando em intervalos de tempo</span><span class="sxs-lookup"><span data-stu-id="4791a-109">Drawing at Timed Intervals</span></span>](drawing-at-timed-intervals.md)

 

 



