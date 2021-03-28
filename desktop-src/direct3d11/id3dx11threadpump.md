---
title: Interface ID3DX11ThreadPump (D3DX11core. h)
description: Uma bomba de thread executa tarefas de forma assíncrona.
ms.assetid: 1a99f728-149d-4800-a6e4-e3a00cf8cf4f
keywords:
- Interface ID3DX11ThreadPump Direct3D 11
- Interface ID3DX11ThreadPump Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b60cedaa4ef84cb9f3ea31cd619d7335cc09324e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085258"
---
# <a name="id3dx11threadpump-interface"></a><span data-ttu-id="eae6d-105">Interface ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="eae6d-105">ID3DX11ThreadPump interface</span></span>

> [!Note]  
> <span data-ttu-id="eae6d-106">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="eae6d-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="eae6d-107">Uma bomba de thread executa tarefas de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="eae6d-107">A thread pump executes tasks asynchronously.</span></span> <span data-ttu-id="eae6d-108">Ele é criado chamando [**D3DX11CreateThreadPump**](d3dx11createthreadpump.md).</span><span class="sxs-lookup"><span data-stu-id="eae6d-108">It is created by calling [**D3DX11CreateThreadPump**](d3dx11createthreadpump.md).</span></span> <span data-ttu-id="eae6d-109">Há várias APIs que usam uma bomba de thread opcional como um parâmetro, como [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) e [**D3DX11CompileFromFile**](d3dx11compilefromfile.md); Se você passar uma interface de bombeamento de thread para essas APIs, as funções serão executadas de forma assíncrona em um thread separado.</span><span class="sxs-lookup"><span data-stu-id="eae6d-109">There are several APIs that take an optional thread pump as a parameter, such as [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) and [**D3DX11CompileFromFile**](d3dx11compilefromfile.md); if you pass a thread pump interface into these APIs, the functions will execute asynchronously on a separate thread.</span></span> <span data-ttu-id="eae6d-110">Especialmente em máquinas com vários processadores, uma bomba de thread pode carregar recursos e processar dados sem uma diminuição perceptível no desempenho.</span><span class="sxs-lookup"><span data-stu-id="eae6d-110">Particularly on multiprocessor machines, a thread pump can load resources and process data without a noticeable decrease in performance.</span></span>

## <a name="members"></a><span data-ttu-id="eae6d-111">Membros</span><span class="sxs-lookup"><span data-stu-id="eae6d-111">Members</span></span>

<span data-ttu-id="eae6d-112">A interface **ID3DX11ThreadPump** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="eae6d-112">The **ID3DX11ThreadPump** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="eae6d-113">**ID3DX11ThreadPump** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="eae6d-113">**ID3DX11ThreadPump** also has these types of members:</span></span>

