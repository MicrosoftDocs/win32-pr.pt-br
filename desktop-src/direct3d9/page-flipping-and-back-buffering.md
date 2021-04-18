---
description: A inversão de página é a chave em multimídia, animação e software de jogos; é análogo à maneira como você pode fazer uma animação com um painel de papel.
ms.assetid: b6824962-c7cb-4e7f-8731-2971b0d9a2b0
title: Inversão de página e buffer de fundo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bffad581c5d4250c7f36980ba1f278a9f770912
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105764207"
---
# <a name="page-flipping-and-back-buffering-direct3d-9"></a><span data-ttu-id="05aff-103">Inversão de página e buffer de fundo (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="05aff-103">Page Flipping and Back Buffering (Direct3D 9)</span></span>

<span data-ttu-id="05aff-104">A inversão de página é a chave em multimídia, animação e software de jogos; é análogo à maneira como você pode fazer uma animação com um painel de papel.</span><span class="sxs-lookup"><span data-stu-id="05aff-104">Page flipping is key in multimedia, animation, and game software; it is analogous to the way you can do animation with a pad of paper.</span></span> <span data-ttu-id="05aff-105">Em cada página, o artista altera a figura ligeiramente, de modo que, quando você virar rapidamente entre as planilhas, o desenho aparecerá animado.</span><span class="sxs-lookup"><span data-stu-id="05aff-105">On each page, the artist changes the figure slightly, so that when you flip rapidly between sheets, the drawing appears animated.</span></span>

<span data-ttu-id="05aff-106">A inversão de página no software é semelhante a esse processo.</span><span class="sxs-lookup"><span data-stu-id="05aff-106">Page flipping in software is similar to this process.</span></span> <span data-ttu-id="05aff-107">O Direct3D implementa a funcionalidade de inversão de página por meio de uma cadeia de permuta, que é uma propriedade do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="05aff-107">Direct3D implements page flipping functionality through a swap chain, which is a property of the device.</span></span> <span data-ttu-id="05aff-108">Inicialmente, você configura uma série de buffers do Direct3D que se alternam para a tela da forma como o papel do artista é invertido para a próxima página.</span><span class="sxs-lookup"><span data-stu-id="05aff-108">Initially, you set up a series of Direct3D buffers that flip to the screen in the way that the artist's paper flips to the next page.</span></span> <span data-ttu-id="05aff-109">O primeiro buffer é referido como o buffer frontal de cor.</span><span class="sxs-lookup"><span data-stu-id="05aff-109">The first buffer is referred to as the color front buffer.</span></span> <span data-ttu-id="05aff-110">Os buffers por trás dele são chamados buffers de fundo.</span><span class="sxs-lookup"><span data-stu-id="05aff-110">The buffers behind it are called back buffers.</span></span> <span data-ttu-id="05aff-111">Seu aplicativo grava em um buffer de fundo e, em seguida, inverte o buffer frontal de cor para que o buffer de fundo apareça na tela.</span><span class="sxs-lookup"><span data-stu-id="05aff-111">Your application writes to a back buffer and then flips the color front buffer so that the back buffer appears on screen.</span></span> <span data-ttu-id="05aff-112">Enquanto o sistema exibe a imagem, seu software está gravando novamente em um buffer de fundo.</span><span class="sxs-lookup"><span data-stu-id="05aff-112">While the system displays the image, your software is again writing to a back buffer.</span></span> <span data-ttu-id="05aff-113">O processo continuará desde que você esteja animando, permitindo que você anime imagens com eficiência.</span><span class="sxs-lookup"><span data-stu-id="05aff-113">The process continues as long as you are animating, enabling you to animate images efficiently.</span></span>

<span data-ttu-id="05aff-114">O Direct3D facilita a configuração de esquemas de inversão de página – a partir de um esquema simples de buffer duplo (um buffer frontal de cor com um buffer de fundo) para esquemas mais sofisticados com buffers de fundo adicionais.</span><span class="sxs-lookup"><span data-stu-id="05aff-114">Direct3D makes it easy to set up page flipping schemes - from a simple double-buffered scheme (a color front buffer with one back buffer) to more sophisticated schemes with additional back buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05aff-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="05aff-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05aff-116">Superfícies de Direct3D</span><span class="sxs-lookup"><span data-stu-id="05aff-116">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> <dt>

[<span data-ttu-id="05aff-117">O que é uma cadeia de permuta? (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="05aff-117">What Is a Swap Chain? (Direct3D 9)</span></span>](what-is-a-swap-chain-.md)
</dt> </dl>

 

 



