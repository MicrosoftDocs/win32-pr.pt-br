---
title: Renderização de imagem
description: Renderização de imagem
ms.assetid: de87f288-f1bd-471c-b594-e9dbde3cff0a
keywords:
- DrawDib, renderização de imagem
- DrawDib, desenho de DIBs
- Função DrawDibDraw
- Função DrawDibGetBuffer
- Função DrawDibUpdate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e0d3f4d770a3acc290273b14ec14ff4b6efa30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006088"
---
# <a name="image-rendering"></a><span data-ttu-id="44ea8-108">Renderização de imagem</span><span class="sxs-lookup"><span data-stu-id="44ea8-108">Image Rendering</span></span>

<span data-ttu-id="44ea8-109">Depois de chamar o [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) para criar um controlador de domínio DrawDib (consulte [DrawDib Operations](drawdib-operations.md)), você pode desenhar uma DIB na tela usando a função [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) .</span><span class="sxs-lookup"><span data-stu-id="44ea8-109">After you call [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) to create a DrawDib DC (see [DrawDib Operations](drawdib-operations.md)), you can draw a DIB to the screen by using the [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) function.</span></span> <span data-ttu-id="44ea8-110">**DrawDibDraw** pontilha os bitmaps de cor verdadeira ao exibi-los com adaptadores de vídeo de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="44ea8-110">**DrawDibDraw** dithers true-color bitmaps when displaying them with 8-bit display adapters.</span></span>

<span data-ttu-id="44ea8-111">O [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) também dá suporte aos compactadores de vídeo de forma transparente ao exibir bitmaps compactados.</span><span class="sxs-lookup"><span data-stu-id="44ea8-111">[**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) also supports video compressors transparently when displaying compressed bitmaps.</span></span> <span data-ttu-id="44ea8-112">Você pode acessar o buffer que contém a imagem descompactada usando a função [**DrawDibGetBuffer**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetbuffer) .</span><span class="sxs-lookup"><span data-stu-id="44ea8-112">You can access the buffer that contains the decompressed image by using the [**DrawDibGetBuffer**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetbuffer) function.</span></span> <span data-ttu-id="44ea8-113">**DrawDibGetBuffer** retorna **NULL** ao desenhar um bitmap descompactado.</span><span class="sxs-lookup"><span data-stu-id="44ea8-113">**DrawDibGetBuffer** returns **NULL** when drawing an uncompressed bitmap.</span></span> <span data-ttu-id="44ea8-114">Você deve preparar seu aplicativo para manipular bitmaps compactados e descompactados.</span><span class="sxs-lookup"><span data-stu-id="44ea8-114">You should prepare your application to handle compressed and uncompressed bitmaps.</span></span>

<span data-ttu-id="44ea8-115">Você pode atualizar uma imagem ou uma parte de uma imagem exibida pelo seu aplicativo usando a macro [**DrawDibUpdate**](/windows/desktop/api/Vfw/nf-vfw-drawdibupdate) .</span><span class="sxs-lookup"><span data-stu-id="44ea8-115">You can refresh an image or a portion of an image displayed by your application by using the [**DrawDibUpdate**](/windows/desktop/api/Vfw/nf-vfw-drawdibupdate) macro.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44ea8-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="44ea8-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44ea8-117">Sobre as funções DrawDib</span><span class="sxs-lookup"><span data-stu-id="44ea8-117">About the DrawDib Functions</span></span>](about-the-drawdib-functions.md)
</dt> </dl>

 

 