-   [<span data-ttu-id="eae6d-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="eae6d-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="eae6d-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="eae6d-115">Methods</span></span>

<span data-ttu-id="eae6d-116">A interface **ID3DX11ThreadPump** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="eae6d-116">The **ID3DX11ThreadPump** interface has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="eae6d-117">Método</span><span class="sxs-lookup"><span data-stu-id="eae6d-117">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="eae6d-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="eae6d-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="eae6d-119"><a href="id3dx11threadpump-addworkitem.md"><strong>AddWorkItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="eae6d-119"><a href="id3dx11threadpump-addworkitem.md"><strong>AddWorkItem</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="eae6d-120">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="eae6d-120">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="eae6d-121">Adiciona um item de trabalho à bomba do thread.</span><span class="sxs-lookup"><span data-stu-id="eae6d-121">Adds a work item to the thread pump.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="eae6d-122"><a href="id3dx11threadpump-getqueuestatus.md"><strong>GetQueueStatus</strong></a></span><span class="sxs-lookup"><span data-stu-id="eae6d-122"><a href="id3dx11threadpump-getqueuestatus.md"><strong>GetQueueStatus</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="eae6d-123">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="eae6d-123">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="eae6d-124">Obtém o número de itens em cada uma das três filas dentro da bomba do thread.</span><span class="sxs-lookup"><span data-stu-id="eae6d-124">Gets the number of items in each of the three queues inside the thread pump.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="eae6d-125"><a href="id3dx11threadpump-getworkitemcount.md"><strong>GetWorkItemCount</strong></a></span><span class="sxs-lookup"><span data-stu-id="eae6d-125"><a href="id3dx11threadpump-getworkitemcount.md"><strong>GetWorkItemCount</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="eae6d-126">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="eae6d-126">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="eae6d-127">Obtém o número de itens de trabalho na bomba do thread.</span><span class="sxs-lookup"><span data-stu-id="eae6d-127">Gets the number of work items in the thread pump.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="eae6d-128"><a href="id3dx11threadpump-processdeviceworkitems.md"><strong>ProcessDeviceWorkItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="eae6d-128"><a href="id3dx11threadpump-processdeviceworkitems.md"><strong>ProcessDeviceWorkItems</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="eae6d-129">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="eae6d-129">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="eae6d-130">Define itens de trabalho para o dispositivo depois que eles terminarem de carregar e processar.</span><span class="sxs-lookup"><span data-stu-id="eae6d-130">Sets work items to the device after they have finished loading and processing.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="eae6d-131"><a href="id3dx11threadpump-purgeallitems.md"><strong>PurgeAllItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="eae6d-131"><a href="id3dx11threadpump-purgeallitems.md"><strong>PurgeAllItems</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="eae6d-132">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="eae6d-132">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="eae6d-133">Limpa todos os itens de trabalho da bomba de thread.</span><span class="sxs-lookup"><span data-stu-id="eae6d-133">Clears all work items from the thread pump.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="eae6d-134"><a href="id3dx11threadpump-waitforallitems.md"><strong>WaitForAllItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="eae6d-134"><a href="id3dx11threadpump-waitforallitems.md"><strong>WaitForAllItems</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="eae6d-135">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="eae6d-135">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="eae6d-136">Aguarda a conclusão de todos os itens de trabalho na bomba do thread.</span><span class="sxs-lookup"><span data-stu-id="eae6d-136">Waits for all work items in the thread pump to finish.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="eae6d-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="eae6d-137">Remarks</span></span>

### <a name="using-a-thread-pump"></a><span data-ttu-id="eae6d-138">Usando uma bomba de thread</span><span class="sxs-lookup"><span data-stu-id="eae6d-138">Using a Thread Pump</span></span>

<span data-ttu-id="eae6d-139">A bomba de thread carrega e processa dados usando o seguinte processo de três etapas:</span><span class="sxs-lookup"><span data-stu-id="eae6d-139">The thread pump loads and processes data using the following three-step process:</span></span>

1.  <span data-ttu-id="eae6d-140">Carregue e descompacte os dados com um [**carregador de dados**](id3dx11dataloader.md).</span><span class="sxs-lookup"><span data-stu-id="eae6d-140">Load and decompress the data with a [**Data Loader**](id3dx11dataloader.md).</span></span> <span data-ttu-id="eae6d-141">O objeto data Loader tem três métodos que a bomba de thread chamará internamente, pois está carregando e descompactando os dados: [**ID3DX11DataLoader:: Load**](id3dx11dataloader-load.md), [**ID3DX11DataLoader::D ecompress**](id3dx11dataloader-decompress.md)e [**ID3DX11DataLoader::D estroy**](id3dx11dataloader-destroy.md).</span><span class="sxs-lookup"><span data-stu-id="eae6d-141">The data loader object has three methods that the thread pump will call internally as it is loading and decompressing the data: [**ID3DX11DataLoader::Load**](id3dx11dataloader-load.md), [**ID3DX11DataLoader::Decompress**](id3dx11dataloader-decompress.md), and [**ID3DX11DataLoader::Destroy**](id3dx11dataloader-destroy.md).</span></span> <span data-ttu-id="eae6d-142">A funcionalidade específica dessas três APIs difere dependendo do tipo de dados que estão sendo carregados e descompactados.</span><span class="sxs-lookup"><span data-stu-id="eae6d-142">The specific functionality of these three APIs differs depending on the type of data being loaded and decompressed.</span></span> <span data-ttu-id="eae6d-143">A interface do carregador de dados também pode ser herdada e suas APIs podem ser alteradas se uma estiver carregando um arquivo de dados definido em um formato personalizado próprio.</span><span class="sxs-lookup"><span data-stu-id="eae6d-143">The data loader interface can also be inherited and its APIs can be changed if one is loading a data file defined in one's own custom format.</span></span>
2.  <span data-ttu-id="eae6d-144">Processe os dados com um [**processador de dados**](id3dx11dataprocessor.md).</span><span class="sxs-lookup"><span data-stu-id="eae6d-144">Process the data with a [**Data Processor**](id3dx11dataprocessor.md).</span></span> <span data-ttu-id="eae6d-145">O objeto de processador de dados tem três métodos que a bomba de thread chamará internamente, pois está processando os dados: [**ID3DX11DataProcessor::P modelos**](id3dx11dataprocessor-process.md), [**ID3DX11DataProcessor:: deviceobject**](id3dx11dataprocessor-createdeviceobject.md)e [**ID3DX11DataProcessor::D estroy**](id3dx11dataprocessor-destroy.md).</span><span class="sxs-lookup"><span data-stu-id="eae6d-145">The data processor object has three methods that the thread pump will call internally as it is processing the data: [**ID3DX11DataProcessor::Process**](id3dx11dataprocessor-process.md), [**ID3DX11DataProcessor::CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md), and [**ID3DX11DataProcessor::Destroy**](id3dx11dataprocessor-destroy.md).</span></span> <span data-ttu-id="eae6d-146">A maneira como ele processa os dados será diferente dependendo do tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="eae6d-146">The way it processes the data will be different depending on the type of data.</span></span> <span data-ttu-id="eae6d-147">Por exemplo, se os dados forem uma textura armazenada como JPEG, [**ID3DX11DataProcessor::P modelos**](id3dx11dataprocessor-process.md) fará a descompactação de JPEG para obter os bits de imagem bruta da imagem.</span><span class="sxs-lookup"><span data-stu-id="eae6d-147">For example, if the data is a texture stored as a JPEG, then [**ID3DX11DataProcessor::Process**](id3dx11dataprocessor-process.md) will do JPEG decompression to get the image's raw image bits.</span></span> <span data-ttu-id="eae6d-148">Se os dados forem um sombreador, [**ID3DX11DataProcessor::P modelos**](id3dx11dataprocessor-process.md) compilará o HLSL em código de bytes.</span><span class="sxs-lookup"><span data-stu-id="eae6d-148">If the data is a shader, then [**ID3DX11DataProcessor::Process**](id3dx11dataprocessor-process.md) will compile the HLSL into bytecode.</span></span> <span data-ttu-id="eae6d-149">Depois que os dados forem processados, um objeto de dispositivo será criado para esses dados (com [**ID3DX11DataProcessor:: Createdeviceobject**](id3dx11dataprocessor-createdeviceobject.md)) e o objeto será adicionado a uma fila de objetos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eae6d-149">After the data has been processed a device object will be created for that data (with [**ID3DX11DataProcessor::CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md)) and the object will be added to a queue of device objects.</span></span> <span data-ttu-id="eae6d-150">A interface do processador de dados também pode ser herdada e suas APIs podem ser alteradas se um estiver processando um arquivo de dados definido em um formato personalizado próprio.</span><span class="sxs-lookup"><span data-stu-id="eae6d-150">The data processor interface can also be inherited and its APIs can be changed if one is processing a data file defined in one's own custom format.</span></span>
3.  <span data-ttu-id="eae6d-151">Associe o objeto de dispositivo ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eae6d-151">Bind the device object to the device.</span></span> <span data-ttu-id="eae6d-152">Isso é feito quando um aplicativo chama [**ID3DX11ThreadPump::P rocessdeviceworkitems**](id3dx11threadpump-processdeviceworkitems.md), que associará um número especificado de objetos na fila de objetos de dispositivo ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eae6d-152">This is done when one's application calls [**ID3DX11ThreadPump::ProcessDeviceWorkItems**](id3dx11threadpump-processdeviceworkitems.md), which will bind a specified number of objects in the queue of device objects to the device.</span></span>

<span data-ttu-id="eae6d-153">A bomba de thread pode ser usada para carregar dados de uma das duas maneiras: chamando uma API que usa uma bomba de thread como um parâmetro, como [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) e [**D3DX11CompileFromFile**](d3dx11compilefromfile.md), ou chamando [**ID3DX11ThreadPump:: AddWorkItem**](id3dx11threadpump-addworkitem.md).</span><span class="sxs-lookup"><span data-stu-id="eae6d-153">The thread pump can be used to load data in one of two ways: by calling an API that takes a thread pump as a parameter, such as [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) and [**D3DX11CompileFromFile**](d3dx11compilefromfile.md), or by calling [**ID3DX11ThreadPump::AddWorkItem**](id3dx11threadpump-addworkitem.md).</span></span> <span data-ttu-id="eae6d-154">No caso das APIs que tomam uma bomba de thread, o carregador de dados e o processador de dados são criados internamente.</span><span class="sxs-lookup"><span data-stu-id="eae6d-154">In the case of the APIs that take a thread pump, the data loader and data processor are created internally.</span></span> <span data-ttu-id="eae6d-155">No caso de AddWorkItem, o carregador de dados e o processador de dados devem ser criados com antecedência e, em seguida, passados para AddWorkItem.</span><span class="sxs-lookup"><span data-stu-id="eae6d-155">In the case of AddWorkItem, the data loader and data processor must be created beforehand and are then passed into AddWorkItem.</span></span> <span data-ttu-id="eae6d-156">O D3DX11 fornece um conjunto de APIs para criar carregadores de dados e processadores de dados que têm funcionalidade para carregar e processar formatos de dados comuns.</span><span class="sxs-lookup"><span data-stu-id="eae6d-156">D3DX11 provides a set of APIs for creating data loaders and data processors that have functionality for loading and processing common data formats.</span></span> <span data-ttu-id="eae6d-157">Para formatos de dados personalizados, as interfaces do carregador de dados e do processador de dados devem ser herdadas e seus métodos devem ser redefinidos.</span><span class="sxs-lookup"><span data-stu-id="eae6d-157">For custom data formats, the data loader and data processor interfaces must be inherited and their methods must be redefined.</span></span>

<span data-ttu-id="eae6d-158">O objeto de bomba de thread ocupa uma quantidade significativa de recursos, portanto, em geral, apenas um deve ser criado por aplicativo.</span><span class="sxs-lookup"><span data-stu-id="eae6d-158">The thread pump object takes up a substantial amount of resources, so generally only one should be created per application.</span></span>

## <a name="requirements"></a><span data-ttu-id="eae6d-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eae6d-159">Requirements</span></span>



| <span data-ttu-id="eae6d-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="eae6d-160">Requirement</span></span> | <span data-ttu-id="eae6d-161">Valor</span><span class="sxs-lookup"><span data-stu-id="eae6d-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eae6d-162">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eae6d-162">Minimum supported client</span></span><br/> | <span data-ttu-id="eae6d-163">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="eae6d-163">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="eae6d-164">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eae6d-164">Minimum supported server</span></span><br/> | <span data-ttu-id="eae6d-165">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="eae6d-165">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="eae6d-166">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eae6d-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="eae6d-167"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="eae6d-167"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="eae6d-168">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eae6d-168">Library</span></span><br/>                  | <dl> <span data-ttu-id="eae6d-169"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eae6d-169"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eae6d-170">Confira também</span><span class="sxs-lookup"><span data-stu-id="eae6d-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eae6d-171">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="eae6d-171">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

