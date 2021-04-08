---
description: A interface IWiaSegmentationFilter detecta as subregiãos de um fluxo de imagem e torna itens IWiaItem2 separados para cada um.
ms.assetid: eb7f1284-ab98-4d86-8b30-7abd504cee12
title: Interface IWiaSegmentationFilter (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaSegmentationFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: b9c0bcdee5b40c37fb38b390f5085fe275f0f660
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827167"
---
# <a name="iwiasegmentationfilter-interface"></a><span data-ttu-id="a648f-103">Interface IWiaSegmentationFilter</span><span class="sxs-lookup"><span data-stu-id="a648f-103">IWiaSegmentationFilter interface</span></span>

<span data-ttu-id="a648f-104">A interface **IWiaSegmentationFilter** detecta as subregiãos de um fluxo de imagem e torna itens [**IWiaItem2**](-wia-iwiaitem2.md) separados para cada um.</span><span class="sxs-lookup"><span data-stu-id="a648f-104">The **IWiaSegmentationFilter** interface detects sub-regions of an image stream and makes separate [**IWiaItem2**](-wia-iwiaitem2.md) items for each.</span></span>

## <a name="members"></a><span data-ttu-id="a648f-105">Membros</span><span class="sxs-lookup"><span data-stu-id="a648f-105">Members</span></span>

<span data-ttu-id="a648f-106">A interface **IWiaSegmentationFilter** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a648f-106">The **IWiaSegmentationFilter** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a648f-107">**IWiaSegmentationFilter** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a648f-107">**IWiaSegmentationFilter** also has these types of members:</span></span>

-   [<span data-ttu-id="a648f-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="a648f-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a648f-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="a648f-109">Methods</span></span>

<span data-ttu-id="a648f-110">A interface **IWiaSegmentationFilter** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="a648f-110">The **IWiaSegmentationFilter** interface has these methods.</span></span>



| <span data-ttu-id="a648f-111">Método</span><span class="sxs-lookup"><span data-stu-id="a648f-111">Method</span></span>                                                             | <span data-ttu-id="a648f-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="a648f-112">Description</span></span>                                                                                                                                              |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a648f-113">**DetectRegions**</span><span class="sxs-lookup"><span data-stu-id="a648f-113">**DetectRegions**</span></span>](-wia-iwiasegmentationfilter-detectregions.md) | <span data-ttu-id="a648f-114">Determina as subregiãos de uma imagem disposta no cilindro de mesa para que cada sub-região possa ser adquirida em um item de imagem separado.</span><span class="sxs-lookup"><span data-stu-id="a648f-114">Determines the sub-regions of an image laid out on the flatbed platen so that each of sub-region can be acquired into a separate image item.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="a648f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a648f-115">Remarks</span></span>

<span data-ttu-id="a648f-116">Um aplicativo deve usar [**IWiaItem2:: GetExtension**](-wia-iwiaitem2-getextension.md) para criar uma nova instância do filtro de segmentação.</span><span class="sxs-lookup"><span data-stu-id="a648f-116">An application should use [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md) to create a new instance of the segmentation filter.</span></span> <span data-ttu-id="a648f-117">Um aplicativo normalmente chama essa função antes de exibir sua janela de visualização.</span><span class="sxs-lookup"><span data-stu-id="a648f-117">An application typically calls this function before displaying its preview window.</span></span>

<span data-ttu-id="a648f-118">Ao implementar esse filtro, use [**IWiaItem2:: createchilditem**](-wia-iwiaitem2-createchilditem.md) para criar os itens filho.</span><span class="sxs-lookup"><span data-stu-id="a648f-118">When implementing this filter, use [**IWiaItem2::CreateChildItem**](-wia-iwiaitem2-createchilditem.md) to create the child items.</span></span> <span data-ttu-id="a648f-119">O aplicativo deve passar **\_ valores de \_ propriedade \_ pai de cópia** para o parâmetro *ICreationFlags* para garantir que as propriedades, como formato de imagem e resolução, sejam as mesmas no filho recém-criado como no item pai.</span><span class="sxs-lookup"><span data-stu-id="a648f-119">The application should pass **COPY\_PARENT\_PROPERTY\_VALUES** to the *ICreationFlags* parameter to ensure that properties such as image format and resolution is the same in the newly created child as in the parent item.</span></span>

<span data-ttu-id="a648f-120">Um filtro de segmentação deve dar suporte a todos os formatos de imagem para os quais o driver que ele é usado oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="a648f-120">A segmentation filter must support all the image formats that the driver it is used with supports.</span></span> <span data-ttu-id="a648f-121">O filtro fornecido pela Microsoft dá suporte a bitmap (BMP), Graphics Interchange Format (GIF), JPEG, Portable Network Graphics (PNG) e TIFF (Tagged Image File Format).</span><span class="sxs-lookup"><span data-stu-id="a648f-121">The Microsoft provided filter supports bitmap (BMP), Graphics Interchange Format (GIF), JPEG, Portable Network Graphics (PNG), and Tagged Image File Format (TIFF).</span></span>

<span data-ttu-id="a648f-122">O filtro de segmentação deve ser usado somente em itens de scanner de filme e de mesa.</span><span class="sxs-lookup"><span data-stu-id="a648f-122">The segmentation filter should be used only on film and flatbed scanner items.</span></span> <span data-ttu-id="a648f-123">Para a verificação de filmes, um scanner geralmente vem com os quadros fixos, caso em que o driver criou os itens filho e o aplicativo não deve invocar o filtro de segmentação.</span><span class="sxs-lookup"><span data-stu-id="a648f-123">For film scanning, a scanner often comes with fixed frames in which case the driver created the child items and the application should not invoke the segmentation filter.</span></span>

<span data-ttu-id="a648f-124">A interface **IWiaSegmentationFilter** , como todas as interfaces de Component Object Model (com), herda os métodos de interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a648f-124">The **IWiaSegmentationFilter** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="a648f-125">Métodos IUnknown</span><span class="sxs-lookup"><span data-stu-id="a648f-125">IUnknown Methods</span></span>                                        | <span data-ttu-id="a648f-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="a648f-126">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="a648f-127">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="a648f-127">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="a648f-128">Retorna ponteiros para interfaces com suporte.</span><span class="sxs-lookup"><span data-stu-id="a648f-128">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="a648f-129">IUnknown:: AddRef</span><span class="sxs-lookup"><span data-stu-id="a648f-129">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="a648f-130">Incrementa a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="a648f-130">Increments reference count.</span></span>               |
| [<span data-ttu-id="a648f-131">IUnknown:: versão</span><span class="sxs-lookup"><span data-stu-id="a648f-131">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="a648f-132">Decrementa a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="a648f-132">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="a648f-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a648f-133">Requirements</span></span>



| <span data-ttu-id="a648f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="a648f-134">Requirement</span></span> | <span data-ttu-id="a648f-135">Valor</span><span class="sxs-lookup"><span data-stu-id="a648f-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a648f-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a648f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a648f-137">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a648f-137">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a648f-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a648f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a648f-139">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a648f-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a648f-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a648f-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="a648f-141"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="a648f-141"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="a648f-142">INSERI</span><span class="sxs-lookup"><span data-stu-id="a648f-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a648f-143"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a648f-143"><dt>Wia.idl</dt></span></span> </dl> |



 

 
