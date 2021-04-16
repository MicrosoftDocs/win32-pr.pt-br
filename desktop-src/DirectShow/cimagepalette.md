---
description: A classe CImagePalette gerencia paletas para renderizadores de vídeo. Ele pode ser usado para criar uma paleta lógica a partir de um formato de vídeo. Essa classe destina-se a ser usada com as classes CBaseWindow e CDrawImage, portanto, é um pouco especializada.
ms.assetid: dcbe5049-0e8c-4221-825a-0fd8e6efd2a5
title: Classe CImagePalette
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette
api_type:
- COM
api_location: ''
ms.openlocfilehash: 696c51e4918815e18accbadd66c764493dc0b98e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105757705"
---
# <a name="cimagepalette-class"></a><span data-ttu-id="bded3-105">Classe CImagePalette</span><span class="sxs-lookup"><span data-stu-id="bded3-105">CImagePalette class</span></span>

<span data-ttu-id="bded3-106">A `CImagePalette` classe gerencia paletas para renderizadores de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bded3-106">The `CImagePalette` class manages palettes for video renderers.</span></span> <span data-ttu-id="bded3-107">Ele pode ser usado para criar uma paleta lógica a partir de um formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bded3-107">It can be used to create a logical palette from a video format.</span></span> <span data-ttu-id="bded3-108">Essa classe destina-se a ser usada com as classes [**CBaseWindow**](cbasewindow.md) e [**CDrawImage**](cdrawimage.md) , portanto, é um pouco especializada.</span><span class="sxs-lookup"><span data-stu-id="bded3-108">This class is intended to be used with the [**CBaseWindow**](cbasewindow.md) and [**CDrawImage**](cdrawimage.md) classes, so it is somewhat specialized.</span></span>



| <span data-ttu-id="bded3-109">Variáveis de membro protegido</span><span class="sxs-lookup"><span data-stu-id="bded3-109">Protected Member Variables</span></span>                                       | <span data-ttu-id="bded3-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="bded3-110">Description</span></span>                                                                                    |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bded3-111">**\_hPalette m**</span><span class="sxs-lookup"><span data-stu-id="bded3-111">**m\_hPalette**</span></span>](cimagepalette-m-hpalette.md)                  | <span data-ttu-id="bded3-112">Identificador para a paleta lógica que este objeto gerencia.</span><span class="sxs-lookup"><span data-stu-id="bded3-112">Handle to the logical palette that this object manages.</span></span>                                        |
| [<span data-ttu-id="bded3-113">**\_pBaseWindow m**</span><span class="sxs-lookup"><span data-stu-id="bded3-113">**m\_pBaseWindow**</span></span>](cimagepalette-m-pbasewindow.md)            | <span data-ttu-id="bded3-114">Ponteiro para o objeto **CBaseWindow** que gerencia a janela.</span><span class="sxs-lookup"><span data-stu-id="bded3-114">Pointer to the **CBaseWindow** object that manages the window.</span></span>                                 |
| [<span data-ttu-id="bded3-115">**\_pDrawImage m**</span><span class="sxs-lookup"><span data-stu-id="bded3-115">**m\_pDrawImage**</span></span>](cimagepalette-m-pdrawimage.md)              | <span data-ttu-id="bded3-116">Ponteiro para o objeto **CDrawImage** que desenha a imagem de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bded3-116">Pointer to the **CDrawImage** object that draws the video image.</span></span>                               |
| [<span data-ttu-id="bded3-117">**\_pFilter m**</span><span class="sxs-lookup"><span data-stu-id="bded3-117">**m\_pFilter**</span></span>](cimagepalette-m-pfilter.md)                    | <span data-ttu-id="bded3-118">Ponteiro para o filtro proprietário.</span><span class="sxs-lookup"><span data-stu-id="bded3-118">Pointer to the owning filter.</span></span>                                                                  |
| <span data-ttu-id="bded3-119">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="bded3-119">Public Methods</span></span>                                                   | <span data-ttu-id="bded3-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="bded3-120">Description</span></span>                                                                                    |
| [<span data-ttu-id="bded3-121">**CImagePalette**</span><span class="sxs-lookup"><span data-stu-id="bded3-121">**CImagePalette**</span></span>](cimagepalette-cimagepalette.md)             | <span data-ttu-id="bded3-122">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="bded3-122">Constructor method.</span></span>                                                                            |
| [<span data-ttu-id="bded3-123">**CopyPalette**</span><span class="sxs-lookup"><span data-stu-id="bded3-123">**CopyPalette**</span></span>](cimagepalette-copypalette.md)                 | <span data-ttu-id="bded3-124">Copia a paleta de qualquer estrutura **VIDEOINFO** para qualquer estrutura **VIDEOINFO** palettized.</span><span class="sxs-lookup"><span data-stu-id="bded3-124">Copies the palette from any **VIDEOINFO** structure to any palettized **VIDEOINFO** structure.</span></span> |
| [<span data-ttu-id="bded3-125">**MakeIdentityPalette**</span><span class="sxs-lookup"><span data-stu-id="bded3-125">**MakeIdentityPalette**</span></span>](cimagepalette-makeidentitypalette.md) | <span data-ttu-id="bded3-126">Tenta criar uma paleta que mapeia diretamente para a paleta selecionada no dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bded3-126">Attempts to make a palette that maps directly to the palette selected in the display device.</span></span>   |
| [<span data-ttu-id="bded3-127">**MakePalette**</span><span class="sxs-lookup"><span data-stu-id="bded3-127">**MakePalette**</span></span>](cimagepalette-makepalette.md)                 | <span data-ttu-id="bded3-128">Cria uma paleta lógica da tabela de cores em um formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bded3-128">Creates a logical palette from the color table in a video format.</span></span>                              |
| [<span data-ttu-id="bded3-129">**PreparePalette**</span><span class="sxs-lookup"><span data-stu-id="bded3-129">**PreparePalette**</span></span>](cimagepalette-preparepalette.md)           | <span data-ttu-id="bded3-130">Configura uma paleta, com base em um tipo de mídia do filtro proprietário.</span><span class="sxs-lookup"><span data-stu-id="bded3-130">Sets up a palette, based on a media type from the owning filter.</span></span>                               |
| [<span data-ttu-id="bded3-131">**RemovePalette**</span><span class="sxs-lookup"><span data-stu-id="bded3-131">**RemovePalette**</span></span>](cimagepalette-removepalette.md)             | <span data-ttu-id="bded3-132">Exclui a paleta lógica existente.</span><span class="sxs-lookup"><span data-stu-id="bded3-132">Deletes the existing logical palette.</span></span>                                                          |



 

 

 



