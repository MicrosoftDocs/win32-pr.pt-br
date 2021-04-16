---
title: Visão geral da miniatura do DWM
description: Gerenciador de Janelas da Área de Trabalho (DWM) permite a exibição de representações em miniatura de janelas de aplicativos.
ms.assetid: 6d71fcda-0cf0-463c-8c60-0415109d154f
keywords:
- Gerenciador de Janelas da Área de Trabalho (DWM), miniaturas
- DWM (Gerenciador de Janelas da Área de Trabalho), miniaturas
- Gerenciador de Janelas da Área de Trabalho (DWM), relações de miniatura
- DWM (Gerenciador de Janelas da Área de Trabalho), relações de miniatura
- miniaturas
- relações de miniatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3e0f1e6875e447a18ff5e63d703460ff909b25
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104566630"
---
# <a name="dwm-thumbnail-overview"></a><span data-ttu-id="34291-109">Visão geral da miniatura do DWM</span><span class="sxs-lookup"><span data-stu-id="34291-109">DWM Thumbnail Overview</span></span>

<span data-ttu-id="34291-110">Gerenciador de Janelas da Área de Trabalho (DWM) permite a exibição de representações em miniatura de janelas de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="34291-110">Desktop Window Manager (DWM) enables the display of thumbnail representations of application windows.</span></span> <span data-ttu-id="34291-111">Esses não são instantâneos estáticos de uma janela, mas são dinâmicos, em vez de conexões constantes entre uma janela de origem em miniatura e um local em uma janela de destino que recebe a renderização de miniaturas ao vivo.</span><span class="sxs-lookup"><span data-stu-id="34291-111">These are not static snapshots of a window, but are instead dynamic, constant connections between a thumbnail source window and a location on a destination window that receives the live thumbnail rendering.</span></span> <span data-ttu-id="34291-112">Isso permite uma exibição rápida da execução de aplicativos passando o mouse sobre o aplicativo na barra de tarefas ou usando o gesto de tecla ALT-TAB para ver e alternar rapidamente para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="34291-112">This allows a quick view of running applications by hovering over the application on the taskbar or using the ALT-TAB key gesture to see and quickly switch to an application.</span></span>

<span data-ttu-id="34291-113">A imagem a seguir ilustra a miniatura do Windows Vista ao vivo vista quando você passa o mouse sobre o aplicativo na barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="34291-113">The following image illustrates the Windows Vista live thumbnail seen when you hover over the application on the taskbar.</span></span>

![Captura de tela que mostra a miniatura D W M vista ao passar o mouse sobre um aplicativo na barra de tarefas.](images/dwm-livethumbnail.png)

<span data-ttu-id="34291-115">A imagem a seguir ilustra o Windows Vista Flip (ALT-TAB) habilitado pelo DWM.</span><span class="sxs-lookup"><span data-stu-id="34291-115">The following image illustrates the Windows Vista Flip (ALT-TAB) enabled by DWM.</span></span>

![captura de tela da guia Alt habilitada para DWM](images/dwm-flip.png)

> [!Note]  
> <span data-ttu-id="34291-117">As miniaturas do DWM não permitem que os desenvolvedores criem aplicativos como o recurso Windows Vista Flip3D (WINKEY-TAB).</span><span class="sxs-lookup"><span data-stu-id="34291-117">DWM thumbnails do not enable developers to create applications like the Windows Vista Flip3D (WINKEY-TAB) feature.</span></span> <span data-ttu-id="34291-118">As miniaturas são renderizadas diretamente para a janela de destino em 2-D.</span><span class="sxs-lookup"><span data-stu-id="34291-118">Thumbnails are rendered directly to the destination window in 2-D.</span></span>

 

## <a name="dwm-thumbnail-relationships"></a><span data-ttu-id="34291-119">Relações de miniatura do DWM</span><span class="sxs-lookup"><span data-stu-id="34291-119">DWM Thumbnail Relationships</span></span>

