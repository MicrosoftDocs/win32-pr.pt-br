---
title: Controles sem janelas
description: Controles sem janelas
ms.assetid: 1759e5db-423c-44cc-b901-f50046c91956
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 762c839067f32a5ac182ccd6b48bfb81c1c68f13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364468"
---
# <a name="windowless-controls"></a><span data-ttu-id="3013f-103">Controles sem janelas</span><span class="sxs-lookup"><span data-stu-id="3013f-103">Windowless Controls</span></span>

<span data-ttu-id="3013f-104">A especificação de controles ActiveX 96 inclui uma definição para controles sem janela.</span><span class="sxs-lookup"><span data-stu-id="3013f-104">The ActiveX Controls 96 specification includes a definition for windowless controls.</span></span> <span data-ttu-id="3013f-105">Esses controles não operam em sua própria janela e exigem um contêiner para oferecer uma janela compartilhada na qual o controle pode desenhar, consulte o SDK do ActiveX.</span><span class="sxs-lookup"><span data-stu-id="3013f-105">Such controls do not operate in their own window and require a container to offer a shared window into which the control may draw, see the ActiveX SDK.</span></span> <span data-ttu-id="3013f-106">Os controles sem janela são projetados para serem compatíveis com contêineres de controle mais antigos criando sua própria janela nessa situação, os contêineres de controle sem janela devem hospedar controles de janela da maneira tradicional sem problemas.</span><span class="sxs-lookup"><span data-stu-id="3013f-106">Windowless controls are designed to be compatible with older control containers by creating their own window in that situation, windowless control containers should host windowed controls in the traditional way with no problem.</span></span> <span data-ttu-id="3013f-107">No entanto, pode ser útil para um contêiner distinguir os controles que podem operar em modo sem janela, portanto, uma categoria de componente apropriada é definida.</span><span class="sxs-lookup"><span data-stu-id="3013f-107">It may however be useful for a container to distinguish those controls that can operate in a windowless mode, so an appropriate component category is defined.</span></span>

<span data-ttu-id="3013f-108">CATID-{1D06B600-3AE3-11cf-87B9-00AA006C8166} CATID \_ WindowlessObject</span><span class="sxs-lookup"><span data-stu-id="3013f-108">CATID - {1D06B600-3AE3-11cf-87B9-00AA006C8166} CATID\_WindowlessObject</span></span>

## <a name="related-topics"></a><span data-ttu-id="3013f-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3013f-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3013f-110">Categorias de componentes</span><span class="sxs-lookup"><span data-stu-id="3013f-110">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

 




