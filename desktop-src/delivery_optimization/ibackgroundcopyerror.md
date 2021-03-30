---
title: Interface IBackgroundCopyError (Deliveryoptimization. h)
description: Use a interface IBackgroundCopyError para determinar a causa de um erro e se o processo de transferência pode continuar.
ms.assetid: 7DCB63CF-4180-4DC3-9093-07C4F8CF7A8E
keywords:
- Interface IBackgroundCopyError
- Interface IBackgroundCopyError, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f35365d56ce9391a746e479e1b59034342ebf62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455031"
---
# <a name="ibackgroundcopyerror-interface"></a><span data-ttu-id="a935b-105">Interface IBackgroundCopyError</span><span class="sxs-lookup"><span data-stu-id="a935b-105">IBackgroundCopyError interface</span></span>

<span data-ttu-id="a935b-106">Use a interface **IBackgroundCopyError** para determinar a causa de um erro e se o processo de transferência pode continuar.</span><span class="sxs-lookup"><span data-stu-id="a935b-106">Use the **IBackgroundCopyError** interface to determine the cause of an error and if the transfer process can proceed.</span></span>

<span data-ttu-id="a935b-107">O cria um objeto de erro somente quando o estado do trabalho é BG_JOB_STATE_ERROR ou BG_JOB_STATE_TRANSIENT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="a935b-107">DO creates an error object only when the state of the job is BG_JOB_STATE_ERROR or BG_JOB_STATE_TRANSIENT_ERROR.</span></span> <span data-ttu-id="a935b-108">Não cria um objeto de erro quando um método de interface **IBackgroundCopyXXXX** falha.</span><span class="sxs-lookup"><span data-stu-id="a935b-108">DO does not create an error object when an **IBackgroundCopyXXXX** interface method fails.</span></span> <span data-ttu-id="a935b-109">O objeto de erro estará disponível até que o comece a transferir dados (o estado do trabalho é alterado para BG_JOB_STATE_TRANSFERRING) para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="a935b-109">The error object is available until DO begins transferring data (the state of the job changes to BG_JOB_STATE_TRANSFERRING) for the job.</span></span>

<span data-ttu-id="a935b-110">Para obter um objeto **IBackgroundCopyError** , chame o método [**método ibackgroundcopyjob:: GetError**](ibackgroundcopyjob-geterror.md) .</span><span class="sxs-lookup"><span data-stu-id="a935b-110">To get an **IBackgroundCopyError** object, call the [**IBackgroundCopyJob::GetError**](ibackgroundcopyjob-geterror.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="a935b-111">Membros</span><span class="sxs-lookup"><span data-stu-id="a935b-111">Members</span></span>

<span data-ttu-id="a935b-112">A interface **IBackgroundCopyError** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a935b-112">The **IBackgroundCopyError** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a935b-113">**IBackgroundCopyError** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a935b-113">**IBackgroundCopyError** also has these types of members:</span></span>

-   [<span data-ttu-id="a935b-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="a935b-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a935b-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="a935b-115">Methods</span></span>

<span data-ttu-id="a935b-116">A interface **IBackgroundCopyError** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="a935b-116">The **IBackgroundCopyError** interface has these methods.</span></span>



| <span data-ttu-id="a935b-117">Método</span><span class="sxs-lookup"><span data-stu-id="a935b-117">Method</span></span>                                                   | <span data-ttu-id="a935b-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="a935b-118">Description</span></span>                                                                                 |
|:---------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a935b-119">**GetError**</span><span class="sxs-lookup"><span data-stu-id="a935b-119">**GetError**</span></span>](ibackgroundcopyerror-geterror-method.md) | <span data-ttu-id="a935b-120">Recupera o código de erro e identifica o contexto no qual ocorreu o erro.</span><span class="sxs-lookup"><span data-stu-id="a935b-120">Retrieves the error code and identifies the context in which the error occurred.</span></span><br/> |
| [<span data-ttu-id="a935b-121">**GetFile**</span><span class="sxs-lookup"><span data-stu-id="a935b-121">**GetFile**</span></span>](ibackgroundcopyerror-getfile-method.md)   | <span data-ttu-id="a935b-122">Recupera um ponteiro de interface para o objeto de arquivo associado ao erro.</span><span class="sxs-lookup"><span data-stu-id="a935b-122">Retrieves an interface pointer to the file object associated with the error.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="a935b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a935b-123">Requirements</span></span>



| <span data-ttu-id="a935b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a935b-124">Requirement</span></span> | <span data-ttu-id="a935b-125">Valor</span><span class="sxs-lookup"><span data-stu-id="a935b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a935b-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a935b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a935b-127">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="a935b-127">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a935b-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a935b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a935b-129">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="a935b-129">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a935b-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a935b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a935b-131"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="a935b-131"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="a935b-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="a935b-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a935b-133"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a935b-133"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="a935b-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a935b-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="a935b-135"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a935b-135"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="a935b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a935b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a935b-137"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a935b-137"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="a935b-138">IID</span><span class="sxs-lookup"><span data-stu-id="a935b-138">IID</span></span><br/>                      | <span data-ttu-id="a935b-139">IID_IBackgroundCopyError é definido como 19C613A0-FCB8-4F28-81AE-897C3D078F81</span><span class="sxs-lookup"><span data-stu-id="a935b-139">IID_IBackgroundCopyError is defined as 19C613A0-FCB8-4F28-81AE-897C3D078F81</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="a935b-140">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a935b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a935b-141">**BG_JOB_STATE**</span><span class="sxs-lookup"><span data-stu-id="a935b-141">**BG_JOB_STATE**</span></span>](bg-job-state-.md)
</dt> <dt>

[<span data-ttu-id="a935b-142">**Método ibackgroundcopyjob:: GetError**</span><span class="sxs-lookup"><span data-stu-id="a935b-142">**IBackgroundCopyJob::GetError**</span></span>](ibackgroundcopyjob-geterror.md)
</dt> <dt>

[<span data-ttu-id="a935b-143">**Método ibackgroundcopyjob:: GetState**</span><span class="sxs-lookup"><span data-stu-id="a935b-143">**IBackgroundCopyJob::GetState**</span></span>](ibackgroundcopyjob-getstate.md)
</dt> <dt>

[<span data-ttu-id="a935b-144">**IBackgroundCopyCallback::JobError**</span><span class="sxs-lookup"><span data-stu-id="a935b-144">**IBackgroundCopyCallback::JobError**</span></span>](ibackgroundcopycallback-joberror-method.md)
</dt> </dl>

 

