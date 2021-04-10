---
description: Os escapes de impressora fornecidos pelo Windows de 16 bits permitiam acesso a recursos especiais do dispositivo.
ms.assetid: 4bdd1d47-8cf4-4088-aec8-88193e71a828
title: Escapes de impressora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59463c4201e97c5ac1ec689a772581fab28314b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170119"
---
# <a name="printer-escapes"></a><span data-ttu-id="9eb21-103">Escapes de impressora</span><span class="sxs-lookup"><span data-stu-id="9eb21-103">Printer Escapes</span></span>

<span data-ttu-id="9eb21-104">Os escapes de impressora fornecidos pelo Windows de 16 bits permitiam acesso a recursos especiais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9eb21-104">The printer escapes provided by 16-bit Windows allowed access special device features.</span></span> <span data-ttu-id="9eb21-105">A maioria desses escapes é obsoleta, mas alguns são fornecidos para simplificar a portabilidade de aplicativos baseados no Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="9eb21-105">Most of these escapes are obsolete, but a few are provided to simplify the porting of 16-bit Windows-based applications.</span></span> <span data-ttu-id="9eb21-106">O GDI dá suporte a um conjunto completo de funções de caminho que os aplicativos podem usar em vez dos escapes para desenhar caminhos em qualquer dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9eb21-106">GDI supports a complete set of path functions that applications can use instead of the escapes to draw paths on any device.</span></span> <span data-ttu-id="9eb21-107">Para obter uma lista de funções que substituem alguns dos escapes, consulte a função [**escape**](/windows/desktop/api/Wingdi/nf-wingdi-escape) .</span><span class="sxs-lookup"><span data-stu-id="9eb21-107">For a list of functions that replace some of the escapes, see the [**Escape**](/windows/desktop/api/Wingdi/nf-wingdi-escape) function.</span></span>

<span data-ttu-id="9eb21-108">Dos escapes de impressora originais do 64, somente **QUERYESCSUPPORT** e **PassThrough** podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="9eb21-108">Of the 64 original printer escapes, only **QUERYESCSUPPORT** and **PASSTHROUGH** can be used.</span></span>

<span data-ttu-id="9eb21-109">Há também uma função de escape estendida chamada [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="9eb21-109">There is also an extended escape function called [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span> <span data-ttu-id="9eb21-110">Essa função permite que os aplicativos acessem os recursos de um determinado dispositivo que não está diretamente disponível por meio do GDI.</span><span class="sxs-lookup"><span data-stu-id="9eb21-110">This function allows applications to access capabilities of a particular device not directly available through GDI.</span></span>

 

 



