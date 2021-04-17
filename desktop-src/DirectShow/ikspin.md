---
description: A interface IKsPin fornece um método para recuperar os meios suportados por um PIN em um filtro de modo kernel. O IKsPin tem métodos adicionais além daquele mostrado aqui, mas eles não têm suporte para o DirectShow.
ms.assetid: 14d9bef2-e8f0-49d5-bd89-69a95814cf8c
title: Interface IKsPin (ksproxy. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 3d65e5ba5525b977ebae27da9964579614a1d653
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105759541"
---
# <a name="ikspin-interface"></a><span data-ttu-id="55350-104">Interface IKsPin</span><span class="sxs-lookup"><span data-stu-id="55350-104">IKsPin interface</span></span>

<span data-ttu-id="55350-105">A `IKsPin` interface fornece um método para recuperar os meios suportados por um PIN em um filtro de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="55350-105">The `IKsPin` interface provides a method to retrieve the mediums supported by a pin on a kernel-mode filter.</span></span> <span data-ttu-id="55350-106">`IKsPin` tem métodos adicionais além daquele mostrado aqui, mas eles não têm suporte para o DirectShow.</span><span class="sxs-lookup"><span data-stu-id="55350-106">`IKsPin` has additional methods besides the one shown here, but they are not supported for DirectShow.</span></span>

## <a name="members"></a><span data-ttu-id="55350-107">Membros</span><span class="sxs-lookup"><span data-stu-id="55350-107">Members</span></span>

<span data-ttu-id="55350-108">A interface **IKsPin** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="55350-108">The **IKsPin** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="55350-109">**IKsPin** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="55350-109">**IKsPin** also has these types of members:</span></span>

-   [<span data-ttu-id="55350-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="55350-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="55350-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="55350-111">Methods</span></span>

<span data-ttu-id="55350-112">A interface **IKsPin** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="55350-112">The **IKsPin** interface has these methods.</span></span>



| <span data-ttu-id="55350-113">Método</span><span class="sxs-lookup"><span data-stu-id="55350-113">Method</span></span>                                          | <span data-ttu-id="55350-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="55350-114">Description</span></span>                                          |
|:------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="55350-115">**KsQueryMediums**</span><span class="sxs-lookup"><span data-stu-id="55350-115">**KsQueryMediums**</span></span>](ikspin-ksquerymediums.md) | <span data-ttu-id="55350-116">Recupera os meios com suporte por um PIN.</span><span class="sxs-lookup"><span data-stu-id="55350-116">Retrieves the mediums supported by a pin.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="55350-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="55350-117">Remarks</span></span>

<span data-ttu-id="55350-118">Você deve incluir KS. h antes de ksproxy. h.</span><span class="sxs-lookup"><span data-stu-id="55350-118">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="55350-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55350-119">Requirements</span></span>



| <span data-ttu-id="55350-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="55350-120">Requirement</span></span> | <span data-ttu-id="55350-121">Valor</span><span class="sxs-lookup"><span data-stu-id="55350-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55350-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55350-122">Minimum supported client</span></span><br/> | <span data-ttu-id="55350-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="55350-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="55350-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55350-124">Minimum supported server</span></span><br/> | <span data-ttu-id="55350-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="55350-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="55350-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="55350-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="55350-127"><dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="55350-127"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="55350-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="55350-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="55350-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55350-129"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
