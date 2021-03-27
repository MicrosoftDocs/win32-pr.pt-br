---
description: Metaarquivos Enhanced-Format
ms.assetid: 8d7015cb-5e1d-4805-a7a8-1f8b693e0681
title: Metaarquivos Enhanced-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbae113c65e4dd05e67c155c2323698cd023191
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967669"
---
# <a name="enhanced-format-metafiles"></a><span data-ttu-id="8ac8e-103">Metaarquivos Enhanced-Format</span><span class="sxs-lookup"><span data-stu-id="8ac8e-103">Enhanced-Format Metafiles</span></span>

<span data-ttu-id="8ac8e-104">O *metarquivo de formato avançado* consiste nos seguintes elementos:</span><span class="sxs-lookup"><span data-stu-id="8ac8e-104">The *enhanced-format metafile* consists of the following elements:</span></span>

-   <span data-ttu-id="8ac8e-105">Um cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8ac8e-105">A header</span></span>
-   <span data-ttu-id="8ac8e-106">Uma tabela de identificadores para objetos GDI</span><span class="sxs-lookup"><span data-stu-id="8ac8e-106">A table of handles to GDI objects</span></span>
-   <span data-ttu-id="8ac8e-107">Uma paleta privada</span><span class="sxs-lookup"><span data-stu-id="8ac8e-107">A private palette</span></span>
-   <span data-ttu-id="8ac8e-108">Uma matriz de registros de metarquivo</span><span class="sxs-lookup"><span data-stu-id="8ac8e-108">An array of metafile records</span></span>

<span data-ttu-id="8ac8e-109">Os metaarquivos aprimorados fornecem uma verdadeira independência de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8ac8e-109">Enhanced metafiles provide true device independence.</span></span> <span data-ttu-id="8ac8e-110">Você pode considerar a imagem armazenada em um metarquivo avançado como um "instantâneo" da exibição de vídeo feita em um momento específico.</span><span class="sxs-lookup"><span data-stu-id="8ac8e-110">You can think of the picture stored in an enhanced metafile as a "snapshot" of the video display taken at a particular moment.</span></span> <span data-ttu-id="8ac8e-111">Esse "instantâneo" mantém suas dimensões, independentemente de onde aparecem em uma impressora, em uma plotadora, na área de trabalho ou na área cliente de qualquer aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8ac8e-111">This "snapshot" maintains its dimensions no matter where it appears on a printer, a plotter, the desktop, or in the client area of any application.</span></span>

<span data-ttu-id="8ac8e-112">Você pode usar os metaarquivos aprimorados para armazenar uma imagem criada usando as funções GDI (incluindo novas funções de caminho e transformação).</span><span class="sxs-lookup"><span data-stu-id="8ac8e-112">You can use enhanced metafiles to store a picture created by using the GDI functions (including new path and transformation functions).</span></span> <span data-ttu-id="8ac8e-113">Como o formato de metarquivo avançado é padronizado, as imagens armazenadas nesse formato podem ser copiadas de um aplicativo para outro; e, como as imagens são verdadeiramente independentes de dispositivo, eles têm a garantia de manter sua forma e proporção em qualquer dispositivo de saída.</span><span class="sxs-lookup"><span data-stu-id="8ac8e-113">Because the enhanced metafile format is standardized, pictures that are stored in this format can be copied from one application to another; and, because the pictures are truly device independent, they are guaranteed to maintain their shape and proportion on any output device.</span></span>

-   [<span data-ttu-id="8ac8e-114">Registros de metarquivo avançados</span><span class="sxs-lookup"><span data-stu-id="8ac8e-114">Enhanced Metafile Records</span></span>](enhanced-metafile-records.md)
-   [<span data-ttu-id="8ac8e-115">Criação de metarquivo aprimorada</span><span class="sxs-lookup"><span data-stu-id="8ac8e-115">Enhanced Metafile Creation</span></span>](enhanced-metafile-creation.md)
-   [<span data-ttu-id="8ac8e-116">Operações de metarquivo aprimoradas</span><span class="sxs-lookup"><span data-stu-id="8ac8e-116">Enhanced Metafile Operations</span></span>](enhanced-metafile-operations.md)

 

 



