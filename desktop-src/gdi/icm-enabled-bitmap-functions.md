---
description: O Microsoft Image Color Management (ICM) garante que uma imagem colorida, um objeto gráfico ou um objeto de texto seja renderizado o mais próximo possível de sua intenção original em qualquer dispositivo, apesar das diferenças nas tecnologias de geração de imagens e funcionalidades de cores entre os dispositivos.
ms.assetid: 7b3cb9a4-ffd2-4867-85bd-0e663fdde6e3
title: ICM-Enabled funções de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b89dac569aafad1ef94b066bc97f588bac62c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827649"
---
# <a name="icm-enabled-bitmap-functions"></a><span data-ttu-id="8be26-103">ICM-Enabled funções de bitmap</span><span class="sxs-lookup"><span data-stu-id="8be26-103">ICM-Enabled Bitmap Functions</span></span>

<span data-ttu-id="8be26-104">O Microsoft Image Color Management (ICM) garante que uma imagem colorida, um objeto gráfico ou um objeto de texto seja renderizado o mais próximo possível de sua intenção original em qualquer dispositivo, apesar das diferenças nas tecnologias de geração de imagens e funcionalidades de cores entre os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="8be26-104">Microsoft Image Color Management (ICM) ensures that a color image, graphic object, or text object is rendered as closely as possible to its original intent on any device, despite differences in imaging technologies and color capabilities between devices.</span></span> <span data-ttu-id="8be26-105">Quer você esteja verificando uma imagem ou outro gráfico em um scanner de cor, baixando-o pela Internet, exibindo ou editando-o na tela ou imprimindo-o em papel, filme ou outra mídia, o ICM 2,0 ajuda a manter as cores consistentes e precisas.</span><span class="sxs-lookup"><span data-stu-id="8be26-105">Whether you are scanning an image or other graphic on a color scanner, downloading it over the Internet, viewing or editing it onscreen, or printing it on paper, film, or other media, ICM 2.0 helps you keep colors consistent and accurate.</span></span> <span data-ttu-id="8be26-106">Para obter mais informações sobre o ICM, consulte [sistema de cores do Windows](/previous-versions//dd372446(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8be26-106">For more information about ICM, see [Windows Color System](/previous-versions//dd372446(v=vs.85)).</span></span>

<span data-ttu-id="8be26-107">Há várias funções na interface gráfica de dispositivo (GDI) que usam ou operam em dados de cores.</span><span class="sxs-lookup"><span data-stu-id="8be26-107">There are various functions in the graphics device interface (GDI) that use or operate on color data.</span></span> <span data-ttu-id="8be26-108">As seguintes funções de bitmap estão habilitadas para uso com o ICM:</span><span class="sxs-lookup"><span data-stu-id="8be26-108">The following bitmap functions are enabled for use with ICM:</span></span>

-   [<span data-ttu-id="8be26-109">**BitBlt**</span><span class="sxs-lookup"><span data-stu-id="8be26-109">**BitBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-bitblt)
-   [<span data-ttu-id="8be26-110">**CreateDIBitmap**</span><span class="sxs-lookup"><span data-stu-id="8be26-110">**CreateDIBitmap**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)
-   [<span data-ttu-id="8be26-111">**CreateDIBSection**</span><span class="sxs-lookup"><span data-stu-id="8be26-111">**CreateDIBSection**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibsection)
-   [<span data-ttu-id="8be26-112">**MaskBlt**</span><span class="sxs-lookup"><span data-stu-id="8be26-112">**MaskBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-maskblt)
-   [<span data-ttu-id="8be26-113">**SetDIBColorTable**</span><span class="sxs-lookup"><span data-stu-id="8be26-113">**SetDIBColorTable**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdibcolortable)
-   [<span data-ttu-id="8be26-114">**StretchBlt**</span><span class="sxs-lookup"><span data-stu-id="8be26-114">**StretchBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)
-   [<span data-ttu-id="8be26-115">**SetDIBits**</span><span class="sxs-lookup"><span data-stu-id="8be26-115">**SetDIBits**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdibits)
-   [<span data-ttu-id="8be26-116">**SetDIBitsToDevice**</span><span class="sxs-lookup"><span data-stu-id="8be26-116">**SetDIBitsToDevice**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice)
-   [<span data-ttu-id="8be26-117">**StretchDIBits**</span><span class="sxs-lookup"><span data-stu-id="8be26-117">**StretchDIBits**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)

 

 
