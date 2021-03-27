---
description: Esta seção descreve as funções de manipulação da paleta de cores do shell do Windows. Os elementos de programação explicados nesta documentação são exportados por Shlwapi.dll e definidos em Shlwapi. h e shlwapi. lib.
title: Funções de manipulação de paleta de cores do Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 93848cb3-60c6-4b2f-82d9-abfee97e372a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ba92dcf280b8d54b8778e276bb603d888f5991c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169904"
---
# <a name="shell-color-palette-handling-functions"></a><span data-ttu-id="238bf-104">Funções de manipulação de paleta de cores do Shell</span><span class="sxs-lookup"><span data-stu-id="238bf-104">Shell Color Palette Handling Functions</span></span>

<span data-ttu-id="238bf-105">Esta seção descreve as funções de manipulação da paleta de cores do shell do Windows.</span><span class="sxs-lookup"><span data-stu-id="238bf-105">This section describes the Windows Shell color palette handling functions.</span></span> <span data-ttu-id="238bf-106">Os elementos de programação explicados nesta documentação são exportados por Shlwapi.dll e definidos em Shlwapi. h e shlwapi. lib.</span><span class="sxs-lookup"><span data-stu-id="238bf-106">The programming elements explained in this documentation are exported by Shlwapi.dll and defined in Shlwapi.h and Shlwapi.lib.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="238bf-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="238bf-107">In this section</span></span>



| <span data-ttu-id="238bf-108">Tópico</span><span class="sxs-lookup"><span data-stu-id="238bf-108">Topic</span></span>                                                           | <span data-ttu-id="238bf-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="238bf-109">Description</span></span>                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="238bf-110">**ColorAdjustLuma**</span><span class="sxs-lookup"><span data-stu-id="238bf-110">**ColorAdjustLuma**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-coloradjustluma)<br/>           | <span data-ttu-id="238bf-111">Altera a luminância de um valor RGB.</span><span class="sxs-lookup"><span data-stu-id="238bf-111">Changes the luminance of a RGB value.</span></span> <span data-ttu-id="238bf-112">O matiz e a saturação não são afetados.</span><span class="sxs-lookup"><span data-stu-id="238bf-112">Hue and saturation are not affected.</span></span><br/> |
| [<span data-ttu-id="238bf-113">**ColorHLSToRGB**</span><span class="sxs-lookup"><span data-stu-id="238bf-113">**ColorHLSToRGB**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-colorhlstorgb)<br/>               | <span data-ttu-id="238bf-114">Converte as cores de matiz-luminância-saturação (HLS) para o formato RGB.</span><span class="sxs-lookup"><span data-stu-id="238bf-114">Converts colors from hue-luminance-saturation (HLS) to RGB format.</span></span><br/>         |
| [<span data-ttu-id="238bf-115">**ColorRGBToHLS**</span><span class="sxs-lookup"><span data-stu-id="238bf-115">**ColorRGBToHLS**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-colorrgbtohls)<br/>               | <span data-ttu-id="238bf-116">Converte cores de RGB em formato de matiz-luminescência-saturação (HLS).</span><span class="sxs-lookup"><span data-stu-id="238bf-116">Converts colors from RGB to hue-luminance-saturation (HLS) format.</span></span><br/>         |
| [<span data-ttu-id="238bf-117">**SHCreateShellPalette**</span><span class="sxs-lookup"><span data-stu-id="238bf-117">**SHCreateShellPalette**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreateshellpalette)<br/> | <span data-ttu-id="238bf-118">Cria uma paleta de meio-tom para o contexto do dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="238bf-118">Creates a halftone palette for the specified device context.</span></span><br/>               |



 

 

 




