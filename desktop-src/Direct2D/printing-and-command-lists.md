---
title: Listas de comandos e impressão
description: O controle de impressão Direct2D \ 32; é um novo componente do módulo Direct2D no Windows 8.
ms.assetid: C51ACCDE-B205-4F79-A2FD-D112BAAD1616
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6beb16a24c972016686e2dffe915a947128a63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366137"
---
# <a name="printing-and-command-lists"></a><span data-ttu-id="f13fc-103">Listas de comandos e impressão</span><span class="sxs-lookup"><span data-stu-id="f13fc-103">Printing and command lists</span></span>

<span data-ttu-id="f13fc-104">O [](./direct2d-portal.md) [**controle de impressão**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) Direct2D é um novo componente do módulo Direct2D no Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f13fc-104">The [Direct2D](./direct2d-portal.md) [**print control**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) is a new component in the Direct2D module in Windows 8.</span></span> <span data-ttu-id="f13fc-105">Esse componente permite que os aplicativos Direct2D reutilizem suas chamadas de desenho Direct2D (em termos de alterações de estado e primitivos de renderização) para fornecer resultados de impressão semelhantes ao que você vê na tela.</span><span class="sxs-lookup"><span data-stu-id="f13fc-105">This component lets Direct2D apps reuse their Direct2D drawing calls (in terms of state changes and rending primitives) to deliver printing results that are similar to what you see on the screen.</span></span>

<span data-ttu-id="f13fc-106">A interface [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) representa um trabalho de impressão virtual: você pode criar um controle de impressão [Direct2D](./direct2d-portal.md) para iniciar um novo trabalho de impressão, passar o conteúdo do Direct2D para cada página que você deseja imprimir e, em seguida, fechar o controle de impressão para concluir um trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="f13fc-106">The [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) interface represents a virtual print job: you can create a [Direct2D](./direct2d-portal.md) print control to initiate a new print job, pass in Direct2D contents for each page you want to print, then close the print control to complete a print job.</span></span>

> [!Note]  
> <span data-ttu-id="f13fc-107">Um controle de impressão é mapeado para um e exatamente um trabalho de impressão, e você não pode reutilizá-lo.</span><span class="sxs-lookup"><span data-stu-id="f13fc-107">A print control maps to one and exactly one print job, and you can't reuse it.</span></span>

<span data-ttu-id="f13fc-108">O controle de impressão [Direct2D](./direct2d-portal.md) converte e otimiza o conteúdo do Direct2D passado para o subsistema de impressão, que funciona com as impressoras reais para fornecer a impressão real.</span><span class="sxs-lookup"><span data-stu-id="f13fc-108">The [Direct2D](./direct2d-portal.md) print control converts and optimizes the passed in Direct2D contents for the print sub-system, which works with the real printers to deliver the actual printout.</span></span> <span data-ttu-id="f13fc-109">Todos os detalhes específicos de impressão ficam ocultos dos aplicativos Direct2D, o que significa que os aplicativos Direct2D podem imprimir sem saber em quais dispositivos eles estão desenhando ou como os desenhos são convertidos para impressão.</span><span class="sxs-lookup"><span data-stu-id="f13fc-109">All print-specific details are hidden from Direct2D apps, which means Direct2D apps can print without knowing what devices they are drawing to, or how the drawings are translated to printing.</span></span>

<span data-ttu-id="f13fc-110">Para imprimir com o [Direct2D](./direct2d-portal.md), você precisa preparar uma lista de comandos do Direct2D para cada página que deseja imprimir e, em seguida, passar essa lista de comandos para o controle de impressão Direct2D.</span><span class="sxs-lookup"><span data-stu-id="f13fc-110">To print with [Direct2D](./direct2d-portal.md), you need to prepare one Direct2D command list for each page you want to print, then pass that command list to the Direct2D print control.</span></span> <span data-ttu-id="f13fc-111">Para preparar essa lista de comandos do Direct2D, basta criar e definir uma lista de comandos como o destino de desenho do contexto do dispositivo atual e, em seguida, desenhar para esse contexto de dispositivo, exatamente como se você estiver desenhando em um destino de bitmap para exibição.</span><span class="sxs-lookup"><span data-stu-id="f13fc-111">To prepare that Direct2D command list, you simply create and set a command list as the drawing target of the current device context, and then draw to that device context, exactly as if you are drawing to a bitmap target for display.</span></span> <span data-ttu-id="f13fc-112">Confira [dispositivos e contextos de dispositivo](devices-and-device-contexts.md) para obter mais informações sobre dispositivos e destinos.</span><span class="sxs-lookup"><span data-stu-id="f13fc-112">See [Devices and Device Contexts](devices-and-device-contexts.md) for more info on devices and targets.</span></span>

