---
description: O evento UpdateOverlay é enviado quando a superfície de sobreposição foi movida ou redimensionada ou sua chave de cor foi alterada.
ms.assetid: 692cbd26-b7b3-4fa3-9157-ca96a33e3a1e
title: UpdateOverlay (ddraw. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2152e1f58ba161dc8dc3e04c908aaf037f1eed2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757567"
---
# <a name="updateoverlay"></a><span data-ttu-id="ad6bb-103">UpdateOverlay</span><span class="sxs-lookup"><span data-stu-id="ad6bb-103">UpdateOverlay</span></span>

> [!Note]  
> <span data-ttu-id="ad6bb-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ad6bb-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="ad6bb-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="ad6bb-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="ad6bb-106">O evento **UpdateOverlay** é enviado quando a superfície de sobreposição foi movida ou redimensionada ou sua chave de cor foi alterada.</span><span class="sxs-lookup"><span data-stu-id="ad6bb-106">The **UpdateOverlay** event is sent when the overlay surface has been moved or resized or its color key has changed.</span></span>

``` syntax
UpdateOverlay()
```

## <a name="remarks"></a><span data-ttu-id="ad6bb-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad6bb-107">Remarks</span></span>

<span data-ttu-id="ad6bb-108">Os aplicativos nunca devem se preocupar com a superfície de sobreposição sendo redimensionada ou movida.</span><span class="sxs-lookup"><span data-stu-id="ad6bb-108">Applications should never be concerned about the overlay surface being resized or moved.</span></span> <span data-ttu-id="ad6bb-109">Tudo isso é tratado internamente.</span><span class="sxs-lookup"><span data-stu-id="ad6bb-109">This is all handled internally.</span></span> <span data-ttu-id="ad6bb-110">Mas esse evento também é enviado quando a chave de cor é alterada.</span><span class="sxs-lookup"><span data-stu-id="ad6bb-110">But this event is also sent when the color key changes.</span></span> <span data-ttu-id="ad6bb-111">Isso significa que, se um aplicativo estiver hospedando MSWebDVD como um controle sem janela e exibir botões flutuantes sobre a superfície de vídeo no modo de tela inteira, ele deverá responder a esse evento obtendo o novo valor da propriedade **COLORKEY** para que ele possa desenhar os botões corretamente.</span><span class="sxs-lookup"><span data-stu-id="ad6bb-111">That means that if an application is hosting MSWebDVD as a windowless control and displaying floating buttons on top of the video surface in full-screen mode, it should respond to this event by getting the new value of the **ColorKey** property so that it can draw the buttons properly.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad6bb-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad6bb-112">Requirements</span></span>



| <span data-ttu-id="ad6bb-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad6bb-113">Requirement</span></span> | <span data-ttu-id="ad6bb-114">Valor</span><span class="sxs-lookup"><span data-stu-id="ad6bb-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ad6bb-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ad6bb-115">Header</span></span><br/> | <dl> <span data-ttu-id="ad6bb-116"><dt>Ddraw. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad6bb-116"><dt>Ddraw.h</dt></span></span> </dl> |



 

 




