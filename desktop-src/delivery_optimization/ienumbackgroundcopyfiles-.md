---
title: Interface IEnumBackgroundCopyFiles (Deliveryoptimization. h)
description: Use a interface IEnumBackgroundCopyFiles para enumerar os arquivos que um trabalho contém. Para obter um ponteiro de interface IEnumBackgroundCopyFiles, chame o método método ibackgroundcopyjob EnumFiles.
ms.assetid: 539973BA-2756-4163-9D8B-4B7C0A708A8D
keywords:
- Interface IEnumBackgroundCopyFiles
- Interface IEnumBackgroundCopyFiles, descrita
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e46e94139a0c82e6c5b45f9397d76de8b4fdb43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105772522"
---
# <a name="ienumbackgroundcopyfiles-interface"></a><span data-ttu-id="23fb9-106">Interface IEnumBackgroundCopyFiles</span><span class="sxs-lookup"><span data-stu-id="23fb9-106">IEnumBackgroundCopyFiles interface</span></span>

<span data-ttu-id="23fb9-107">Use a interface **IEnumBackgroundCopyFiles** para enumerar os arquivos que um trabalho contém.</span><span class="sxs-lookup"><span data-stu-id="23fb9-107">Use the **IEnumBackgroundCopyFiles** interface to enumerate the files that a job contains.</span></span> <span data-ttu-id="23fb9-108">Para obter um ponteiro de interface **IEnumBackgroundCopyFiles** , chame o método [**método ibackgroundcopyjob:: EnumFiles**](ibackgroundcopyjob-enumfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="23fb9-108">To get an **IEnumBackgroundCopyFiles** interface pointer, call the [**IBackgroundCopyJob::EnumFiles**](ibackgroundcopyjob-enumfiles.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="23fb9-109">Membros</span><span class="sxs-lookup"><span data-stu-id="23fb9-109">Members</span></span>

<span data-ttu-id="23fb9-110">A interface **IEnumBackgroundCopyFiles** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="23fb9-110">The **IEnumBackgroundCopyFiles** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="23fb9-111">**IEnumBackgroundCopyFiles** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="23fb9-111">**IEnumBackgroundCopyFiles** also has these types of members:</span></span>

-   [<span data-ttu-id="23fb9-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="23fb9-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="23fb9-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="23fb9-113">Methods</span></span>

<span data-ttu-id="23fb9-114">A interface **IEnumBackgroundCopyFiles** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="23fb9-114">The **IEnumBackgroundCopyFiles** interface has these methods.</span></span>



| <span data-ttu-id="23fb9-115">Método</span><span class="sxs-lookup"><span data-stu-id="23fb9-115">Method</span></span>                                                | <span data-ttu-id="23fb9-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="23fb9-116">Description</span></span>                                                                   |
|:------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="23fb9-117">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="23fb9-117">**GetCount**</span></span>](ienumbackgroundcopyfiles-getcount.md) | <span data-ttu-id="23fb9-118">Recupera o número de itens na enumeração.</span><span class="sxs-lookup"><span data-stu-id="23fb9-118">Retrieves the number of items in the enumeration.</span></span><br/>                  |
| [<span data-ttu-id="23fb9-119">**Avançar**</span><span class="sxs-lookup"><span data-stu-id="23fb9-119">**Next**</span></span>](ienumbackgroundcopyfiles-next.md)         | <span data-ttu-id="23fb9-120">Recupera um número especificado de itens na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="23fb9-120">Retrieves a specified number of items in the enumeration sequence.</span></span><br/> |
| [<span data-ttu-id="23fb9-121">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="23fb9-121">**Reset**</span></span>](ienumbackgroundcopyfiles-reset.md)       | <span data-ttu-id="23fb9-122">Redefine a sequência de enumeração para o início.</span><span class="sxs-lookup"><span data-stu-id="23fb9-122">Resets the enumeration sequence to the beginning.</span></span><br/>                  |
| [<span data-ttu-id="23fb9-123">**Ignorar**</span><span class="sxs-lookup"><span data-stu-id="23fb9-123">**Skip**</span></span>](ienumbackgroundcopyfiles-skip.md)         | <span data-ttu-id="23fb9-124">Ignora um número especificado de itens na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="23fb9-124">Skips a specified number of items in the enumeration sequence.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="23fb9-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23fb9-125">Requirements</span></span>



| <span data-ttu-id="23fb9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="23fb9-126">Requirement</span></span> | <span data-ttu-id="23fb9-127">Valor</span><span class="sxs-lookup"><span data-stu-id="23fb9-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23fb9-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23fb9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="23fb9-129">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="23fb9-129">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="23fb9-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23fb9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="23fb9-131">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="23fb9-131">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="23fb9-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="23fb9-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="23fb9-133"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="23fb9-133"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="23fb9-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="23fb9-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="23fb9-135"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="23fb9-135"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="23fb9-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="23fb9-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="23fb9-137"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23fb9-137"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="23fb9-138">DLL</span><span class="sxs-lookup"><span data-stu-id="23fb9-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23fb9-139"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23fb9-139"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="23fb9-140">IID</span><span class="sxs-lookup"><span data-stu-id="23fb9-140">IID</span></span><br/>                      | <span data-ttu-id="23fb9-141">IID_IEnumBackgroundCopyFiles é definido como CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="23fb9-141">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="23fb9-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="23fb9-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23fb9-143">**Método ibackgroundcopyjob:: EnumFiles**</span><span class="sxs-lookup"><span data-stu-id="23fb9-143">**IBackgroundCopyJob::EnumFiles**</span></span>](ibackgroundcopyjob-enumfiles.md)
</dt> </dl>

 

