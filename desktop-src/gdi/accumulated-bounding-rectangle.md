---
description: O retângulo delimitador acumulado é o menor retângulo que envolve a parte de uma janela ou área de cliente afetada por operações de desenho recentes.
ms.assetid: 8ae13486-a9e2-4841-ada3-c70d30450ac8
title: Retângulo delimitador acumulado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ae3237304af68a4b8ff447b7ea2d64d3f81053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502438"
---
# <a name="accumulated-bounding-rectangle"></a><span data-ttu-id="d2adf-103">Retângulo delimitador acumulado</span><span class="sxs-lookup"><span data-stu-id="d2adf-103">Accumulated Bounding Rectangle</span></span>

<span data-ttu-id="d2adf-104">O *retângulo delimitador acumulado* é o menor retângulo que envolve a parte de uma janela ou área de cliente afetada por operações de desenho recentes.</span><span class="sxs-lookup"><span data-stu-id="d2adf-104">The *accumulated bounding rectangle* is the smallest rectangle enclosing the portion of a window or client area affected by recent drawing operations.</span></span> <span data-ttu-id="d2adf-105">Um aplicativo pode usar esse retângulo para determinar convenientemente a extensão das alterações causadas por operações de desenho.</span><span class="sxs-lookup"><span data-stu-id="d2adf-105">An application can use this rectangle to conveniently determine the extent of changes caused by drawing operations.</span></span> <span data-ttu-id="d2adf-106">Às vezes, ele é usado em conjunto com [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) para determinar qual parte da área do cliente deve ser redesenhada após a limpeza do bloqueio de atualização.</span><span class="sxs-lookup"><span data-stu-id="d2adf-106">It is sometimes used in conjunction with [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) to determine which portion of the client area must be redrawn after the update lock is cleared.</span></span>

<span data-ttu-id="d2adf-107">Um aplicativo usa a função [**SetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect) (especificando DCB \_ enable) para começar a acumular o retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="d2adf-107">An application uses the [**SetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect) function (specifying DCB\_ENABLE) to begin accumulating the bounding rectangle.</span></span> <span data-ttu-id="d2adf-108">O sistema, subsequentemente, acumula pontos para o retângulo delimitador, pois o aplicativo usa o contexto do dispositivo de exibição especificado.</span><span class="sxs-lookup"><span data-stu-id="d2adf-108">The system subsequently accumulates points for the bounding rectangle as the application uses the specified display device context.</span></span> <span data-ttu-id="d2adf-109">O aplicativo pode recuperar o retângulo delimitador atual a qualquer momento usando a função [**GetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect) .</span><span class="sxs-lookup"><span data-stu-id="d2adf-109">The application can retrieve the current bounding rectangle at any time by using the [**GetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect) function.</span></span> <span data-ttu-id="d2adf-110">O aplicativo interrompe a acumulação chamando **SetBoundsRect** novamente, especificando o \_ valor de desabilitação de DCB.</span><span class="sxs-lookup"><span data-stu-id="d2adf-110">The application stops the accumulation by calling **SetBoundsRect** again, specifying the DCB\_DISABLE value.</span></span>

 

 



