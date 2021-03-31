---
description: Exibir caixas de diálogo de captura do VFW
ms.assetid: 708212ca-d148-4079-8052-3bf6696a33ab
title: Exibir caixas de diálogo de captura do VFW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45b8b51b164630a8fa6e91b2e68ca8a9a3a875b6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645687"
---
# <a name="display-vfw-capture-dialog-boxes"></a><span data-ttu-id="41a09-103">Exibir caixas de diálogo de captura do VFW</span><span class="sxs-lookup"><span data-stu-id="41a09-103">Display VFW Capture Dialog Boxes</span></span>

<span data-ttu-id="41a09-104">Um dispositivo de captura que ainda usa um driver de vídeo para Windows (VFW) pode dar suporte a qualquer uma das três caixas de diálogo a seguir, que são usadas para configurar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="41a09-104">A capture device that still uses a Video for Windows (VFW) driver can support any of the following three dialog boxes, which are used to configure the device.</span></span>



| <span data-ttu-id="41a09-105">Caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="41a09-105">Dialog box</span></span>    | <span data-ttu-id="41a09-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="41a09-106">Description</span></span>                                                                                           |
|---------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41a09-107">Fonte de vídeo</span><span class="sxs-lookup"><span data-stu-id="41a09-107">Video Source</span></span>  | <span data-ttu-id="41a09-108">Usado para selecionar a entrada de vídeo e ajustar as configurações do dispositivo, como o brilho ou o contraste da imagem.</span><span class="sxs-lookup"><span data-stu-id="41a09-108">Used to select the video input and to adjust device settings, such as picture brightness or contrast.</span></span> |
| <span data-ttu-id="41a09-109">Formato de vídeo</span><span class="sxs-lookup"><span data-stu-id="41a09-109">Video Format</span></span>  | <span data-ttu-id="41a09-110">Usado para selecionar as dimensões da imagem e a profundidade de bits.</span><span class="sxs-lookup"><span data-stu-id="41a09-110">Used to select the image dimensions and bit depth.</span></span>                                                    |
| <span data-ttu-id="41a09-111">Vídeo</span><span class="sxs-lookup"><span data-stu-id="41a09-111">Video Display</span></span> | <span data-ttu-id="41a09-112">Usado para controlar a aparência do vídeo renderizado.</span><span class="sxs-lookup"><span data-stu-id="41a09-112">Used to control the appearance of the rendered video.</span></span>                                                 |



 

<span data-ttu-id="41a09-113">Para mostrar uma dessas caixas de diálogo, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="41a09-113">To show one of these dialog boxes, do the following:</span></span>

1.  <span data-ttu-id="41a09-114">Pare o gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="41a09-114">Stop the filter graph.</span></span>
2.  <span data-ttu-id="41a09-115">Consulte o filtro de captura para a interface [**IAMVfwCaptureDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs) .</span><span class="sxs-lookup"><span data-stu-id="41a09-115">Query the capture filter for the [**IAMVfwCaptureDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs) interface.</span></span> <span data-ttu-id="41a09-116">Se **QueryInterface** for bem-sucedidos, isso significa que o dispositivo de captura é um dispositivo VFW.</span><span class="sxs-lookup"><span data-stu-id="41a09-116">If **QueryInterface** succeeds, it means the capture device is a VFW device.</span></span>
3.  <span data-ttu-id="41a09-117">Chame [**IAMVfwCaptureDialogs:: HasDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-hasdialog) para verificar se o driver dá suporte à caixa de diálogo que você deseja exibir.</span><span class="sxs-lookup"><span data-stu-id="41a09-117">Call [**IAMVfwCaptureDialogs::HasDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-hasdialog) to check if the driver supports the dialog box that you wish to display.</span></span> <span data-ttu-id="41a09-118">A enumeração [**VfwCaptureDialogs**](/windows/desktop/api/strmif/ne-strmif-vfwcapturedialogs) define sinalizadores para cada uma das caixas de diálogo VFW.</span><span class="sxs-lookup"><span data-stu-id="41a09-118">The [**VfwCaptureDialogs**](/windows/desktop/api/strmif/ne-strmif-vfwcapturedialogs) enumeration defines flags for each of the VFW dialog boxes.</span></span> <span data-ttu-id="41a09-119">**HasDialog** retornará S \_ OK se a caixa de diálogo tiver suporte.</span><span class="sxs-lookup"><span data-stu-id="41a09-119">**HasDialog** returns S\_OK if the dialog box is supported.</span></span> <span data-ttu-id="41a09-120">\_Caso contrário, retornará s false, portanto, verifique o valor s \_ OK diretamente, em vez de usar a macro **Succeeded** .</span><span class="sxs-lookup"><span data-stu-id="41a09-120">It returns S\_FALSE otherwise, so check for the value S\_OK directly, rather than using the **SUCCEEDED** macro.</span></span>
4.  <span data-ttu-id="41a09-121">Se a caixa de diálogo tiver suporte, chame [**IAMVfwCaptureDialogs:: ShowDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-showdialog) para exibir a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="41a09-121">If the dialog box is supported, call [**IAMVfwCaptureDialogs::ShowDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-showdialog) to display the dialog box.</span></span>
5.  <span data-ttu-id="41a09-122">Reinicie o grafo.</span><span class="sxs-lookup"><span data-stu-id="41a09-122">Restart the graph.</span></span>

<span data-ttu-id="41a09-123">O código a seguir mostra estas etapas para a caixa de diálogo fonte de vídeo:</span><span class="sxs-lookup"><span data-stu-id="41a09-123">The following code shows these steps for the Video Source dialog box:</span></span>


```C++
pControl->Stop(); // Stop the graph.

// Query the capture filter for the IAMVfwCaptureDialogs interface.
IAMVfwCaptureDialogs *pVfw = 0;
hr = pCap->QueryInterface(IID_IAMVfwCaptureDialogs, (void**)&pVfw);
if (SUCCEEDED(hr))
{
    // Check if the device supports this dialog box.
    if (S_OK == pVfw->HasDialog(VfwCaptureDialog_Source))
    {
        // Show the dialog box.
        hr = pVfw->ShowDialog(VfwCaptureDialog_Source, hwndParent);
    }
}
pControl->Run();
```



## <a name="related-topics"></a><span data-ttu-id="41a09-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="41a09-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41a09-125">Configurando um dispositivo de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="41a09-125">Configuring a Video Capture Device</span></span>](configuring-a-video-capture-device.md)
</dt> </dl>

 

 



