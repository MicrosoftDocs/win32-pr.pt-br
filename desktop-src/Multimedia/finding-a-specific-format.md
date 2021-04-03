---
title: Localizando um formato específico
description: Localizando um formato específico
ms.assetid: 0c892758-d409-4ed7-8f38-a24eee646b65
keywords:
- Gerenciador de compactação de áudio (ACM), localizando formatos
- ACM (Gerenciador de compactação de áudio), localizando formatos
- Exemplos do ACM, localização de formatos
- Localizando formatos
- função acmFormatEnum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c148c075df09cb702caf6b1d192fe8ce41b48ad0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916539"
---
# <a name="finding-a-specific-format"></a><span data-ttu-id="fc97e-108">Localizando um formato específico</span><span class="sxs-lookup"><span data-stu-id="fc97e-108">Finding a Specific Format</span></span>

<span data-ttu-id="fc97e-109">Um aplicativo pode ter apenas uma especificação parcial para um formato quando precisa da especificação completa.</span><span class="sxs-lookup"><span data-stu-id="fc97e-109">An application might have only a partial specification for a format when it needs the full specification.</span></span> <span data-ttu-id="fc97e-110">Por exemplo, a especificação pode estipular um formato de um mono de 4 bits, uma ADPCM, mas não a média de bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="fc97e-110">For example, the specification might stipulate an 11-kHz mono, 4-bit ADPCM format, but not the average bytes per second.</span></span> <span data-ttu-id="fc97e-111">O aplicativo pode obter o formato completo sem intervenção do usuário usando a função [**acmFormatEnum**](/windows/desktop/api/Msacm/nf-msacm-acmformatenum) e especificando sinalizadores no parâmetro *fdwEnum* .</span><span class="sxs-lookup"><span data-stu-id="fc97e-111">The application can get the full format without user intervention by using the [**acmFormatEnum**](/windows/desktop/api/Msacm/nf-msacm-acmformatenum) function and specifying flags in the *fdwEnum* parameter.</span></span>

 

 




