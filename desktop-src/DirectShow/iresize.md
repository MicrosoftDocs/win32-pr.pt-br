---
description: 'A interface IResize deve ter suporte de qualquer filtro personalizado de redimensionador de vídeo para os serviços de edição do DirectShow (DES). Para definir um filtro de redimensionador personalizado, chame o método IRenderEngine2:: SetResizerGUID no mecanismo de processamento.'
ms.assetid: 4740dbff-0881-45e8-b382-98ed9d055403
title: Interface IResize (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1b9684ed6f2d2901159dde5a79bb4563ca0b2bda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760736"
---
# <a name="iresize-interface"></a><span data-ttu-id="6eb13-104">Interface IResize</span><span class="sxs-lookup"><span data-stu-id="6eb13-104">IResize interface</span></span>

> [!Note]  
> <span data-ttu-id="6eb13-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="6eb13-105">\[Deprecated.</span></span> <span data-ttu-id="6eb13-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6eb13-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6eb13-107">A `IResize` interface deve ter suporte de qualquer filtro personalizado de redimensionador de vídeo para os serviços de edição do DirectShow (des).</span><span class="sxs-lookup"><span data-stu-id="6eb13-107">The `IResize` interface must be supported by any custom video resizer filter for DirectShow Editing Services (DES).</span></span> <span data-ttu-id="6eb13-108">Para definir um filtro de redimensionador personalizado, chame o método [**IRenderEngine2:: SetResizerGUID**](irenderengine2-setresizerguid.md) no mecanismo de processamento.</span><span class="sxs-lookup"><span data-stu-id="6eb13-108">To set a custom resizer filter, call the [**IRenderEngine2::SetResizerGUID**](irenderengine2-setresizerguid.md) method on the render engine.</span></span>

## <a name="members"></a><span data-ttu-id="6eb13-109">Membros</span><span class="sxs-lookup"><span data-stu-id="6eb13-109">Members</span></span>

<span data-ttu-id="6eb13-110">A interface **IResize** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6eb13-110">The **IResize** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6eb13-111">**IResize** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6eb13-111">**IResize** also has these types of members:</span></span>

-   [<span data-ttu-id="6eb13-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="6eb13-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6eb13-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="6eb13-113">Methods</span></span>

<span data-ttu-id="6eb13-114">A interface **IResize** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="6eb13-114">The **IResize** interface has these methods.</span></span>



| <span data-ttu-id="6eb13-115">Método</span><span class="sxs-lookup"><span data-stu-id="6eb13-115">Method</span></span>                                          | <span data-ttu-id="6eb13-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="6eb13-116">Description</span></span>                                                  |
|:------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="6eb13-117">**obter \_ Incolocar**</span><span class="sxs-lookup"><span data-stu-id="6eb13-117">**get\_InputSize**</span></span>](iresize-get-inputsize.md) | <span data-ttu-id="6eb13-118">Retorna o tamanho de entrada atual do filtro de redimensionador.</span><span class="sxs-lookup"><span data-stu-id="6eb13-118">Returns the resizer filter's current input size.</span></span><br/>  |
| [<span data-ttu-id="6eb13-119">**obter \_ MediaType**</span><span class="sxs-lookup"><span data-stu-id="6eb13-119">**get\_MediaType**</span></span>](iresize-get-mediatype.md) | <span data-ttu-id="6eb13-120">Retorna o tipo de mídia de saída do filtro de redimensionador.</span><span class="sxs-lookup"><span data-stu-id="6eb13-120">Returns the resizer filter's output media type.</span></span><br/>   |
| [<span data-ttu-id="6eb13-121">**obter \_ tamanho**</span><span class="sxs-lookup"><span data-stu-id="6eb13-121">**get\_Size**</span></span>](iresize-get-size.md)           | <span data-ttu-id="6eb13-122">Retorna o tamanho de saída atual e o modo de ampliação.</span><span class="sxs-lookup"><span data-stu-id="6eb13-122">Returns the current output size and stretch mode.</span></span><br/> |
| [<span data-ttu-id="6eb13-123">**colocar \_ MediaType**</span><span class="sxs-lookup"><span data-stu-id="6eb13-123">**put\_MediaType**</span></span>](iresize-put-mediatype.md) | <span data-ttu-id="6eb13-124">Define o tipo de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="6eb13-124">Sets the output media type.</span></span><br/>                       |
| [<span data-ttu-id="6eb13-125">**tamanho de Put \_**</span><span class="sxs-lookup"><span data-stu-id="6eb13-125">**put\_Size**</span></span>](iresize-put-size.md)           | <span data-ttu-id="6eb13-126">Define o tamanho de saída e o modo de ampliação.</span><span class="sxs-lookup"><span data-stu-id="6eb13-126">Sets the output size and stretch mode.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="6eb13-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="6eb13-127">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6eb13-128">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="6eb13-128">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6eb13-129">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6eb13-129">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6eb13-130">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6eb13-130">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6eb13-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6eb13-131">Requirements</span></span>



| <span data-ttu-id="6eb13-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="6eb13-132">Requirement</span></span> | <span data-ttu-id="6eb13-133">Valor</span><span class="sxs-lookup"><span data-stu-id="6eb13-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6eb13-134">Versão</span><span class="sxs-lookup"><span data-stu-id="6eb13-134">Version</span></span><br/> | <span data-ttu-id="6eb13-135">DirectX 9,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="6eb13-135">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="6eb13-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6eb13-136">Header</span></span><br/>  | <dl> <span data-ttu-id="6eb13-137"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6eb13-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6eb13-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6eb13-138">Library</span></span><br/> | <dl> <span data-ttu-id="6eb13-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6eb13-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6eb13-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="6eb13-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6eb13-141">Fornecendo um redimensionador de vídeo personalizado</span><span class="sxs-lookup"><span data-stu-id="6eb13-141">Providing a Custom Video Resizer</span></span>](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
