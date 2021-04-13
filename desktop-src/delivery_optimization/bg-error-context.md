---
title: Enumeração de BG_ERROR_CONTEXT (Deliveryoptimization. h)
description: A enumeração BG_ERROR_CONTEXT define os valores constantes que especificam o contexto no qual o erro ocorreu.
ms.assetid: 86202343-5B5B-4A2E-A58D-7634BCB41E1C
keywords:
- Enumeração de BG_ERROR_CONTEXT
topic_type:
- apiref
api_name:
- BG_ERROR_CONTEXT
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf6c68c20a5117e6cd8a02f8b4608b494c0ea93f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454966"
---
# <a name="bg_error_context-enumeration"></a><span data-ttu-id="fbb98-104">Enumeração de BG_ERROR_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="fbb98-104">BG_ERROR_CONTEXT enumeration</span></span>

<span data-ttu-id="fbb98-105">A enumeração **BG_ERROR_CONTEXT** define os valores constantes que especificam o contexto no qual o erro ocorreu.</span><span class="sxs-lookup"><span data-stu-id="fbb98-105">The **BG_ERROR_CONTEXT** enumeration defines the constant values that specify the context in which the error occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbb98-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbb98-106">Syntax</span></span>


```C++
typedef enum  { 
  BG_ERROR_CONTEXT_NONE                        = 0,
  BG_ERROR_CONTEXT_UNKNOWN                     = 1,
  BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER       = 2,
  BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION  = 3,
  BG_ERROR_CONTEXT_LOCAL_FILE                  = 4,
  BG_ERROR_CONTEXT_REMOTE_FILE                 = 5,
  BG_ERROR_CONTEXT_GENERAL_TRANSPORT           = 6,
  BG_ERROR_CONTEXT_REMOTE_APPLICATION          = 7
} BG_ERROR_CONTEXT;
```



## <a name="constants"></a><span data-ttu-id="fbb98-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="fbb98-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fbb98-108"><span id="BG_ERROR_CONTEXT_NONE"></span><span id="bg_error_context_none"></span>**BG_ERROR_CONTEXT_NONE**</span><span class="sxs-lookup"><span data-stu-id="fbb98-108"><span id="BG_ERROR_CONTEXT_NONE"></span><span id="bg_error_context_none"></span>**BG_ERROR_CONTEXT_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="fbb98-109">Não ocorreu um erro.</span><span class="sxs-lookup"><span data-stu-id="fbb98-109">An error has not occurred.</span></span>

</dd> <dt>

<span data-ttu-id="fbb98-110"><span id="BG_ERROR_CONTEXT_UNKNOWN"></span><span id="bg_error_context_unknown"></span>**BG_ERROR_CONTEXT_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="fbb98-110"><span id="BG_ERROR_CONTEXT_UNKNOWN"></span><span id="bg_error_context_unknown"></span>**BG_ERROR_CONTEXT_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="fbb98-111">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="fbb98-111">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="fbb98-112"><span id="BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER"></span><span id="bg_error_context_general_queue_manager"></span>**BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER**</span><span class="sxs-lookup"><span data-stu-id="fbb98-112"><span id="BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER"></span><span id="bg_error_context_general_queue_manager"></span>**BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER**</span></span>
</dt> <dd>

<span data-ttu-id="fbb98-113">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="fbb98-113">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="fbb98-114"><span id="BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION"></span><span id="bg_error_context_queue_manager_notification"></span>**BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="fbb98-114"><span id="BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION"></span><span id="bg_error_context_queue_manager_notification"></span>**BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION**</span></span>
</dt> <dd>

<span data-ttu-id="fbb98-115">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="fbb98-115">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="fbb98-116"><span id="BG_ERROR_CONTEXT_LOCAL_FILE"></span><span id="bg_error_context_local_file"></span>**BG_ERROR_CONTEXT_LOCAL_FILE**</span><span class="sxs-lookup"><span data-stu-id="fbb98-116"><span id="BG_ERROR_CONTEXT_LOCAL_FILE"></span><span id="bg_error_context_local_file"></span>**BG_ERROR_CONTEXT_LOCAL_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="fbb98-117">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="fbb98-117">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="fbb98-118"><span id="BG_ERROR_CONTEXT_REMOTE_FILE"></span><span id="bg_error_context_remote_file"></span>**BG_ERROR_CONTEXT_REMOTE_FILE**</span><span class="sxs-lookup"><span data-stu-id="fbb98-118"><span id="BG_ERROR_CONTEXT_REMOTE_FILE"></span><span id="bg_error_context_remote_file"></span>**BG_ERROR_CONTEXT_REMOTE_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="fbb98-119">O erro estava relacionado ao arquivo remoto especificado.</span><span class="sxs-lookup"><span data-stu-id="fbb98-119">The error was related to the specified remote file.</span></span> <span data-ttu-id="fbb98-120">Por exemplo, a URL não estava acessível.</span><span class="sxs-lookup"><span data-stu-id="fbb98-120">For example, the URL was not accessible.</span></span>

</dd> <dt>

<span data-ttu-id="fbb98-121"><span id="BG_ERROR_CONTEXT_GENERAL_TRANSPORT"></span><span id="bg_error_context_general_transport"></span>**BG_ERROR_CONTEXT_GENERAL_TRANSPORT**</span><span class="sxs-lookup"><span data-stu-id="fbb98-121"><span id="BG_ERROR_CONTEXT_GENERAL_TRANSPORT"></span><span id="bg_error_context_general_transport"></span>**BG_ERROR_CONTEXT_GENERAL_TRANSPORT**</span></span>
</dt> <dd>

<span data-ttu-id="fbb98-122">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="fbb98-122">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="fbb98-123"><span id="BG_ERROR_CONTEXT_REMOTE_APPLICATION"></span><span id="bg_error_context_remote_application"></span>**BG_ERROR_CONTEXT_REMOTE_APPLICATION**</span><span class="sxs-lookup"><span data-stu-id="fbb98-123"><span id="BG_ERROR_CONTEXT_REMOTE_APPLICATION"></span><span id="bg_error_context_remote_application"></span>**BG_ERROR_CONTEXT_REMOTE_APPLICATION**</span></span>
</dt> <dd>

<span data-ttu-id="fbb98-124">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="fbb98-124">Not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fbb98-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbb98-125">Requirements</span></span>



| <span data-ttu-id="fbb98-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbb98-126">Requirement</span></span> | <span data-ttu-id="fbb98-127">Valor</span><span class="sxs-lookup"><span data-stu-id="fbb98-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbb98-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbb98-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fbb98-129">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="fbb98-129">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fbb98-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbb98-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fbb98-131">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="fbb98-131">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fbb98-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fbb98-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbb98-133"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbb98-133"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbb98-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="fbb98-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbb98-135">**IBackgroundCopyError:: GetError**</span><span class="sxs-lookup"><span data-stu-id="fbb98-135">**IBackgroundCopyError::GetError**</span></span>](ibackgroundcopyerror-geterror-method.md)
</dt> </dl>

 

 





