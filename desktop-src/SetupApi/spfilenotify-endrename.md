---
description: A \_ notificação rerename do SPFILENOTIFY é enviada para a rotina de retorno de chamada quando a fila conclui uma operação de renomeação. Essa notificação é enviada mesmo que o usuário cancele ou se ocorrer um erro.
ms.assetid: 8d5a8d17-de4f-4100-aa72-dfefeb8d4db9
title: Mensagem de SPFILENOTIFY_ENDRENAME (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a316d4dfe72ee9eb7d85fdb70eb90e1cf3d3f463
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755782"
---
# <a name="spfilenotify_endrename-message"></a><span data-ttu-id="47351-104">SPFILENOTIFY \_ renomear mensagem</span><span class="sxs-lookup"><span data-stu-id="47351-104">SPFILENOTIFY\_ENDRENAME message</span></span>

<span data-ttu-id="47351-105">A **notificação \_ rerename do SPFILENOTIFY** é enviada para a rotina de retorno de chamada quando a fila conclui uma operação de renomeação.</span><span class="sxs-lookup"><span data-stu-id="47351-105">The **SPFILENOTIFY\_ENDRENAME** notification is sent to the callback routine when the queue completes a rename operation.</span></span> <span data-ttu-id="47351-106">Essa notificação é enviada mesmo que o usuário cancele ou se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="47351-106">This notification is sent even if the user cancels or if an error occurs.</span></span>


```C++
SPFILENOTIFY_ENDRENAME
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="47351-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47351-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47351-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="47351-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="47351-109">Ponteiro para uma estrutura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="47351-109">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="47351-110">O membro **Win32Error** da estrutura **filePaths** indica o resultado da operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="47351-110">The **Win32Error** member of the **FILEPATHS** structure indicates the outcome of the copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="47351-111">*Param2*</span><span class="sxs-lookup"><span data-stu-id="47351-111">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="47351-112">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="47351-112">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47351-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="47351-113">Return value</span></span>

<span data-ttu-id="47351-114">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="47351-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="47351-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47351-115">Requirements</span></span>



| <span data-ttu-id="47351-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="47351-116">Requirement</span></span> | <span data-ttu-id="47351-117">Valor</span><span class="sxs-lookup"><span data-stu-id="47351-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="47351-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47351-118">Minimum supported client</span></span><br/> | <span data-ttu-id="47351-119">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="47351-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="47351-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47351-120">Minimum supported server</span></span><br/> | <span data-ttu-id="47351-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="47351-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="47351-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="47351-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="47351-123"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="47351-123"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47351-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="47351-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47351-125">Visão geral</span><span class="sxs-lookup"><span data-stu-id="47351-125">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="47351-126">Notificações</span><span class="sxs-lookup"><span data-stu-id="47351-126">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="47351-127">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="47351-127">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="47351-128">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="47351-128">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="47351-129">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="47351-129">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




