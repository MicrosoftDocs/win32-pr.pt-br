---
description: A interface ISmartRenderEngine fornece métodos que dão suporte à recompactação inteligente nos serviços de edição do DirectShow (DES). O mecanismo de processamento inteligente expõe essa interface.
ms.assetid: 0e03708f-e471-4188-a212-ec5e951d20fa
title: Interface ISmartRenderEngine (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e82ba73764adc27ff366533c3b5cfdc2eebc7e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759532"
---
# <a name="ismartrenderengine-interface"></a><span data-ttu-id="54990-104">Interface ISmartRenderEngine</span><span class="sxs-lookup"><span data-stu-id="54990-104">ISmartRenderEngine interface</span></span>

> [!Note]  
> <span data-ttu-id="54990-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="54990-105">\[Deprecated.</span></span> <span data-ttu-id="54990-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="54990-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="54990-107">A `ISmartRenderEngine` interface fornece métodos que dão suporte à recompactação inteligente nos [serviços de edição do DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="54990-107">The `ISmartRenderEngine` interface provides methods that support smart recompression in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="54990-108">O mecanismo de processamento inteligente expõe essa interface.</span><span class="sxs-lookup"><span data-stu-id="54990-108">The smart render engine exposes this interface.</span></span>

## <a name="members"></a><span data-ttu-id="54990-109">Membros</span><span class="sxs-lookup"><span data-stu-id="54990-109">Members</span></span>

<span data-ttu-id="54990-110">A interface **ISmartRenderEngine** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="54990-110">The **ISmartRenderEngine** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="54990-111">**ISmartRenderEngine** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="54990-111">**ISmartRenderEngine** also has these types of members:</span></span>

-   [<span data-ttu-id="54990-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="54990-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="54990-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="54990-113">Methods</span></span>

<span data-ttu-id="54990-114">A interface **ISmartRenderEngine** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="54990-114">The **ISmartRenderEngine** interface has these methods.</span></span>



| <span data-ttu-id="54990-115">Método</span><span class="sxs-lookup"><span data-stu-id="54990-115">Method</span></span>                                                                | <span data-ttu-id="54990-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="54990-116">Description</span></span>                                                                          |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="54990-117">**GetGroupCompressor**</span><span class="sxs-lookup"><span data-stu-id="54990-117">**GetGroupCompressor**</span></span>](ismartrenderengine-getgroupcompressor.md)   | <span data-ttu-id="54990-118">Recupera o filtro de compactação para o grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="54990-118">Retrieves the compression filter for the specified group.</span></span><br/>                 |
| [<span data-ttu-id="54990-119">**SetFindCompressorCB**</span><span class="sxs-lookup"><span data-stu-id="54990-119">**SetFindCompressorCB**</span></span>](ismartrenderengine-setfindcompressorcb.md) | <span data-ttu-id="54990-120">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="54990-120">Not implemented.</span></span><br/>                                                          |
| [<span data-ttu-id="54990-121">**SetGroupCompressor**</span><span class="sxs-lookup"><span data-stu-id="54990-121">**SetGroupCompressor**</span></span>](ismartrenderengine-setgroupcompressor.md)   | <span data-ttu-id="54990-122">Especifica um filtro de compactação a ser usado ao renderizar o grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="54990-122">Specifies a compression filter to use when rendering the specified group.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="54990-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="54990-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="54990-124">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="54990-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="54990-125">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="54990-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="54990-126">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="54990-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="54990-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54990-127">Requirements</span></span>



| <span data-ttu-id="54990-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="54990-128">Requirement</span></span> | <span data-ttu-id="54990-129">Valor</span><span class="sxs-lookup"><span data-stu-id="54990-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54990-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="54990-130">Header</span></span><br/>  | <dl> <span data-ttu-id="54990-131"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="54990-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="54990-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="54990-132">Library</span></span><br/> | <dl> <span data-ttu-id="54990-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54990-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54990-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="54990-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54990-135">Renderizando um projeto</span><span class="sxs-lookup"><span data-stu-id="54990-135">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 
