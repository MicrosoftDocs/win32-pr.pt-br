---
description: A interface IRenderEngine2 permite que o aplicativo substitua o filtro de redimensionamento de vídeo padrão usado pelos serviços de edição do DirectShow (DES). O mecanismo de renderização básico e o mecanismo de processamento inteligente dão suporte a essa interface.
ms.assetid: 37603c73-e199-431a-9a1e-a40c77755c70
title: Interface IRenderEngine2 (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ed7802cf3d47d745b4e4733bb1fb60c61130b44a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779520"
---
# <a name="irenderengine2-interface"></a><span data-ttu-id="c2111-104">Interface IRenderEngine2</span><span class="sxs-lookup"><span data-stu-id="c2111-104">IRenderEngine2 interface</span></span>

> [!Note]  
> <span data-ttu-id="c2111-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="c2111-105">\[Deprecated.</span></span> <span data-ttu-id="c2111-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c2111-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c2111-107">A `IRenderEngine2` interface permite que o aplicativo substitua o filtro de redimensionamento de vídeo padrão usado pelos serviços de edição do DirectShow (des).</span><span class="sxs-lookup"><span data-stu-id="c2111-107">The `IRenderEngine2` interface enables the application to replace the default video resizing filter used by DirectShow Editing Services (DES).</span></span> <span data-ttu-id="c2111-108">O [mecanismo de renderização básico](basic-render-engine.md) e o [mecanismo de processamento inteligente](smart-render-engine.md) dão suporte a essa interface.</span><span class="sxs-lookup"><span data-stu-id="c2111-108">The [Basic Render Engine](basic-render-engine.md) and the [Smart Render Engine](smart-render-engine.md) both support this interface.</span></span>

## <a name="members"></a><span data-ttu-id="c2111-109">Membros</span><span class="sxs-lookup"><span data-stu-id="c2111-109">Members</span></span>

<span data-ttu-id="c2111-110">A interface **IRenderEngine2** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c2111-110">The **IRenderEngine2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c2111-111">**IRenderEngine2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c2111-111">**IRenderEngine2** also has these types of members:</span></span>

-   [<span data-ttu-id="c2111-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="c2111-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c2111-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="c2111-113">Methods</span></span>

<span data-ttu-id="c2111-114">A interface **IRenderEngine2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c2111-114">The **IRenderEngine2** interface has these methods.</span></span>



| <span data-ttu-id="c2111-115">Método</span><span class="sxs-lookup"><span data-stu-id="c2111-115">Method</span></span>                                                  | <span data-ttu-id="c2111-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2111-116">Description</span></span>                                                                             |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2111-117">**SetResizerGUID**</span><span class="sxs-lookup"><span data-stu-id="c2111-117">**SetResizerGUID**</span></span>](irenderengine2-setresizerguid.md) | <span data-ttu-id="c2111-118">Especifica o CLSID de um filtro de redimensionamento personalizado fornecido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c2111-118">Specifies the CLSID of a custom resizing filter provided by the application.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c2111-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2111-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c2111-120">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="c2111-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c2111-121">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c2111-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c2111-122">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c2111-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c2111-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2111-123">Requirements</span></span>



| <span data-ttu-id="c2111-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2111-124">Requirement</span></span> | <span data-ttu-id="c2111-125">Valor</span><span class="sxs-lookup"><span data-stu-id="c2111-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2111-126">Versão</span><span class="sxs-lookup"><span data-stu-id="c2111-126">Version</span></span><br/> | <span data-ttu-id="c2111-127">DirectX 9,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="c2111-127">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="c2111-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c2111-128">Header</span></span><br/>  | <dl> <span data-ttu-id="c2111-129"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2111-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c2111-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c2111-130">Library</span></span><br/> | <dl> <span data-ttu-id="c2111-131"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2111-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2111-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2111-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2111-133">Fornecendo um redimensionador de vídeo personalizado</span><span class="sxs-lookup"><span data-stu-id="c2111-133">Providing a Custom Video Resizer</span></span>](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
