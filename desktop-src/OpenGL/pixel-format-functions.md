---
title: Funções de formato de pixel
description: As funções do Windows a seguir gerenciam formatos de pixel.
ms.assetid: 78a6be75-72f6-4aef-a6bc-5f052c6fe2e9
keywords:
- Funções WGL, formato de pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e219fc6a2aafecdcda43708cdb4c77553c88f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823002"
---
# <a name="pixel-format-functions"></a><span data-ttu-id="76990-104">Funções de formato de pixel</span><span class="sxs-lookup"><span data-stu-id="76990-104">Pixel Format Functions</span></span>

<span data-ttu-id="76990-105">As funções do Windows a seguir gerenciam formatos de pixel.</span><span class="sxs-lookup"><span data-stu-id="76990-105">The following Windows functions manage pixel formats.</span></span>



| <span data-ttu-id="76990-106">Função do Windows</span><span class="sxs-lookup"><span data-stu-id="76990-106">Windows Function</span></span>                                               | <span data-ttu-id="76990-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="76990-107">Description</span></span>                                                                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76990-108">**ChoosePixelFormat**</span><span class="sxs-lookup"><span data-stu-id="76990-108">**ChoosePixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                 | <span data-ttu-id="76990-109">Obtém o formato de pixel do contexto do dispositivo que é a correspondência mais próxima a um formato de pixel especificado.</span><span class="sxs-lookup"><span data-stu-id="76990-109">Obtains the device context's pixel format that is the closest match to a specified pixel format.</span></span>                                                                      |
| [<span data-ttu-id="76990-110">**SetPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="76990-110">**SetPixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                       | <span data-ttu-id="76990-111">Define o formato de pixel atual de um contexto de dispositivo para o formato de pixel especificado por um índice de formato de pixel.</span><span class="sxs-lookup"><span data-stu-id="76990-111">Sets a device context's current pixel format to the pixel format specified by a pixel format index.</span></span>                                                                   |
| [<span data-ttu-id="76990-112">**GetPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="76990-112">**GetPixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                       | <span data-ttu-id="76990-113">Obtém o índice de formato de pixel do formato de pixel atual de um contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="76990-113">Obtains the pixel format index of a device context's current pixel format.</span></span>                                                                                            |
| [<span data-ttu-id="76990-114">**DescribePixelFormat**</span><span class="sxs-lookup"><span data-stu-id="76990-114">**DescribePixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)             | <span data-ttu-id="76990-115">Dado um contexto de dispositivo e um índice de formato de pixel, preenche uma estrutura de dados [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) com as propriedades do formato de pixel.</span><span class="sxs-lookup"><span data-stu-id="76990-115">Given a device context and a pixel format index, fills in a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure with the pixel format's properties.</span></span> |
| [<span data-ttu-id="76990-116">**GetEnhMetaFilePixelFormat**</span><span class="sxs-lookup"><span data-stu-id="76990-116">**GetEnhMetaFilePixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilepixelformat) | <span data-ttu-id="76990-117">Recupera informações de formato de pixel para um metarquivo avançado.</span><span class="sxs-lookup"><span data-stu-id="76990-117">Retrieves pixel format information for an enhanced metafile.</span></span>                                                                                                          |



 

<span data-ttu-id="76990-118">A função [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) retorna um índice de formato de pixel baseado em um que identifica a melhor correspondência dos formatos de pixel com suporte do contexto do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="76990-118">The [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) function returns a one-based pixel format index that identifies the best match from the device context's supported pixel formats.</span></span>

<span data-ttu-id="76990-119">A função [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) identifica o formato desejado usando um índice de formato de pixel baseado em um.</span><span class="sxs-lookup"><span data-stu-id="76990-119">The [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) function identifies the desired format using a one-based pixel format index.</span></span> <span data-ttu-id="76990-120">Normalmente, você chama **ChoosePixelFormat** para encontrar um formato de pixel de melhor correspondência e, em seguida, chamar **SetPixelFormat** com o resultado de **ChoosePixelFormat**.</span><span class="sxs-lookup"><span data-stu-id="76990-120">Typically, you call **ChoosePixelFormat** to find a best-match pixel format, and then call **SetPixelFormat** with the result of **ChoosePixelFormat**.</span></span>

<span data-ttu-id="76990-121">Se você chamar **SetPixelFormat** para um contexto de dispositivo que faz referência a uma janela, **SetPixelFormat** também alterará o formato de pixel da janela.</span><span class="sxs-lookup"><span data-stu-id="76990-121">If you call **SetPixelFormat** for a device context that references a window, **SetPixelFormat** also changes the pixel format of the window.</span></span> <span data-ttu-id="76990-122">Definir o formato de pixel de uma janela mais de uma vez pode levar a complicações significativas para o Gerenciador de janelas e para aplicativos multithread, portanto, não é permitido.</span><span class="sxs-lookup"><span data-stu-id="76990-122">Setting the pixel format of a window more than once can lead to significant complications for the Window Manager and for multithread applications, so it is not allowed.</span></span> <span data-ttu-id="76990-123">Você pode definir o formato de pixel de uma janela somente uma vez; Depois disso, o formato de pixel da janela não pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="76990-123">You can set the pixel format of a window only one time; after that, the window's pixel format cannot be changed.</span></span>

<span data-ttu-id="76990-124">A função [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) retorna um índice de formato de pixel baseado em um.</span><span class="sxs-lookup"><span data-stu-id="76990-124">The [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) function returns a one-based pixel format index.</span></span>

<span data-ttu-id="76990-125">A função [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) usa o seguinte como parâmetros:</span><span class="sxs-lookup"><span data-stu-id="76990-125">The [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) function takes the following as parameters:</span></span>

-   <span data-ttu-id="76990-126">Um identificador para um contexto de dispositivo</span><span class="sxs-lookup"><span data-stu-id="76990-126">A handle to a device context</span></span>
-   <span data-ttu-id="76990-127">Um índice de formato de pixel</span><span class="sxs-lookup"><span data-stu-id="76990-127">A pixel format index</span></span>
-   <span data-ttu-id="76990-128">Um ponteiro para uma estrutura de dados [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)</span><span class="sxs-lookup"><span data-stu-id="76990-128">A pointer to a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure</span></span>

<span data-ttu-id="76990-129">A função [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) retorna com os membros de **PIXELFORMATDESCRIPTOR** definidos adequadamente.</span><span class="sxs-lookup"><span data-stu-id="76990-129">The [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) function returns with the members of **PIXELFORMATDESCRIPTOR** appropriately set.</span></span>

<span data-ttu-id="76990-130">A função **GetEnhMetaFilePixelFormat** retorna o tamanho do formato de pixel de um metarquivo e recupera as informações de formato de pixel do metarquivo.</span><span class="sxs-lookup"><span data-stu-id="76990-130">The **GetEnhMetaFilePixelFormat** function returns the size of a metafile's pixel format and retrieves the pixel format information of the metafile.</span></span>

 

 




