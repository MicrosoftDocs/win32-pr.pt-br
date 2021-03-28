---
description: Fontes de vários arquivos de recurso
ms.assetid: 4625fe62-d55d-4828-9174-975a731a8f62
title: Fontes de vários arquivos de recurso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3802705ba4b199fa00d2cc2961d3c4472c4e365
ms.sourcegitcommit: fa5c081bf792b119a7bb92182cde1f85ca75967b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/17/2021
ms.locfileid: "104989458"
---
# <a name="fonts-from-multiple-resource-files"></a><span data-ttu-id="1de21-103">Fontes de vários arquivos de recurso</span><span class="sxs-lookup"><span data-stu-id="1de21-103">Fonts from Multiple Resource Files</span></span>

<span data-ttu-id="1de21-104">Normalmente, uma fonte está contida em um único arquivo de recurso de fonte.</span><span class="sxs-lookup"><span data-stu-id="1de21-104">Typically, a font is contained in a single font resource file.</span></span> <span data-ttu-id="1de21-105">No entanto, as informações de algumas fontes são distribuídas entre vários arquivos.</span><span class="sxs-lookup"><span data-stu-id="1de21-105">However, the information for some fonts is spread among several files.</span></span> <span data-ttu-id="1de21-106">Por exemplo, digite 1 várias fontes mestras exigem dois arquivos:</span><span class="sxs-lookup"><span data-stu-id="1de21-106">For example, Type 1 multiple master fonts require two files:</span></span>

-   <span data-ttu-id="1de21-107">. PFM para as métricas de fonte</span><span class="sxs-lookup"><span data-stu-id="1de21-107">.pfm for the font metrics</span></span>
-   <span data-ttu-id="1de21-108">. pfb para os bits de fonte</span><span class="sxs-lookup"><span data-stu-id="1de21-108">.pfb for the font bits</span></span>

<span data-ttu-id="1de21-109">Para adicionar uma fonte de vários arquivos ao sistema, use as funções [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) ou [**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) .</span><span class="sxs-lookup"><span data-stu-id="1de21-109">To add a font from multiple files to the system, use the [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) or [**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) functions.</span></span> <span data-ttu-id="1de21-110">O parâmetro *lpszFileName* nessas funções deve apontar para uma cadeia de caracteres que contém os nomes de arquivo separados pela barra vertical ou pelo pipe ( \| ).</span><span class="sxs-lookup"><span data-stu-id="1de21-110">The *lpszFilename* parameter in these functions must point to a string that contains the file names separated by the vertical bar or pipe ( \| ).</span></span> <span data-ttu-id="1de21-111">Por exemplo, para especificar abcxxxxx. PFM e abcxxxxx. pfb para uma fonte do tipo 1, use a cadeia de caracteres "abcxxxxx. PFM \| abcxxxxx. pfb".</span><span class="sxs-lookup"><span data-stu-id="1de21-111">For example, to specify abcxxxxx.pfm and abcxxxxx.pfb for a Type 1 font, use the string "abcxxxxx.pfm \| abcxxxxx.pfb."</span></span>

<span data-ttu-id="1de21-112">O [**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) é diferente de [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) , pois o aplicativo que chama **AddFontResourceEx** pode especificar a fonte como particular para si mesmo ou não enumerável.</span><span class="sxs-lookup"><span data-stu-id="1de21-112">[**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) differs from [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) in that the application calling **AddFontResourceEx** can specify the font as private to itself or non-enumerable.</span></span>

<span data-ttu-id="1de21-113">Para adicionar uma fonte de uma imagem de memória, use [**AddFontMemResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontmemresourceex).</span><span class="sxs-lookup"><span data-stu-id="1de21-113">To add a font from a memory image, use [**AddFontMemResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontmemresourceex).</span></span> <span data-ttu-id="1de21-114">Isso permite que um aplicativo use uma fonte inserida em um documento ou em uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="1de21-114">This allows an application to use a font that is embedded in a document or a webpage.</span></span>

<span data-ttu-id="1de21-115">Para remover uma fonte que veio de vários arquivos de recursos, chame [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) ou [**RemoveFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourceexa), dependendo da função usada para adicionar a fonte.</span><span class="sxs-lookup"><span data-stu-id="1de21-115">To remove a font that came from multiple resource files, call [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) or [**RemoveFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourceexa), depending on the function used to add the font.</span></span> <span data-ttu-id="1de21-116">Você deve especificar os mesmos sinalizadores que foram usados para adicionar a fonte.</span><span class="sxs-lookup"><span data-stu-id="1de21-116">You must specify the same flags that were used to add the font.</span></span> <span data-ttu-id="1de21-117">Para remover uma fonte que foi adicionada de uma imagem de memória, use [**RemoveFontMemResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontmemresourceex).</span><span class="sxs-lookup"><span data-stu-id="1de21-117">To remove a font that was added from a memory image, use [**RemoveFontMemResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontmemresourceex).</span></span>

<span data-ttu-id="1de21-118">O uso de uma fonte proveniente de vários arquivos de recurso de fonte é idêntico ao uso de uma fonte de um único arquivo de recurso.</span><span class="sxs-lookup"><span data-stu-id="1de21-118">Using a font that comes from multiple font-resource files is identical to using a font from a single resource file.</span></span>

 

 
