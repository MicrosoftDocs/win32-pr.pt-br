---
description: As funções de modificação de imagem permitem que você altere a imagem executável.
ms.assetid: 195959cb-e1ab-4c76-b7f9-f20522feac8c
title: Funções de modificação de imagem do ImageHlp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f6be83457738d1237865940463f438d3b73afa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646248"
---
# <a name="imagehlp-image-modification-functions"></a><span data-ttu-id="45d43-103">Funções de modificação de imagem do ImageHlp</span><span class="sxs-lookup"><span data-stu-id="45d43-103">ImageHlp Image Modification Functions</span></span>

<span data-ttu-id="45d43-104">As funções de modificação de imagem permitem que você altere a imagem executável.</span><span class="sxs-lookup"><span data-stu-id="45d43-104">The image modification functions allow you to change the executable image.</span></span> <span data-ttu-id="45d43-105">Eles são principalmente para uso pelas ferramentas de desenvolvimento e instalam programas.</span><span class="sxs-lookup"><span data-stu-id="45d43-105">They are mostly for use by development tools and install programs.</span></span> <span data-ttu-id="45d43-106">Eles podem ser usados para associar uma imagem, calcular sua soma de verificação (o que é importante para garantir a integridade da imagem), alterar seu endereço de carregamento e produzir arquivos de símbolo.</span><span class="sxs-lookup"><span data-stu-id="45d43-106">They can be used to bind an image, compute its checksum (which is important for ensuring image integrity), change its load address, and produce symbol files.</span></span>

<span data-ttu-id="45d43-107">A seguir estão as funções de modificação de imagem.</span><span class="sxs-lookup"><span data-stu-id="45d43-107">The following are the image modification functions.</span></span>

-   [<span data-ttu-id="45d43-108">**BindImage**</span><span class="sxs-lookup"><span data-stu-id="45d43-108">**BindImage**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-bindimage)
-   [<span data-ttu-id="45d43-109">**BindImageEx**</span><span class="sxs-lookup"><span data-stu-id="45d43-109">**BindImageEx**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-bindimageex)
-   [<span data-ttu-id="45d43-110">**CheckSumMappedFile**</span><span class="sxs-lookup"><span data-stu-id="45d43-110">**CheckSumMappedFile**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-checksummappedfile)
-   [<span data-ttu-id="45d43-111">**MapFileAndCheckSum**</span><span class="sxs-lookup"><span data-stu-id="45d43-111">**MapFileAndCheckSum**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-mapfileandchecksuma)
-   [<span data-ttu-id="45d43-112">**ReBaseImage**</span><span class="sxs-lookup"><span data-stu-id="45d43-112">**ReBaseImage**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-rebaseimage)
-   [<span data-ttu-id="45d43-113">**SplitSymbols**</span><span class="sxs-lookup"><span data-stu-id="45d43-113">**SplitSymbols**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-splitsymbols)
-   [<span data-ttu-id="45d43-114">**StatusRoutine**</span><span class="sxs-lookup"><span data-stu-id="45d43-114">**StatusRoutine**</span></span>](/windows/desktop/api/Imagehlp/nc-imagehlp-pimagehlp_status_routine)
-   [<span data-ttu-id="45d43-115">**TouchFileTimes**</span><span class="sxs-lookup"><span data-stu-id="45d43-115">**TouchFileTimes**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-touchfiletimes)
-   [<span data-ttu-id="45d43-116">**UpdateDebugInfoFile**</span><span class="sxs-lookup"><span data-stu-id="45d43-116">**UpdateDebugInfoFile**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-updatedebuginfofile)
-   [<span data-ttu-id="45d43-117">**UpdateDebugInfoFileEx**</span><span class="sxs-lookup"><span data-stu-id="45d43-117">**UpdateDebugInfoFileEx**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-updatedebuginfofileex)

 

 



