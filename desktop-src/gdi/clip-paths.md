---
description: Como uma região de recorte, um caminho de clipe é outro objeto gráfico que um aplicativo pode selecionar em um contexto de dispositivo.
ms.assetid: 35c4052b-3f11-40bc-9cc9-6f999326a656
title: Caminhos de clipes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc4a93b0047110a6adb2f68d413e89cb1e97fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967705"
---
# <a name="clip-paths"></a><span data-ttu-id="5f349-103">Caminhos de clipes</span><span class="sxs-lookup"><span data-stu-id="5f349-103">Clip Paths</span></span>

<span data-ttu-id="5f349-104">Como uma região de recorte, um caminho de clipe é outro objeto gráfico que um aplicativo pode selecionar em um contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f349-104">Like a clipping region, a clip path is another graphics object that an application can select into a device context.</span></span> <span data-ttu-id="5f349-105">Ao contrário de uma região de recorte, um caminho de clipe é sempre criado por um aplicativo e é usado para recortar em uma ou mais formas irregulares.</span><span class="sxs-lookup"><span data-stu-id="5f349-105">Unlike a clipping region, a clip path is always created by an application and it is used for clipping to one or more irregular shapes.</span></span> <span data-ttu-id="5f349-106">Por exemplo, um aplicativo pode usar as linhas e curvas que formam os contornos de caracteres em uma cadeia de caracteres de texto para definir um caminho de clipe.</span><span class="sxs-lookup"><span data-stu-id="5f349-106">For example, an application can use the lines and curves that form the outlines of characters in a string of text to define a clip path.</span></span>

<span data-ttu-id="5f349-107">Para criar um caminho de clipe, primeiro é necessário criar um caminho que descreva a forma irregular necessária.</span><span class="sxs-lookup"><span data-stu-id="5f349-107">To create a clip path, it's first necessary to create a path that describes the required irregular shape.</span></span> <span data-ttu-id="5f349-108">Os caminhos são criados chamando as funções de desenho da interface de dispositivo gráfico (GDI) apropriada depois de chamar a função [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) e antes de chamar a função [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) .</span><span class="sxs-lookup"><span data-stu-id="5f349-108">Paths are created by calling the appropriate graphics device interface (GDI) drawing functions after calling the [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) function and before calling the [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) function.</span></span> <span data-ttu-id="5f349-109">Essa coleção de funções é chamada de colchete de caminho.</span><span class="sxs-lookup"><span data-stu-id="5f349-109">This collection of functions is called a path bracket.</span></span> <span data-ttu-id="5f349-110">Para obter mais informações sobre caminhos e colchetes de caminho, consulte [caminhos](paths.md).</span><span class="sxs-lookup"><span data-stu-id="5f349-110">For more information about paths and path brackets, see [Paths](paths.md).</span></span>

<span data-ttu-id="5f349-111">Depois que o caminho é criado, ele pode ser convertido em um caminho de clipe chamando a função [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) , identificando um contexto de dispositivo e especificando um modo de uso.</span><span class="sxs-lookup"><span data-stu-id="5f349-111">After the path is created, it can be converted to a clip path by calling the [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) function, identifying a device context, and specifying a usage mode.</span></span> <span data-ttu-id="5f349-112">O modo de uso determina como o sistema combina o novo caminho de clipe com a região de recorte original do contexto do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f349-112">The usage mode determines how the system combines the new clip path with the device context's original clipping region.</span></span> <span data-ttu-id="5f349-113">A tabela a seguir descreve os modos de uso.</span><span class="sxs-lookup"><span data-stu-id="5f349-113">The following table describes the usage modes.</span></span>



| <span data-ttu-id="5f349-114">Mode</span><span class="sxs-lookup"><span data-stu-id="5f349-114">Mode</span></span>      | <span data-ttu-id="5f349-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f349-115">Description</span></span>                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f349-116">RGN \_ e</span><span class="sxs-lookup"><span data-stu-id="5f349-116">RGN\_AND</span></span>  | <span data-ttu-id="5f349-117">O caminho do clipe inclui a interseção (áreas sobrepostas) da região de recorte do contexto do dispositivo e o caminho atual.</span><span class="sxs-lookup"><span data-stu-id="5f349-117">The clip path includes the intersection (overlapping areas) of the device context's clipping region and the current path.</span></span>    |
| <span data-ttu-id="5f349-118">\_cópia RGN</span><span class="sxs-lookup"><span data-stu-id="5f349-118">RGN\_COPY</span></span> | <span data-ttu-id="5f349-119">O caminho do clipe é o caminho atual.</span><span class="sxs-lookup"><span data-stu-id="5f349-119">The clip path is the current path.</span></span>                                                                                           |
| <span data-ttu-id="5f349-120">RGN \_ diff</span><span class="sxs-lookup"><span data-stu-id="5f349-120">RGN\_DIFF</span></span> | <span data-ttu-id="5f349-121">O caminho do clipe inclui a região de recorte do contexto do dispositivo com qualquer parte de interseção do caminho atual excluído.</span><span class="sxs-lookup"><span data-stu-id="5f349-121">The clip path includes the device context's clipping region with any intersecting parts of the current path excluded.</span></span>        |
| <span data-ttu-id="5f349-122">RGN \_ ou</span><span class="sxs-lookup"><span data-stu-id="5f349-122">RGN\_OR</span></span>   | <span data-ttu-id="5f349-123">O caminho do clipe inclui a União (áreas combinadas) da região de recorte do contexto do dispositivo e o caminho atual.</span><span class="sxs-lookup"><span data-stu-id="5f349-123">The clip path includes the union (combined areas) of the device context's clipping region and the current path.</span></span>              |
| <span data-ttu-id="5f349-124">\_XOR RGN</span><span class="sxs-lookup"><span data-stu-id="5f349-124">RGN\_XOR</span></span>  | <span data-ttu-id="5f349-125">O caminho do clipe inclui a União da região de recorte do contexto do dispositivo e o caminho atual, mas exclui a interseção.</span><span class="sxs-lookup"><span data-stu-id="5f349-125">The clip path includes the union of the device context's clipping region and the current path but excludes the intersection.</span></span> |



 

 

 



