---
description: A interface IWiaPreview armazena em cache as imagens não filtradas internamente e as passa por filtros de processamento de imagem.
ms.assetid: 8a51c42b-aa1d-4df0-aba3-6aeb8e1ca2cf
title: Interface IWiaPreview (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 5e1c01daae4e86fa18c087b67bf902daaf6f8793
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164532"
---
# <a name="iwiapreview-interface"></a><span data-ttu-id="a4dd7-103">Interface IWiaPreview</span><span class="sxs-lookup"><span data-stu-id="a4dd7-103">IWiaPreview interface</span></span>

<span data-ttu-id="a4dd7-104">A interface **IWiaPreview** armazena em cache as imagens não filtradas internamente e as passa por filtros de processamento de imagem.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-104">The **IWiaPreview** interface caches unfiltered images internally and passes them through image processing filters.</span></span>

## <a name="members"></a><span data-ttu-id="a4dd7-105">Membros</span><span class="sxs-lookup"><span data-stu-id="a4dd7-105">Members</span></span>

<span data-ttu-id="a4dd7-106">A interface **IWiaPreview** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a4dd7-106">The **IWiaPreview** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a4dd7-107">**IWiaPreview** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a4dd7-107">**IWiaPreview** also has these types of members:</span></span>

-   [<span data-ttu-id="a4dd7-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="a4dd7-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a4dd7-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="a4dd7-109">Methods</span></span>

<span data-ttu-id="a4dd7-110">A interface **IWiaPreview** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-110">The **IWiaPreview** interface has these methods.</span></span>



| <span data-ttu-id="a4dd7-111">Método</span><span class="sxs-lookup"><span data-stu-id="a4dd7-111">Method</span></span>                                                  | <span data-ttu-id="a4dd7-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4dd7-112">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a4dd7-113">**Formatação**</span><span class="sxs-lookup"><span data-stu-id="a4dd7-113">**Clear**</span></span>](-wia-iwiapreview-clear.md)                 | <span data-ttu-id="a4dd7-114">Libera a imagem não filtrada armazenada em cache pelo método [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="a4dd7-114">Releases the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <span data-ttu-id="a4dd7-115">Ele também libera o filtro de processamento de imagem.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-115">It also releases the image processing filter.</span></span> <br/>          |
| [<span data-ttu-id="a4dd7-116">**DetectRegions**</span><span class="sxs-lookup"><span data-stu-id="a4dd7-116">**DetectRegions**</span></span>](-wia-iwiapreview-detectregions.md) | <span data-ttu-id="a4dd7-117">Invoca o filtro de segmentação de driver e passa a imagem não filtrada armazenada em cache pelo método [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) para o filtro.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-117">Invokes the driver segmentation filter and passes the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method to the filter.</span></span> <br/> |
| [<span data-ttu-id="a4dd7-118">**GetNewPreview**</span><span class="sxs-lookup"><span data-stu-id="a4dd7-118">**GetNewPreview**</span></span>](-wia-iwiapreview-getnewpreview.md) | <span data-ttu-id="a4dd7-119">Armazena internamente em cache a imagem não filtrada retornada do driver.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-119">Caches internally the unfiltered image returned from the driver.</span></span> <br/>                                                                                                                |
| [<span data-ttu-id="a4dd7-120">**UpdatePreview**</span><span class="sxs-lookup"><span data-stu-id="a4dd7-120">**UpdatePreview**</span></span>](-wia-iwiapreview-updatepreview.md) | <span data-ttu-id="a4dd7-121">Obtém a imagem não filtrada armazenada em cache pelo método [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="a4dd7-121">Gets the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="a4dd7-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4dd7-122">Remarks</span></span>

<span data-ttu-id="a4dd7-123">Esse filtro é chamado automaticamente pelo método [**IWiaTransfer::D aixar**](-wia-iwiatransfer-download.md) .</span><span class="sxs-lookup"><span data-stu-id="a4dd7-123">This filter is called automatically by the [**IWiaTransfer::Download**](-wia-iwiatransfer-download.md) method.</span></span>

<span data-ttu-id="a4dd7-124">A interface **IWiaPreview** , como todas as interfaces de Component Object Model (com), herda os métodos de interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a4dd7-124">The **IWiaPreview** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="a4dd7-125">Métodos IUnknown</span><span class="sxs-lookup"><span data-stu-id="a4dd7-125">IUnknown Methods</span></span>                                        | <span data-ttu-id="a4dd7-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4dd7-126">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="a4dd7-127">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="a4dd7-127">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="a4dd7-128">Retorna ponteiros para interfaces com suporte.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-128">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="a4dd7-129">IUnknown:: AddRef</span><span class="sxs-lookup"><span data-stu-id="a4dd7-129">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="a4dd7-130">Incrementa a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-130">Increments reference count.</span></span>               |
| [<span data-ttu-id="a4dd7-131">IUnknown:: versão</span><span class="sxs-lookup"><span data-stu-id="a4dd7-131">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="a4dd7-132">Decrementa a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-132">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="a4dd7-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4dd7-133">Requirements</span></span>



| <span data-ttu-id="a4dd7-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4dd7-134">Requirement</span></span> | <span data-ttu-id="a4dd7-135">Valor</span><span class="sxs-lookup"><span data-stu-id="a4dd7-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a4dd7-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4dd7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a4dd7-137">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a4dd7-137">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a4dd7-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4dd7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a4dd7-139">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a4dd7-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a4dd7-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a4dd7-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4dd7-141"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4dd7-141"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="a4dd7-142">INSERI</span><span class="sxs-lookup"><span data-stu-id="a4dd7-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a4dd7-143"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a4dd7-143"><dt>Wia.idl</dt></span></span> </dl> |



 

 
