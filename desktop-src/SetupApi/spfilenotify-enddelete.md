---
description: A \_ notificação EndDelete do SPFILENOTIFY é retornada para a rotina de retorno de chamada quando uma fila conclui uma operação de exclusão. Essa notificação é enviada mesmo que o usuário cancele ou se ocorrer um erro.
ms.assetid: 78859854-8411-4c51-9c3c-628315cf1c41
title: Mensagem de SPFILENOTIFY_ENDDELETE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4ee4762dc33f8b8ec16a6be273cb42f41aeafce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755941"
---
# <a name="spfilenotify_enddelete-message"></a><span data-ttu-id="9eb85-104">SPFILENOTIFY mensagem de fim de \_ exclusão</span><span class="sxs-lookup"><span data-stu-id="9eb85-104">SPFILENOTIFY\_ENDDELETE message</span></span>

<span data-ttu-id="9eb85-105">A **notificação \_ EndDelete do SPFILENOTIFY** é retornada para a rotina de retorno de chamada quando uma fila conclui uma operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="9eb85-105">The **SPFILENOTIFY\_ENDDELETE** notification is returned to the callback routine when a queue completes a delete operation.</span></span> <span data-ttu-id="9eb85-106">Essa notificação é enviada mesmo que o usuário cancele ou se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="9eb85-106">This notification is sent even if the user cancels or if an error occurs.</span></span>


```C++
SPFILENOTIFY_ENDDELETE
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="9eb85-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9eb85-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eb85-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="9eb85-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="9eb85-109">Ponteiro para uma estrutura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="9eb85-109">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="9eb85-110">O membro **Win32Error** da estrutura **filePaths** indica o resultado de uma operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="9eb85-110">The **Win32Error** member of the **FILEPATHS** structure indicates the outcome of a copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="9eb85-111">*Param2*</span><span class="sxs-lookup"><span data-stu-id="9eb85-111">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="9eb85-112">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="9eb85-112">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eb85-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9eb85-113">Return value</span></span>

<span data-ttu-id="9eb85-114">O código de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="9eb85-114">The return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="9eb85-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9eb85-115">Requirements</span></span>



| <span data-ttu-id="9eb85-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9eb85-116">Requirement</span></span> | <span data-ttu-id="9eb85-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9eb85-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9eb85-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9eb85-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9eb85-119">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9eb85-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9eb85-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9eb85-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9eb85-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9eb85-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9eb85-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9eb85-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9eb85-123"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9eb85-123"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9eb85-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="9eb85-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eb85-125">Visão geral</span><span class="sxs-lookup"><span data-stu-id="9eb85-125">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="9eb85-126">Notificações</span><span class="sxs-lookup"><span data-stu-id="9eb85-126">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="9eb85-127">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="9eb85-127">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="9eb85-128">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="9eb85-128">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="9eb85-129">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="9eb85-129">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




