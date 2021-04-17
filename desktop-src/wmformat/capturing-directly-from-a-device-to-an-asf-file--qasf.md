---
title: Capturando diretamente de um dispositivo para um arquivo ASF (QASF)
description: Capturando diretamente de um dispositivo para um arquivo ASF (QASF)
ms.assetid: 684a11e3-d507-4219-bc0b-6dfe5e85dad1
keywords:
- SDK do Windows Media Format, capturando de dispositivos para arquivos ASF (QASF)
- SDK do Windows Media Format, DirectShow
- ASF (Advanced Systems Format), capturando de dispositivos (QASF)
- ASF (formato de sistemas avançados), capturando de dispositivos (QASF)
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- DirectShow, capturando de dispositivos para arquivos ASF (QASF)
- SDK do Windows Media Format, QASF
- ASF (Advanced Systems Format), QASF
- ASF (formato de sistemas avançados), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faaf5ba8df3cffbb2121451d3bd1b456fc994078
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105812234"
---
# <a name="capturing-directly-from-a-device-to-an-asf-file-qasf"></a><span data-ttu-id="86a48-114">Capturando diretamente de um dispositivo para um arquivo ASF (QASF)</span><span class="sxs-lookup"><span data-stu-id="86a48-114">Capturing Directly from a Device to an ASF File (QASF)</span></span>

<span data-ttu-id="86a48-115">Ao capturar áudio ou vídeo diretamente em um arquivo ASF, o grafo de filtro é semelhante ao diagrama a seguir, dependendo do tipo de dispositivo de captura que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="86a48-115">When capturing audio or video directly to an ASF file, the filter graph looks something like the following diagram, depending on the type of capture device being used.</span></span>

![Grafo de captura de webcam para WMV](images/asf-webcam.png)

<span data-ttu-id="86a48-117">A documentação do SDK do DirectShow descreve detalhadamente como criar gráficos de captura, mas há um ponto importante a ser lembrado ao criar gráficos de captura usando o gravador ASF do WM: o gravador ASF do WM não será executado, a menos que todos os seus PINs estejam conectados.</span><span class="sxs-lookup"><span data-stu-id="86a48-117">The DirectShow SDK documentation describes in detail how to create capture graphs, but there is one important point to remember when creating capture graphs using the WM ASF Writer: the WM ASF Writer will not run unless all of its pins are connected.</span></span> <span data-ttu-id="86a48-118">Se você configurar o gravador ASF do WM com o perfil de sistema padrão (não recomendado) ou qualquer perfil com fluxos de áudio e vídeo, ele criará um PIN de entrada para cada fluxo e cada um desses Pins deverá ser conectado.</span><span class="sxs-lookup"><span data-stu-id="86a48-118">If you configure the WM ASF Writer with the default system profile (not recommended), or any profile with audio and video streams, then it will create an input pin for each stream and each of those pins must be connected.</span></span> <span data-ttu-id="86a48-119">Se você não pretende capturar áudio, por exemplo, certifique-se de configurar o filtro com um perfil somente de vídeo para que nenhum PIN de áudio seja criado.</span><span class="sxs-lookup"><span data-stu-id="86a48-119">If you do not intend to capture audio, for example, then be sure to configure the filter with a video-only profile so that no audio pin is created.</span></span>

 

 




