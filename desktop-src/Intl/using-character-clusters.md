---
description: Os clusters de caracteres são sequências de glifos que não podem ser divididas entre as linhas.
ms.assetid: ab852feb-9e26-429e-a02a-11fe0abdfafc
title: Usando clusters de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11357a929cf8fec2a7b0caa2bb6ae1ac403e3b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663484"
---
# <a name="using-character-clusters"></a><span data-ttu-id="fb3ab-103">Usando clusters de caracteres</span><span class="sxs-lookup"><span data-stu-id="fb3ab-103">Using Character Clusters</span></span>

<span data-ttu-id="fb3ab-104">Os clusters de caracteres são sequências de glifos que não podem ser divididas entre as linhas.</span><span class="sxs-lookup"><span data-stu-id="fb3ab-104">Character clusters are glyph sequences that cannot be split between lines.</span></span> <span data-ttu-id="fb3ab-105">Alguns idiomas, por exemplo, tailandês e Índico, restringem o posicionamento do cursor para pontos entre clusters.</span><span class="sxs-lookup"><span data-stu-id="fb3ab-105">Some languages, for example Thai and Indic, restrict caret placement to points between clusters.</span></span> <span data-ttu-id="fb3ab-106">Essa restrição se aplica ao movimento de cursor iniciado com ações de teclado ou mouse (teste de clique).</span><span class="sxs-lookup"><span data-stu-id="fb3ab-106">This restriction applies to caret movement initiated with keyboard or mouse actions (hit testing).</span></span>

<span data-ttu-id="fb3ab-107">O Uniscribe fornece informações de cluster em ambos os atributos visuais contidos em uma estrutura [**\_ VISATTR de script**](/windows/win32/api/usp10/ns-usp10-script_visattr) e os atributos lógicos contidos em uma estrutura [**\_ LOGATTR de script**](/windows/win32/api/usp10/ns-usp10-script_logattr) .</span><span class="sxs-lookup"><span data-stu-id="fb3ab-107">Uniscribe provides cluster information in both the visual attributes contained in a [**SCRIPT\_VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) structure, and the logical attributes contained in a [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure.</span></span> <span data-ttu-id="fb3ab-108">Depois que o aplicativo chama [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), as informações do cluster são representadas por sequências do mesmo valor na matriz **\_ LOGATTR de script** e pelo membro **fClusterStart** no **script \_ VISATTR** array.</span><span class="sxs-lookup"><span data-stu-id="fb3ab-108">After the application calls [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), the cluster information is represented both by sequences of the same value in the **SCRIPT\_LOGATTR** array, and by the **fClusterStart** member in the **SCRIPT\_VISATTR** array.</span></span>

<span data-ttu-id="fb3ab-109">[**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak) também recupera o membro **fCharStop** da estrutura [**\_ LOGATTR do script**](/windows/win32/api/usp10/ns-usp10-script_logattr) para identificar as posições do cluster.</span><span class="sxs-lookup"><span data-stu-id="fb3ab-109">[**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak) also retrieves the **fCharStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure to identify cluster positions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb3ab-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fb3ab-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb3ab-111">Usando o Uniscribe</span><span class="sxs-lookup"><span data-stu-id="fb3ab-111">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 



