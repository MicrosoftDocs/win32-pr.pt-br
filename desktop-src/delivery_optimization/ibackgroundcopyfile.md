---
title: Interface IBackgroundCopyFile (Deliveryoptimization. h)
description: IBackgroundCopyFile contém informações sobre um arquivo que faz parte de um trabalho. Por exemplo, você pode usar métodos IBackgroundCopyFile para recuperar os nomes locais e remotos do arquivo e transferir as informações de progresso.
ms.assetid: 463ED61A-D7C5-4B44-97CF-FDAA138CE9E3
keywords:
- Interface IBackgroundCopyFile
- Interface IBackgroundCopyFile, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e4a54a66dee87770326d2456cb384e9d77f15e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761524"
---
# <a name="ibackgroundcopyfile-interface"></a><span data-ttu-id="fc3e2-106">Interface IBackgroundCopyFile</span><span class="sxs-lookup"><span data-stu-id="fc3e2-106">IBackgroundCopyFile interface</span></span>

<span data-ttu-id="fc3e2-107">**IBackgroundCopyFile** contém informações sobre um arquivo que faz parte de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="fc3e2-107">**IBackgroundCopyFile** contains information about a file that is part of a job.</span></span> <span data-ttu-id="fc3e2-108">Por exemplo, você pode usar métodos **IBackgroundCopyFile** para recuperar os nomes locais e remotos do arquivo e transferir as informações de progresso.</span><span class="sxs-lookup"><span data-stu-id="fc3e2-108">For example, you can use **IBackgroundCopyFile** methods to retrieve the local and remote names of the file and transfer progress information.</span></span>

<span data-ttu-id="fc3e2-109">Para obter um ponteiro de interface **IBackgroundCopyFile** , chame o método [**IBackgroundCopyError:: GetFile**](ibackgroundcopyerror-getfile-method.md) ou o método [**IEnumBackgroundCopyFiles:: Next**](ienumbackgroundcopyfiles-next.md) .</span><span class="sxs-lookup"><span data-stu-id="fc3e2-109">To get an **IBackgroundCopyFile** interface pointer, call the [**IBackgroundCopyError::GetFile**](ibackgroundcopyerror-getfile-method.md) method or the [**IEnumBackgroundCopyFiles::Next**](ienumbackgroundcopyfiles-next.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="fc3e2-110">Membros</span><span class="sxs-lookup"><span data-stu-id="fc3e2-110">Members</span></span>

<span data-ttu-id="fc3e2-111">A interface **IBackgroundCopyFile** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="fc3e2-111">The **IBackgroundCopyFile** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fc3e2-112">**IBackgroundCopyFile** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fc3e2-112">**IBackgroundCopyFile** also has these types of members:</span></span>

-   [<span data-ttu-id="fc3e2-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="fc3e2-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fc3e2-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="fc3e2-114">Methods</span></span>

<span data-ttu-id="fc3e2-115">A interface **IBackgroundCopyFile** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="fc3e2-115">The **IBackgroundCopyFile** interface has these methods.</span></span>



| <span data-ttu-id="fc3e2-116">Método</span><span class="sxs-lookup"><span data-stu-id="fc3e2-116">Method</span></span>                                                            | <span data-ttu-id="fc3e2-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc3e2-117">Description</span></span>                                             |
|:------------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="fc3e2-118">**Getlocalname**</span><span class="sxs-lookup"><span data-stu-id="fc3e2-118">**GetLocalName**</span></span>](ibackgroundcopyfile-getlocalname-method.md)   | <span data-ttu-id="fc3e2-119">Recupera o nome local do arquivo.</span><span class="sxs-lookup"><span data-stu-id="fc3e2-119">Retrieves the local name of the file.</span></span><br/>        |
| [<span data-ttu-id="fc3e2-120">**GetProgress**</span><span class="sxs-lookup"><span data-stu-id="fc3e2-120">**GetProgress**</span></span>](ibackgroundcopyfile-getprogress-method.md)     | <span data-ttu-id="fc3e2-121">Recupera o progresso da transferência de arquivo.</span><span class="sxs-lookup"><span data-stu-id="fc3e2-121">Retrieves the progress of the file transfer.</span></span><br/> |
| [<span data-ttu-id="fc3e2-122">**Getremotename**</span><span class="sxs-lookup"><span data-stu-id="fc3e2-122">**GetRemoteName**</span></span>](ibackgroundcopyfile-getremotename-method.md) | <span data-ttu-id="fc3e2-123">Recupera o nome remoto do arquivo.</span><span class="sxs-lookup"><span data-stu-id="fc3e2-123">Retrieves the remote name of the file.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="fc3e2-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc3e2-124">Requirements</span></span>



| <span data-ttu-id="fc3e2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc3e2-125">Requirement</span></span> | <span data-ttu-id="fc3e2-126">Valor</span><span class="sxs-lookup"><span data-stu-id="fc3e2-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc3e2-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc3e2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fc3e2-128">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="fc3e2-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fc3e2-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc3e2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fc3e2-130">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="fc3e2-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="fc3e2-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fc3e2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc3e2-132"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc3e2-132"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="fc3e2-133">INSERI</span><span class="sxs-lookup"><span data-stu-id="fc3e2-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fc3e2-134"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fc3e2-134"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="fc3e2-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fc3e2-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="fc3e2-136"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc3e2-136"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="fc3e2-137">DLL</span><span class="sxs-lookup"><span data-stu-id="fc3e2-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc3e2-138"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc3e2-138"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="fc3e2-139">IID</span><span class="sxs-lookup"><span data-stu-id="fc3e2-139">IID</span></span><br/>                      | <span data-ttu-id="fc3e2-140">IID_IBackgroundCopyFile é definido como 01B7BD23-FB88-4A77-8490-5891D3E4653A</span><span class="sxs-lookup"><span data-stu-id="fc3e2-140">IID_IBackgroundCopyFile is defined as 01B7BD23-FB88-4A77-8490-5891D3E4653A</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="fc3e2-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc3e2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc3e2-142">**IBackgroundCopyError**</span><span class="sxs-lookup"><span data-stu-id="fc3e2-142">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="fc3e2-143">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="fc3e2-143">**IBackgroundCopyFile2**</span></span>](ibackgroundcopyfile2.md)
</dt> <dt>

[<span data-ttu-id="fc3e2-144">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="fc3e2-144">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="fc3e2-145">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="fc3e2-145">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

