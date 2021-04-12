---
title: Enumeração de BG_JOB_TYPE (Deliveryoptimization. h)
description: A enumeração BG_JOB_TYPE define valores constantes que especificam o tipo de trabalho de transferência, como download.
ms.assetid: 696A43C3-1FA2-436D-B34A-3544E7C9A66A
keywords:
- Enumeração de BG_JOB_TYPE
topic_type:
- apiref
api_name:
- BG_JOB_TYPE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1f672bcf2d2538bfaa9b9573fa1dfa71ee7b9cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454965"
---
# <a name="bg_job_type-enumeration"></a><span data-ttu-id="ead2d-104">Enumeração de BG_JOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="ead2d-104">BG_JOB_TYPE enumeration</span></span>

<span data-ttu-id="ead2d-105">A enumeração **BG_JOB_TYPE** define valores constantes que especificam o tipo de trabalho de transferência, como download.</span><span class="sxs-lookup"><span data-stu-id="ead2d-105">The **BG_JOB_TYPE** enumeration defines constant values that specify the type of transfer job, such as download.</span></span>

## <a name="syntax"></a><span data-ttu-id="ead2d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ead2d-106">Syntax</span></span>


```C++
typedef enum  { 
  BG_JOB_TYPE_DOWNLOAD
} BG_JOB_TYPE;
```



## <a name="constants"></a><span data-ttu-id="ead2d-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="ead2d-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ead2d-108"><span id="BG_JOB_TYPE_DOWNLOAD"></span><span id="bg_job_type_download"></span>**BG_JOB_TYPE_DOWNLOAD**</span><span class="sxs-lookup"><span data-stu-id="ead2d-108"><span id="BG_JOB_TYPE_DOWNLOAD"></span><span id="bg_job_type_download"></span>**BG_JOB_TYPE_DOWNLOAD**</span></span>
</dt> <dd>

<span data-ttu-id="ead2d-109">Especifica que o trabalho baixa arquivos para o cliente.</span><span class="sxs-lookup"><span data-stu-id="ead2d-109">Specifies that the job downloads files to the client.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ead2d-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ead2d-110">Requirements</span></span>



| <span data-ttu-id="ead2d-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="ead2d-111">Requirement</span></span> | <span data-ttu-id="ead2d-112">Valor</span><span class="sxs-lookup"><span data-stu-id="ead2d-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ead2d-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ead2d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="ead2d-114">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="ead2d-114">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ead2d-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ead2d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="ead2d-116">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="ead2d-116">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ead2d-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ead2d-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="ead2d-118"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="ead2d-118"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ead2d-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="ead2d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ead2d-120">**Método ibackgroundcopyjob:: GetType**</span><span class="sxs-lookup"><span data-stu-id="ead2d-120">**IBackgroundCopyJob::GetType**</span></span>](ibackgroundcopyjob-gettype.md)
</dt> <dt>

[<span data-ttu-id="ead2d-121">**IBackgroundCopyManager:: CreateJob**</span><span class="sxs-lookup"><span data-stu-id="ead2d-121">**IBackgroundCopyManager::CreateJob**</span></span>](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