<span data-ttu-id="34291-120">Para exibir miniaturas em seu aplicativo, primeiro você deve estabelecer uma relação entre uma janela de origem e uma janela de destino.</span><span class="sxs-lookup"><span data-stu-id="34291-120">To display thumbnails in your application, you must first establish a relationship between a source window and a destination window.</span></span> <span data-ttu-id="34291-121">Isso é feito chamando a função [**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="34291-121">This is done by calling the [**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) function.</span></span>

<span data-ttu-id="34291-122">[**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) não processa uma miniatura na janela de destino, mas apenas cria a relação e fornece o identificador de miniatura.</span><span class="sxs-lookup"><span data-stu-id="34291-122">[**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) does not render a thumbnail on the destination window but merely creates the relationship and provides the thumbnail handle.</span></span> <span data-ttu-id="34291-123">A miniatura é renderizada depois que as [**\_ \_ Propriedades de miniatura do DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) tiverem sido definidas e a função [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) tiver sido chamada.</span><span class="sxs-lookup"><span data-stu-id="34291-123">The thumbnail is rendered after the [**DWM\_THUMBNAIL\_PROPERTIES**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) have been set and the [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) function has been called.</span></span> <span data-ttu-id="34291-124">As chamadas subsequentes para **DwmUpdateThumbnailProperties** atualizam a miniatura com um novo conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="34291-124">Subsequent calls to **DwmUpdateThumbnailProperties** update the thumbnail with a new set of properties.</span></span> <span data-ttu-id="34291-125">O DWM também fornece a função auxiliar [**DwmQueryThumbnailSourceSize**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize) para obter o tamanho da janela de origem da miniatura.</span><span class="sxs-lookup"><span data-stu-id="34291-125">The DWM also provides the helper function [**DwmQueryThumbnailSourceSize**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize) to obtain the size of the source window from the thumbnail.</span></span>

<span data-ttu-id="34291-126">Para encerrar uma relação de miniatura, chame a função [**DwmUnregisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="34291-126">To end a thumbnail relationship, call the [**DwmUnregisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail) function.</span></span>

<span data-ttu-id="34291-127">O exemplo a seguir demonstra como criar um releationship com a área de trabalho do Windows e exibi-lo em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="34291-127">The following example demonstrates how to create a releationship with the Windows desktop and display it in an application.</span></span>


```
HRESULT hr = S_OK;
HTHUMBNAIL thumbnail = NULL;

// Register the thumbnail
hr = DwmRegisterThumbnail(hwnd, FindWindow(_T("Progman"), NULL), &thumbnail);
if (SUCCEEDED(hr))
{
    // Specify the destination rectangle size
    RECT dest = {0,50,100,150};

    // Set the thumbnail properties for use
    DWM_THUMBNAIL_PROPERTIES dskThumbProps;
    dskThumbProps.dwFlags = DWM_TNP_SOURCECLIENTAREAONLY | DWM_TNP_VISIBLE | DWM_TNP_OPACITY | DWM_TNP_RECTDESTINATION;
    dskThumbProps.fSourceClientAreaOnly = FALSE; 
    dskThumbProps.fVisible = TRUE;
    dskThumbProps.opacity = (255 * 70)/100;
    dskThumbProps.rcDestination = dest;

    // Display the thumbnail
    hr = DwmUpdateThumbnailProperties(thumbnail,&dskThumbProps);
    if (SUCCEEDED(hr))
    {
        // ...
    }
}
return hr;
```



## <a name="related-topics"></a><span data-ttu-id="34291-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="34291-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34291-129">Visão geral do Gerenciador de Janelas da Área de Trabalho</span><span class="sxs-lookup"><span data-stu-id="34291-129">Desktop Window Manager Overview</span></span>](dwm-overview.md)
</dt> <dt>

[<span data-ttu-id="34291-130">Habilitar e controlar a composição do DWM</span><span class="sxs-lookup"><span data-stu-id="34291-130">Enable and Control DWM Composition</span></span>](composition-ovw.md)
</dt> <dt>

[<span data-ttu-id="34291-131">Considerações sobre desempenho e práticas recomendadas</span><span class="sxs-lookup"><span data-stu-id="34291-131">Performance Considerations and Best Practices</span></span>](bestpractices-ovw.md)
</dt> </dl>

 

 




