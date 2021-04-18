---
description: Adicionando nós de saída com TopoEdit
ms.assetid: 23d60fc7-547b-4ef5-b334-5f1b38e58e92
title: Adicionando nós de saída com TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84dc30631332e8138b35e4bbc0ccde75ec9b0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813665"
---
# <a name="adding-output-nodes-with-topoedit"></a><span data-ttu-id="09693-103">Adicionando nós de saída com TopoEdit</span><span class="sxs-lookup"><span data-stu-id="09693-103">Adding Output Nodes with TopoEdit</span></span>

<span data-ttu-id="09693-104">Em uma topologia, um nó de saída representa um coletor de mídia que recebe dados de mídia de um nó de transformação e o apresenta para reprodução.</span><span class="sxs-lookup"><span data-stu-id="09693-104">In a topology, an output node represents a media sink that receives media data from a transform node and presents it for playback.</span></span> <span data-ttu-id="09693-105">O tipo de nó de saída depende do tipo de mídia do nó de origem.</span><span class="sxs-lookup"><span data-stu-id="09693-105">The type of output node depends on the media type of the source node.</span></span>

<span data-ttu-id="09693-106">A tabela a seguir mostra o comando de menu/barra de ferramentas para adicionar um nó de saída à topologia.</span><span class="sxs-lookup"><span data-stu-id="09693-106">The following table shows the menu/toolbar command for adding an output node to the topology.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="09693-107">Tipo de mídia de origem</span><span class="sxs-lookup"><span data-stu-id="09693-107">Source media type</span></span></th>
<th><span data-ttu-id="09693-108">Comando de menu/barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="09693-108">Menu/Toolbar Command</span></span></th>
<th><span data-ttu-id="09693-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="09693-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="09693-110">Fluxo de áudio</span><span class="sxs-lookup"><span data-stu-id="09693-110">Audio stream</span></span></td>
<td><span data-ttu-id="09693-111">No menu <strong>topologia</strong> , clique em <strong>Adicionar SAR</strong>.</span><span class="sxs-lookup"><span data-stu-id="09693-111">On the <strong>Topology</strong> menu, click <strong>Add SAR</strong>.</span></span></td>
<td><span data-ttu-id="09693-112">Cria um nó de saída para o processador de áudio de streaming (SAR) que reproduz um fluxo de áudio por meio de um dispositivo de áudio, como uma placa de som.</span><span class="sxs-lookup"><span data-stu-id="09693-112">Creates an output node for the Streaming Audio Renderer (SAR) that plays an audio stream through an audio device such as a sound card.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09693-113">Fluxo de vídeo</span><span class="sxs-lookup"><span data-stu-id="09693-113">Video stream</span></span></td>
<td><span data-ttu-id="09693-114">No menu <strong>topologia</strong> , clique em <strong>Adicionar EVR</strong>.</span><span class="sxs-lookup"><span data-stu-id="09693-114">On the <strong>Topology</strong> menu, click <strong>Add EVR</strong>.</span></span></td>
<td><span data-ttu-id="09693-115">Cria um nó de saída para o processador de vídeo avançado (EVR) que exibe quadros para um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="09693-115">Creates an output node for the enhanced video renderer (EVR) that displays frames for a video stream.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09693-116">Coletor de mídia personalizado</span><span class="sxs-lookup"><span data-stu-id="09693-116">Custom media sink</span></span></td>
<td><ol>
<li><span data-ttu-id="09693-117">No menu <strong>topologia</strong> , clique em <strong>Adicionar coletor personalizado</strong>.</span><span class="sxs-lookup"><span data-stu-id="09693-117">On the <strong>Topology</strong> menu, click <strong>Add Custom Sink</strong>.</span></span><br/> <span data-ttu-id="09693-118">A caixa de diálogo <strong>GUID personalizado de entrada</strong> é aberta.</span><span class="sxs-lookup"><span data-stu-id="09693-118">The <strong>Input Custom GUID</strong> dialog box opens.</span></span><br/></li>
<li><p><span data-ttu-id="09693-119">No campo <strong>GUID:</strong> , insira o GUID do seu coletor personalizado que você deseja adicionar à topologia.</span><span class="sxs-lookup"><span data-stu-id="09693-119">In the <strong>GUID:</strong> field, enter the GUID of your custom sink that you want to add to the topology.</span></span><br/></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="09693-120">TopoEdit espera o GUID no formato &quot; {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} &quot; .</span><span class="sxs-lookup"><span data-stu-id="09693-120">TopoEdit expects the GUID in the format &quot;{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}&quot;.</span></span> <span data-ttu-id="09693-121">Caso contrário, ele não adicionará o nó e exibirá uma &quot; mensagem de erro GUID inválida &quot; .</span><span class="sxs-lookup"><span data-stu-id="09693-121">Otherwise, it fails to add the node and displays an &quot;Invalid GUID&quot; error message.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="09693-122">Clique em <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="09693-122">Click <strong>OK</strong>.</span></span><br/></li>
</ol></td>
<td><span data-ttu-id="09693-123">Cria um nó de saída para o coletor de fluxo para uma fonte de mídia personalizada.</span><span class="sxs-lookup"><span data-stu-id="09693-123">Creates an output node for the stream sink for a custom media source.</span></span><br/> <span data-ttu-id="09693-124">O coletor personalizado deve dar suporte a <strong>CoCreateInstance</strong> para que o coletor possa ser especificado com um CLSID.</span><span class="sxs-lookup"><span data-stu-id="09693-124">The custom sink must support <strong>CoCreateInstance</strong> so that the sink can be specified with a CLSID.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="09693-125">TopoEdit cria o nó de saída especificado.</span><span class="sxs-lookup"><span data-stu-id="09693-125">TopoEdit creates the specified output node.</span></span> <span data-ttu-id="09693-126">O **painel topologia** mostra o nó de saída como uma caixa verde que mostra o nome do coletor de fluxo.</span><span class="sxs-lookup"><span data-stu-id="09693-126">The **Topology Pane** shows the output node as a green box that shows the name of the stream sink.</span></span>

<span data-ttu-id="09693-127">Para obter informações sobre como adicionar nós de saída programaticamente usando APIs Media Foundation, consulte [criando nós de saída](creating-output-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="09693-127">For information about adding output nodes programmatically by using Media Foundation APIs, see [Creating Output Nodes](creating-output-nodes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="09693-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="09693-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09693-129">Criando topologias usando TopoEdit</span><span class="sxs-lookup"><span data-stu-id="09693-129">Building Topologies by Using TopoEdit</span></span>](building-topologies-by-using-topoedit.md)
</dt> <dt>

[<span data-ttu-id="09693-130">Processador de streaming de áudio</span><span class="sxs-lookup"><span data-stu-id="09693-130">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> <dt>

[<span data-ttu-id="09693-131">Processador de vídeo aprimorado</span><span class="sxs-lookup"><span data-stu-id="09693-131">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="09693-132">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="09693-132">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 




