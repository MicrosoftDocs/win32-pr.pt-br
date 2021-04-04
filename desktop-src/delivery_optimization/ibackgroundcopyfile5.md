---
title: Interface IBackgroundCopyFile5 (Deliveryoptimization. h)
description: Use essa interface para obter ou definir propriedades genéricas de transferências de arquivos de otimização de entrega.
ms.assetid: 2D729717-62D2-4C69-92FE-F4289EC48DF1
keywords:
- Interface IBackgroundCopyFile5
- Interface IBackgroundCopyFile5, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2f23fdb99ba24b4faeca7a65930bf83d4634a979
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085476"
---
# <a name="ibackgroundcopyfile5-interface"></a><span data-ttu-id="ab41c-105">Interface IBackgroundCopyFile5</span><span class="sxs-lookup"><span data-stu-id="ab41c-105">IBackgroundCopyFile5 interface</span></span>

<span data-ttu-id="ab41c-106">Use essa interface para obter ou definir propriedades genéricas de transferências de arquivos de otimização de entrega.</span><span class="sxs-lookup"><span data-stu-id="ab41c-106">Use this interface to get or set generic properties of Delivery Optimization (DO) file transfers.</span></span>

<span data-ttu-id="ab41c-107">Para obter um ponteiro de interface **IBackgroundCopyFile5** , chame o método **IBackgroundCopyFile:: QueryInterface** usando __uuidof (IBackgroundCopyFile5) para o identificador de interface.</span><span class="sxs-lookup"><span data-stu-id="ab41c-107">To get an **IBackgroundCopyFile5** interface pointer, call the **IBackgroundCopyFile::QueryInterface** method using __uuidof(IBackgroundCopyFile5) for the interface identifier.</span></span>

## <a name="members"></a><span data-ttu-id="ab41c-108">Membros</span><span class="sxs-lookup"><span data-stu-id="ab41c-108">Members</span></span>

<span data-ttu-id="ab41c-109">A interface **IBackgroundCopyFile5** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ab41c-109">The **IBackgroundCopyFile5** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ab41c-110">**IBackgroundCopyFile5** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ab41c-110">**IBackgroundCopyFile5** also has these types of members:</span></span>

-   [<span data-ttu-id="ab41c-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="ab41c-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ab41c-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="ab41c-112">Methods</span></span>

<span data-ttu-id="ab41c-113">A interface **IBackgroundCopyFile5** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ab41c-113">The **IBackgroundCopyFile5** interface has these methods.</span></span>



| <span data-ttu-id="ab41c-114">Método</span><span class="sxs-lookup"><span data-stu-id="ab41c-114">Method</span></span>                                                  | <span data-ttu-id="ab41c-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab41c-115">Description</span></span>                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="ab41c-116">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="ab41c-116">**GetProperty**</span></span>](ibackgroundcopyfile5-getproperty.md) | <span data-ttu-id="ab41c-117">Obtém o valor de uma propriedade BackgroundCopyFile genérica.</span><span class="sxs-lookup"><span data-stu-id="ab41c-117">Gets the value of a generic BackgroundCopyFile property.</span></span><br/> |
| [<span data-ttu-id="ab41c-118">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="ab41c-118">**SetProperty**</span></span>](ibackgroundcopyfile5-setproperty.md) | <span data-ttu-id="ab41c-119">Define o valor de uma propriedade BackgroundCopyFile genérica.</span><span class="sxs-lookup"><span data-stu-id="ab41c-119">Sets the value of a generic BackgroundCopyFile property.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ab41c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab41c-120">Requirements</span></span>



| <span data-ttu-id="ab41c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab41c-121">Requirement</span></span> | <span data-ttu-id="ab41c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ab41c-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab41c-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab41c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ab41c-124">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="ab41c-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ab41c-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab41c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ab41c-126">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="ab41c-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ab41c-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ab41c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab41c-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab41c-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="ab41c-129">INSERI</span><span class="sxs-lookup"><span data-stu-id="ab41c-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ab41c-130"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ab41c-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="ab41c-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ab41c-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="ab41c-132"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab41c-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="ab41c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ab41c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab41c-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab41c-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="ab41c-135">IID</span><span class="sxs-lookup"><span data-stu-id="ab41c-135">IID</span></span><br/>                      | <span data-ttu-id="ab41c-136">IID_IBackgroundCopyFile5 é definido como 85C1657F-DAFC-40E8-8834-DF18EA25717E</span><span class="sxs-lookup"><span data-stu-id="ab41c-136">IID_IBackgroundCopyFile5 is defined as 85C1657F-DAFC-40E8-8834-DF18EA25717E</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="ab41c-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab41c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab41c-138">**IBackgroundCopyFile**</span><span class="sxs-lookup"><span data-stu-id="ab41c-138">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="ab41c-139">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="ab41c-139">**IBackgroundCopyFile2**</span></span>](ibackgroundcopyfile2.md)
</dt> </dl>

 

