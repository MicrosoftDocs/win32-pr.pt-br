---
title: Direct2D e alto DPI
description: Descreve como o Direct2D acomoda a exibição de alto DPI.
ms.assetid: 1809ab0e-853f-4dac-be97-563c92b9caee
keywords:
- Direct2D, alto DPI
- DPI alto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6548849416268f31b8b0c4a4261347c818ffa24c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917623"
---
# <a name="direct2d-and-high-dpi"></a><span data-ttu-id="0ae7c-105">Direct2D e alto DPI</span><span class="sxs-lookup"><span data-stu-id="0ae7c-105">Direct2D and High-DPI</span></span>

<span data-ttu-id="0ae7c-106">Escrever um aplicativo com reconhecimento de DPI é a chave para tornar uma interface do usuário uma aparência consistente em uma grande variedade de configurações de vídeo de alto DPI.</span><span class="sxs-lookup"><span data-stu-id="0ae7c-106">Writing a DPI-aware application is the key to making a user interface (UI) look consistently good across a wide variety of high-DPI display settings.</span></span> <span data-ttu-id="0ae7c-107">Um aplicativo que não reconhece DPI, mas que está sendo executado em uma configuração de exibição de alto DPI pode ser afetado por vários artefatos visuais, incluindo o dimensionamento incorreto de elementos da interface do usuário, texto recortado e imagens borradas.</span><span class="sxs-lookup"><span data-stu-id="0ae7c-107">An application that is not DPI-aware but is running on a high-DPI display setting can suffer from many visual artifacts, including incorrect scaling of UI elements, clipped text, and blurry images.</span></span> <span data-ttu-id="0ae7c-108">Ao adicionar suporte em seu aplicativo para reconhecimento de DPI, você torna a apresentação da interface do usuário mais previsível, tornando-a mais visualmente atraente e mais fácil de ler para os usuários.</span><span class="sxs-lookup"><span data-stu-id="0ae7c-108">By adding support in your application for DPI-awareness, you make the presentation of your application's UI more predictable, making it more visually appealing and easier to read for users.</span></span> <span data-ttu-id="0ae7c-109">Felizmente, o Direct2D facilita ainda mais a gravação de aplicativos que funcionam bem em alto DPI.</span><span class="sxs-lookup"><span data-stu-id="0ae7c-109">Fortunately, Direct2D makes it easier than ever to write applications that work well in high-DPI.</span></span> <span data-ttu-id="0ae7c-110">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="0ae7c-110">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="0ae7c-111">Suporte a alto DPI no Direct2D</span><span class="sxs-lookup"><span data-stu-id="0ae7c-111">High-DPI Support in Direct2D</span></span>](#high-dpi-support-in-direct2d)
-   [<span data-ttu-id="0ae7c-112">Windows 8 e DPI alto</span><span class="sxs-lookup"><span data-stu-id="0ae7c-112">Windows 8 and High-DPI</span></span>](#windows-8-and-high-dpi)
-   [<span data-ttu-id="0ae7c-113">O que é um DIP?</span><span class="sxs-lookup"><span data-stu-id="0ae7c-113">What is a DIP?</span></span>](#what-is-a-dip)
-   [<span data-ttu-id="0ae7c-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0ae7c-114">Related topics</span></span>](#related-topics)

## <a name="high-dpi-support-in-direct2d"></a><span data-ttu-id="0ae7c-115">Suporte a alto DPI no Direct2D</span><span class="sxs-lookup"><span data-stu-id="0ae7c-115">High-DPI Support in Direct2D</span></span>

<span data-ttu-id="0ae7c-116">O Direct2D fornece os seguintes recursos para trabalhar com cenários de alto DPI:</span><span class="sxs-lookup"><span data-stu-id="0ae7c-116">Direct2D provides the following features for working with high-DPI scenarios:</span></span>

-   <span data-ttu-id="0ae7c-117">Ele honra automaticamente o DPI do sistema ao criar um destino de renderização em janelas, desde que o manifesto do aplicativo indique que o aplicativo lida com o DPI corretamente.</span><span class="sxs-lookup"><span data-stu-id="0ae7c-117">It automatically honors the system DPI when creating a windowed render target, so long as the application manifest indicates that the application handles DPI correctly.</span></span> <span data-ttu-id="0ae7c-118">(Para obter informações sobre como declarar que seu aplicativo reconhece DPI, consulte [como garantir que seu aplicativo seja exibido corretamente em monitores de alto dpi](how-to--size-a-window-properly-for-high-dpi-displays.md).)</span><span class="sxs-lookup"><span data-stu-id="0ae7c-118">(For information on how to declare that your application is DPI-aware, see [How to Ensure That Your Application Displays Properly on High-DPI Displays](how-to--size-a-window-properly-for-high-dpi-displays.md).)</span></span>
-   <span data-ttu-id="0ae7c-119">Ele expressa coordenadas em DIPs (pixels independentes de dispositivo), o que permite que o aplicativo seja dimensionado automaticamente quando a configuração de DPI é alterada.</span><span class="sxs-lookup"><span data-stu-id="0ae7c-119">It expresses coordinates in DIPs (Device Independent Pixels), which enables the application to scale automatically when the DPI setting changes.</span></span>
-   <span data-ttu-id="0ae7c-120">Ele permite que os bitmaps tenham um DPI e dimensionam-os corretamente levando o DPI em conta.</span><span class="sxs-lookup"><span data-stu-id="0ae7c-120">It enables bitmaps to have a DPI and correctly scales them by taking the DPI into account.</span></span> <span data-ttu-id="0ae7c-121">Esse recurso também pode ser usado para manter ícones em resoluções diferentes.</span><span class="sxs-lookup"><span data-stu-id="0ae7c-121">This feature can also be used to maintain icons at different resolutions.</span></span>
-   <span data-ttu-id="0ae7c-122">Ele expressa a maioria dos recursos em DIPs, o que torna os recursos automaticamente independentes da resolução.</span><span class="sxs-lookup"><span data-stu-id="0ae7c-122">It expresses most resources in DIPs, which makes the resources automatically independent of resolution.</span></span>
-   <span data-ttu-id="0ae7c-123">Ele usa um espaço de coordenadas de ponto flutuante e uma suavização, de modo que qualquer conteúdo pode ser dimensionado para qualquer DPI arbitrária.</span><span class="sxs-lookup"><span data-stu-id="0ae7c-123">It uses a floating-point coordinate space and antialiasing, so any content can be scaled to any arbitrary DPI.</span></span>

<span data-ttu-id="0ae7c-124">O pipeline de gráficos Direct2D foi projetado para dimensionar de 96 DPI para 1200DPI.</span><span class="sxs-lookup"><span data-stu-id="0ae7c-124">The Direct2D graphics pipeline is designed to scale from 96 DPI to 1200DPI.</span></span>

## <a name="windows-8-and-high-dpi"></a><span data-ttu-id="0ae7c-125">Windows 8 e DPI alto</span><span class="sxs-lookup"><span data-stu-id="0ae7c-125">Windows 8 and High-DPI</span></span>

<span data-ttu-id="0ae7c-126">A partir do Windows 8, há recursos adicionais para o suporte a alto DPI.</span><span class="sxs-lookup"><span data-stu-id="0ae7c-126">Starting with Windows 8, there are additional features for high-DPI support.</span></span>

<span data-ttu-id="0ae7c-127">Se o DPI do contexto do dispositivo for alto o suficiente, o Direct2D alterará o limite usado para habilitar a anti-aliasing vertical do texto.</span><span class="sxs-lookup"><span data-stu-id="0ae7c-127">If the device context DPI is high enough, Direct2D changes the threshold it uses to enable vertical antialiasing of text.</span></span> <span data-ttu-id="0ae7c-128">Isso resulta em renderização de texto mais rápida em monitores de alto DPI.</span><span class="sxs-lookup"><span data-stu-id="0ae7c-128">This results in faster text rendering on high-DPI displays.</span></span> <span data-ttu-id="0ae7c-129">Além disso, você pode alternar o modo de unidade para pixels em vez de DIPs usando o método [**ID2D1DeviceContext:: Setunitmode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) .</span><span class="sxs-lookup"><span data-stu-id="0ae7c-129">Additionally, you can switch the unit mode to pixels instead of DIPs using the [**ID2D1DeviceContext::SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) method.</span></span> <span data-ttu-id="0ae7c-130">Se você definir o modo de unidade como pixels e o contexto do dispositivo DPI para o DPI da tela, a otimização ainda estará habilitada.</span><span class="sxs-lookup"><span data-stu-id="0ae7c-130">If you set the unit mode to pixels and the device context DPI to the screen DPI, the optimization is still enabled.</span></span>

## <a name="what-is-a-dip"></a><span data-ttu-id="0ae7c-131">O que é um DIP?</span><span class="sxs-lookup"><span data-stu-id="0ae7c-131">What is a DIP?</span></span>

<span data-ttu-id="0ae7c-132">Um DIP (pixel independente de dispositivo) é um pixel lógico que mapeia para os pixels do dispositivo físico por meio de um escalar, o DPI.</span><span class="sxs-lookup"><span data-stu-id="0ae7c-132">A device independent pixel (DIP) is a logical pixel that maps to the pixels of the physical device through a scalar, the DPI.</span></span> <span data-ttu-id="0ae7c-133">DPI significa pontos por polegada, em que um ponto representa um pixel de dispositivo físico.</span><span class="sxs-lookup"><span data-stu-id="0ae7c-133">DPI stands for dots per inch, where a dot represents a physical device pixel.</span></span> <span data-ttu-id="0ae7c-134">(O nomenclatura vem da impressão, onde os pontos são o menor ponto de tinta que um processo de impressão pode produzir).</span><span class="sxs-lookup"><span data-stu-id="0ae7c-134">(The nomenclature comes from printing, where dots are the smallest ink dot that a printing process can produce).</span></span> <span data-ttu-id="0ae7c-135">Como um monitor padrão costumava ter 96 pontos por polegada, um DPI de 96 significava que um pixel independente de dispositivo (ou DIP) mapeou 1:1 com um pixel físico.</span><span class="sxs-lookup"><span data-stu-id="0ae7c-135">Because a standard monitor used to have 96 dots per inch, a DPI of 96 meant that a device independent pixel (or DIP) mapped 1:1 with a physical pixel.</span></span> <span data-ttu-id="0ae7c-136">Por exemplo, se o DPI fosse 96 \* 2 = 192, um único DIP abrange dois pixels físicos.</span><span class="sxs-lookup"><span data-stu-id="0ae7c-136">For example, if the DPI were 96\*2 = 192, then a single DIP would encompass two physical pixels.</span></span>

<span data-ttu-id="0ae7c-137">Há muitas razões pelas quais os aplicativos não manipulam necessariamente esse dimensionamento corretamente; uma das razões mais simples é que ele requer um trabalho extra para descobrir e usar esse valor escalar durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="0ae7c-137">There are many reasons why applications don't necessarily handle this scaling correctly; one of the simplest reasons is that it requires extra work to discover and use this scalar value when rendering.</span></span> <span data-ttu-id="0ae7c-138">No Direct2D, o dimensionamento é aplicado por padrão.</span><span class="sxs-lookup"><span data-stu-id="0ae7c-138">In Direct2D, the scaling is applied by default.</span></span> <span data-ttu-id="0ae7c-139">Devido a esse mapeamento, os pixels de dispositivo físico podem acabar em coordenadas de DIP fracionários, que é um dos motivos pelos quais o Direct2D usa um espaço de coordenadas de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="0ae7c-139">Because of this mapping, physical device pixels might end up at fractional DIP coordinates, which is one of the reasons why Direct2D uses a floating-point coordinate space.</span></span>

<dl> <span data-ttu-id="0ae7c-140">pixel físico = (DIP × DPI)/96</span><span class="sxs-lookup"><span data-stu-id="0ae7c-140">physical pixel = (dip × DPI) / 96</span></span>  
</dl>

<span data-ttu-id="0ae7c-141">Para converter um pixel físico em um DIP, use esta fórmula:</span><span class="sxs-lookup"><span data-stu-id="0ae7c-141">To convert a physical pixel to a DIP, use this formula:</span></span>

<dl> <span data-ttu-id="0ae7c-142">DIP = (pixel físico × 96)/DPI</span><span class="sxs-lookup"><span data-stu-id="0ae7c-142">dip = (physical pixel × 96) / DPI</span></span>  
</dl>

> [!Note]
>
> <span data-ttu-id="0ae7c-143">A partir do Windows 8, você pode alternar o modo de unidade para pixels em vez de DIPs usando o método [**ID2D1DeviceContext:: Setunitmode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) .</span><span class="sxs-lookup"><span data-stu-id="0ae7c-143">Starting with Windows 8, you can switch the unit mode to pixels instead of DIPs using the [**ID2D1DeviceContext::SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) method.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0ae7c-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0ae7c-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ae7c-145">Como garantir que seu aplicativo seja exibido corretamente em monitores de alto DPI</span><span class="sxs-lookup"><span data-stu-id="0ae7c-145">How to Ensure That Your Application Displays Properly on High-DPI Displays</span></span>](how-to--size-a-window-properly-for-high-dpi-displays.md)
</dt> </dl>

 

 