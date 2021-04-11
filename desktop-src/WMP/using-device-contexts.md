---
title: Usando contextos de dispositivo
description: Usando contextos de dispositivo
ms.assetid: 2e8de313-6218-4401-a578-73140e7fdae1
keywords:
- visualizações, contexto do dispositivo
- visualizações personalizadas, contexto do dispositivo
- visualizações, função render
- visualizações personalizadas, função render
- Função render, contexto do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c315d5004565644750f4adcd099fc165e81575
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292323"
---
# <a name="using-device-contexts"></a><span data-ttu-id="02d7a-108">Usando contextos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="02d7a-108">Using Device Contexts</span></span>

<span data-ttu-id="02d7a-109">O contexto do dispositivo é um identificador padrão para um contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="02d7a-109">The device context is a standard handle to a device context.</span></span> <span data-ttu-id="02d7a-110">Você precisa disso para muitas funções de desenho para que o Microsoft Windows saiba em qual janela desenhar.</span><span class="sxs-lookup"><span data-stu-id="02d7a-110">You need this for many drawing functions so that Microsoft Windows knows which window to draw in.</span></span> <span data-ttu-id="02d7a-111">Por exemplo, para desenhar um retângulo, você precisa especificar o contexto do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="02d7a-111">For example, to draw a rectangle, you need to specify the device context.</span></span>


```C++
HDC hdc;
::Rectangle( hdc, 1, 1, 100, 100 );

```



<span data-ttu-id="02d7a-112">O contexto do dispositivo é especificado pelo Windows Media Player por meio da função **render** .</span><span class="sxs-lookup"><span data-stu-id="02d7a-112">The device context is specified by Windows Media Player through the **Render** function.</span></span> <span data-ttu-id="02d7a-113">Se o seu plug-in renderizar usando uma janela, você precisará usar o contexto do dispositivo dessa janela.</span><span class="sxs-lookup"><span data-stu-id="02d7a-113">If your plug-in renders using a window, you'll need to use the device context of that window.</span></span> <span data-ttu-id="02d7a-114">Use este contexto de dispositivo para qualquer ferramenta de desenho que exija um contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="02d7a-114">Use this device context for any drawing tool that requires a device context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02d7a-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="02d7a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02d7a-116">**Implementando renderização**</span><span class="sxs-lookup"><span data-stu-id="02d7a-116">**Implementing Render**</span></span>](implementing-render.md)
</dt> </dl>

 

 




