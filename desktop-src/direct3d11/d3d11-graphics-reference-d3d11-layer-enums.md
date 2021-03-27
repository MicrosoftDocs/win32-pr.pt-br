---
title: Enumerações de camada
description: Esta seção contém informações sobre as enumerações de camada.
ms.assetid: 0fd0456b-2638-4b4c-8a34-a3e104a1a034
keywords:
- enumerações, camada do Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e1cca3fa500a529930c8d0c39005697045d18b
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104967242"
---
# <a name="layer-enumerations"></a><span data-ttu-id="ac841-104">Enumerações de camada</span><span class="sxs-lookup"><span data-stu-id="ac841-104">Layer Enumerations</span></span>

<span data-ttu-id="ac841-105">Esta seção contém informações sobre as enumerações de camada.</span><span class="sxs-lookup"><span data-stu-id="ac841-105">This section contains information about the layer enumerations.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="ac841-106">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="ac841-106">In this section</span></span>



| <span data-ttu-id="ac841-107">Tópico</span><span class="sxs-lookup"><span data-stu-id="ac841-107">Topic</span></span>                                                                                             | <span data-ttu-id="ac841-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ac841-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ac841-109">**\_Categoria de mensagem D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="ac841-109">**D3D11\_MESSAGE\_CATEGORY**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_category)<br/>                             | <span data-ttu-id="ac841-110">Categorias de mensagens de depuração.</span><span class="sxs-lookup"><span data-stu-id="ac841-110">Categories of debug messages.</span></span> <span data-ttu-id="ac841-111">Isso identificará a categoria de uma mensagem ao recuperar uma mensagem com [**ID3D11InfoQueue:: GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) e ao adicionar uma mensagem com [**ID3D11InfoQueue:: AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage).</span><span class="sxs-lookup"><span data-stu-id="ac841-111">This will identify the category of a message when retrieving a message with [**ID3D11InfoQueue::GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) and when adding a message with [**ID3D11InfoQueue::AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage).</span></span> <span data-ttu-id="ac841-112">Ao criar um [**filtro de fila de informações**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter), esses valores podem ser usados para permitir ou negar quaisquer categorias de mensagens a serem passadas pelos filtros de armazenamento e recuperação.</span><span class="sxs-lookup"><span data-stu-id="ac841-112">When creating an [**info queue filter**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter), these values can be used to allow or deny any categories of messages to pass through the storage and retrieval filters.</span></span><br/> |
| [<span data-ttu-id="ac841-113">**\_ID da mensagem D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="ac841-113">**D3D11\_MESSAGE\_ID**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_id)<br/>                                         | <span data-ttu-id="ac841-114">Mensagens de depuração para configurar um filtro de fila de informações (consulte [**D3D11 \_ info \_ Queue \_ Filter**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)); Use essas mensagens para permitir ou negar as categorias de mensagens a serem passadas pelos filtros de armazenamento e recuperação.</span><span class="sxs-lookup"><span data-stu-id="ac841-114">Debug messages for setting up an info-queue filter (see [**D3D11\_INFO\_QUEUE\_FILTER**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)); use these messages to allow or deny message categories to pass through the storage and retrieval filters.</span></span> <span data-ttu-id="ac841-115">Essas IDs são usadas por métodos como [**ID3D11InfoQueue:: GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) ou [**ID3D11InfoQueue:: AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage).</span><span class="sxs-lookup"><span data-stu-id="ac841-115">These IDs are used by methods such as [**ID3D11InfoQueue::GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) or [**ID3D11InfoQueue::AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage).</span></span> <br/>                                                             |
| [<span data-ttu-id="ac841-116">**\_Severidade da mensagem D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="ac841-116">**D3D11\_MESSAGE\_SEVERITY**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_severity)<br/>                             | <span data-ttu-id="ac841-117">Depurar níveis de severidade de mensagem para uma fila de informações.</span><span class="sxs-lookup"><span data-stu-id="ac841-117">Debug message severity levels for an information queue.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="ac841-118">**\_Sinalizadores D3D11 RLDO \_**</span><span class="sxs-lookup"><span data-stu-id="ac841-118">**D3D11\_RLDO\_FLAGS**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_rldo_flags)<br/>                                         | <span data-ttu-id="ac841-119">Opções para a quantidade de informações a serem relatadas sobre o tempo de vida de um objeto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ac841-119">Options for the amount of information to report about a device object's lifetime.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="ac841-120">**\_Opções de acompanhamento do sombreador D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ac841-120">**D3D11\_SHADER\_TRACKING\_OPTIONS**</span></span>](/windows/win32/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_shader_tracking_options)<br/>              | <span data-ttu-id="ac841-121">Opções que especificam como executar o rastreamento de depuração do sombreador.</span><span class="sxs-lookup"><span data-stu-id="ac841-121">Options that specify how to perform shader debug tracking.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="ac841-122">**\_Tipo de \_ recurso de acompanhamento de SOMBREAdor D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ac841-122">**D3D11\_SHADER\_TRACKING\_RESOURCE\_TYPE**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_shader_tracking_resource_type)<br/> | <span data-ttu-id="ac841-123">Indica quais tipos de recursos controlar.</span><span class="sxs-lookup"><span data-stu-id="ac841-123">Indicates which resource types to track.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="ac841-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ac841-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac841-125">Referência de camada</span><span class="sxs-lookup"><span data-stu-id="ac841-125">Layer Reference</span></span>](d3d11-graphics-reference-d3d11-layer.md)
</dt> </dl>

 

 





