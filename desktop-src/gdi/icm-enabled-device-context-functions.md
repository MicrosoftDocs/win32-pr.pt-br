---
description: O Microsoft Image Color Management (ICM) garante que uma imagem colorida, um elemento gráfico ou um objeto de texto seja renderizado o mais próximo possível de sua intenção original em qualquer dispositivo, apesar das diferenças nas tecnologias de geração de imagens e funcionalidades de cores entre os dispositivos.
ms.assetid: eced18cf-be5a-4c61-b0e5-36d607daa6ff
title: ICM-Enabled funções de contexto de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a0b49e62d0b4d05e0690d2aee0d3c5f0f530cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967658"
---
# <a name="icm-enabled-device-context-functions"></a><span data-ttu-id="61777-103">ICM-Enabled funções de contexto de dispositivo</span><span class="sxs-lookup"><span data-stu-id="61777-103">ICM-Enabled Device Context Functions</span></span>

<span data-ttu-id="61777-104">O Microsoft Image Color Management (ICM) garante que uma imagem colorida, um elemento gráfico ou um objeto de texto seja renderizado o mais próximo possível de sua intenção original em qualquer dispositivo, apesar das diferenças nas tecnologias de geração de imagens e funcionalidades de cores entre os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="61777-104">Microsoft Image Color Management (ICM) ensures that a color image, graphic, or text object is rendered as closely as possible to its original intent on any device, despite differences in imaging technologies and color capabilities between devices.</span></span> <span data-ttu-id="61777-105">(Para obter mais informações, consulte [sistema de cores do Windows](/previous-versions//dd372446(v=vs.85)).)</span><span class="sxs-lookup"><span data-stu-id="61777-105">(For more information, see [Windows Color System](/previous-versions//dd372446(v=vs.85)).)</span></span>

<span data-ttu-id="61777-106">Há várias funções na interface gráfica de dispositivo (GDI) que usam ou operam em dados de cores.</span><span class="sxs-lookup"><span data-stu-id="61777-106">There are various functions in the graphics device interface (GDI) that use or operate on color data.</span></span> <span data-ttu-id="61777-107">As seguintes funções de contexto de dispositivo estão habilitadas para uso com o ICM:</span><span class="sxs-lookup"><span data-stu-id="61777-107">The following device context functions are enabled for use with ICM:</span></span>

-   [<span data-ttu-id="61777-108">**CreateCompatibleDC**</span><span class="sxs-lookup"><span data-stu-id="61777-108">**CreateCompatibleDC**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)
-   [<span data-ttu-id="61777-109">**CreateDC**</span><span class="sxs-lookup"><span data-stu-id="61777-109">**CreateDC**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdca)
-   [<span data-ttu-id="61777-110">**GetDCBrushColor**</span><span class="sxs-lookup"><span data-stu-id="61777-110">**GetDCBrushColor**</span></span>](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)
-   [<span data-ttu-id="61777-111">**GetDCPenColor**</span><span class="sxs-lookup"><span data-stu-id="61777-111">**GetDCPenColor**</span></span>](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)
-   [<span data-ttu-id="61777-112">**ResetDC**</span><span class="sxs-lookup"><span data-stu-id="61777-112">**ResetDC**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)
-   [<span data-ttu-id="61777-113">**Selecionarobject**</span><span class="sxs-lookup"><span data-stu-id="61777-113">**SelectObject**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)
-   [<span data-ttu-id="61777-114">**SetDCBrushColor**</span><span class="sxs-lookup"><span data-stu-id="61777-114">**SetDCBrushColor**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)
-   [<span data-ttu-id="61777-115">**SetDCPenColor**</span><span class="sxs-lookup"><span data-stu-id="61777-115">**SetDCPenColor**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)

 

 
