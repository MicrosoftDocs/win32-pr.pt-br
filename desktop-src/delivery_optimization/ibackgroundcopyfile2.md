---
title: Interface IBackgroundCopyFile2 (Deliveryoptimization. h)
description: Use a interface IBackgroundCopyFile2 para especificar um novo nome remoto para o arquivo e recuperar a lista de intervalos a serem baixados.
ms.assetid: 28233310-9F2A-4567-B0B1-B549F862F3C8
keywords:
- Interface IBackgroundCopyFile2
- Interface IBackgroundCopyFile2, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a866c8f18ee1dfb57f32ac3b2b9999e10106522
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009280"
---
# <a name="ibackgroundcopyfile2-interface"></a><span data-ttu-id="c7dc4-105">Interface IBackgroundCopyFile2</span><span class="sxs-lookup"><span data-stu-id="c7dc4-105">IBackgroundCopyFile2 interface</span></span>

<span data-ttu-id="c7dc4-106">Use a interface **IBackgroundCopyFile2** para especificar um novo nome remoto para o arquivo e recuperar a lista de intervalos a serem baixados.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-106">Use the **IBackgroundCopyFile2** interface to specify a new remote name for the file and retrieve the list of ranges to download.</span></span>

<span data-ttu-id="c7dc4-107">A interface **IBackgroundCopyFile2** herda da interface [**IBackgroundCopyFile**](ibackgroundcopyfile.md) .</span><span class="sxs-lookup"><span data-stu-id="c7dc4-107">The **IBackgroundCopyFile2** interface inherits from the [**IBackgroundCopyFile**](ibackgroundcopyfile.md) interface.</span></span>

<span data-ttu-id="c7dc4-108">Para obter um ponteiro de interface **IBackgroundCopyFile2** , chame o método **IBackgroundCopyFile:: QueryInterface** usando __uuidof (IBackgroundCopyFile2) para o identificador de interface.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-108">To get an **IBackgroundCopyFile2** interface pointer, call the **IBackgroundCopyFile::QueryInterface** method using __uuidof(IBackgroundCopyFile2) for the interface identifier.</span></span> <span data-ttu-id="c7dc4-109">Use o ponteiro de interface **IBackgroundCopyFile2** para chamar os métodos [**IBackgroundCopyFile**](ibackgroundcopyfile.md) e **IBackgroundCopyFile2** .</span><span class="sxs-lookup"><span data-stu-id="c7dc4-109">Use the **IBackgroundCopyFile2** interface pointer to call both the [**IBackgroundCopyFile**](ibackgroundcopyfile.md) and **IBackgroundCopyFile2** methods.</span></span>

## <a name="members"></a><span data-ttu-id="c7dc4-110">Membros</span><span class="sxs-lookup"><span data-stu-id="c7dc4-110">Members</span></span>

<span data-ttu-id="c7dc4-111">A interface **IBackgroundCopyFile2** herda de [**IBackgroundCopyFile**](ibackgroundcopyfile.md).</span><span class="sxs-lookup"><span data-stu-id="c7dc4-111">The **IBackgroundCopyFile2** interface inherits from [**IBackgroundCopyFile**](ibackgroundcopyfile.md).</span></span> <span data-ttu-id="c7dc4-112">**IBackgroundCopyFile2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c7dc4-112">**IBackgroundCopyFile2** also has these types of members:</span></span>

-   [<span data-ttu-id="c7dc4-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="c7dc4-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c7dc4-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="c7dc4-114">Methods</span></span>

<span data-ttu-id="c7dc4-115">A interface **IBackgroundCopyFile2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-115">The **IBackgroundCopyFile2** interface has these methods.</span></span>



| <span data-ttu-id="c7dc4-116">Método</span><span class="sxs-lookup"><span data-stu-id="c7dc4-116">Method</span></span>                                                             | <span data-ttu-id="c7dc4-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="c7dc4-117">Description</span></span>                                                                      |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="c7dc4-118">**GetFileRanges**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-118">**GetFileRanges**</span></span>](ibackgroundcopyfile2-getfileranges-method.md) | <span data-ttu-id="c7dc4-119">Recupera a matriz de intervalos que você deseja baixar da URL.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-119">Retrieves the array of ranges that you want to download from the URL.</span></span><br/> |
| [<span data-ttu-id="c7dc4-120">**Setremotename**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-120">**SetRemoteName**</span></span>](ibackgroundcopyfile2-setremotename-method.md) | <span data-ttu-id="c7dc4-121">Altera o nome remoto para uma nova URL.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-121">Changes the remote name to a new URL.</span></span><br/>                                 |



 

## <a name="requirements"></a><span data-ttu-id="c7dc4-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7dc4-122">Requirements</span></span>



| <span data-ttu-id="c7dc4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7dc4-123">Requirement</span></span> | <span data-ttu-id="c7dc4-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c7dc4-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7dc4-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7dc4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c7dc4-126">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="c7dc4-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c7dc4-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7dc4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c7dc4-128">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="c7dc4-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c7dc4-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c7dc4-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7dc4-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7dc4-130"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="c7dc4-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="c7dc4-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c7dc4-132"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c7dc4-132"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="c7dc4-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c7dc4-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="c7dc4-134"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7dc4-134"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="c7dc4-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c7dc4-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7dc4-136"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7dc4-136"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="c7dc4-137">IID</span><span class="sxs-lookup"><span data-stu-id="c7dc4-137">IID</span></span><br/>                      | <span data-ttu-id="c7dc4-138">IID_IBackgroundCopyFile2 é definido como 83E81B93-0873-474D-8A8C-F2018B1A939C</span><span class="sxs-lookup"><span data-stu-id="c7dc4-138">IID_IBackgroundCopyFile2 is defined as 83E81B93-0873-474D-8A8C-F2018B1A939C</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="c7dc4-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7dc4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7dc4-140">**IBackgroundCopyFile**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-140">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> </dl>

 

 





