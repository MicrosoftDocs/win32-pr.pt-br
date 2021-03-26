---
title: Interfaces de camada
description: Esta seção contém informações sobre as interfaces de camada.
ms.assetid: 100cb66a-9bf5-4d0b-9f03-ad7c00e76d9d
keywords:
- interfaces, camada do Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a57945866e8dea1b04c4066362105c8ac6e259a5
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104988722"
---
# <a name="layer-interfaces"></a><span data-ttu-id="ec550-104">Interfaces de camada</span><span class="sxs-lookup"><span data-stu-id="ec550-104">Layer Interfaces</span></span>

<span data-ttu-id="ec550-105">Esta seção contém informações sobre as interfaces de camada.</span><span class="sxs-lookup"><span data-stu-id="ec550-105">This section contains information about the layer interfaces.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="ec550-106">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="ec550-106">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ec550-107">Tópico</span><span class="sxs-lookup"><span data-stu-id="ec550-107">Topic</span></span></th>
<th><span data-ttu-id="ec550-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ec550-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ec550-109"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11debug"><strong>ID3D11Debug</strong></a></span><span class="sxs-lookup"><span data-stu-id="ec550-109"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11debug"><strong>ID3D11Debug</strong></a></span></span><br/></td>
<td><span data-ttu-id="ec550-110">Uma interface de depuração controla as configurações de depuração, valida o estado do pipeline e só pode ser usada se a camada de depuração estiver ativada.</span><span class="sxs-lookup"><span data-stu-id="ec550-110">A debug interface controls debug settings, validates pipeline state and can only be used if the debug layer is turned on.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec550-111"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11infoqueue"><strong>ID3D11InfoQueue</strong></a></span><span class="sxs-lookup"><span data-stu-id="ec550-111"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11infoqueue"><strong>ID3D11InfoQueue</strong></a></span></span><br/></td>
<td><span data-ttu-id="ec550-112">Uma interface de fila de informações armazena, recupera e filtra mensagens de depuração.</span><span class="sxs-lookup"><span data-stu-id="ec550-112">An information-queue interface stores, retrieves, and filters debug messages.</span></span> <span data-ttu-id="ec550-113">A fila consiste em uma fila de mensagens, uma pilha de filtro de armazenamento opcional e uma pilha de filtro de recuperação opcional.</span><span class="sxs-lookup"><span data-stu-id="ec550-113">The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec550-114"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11refdefaulttrackingoptions"><strong>ID3D11RefDefaultTrackingOptions</strong></a></span><span class="sxs-lookup"><span data-stu-id="ec550-114"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11refdefaulttrackingoptions"><strong>ID3D11RefDefaultTrackingOptions</strong></a></span></span><br/></td>
<td><span data-ttu-id="ec550-115">A interface de rastreamento padrão define as opções de controle padrão de referência.</span><span class="sxs-lookup"><span data-stu-id="ec550-115">The default tracking interface sets reference default tracking options.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec550-116"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11reftrackingoptions"><strong>ID3D11RefTrackingOptions</strong></a></span><span class="sxs-lookup"><span data-stu-id="ec550-116"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11reftrackingoptions"><strong>ID3D11RefTrackingOptions</strong></a></span></span><br/></td>
<td><span data-ttu-id="ec550-117">A interface de acompanhamento define as opções de acompanhamento de referência.</span><span class="sxs-lookup"><span data-stu-id="ec550-117">The tracking interface sets reference tracking options.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec550-118"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a></span><span class="sxs-lookup"><span data-stu-id="ec550-118"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="ec550-119">Não há suporte para a interface <a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a> e seus métodos no Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="ec550-119">The <a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a> interface and its methods are not supported in Direct3D 11.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec550-120"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11tracingdevice"><strong>ID3D11TracingDevice</strong></a></span><span class="sxs-lookup"><span data-stu-id="ec550-120"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11tracingdevice"><strong>ID3D11TracingDevice</strong></a></span></span><br/></td>
<td><span data-ttu-id="ec550-121">A interface do dispositivo de rastreamento define informações de rastreamento do sombreador, que permite o registro em log preciso e a reprodução da execução do sombreador.</span><span class="sxs-lookup"><span data-stu-id="ec550-121">The tracing device interface sets shader tracking information, which enables accurate logging and playback of shader execution.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="ec550-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ec550-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec550-123">Referência de camada</span><span class="sxs-lookup"><span data-stu-id="ec550-123">Layer Reference</span></span>](d3d11-graphics-reference-d3d11-layer.md)
</dt> </dl>

 

 