<span data-ttu-id="f13fc-113">O diagrama aqui ilustra a interação entre o aplicativo, o contexto do dispositivo, o destino de bitmap, o destino da lista de comandos e o controle de impressão.</span><span class="sxs-lookup"><span data-stu-id="f13fc-113">The diagram here illustrates the interaction between the app, device context, bitmap target, command list target, and the print control.</span></span>

> [!Note]  
> <span data-ttu-id="f13fc-114">Os componentes de impressora e Sub-System de impressão do Windows estão em cinza porque estão completamente ocultos dos aplicativos [Direct2D](./direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="f13fc-114">The Windows Print Sub-System and Printer components are in gray because they are completely hidden from [Direct2D](./direct2d-portal.md) apps.</span></span>

![um diagrama que mostra como os comandos e a impressão interagem com um aplicativo e Direct2D.](images/d2dprintcontroldiagram.png)

## <a name="example"></a><span data-ttu-id="f13fc-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="f13fc-116">Example</span></span>

<span data-ttu-id="f13fc-117">O processo completo de impressão do conteúdo do Direct2D inclui as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="f13fc-117">The complete process of printing Direct2D content includes the following steps.</span></span>

1.  <span data-ttu-id="f13fc-118">Crie um controle de impressão para iniciar um trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="f13fc-118">Create a print control to initiate a print job.</span></span>
2.  <span data-ttu-id="f13fc-119">Adicione uma página ao controle de impressão passando uma lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="f13fc-119">Add a page to the print control by passing in a command list.</span></span>
3.  <span data-ttu-id="f13fc-120">Repita a etapa 2 para cada página no restante do documento</span><span class="sxs-lookup"><span data-stu-id="f13fc-120">Repeat step 2 for each page in the rest of the document</span></span>
4.  <span data-ttu-id="f13fc-121">Feche o controle de impressão para concluir o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="f13fc-121">Close the print control to complete the print job.</span></span>

<span data-ttu-id="f13fc-122">Este é um exemplo de código que mostra o processo.</span><span class="sxs-lookup"><span data-stu-id="f13fc-122">Here is a code example showing the process.</span></span>

```cpp
ID2D1CommandList* commandList;
// Skip command list creation and drawing for simplicity.

// Set print control properties.
D2D1_PRINT_CONTROL_PROPERTIES printControlProperties;
printControlProperties.rasterDPI = 150.0f; // Use the default rasterization DPI for all unsupported Direct2D commands 
                                                                                                                                                                            //  or options.
printControlProperties.fontSubset = D2D1_PRINT_FONT_SUBSET_MODE_DEFAULT; // Using the default font subset strategy.
printControlProperties.colorSpace = D2D1_COLOR_SPACE_SRGB; // Color space for vector graphics in Direct2D print control.

// Create a Direct2D Print Control to initiate a print job.
ID2D1PrintControl* d2dPrintControl;
d2dDevice->CreatePrintControl(
    wicFactory,
    documentTarget,
    printControlProperties,
    &d2dPrintControl
    );

// Add Direct2D drawing commands encapsulated in a command list.
// You can add in more pages by calling this API multiple times.
d2dPrintControl->AddPage(commandList);

// Close the print control to complete a print job.
d2dPrintControl->Close();
```

## <a name="related-topics"></a><span data-ttu-id="f13fc-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f13fc-123">Related topics</span></span>

[<span data-ttu-id="f13fc-124">**ID2D1CommandList**</span><span class="sxs-lookup"><span data-stu-id="f13fc-124">**ID2D1CommandList**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist)

[<span data-ttu-id="f13fc-125">**ID2D1PrintControl**</span><span class="sxs-lookup"><span data-stu-id="f13fc-125">**ID2D1PrintControl**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)

[<span data-ttu-id="f13fc-126">Melhorando o desempenho de aplicativos Direct2D e impressão</span><span class="sxs-lookup"><span data-stu-id="f13fc-126">Improving the Performance of Direct2D Applications and Printing</span></span>](improving-direct2d-performance.md)