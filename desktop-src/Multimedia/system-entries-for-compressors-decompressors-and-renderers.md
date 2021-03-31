---
title: Entradas do sistema para compactadores, descompactadores e renderizadores
description: Entradas do sistema para compactadores, descompactadores e renderizadores
ms.assetid: b27bbd5b-a218-49bb-b179-b24ce39869a1
keywords:
- Vídeo para Windows (VFW), compressor entradas do sistema
- VFW (vídeo para Windows), entradas do sistema de compressor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b46d9c6fd8974511698bcb687c580e68be3757ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636835"
---
# <a name="system-entries-for-compressors-decompressors-and-renderers"></a><span data-ttu-id="1770f-105">Entradas do sistema para compactadores, descompactadores e renderizadores</span><span class="sxs-lookup"><span data-stu-id="1770f-105">System Entries for Compressors, Decompressors, and Renderers</span></span>

<span data-ttu-id="1770f-106">O sistema usa entradas no registro para localizar drivers VCM.</span><span class="sxs-lookup"><span data-stu-id="1770f-106">The system uses entries in the registry to find VCM drivers.</span></span> <span data-ttu-id="1770f-107">Essas entradas estão na forma de códigos de 2 4 caracteres separados por um ponto.</span><span class="sxs-lookup"><span data-stu-id="1770f-107">These entries are in the form of two four-character codes separated by a period.</span></span> <span data-ttu-id="1770f-108">O primeiro código de quatro caracteres é definido pelo sistema e pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="1770f-108">The first four-character code is defined by the system and can be one of the following:</span></span>



| <span data-ttu-id="1770f-109">Código de quatro caracteres</span><span class="sxs-lookup"><span data-stu-id="1770f-109">Four-character code</span></span> | <span data-ttu-id="1770f-110">Description</span><span class="sxs-lookup"><span data-stu-id="1770f-110">Description</span></span>                               |
|---------------------|-------------------------------------------|
| <span data-ttu-id="1770f-111">VIDC</span><span class="sxs-lookup"><span data-stu-id="1770f-111">"VIDC"</span></span>              | <span data-ttu-id="1770f-112">Identifica os compactadores e os descompactadores.</span><span class="sxs-lookup"><span data-stu-id="1770f-112">Identifies compressors and decompressors.</span></span> |
| <span data-ttu-id="1770f-113">"VIDS"</span><span class="sxs-lookup"><span data-stu-id="1770f-113">"VIDS"</span></span>              | <span data-ttu-id="1770f-114">Identifica renderizadores de fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1770f-114">Identifies video-stream renderers.</span></span>        |
| <span data-ttu-id="1770f-115">"TXTS"</span><span class="sxs-lookup"><span data-stu-id="1770f-115">"TXTS"</span></span>              | <span data-ttu-id="1770f-116">Identifica renderizadores de fluxo de texto.</span><span class="sxs-lookup"><span data-stu-id="1770f-116">Identifies text-stream renderers.</span></span>         |
| <span data-ttu-id="1770f-117">"AUDS"</span><span class="sxs-lookup"><span data-stu-id="1770f-117">"AUDS"</span></span>              | <span data-ttu-id="1770f-118">Identifica os manipuladores de fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="1770f-118">Identifies audio-stream handlers.</span></span>         |



 

<span data-ttu-id="1770f-119">Renderizadores personalizados podem definir seus próprios códigos de quatro caracteres.</span><span class="sxs-lookup"><span data-stu-id="1770f-119">Custom renderers can define their own four-character codes.</span></span>

<span data-ttu-id="1770f-120">O segundo código de quatro caracteres é definido pelo driver.</span><span class="sxs-lookup"><span data-stu-id="1770f-120">The second four-character code is defined by the driver.</span></span> <span data-ttu-id="1770f-121">Normalmente, o segundo código de quatro caracteres corresponde ao tipo de dados que o driver pode manipular.</span><span class="sxs-lookup"><span data-stu-id="1770f-121">Typically, the second four-character code corresponds to the type of data the driver can handle.</span></span>

<span data-ttu-id="1770f-122">Ao abrir um driver VCM, um aplicativo especifica o tipo de driver e o tipo de manipulador de dados necessário.</span><span class="sxs-lookup"><span data-stu-id="1770f-122">When opening a VCM driver, an application specifies the type of driver and the type of data handler it needs.</span></span> <span data-ttu-id="1770f-123">Normalmente, essas informações vêm do cabeçalho de fluxo.</span><span class="sxs-lookup"><span data-stu-id="1770f-123">Typically, this information comes from the stream header.</span></span> <span data-ttu-id="1770f-124">O sistema tenta abrir o manipulador de dados especificado, mas se ele falhar, o sistema pesquisará o registro em busca de um driver que tenha o manipulador necessário.</span><span class="sxs-lookup"><span data-stu-id="1770f-124">The system tries to open the specified data handler, but if it fails, the system searches the registry for a driver that has the required handler.</span></span>

<span data-ttu-id="1770f-125">Ao procurar o driver, o sistema tenta corresponder os códigos de quatro caracteres especificados para o tipo de driver e o manipulador de dados com os especificados na entrada do driver.</span><span class="sxs-lookup"><span data-stu-id="1770f-125">When searching for the driver, the system tries to match the four-character codes specified for the driver type and data handler with those specified in the driver entry.</span></span> <span data-ttu-id="1770f-126">Por exemplo, se um aplicativo especificar o compressor MSSQ, o sistema pesquisará o registro para a entrada de driver VIDC. MSSQ.</span><span class="sxs-lookup"><span data-stu-id="1770f-126">For example, if an application specifies the compressor MSSQ, the system searches the registry for the driver entry VIDC.MSSQ.</span></span> <span data-ttu-id="1770f-127">Se não for possível encontrar uma correspondência, ele abrirá cada driver correspondente ao tipo de driver e localizará um que possa manipular o tipo de dados que seu aplicativo especifica.</span><span class="sxs-lookup"><span data-stu-id="1770f-127">If it cannot find a match, it opens each driver corresponding to the driver type and locates one that can handle the type of data your application specifies.</span></span> <span data-ttu-id="1770f-128">No exemplo anterior, se o sistema não pôde localizar VIDC. MSSQ, ele abriria todos os drivers com o código de quatro caracteres "VIDC" e localizará um que possa lidar com os dados.</span><span class="sxs-lookup"><span data-stu-id="1770f-128">In the previous example, if the system could not find VIDC.MSSQ, it would open all drivers with the "VIDC" four-character code and locate one that can handle the data.</span></span>

 

 




