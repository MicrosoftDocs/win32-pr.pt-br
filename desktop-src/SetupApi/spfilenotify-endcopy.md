---
description: A \_ notificação EndCopy do SPFILENOTIFY é passada para a função de retorno de chamada quando a fila conclui uma operação de cópia. Essa notificação é enviada mesmo que o usuário cancele ou se ocorrer um erro.
ms.assetid: d58dc397-8803-466c-9069-728faf2c2030
title: Mensagem de SPFILENOTIFY_ENDCOPY (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75dba56c4a38ac87003a3b59b594135e55a462f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756363"
---
# <a name="spfilenotify_endcopy-message"></a><span data-ttu-id="b1023-104">\_Mensagem de ENDcopy do SPFILENOTIFY</span><span class="sxs-lookup"><span data-stu-id="b1023-104">SPFILENOTIFY\_ENDCOPY message</span></span>

<span data-ttu-id="b1023-105">A **notificação \_ EndCopy do SPFILENOTIFY** é passada para a função de retorno de chamada quando a fila conclui uma operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="b1023-105">The **SPFILENOTIFY\_ENDCOPY** notification is passed to the callback function when the queue completes a copy operation.</span></span> <span data-ttu-id="b1023-106">Essa notificação é enviada mesmo que o usuário cancele ou se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="b1023-106">This notification is sent even if the user cancels or if an error occurs.</span></span>


```C++
SPFILENOTIFY_ENDCOPY
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="b1023-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1023-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1023-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="b1023-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="b1023-109">Ponteiro para uma estrutura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="b1023-109">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="b1023-110">O membro **Win32Error** da estrutura **filePaths** indica o resultado da operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="b1023-110">The **Win32Error** member of the **FILEPATHS** structure indicates the outcome of the copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="b1023-111">*Param2*</span><span class="sxs-lookup"><span data-stu-id="b1023-111">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="b1023-112">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="b1023-112">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1023-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b1023-113">Return value</span></span>

<span data-ttu-id="b1023-114">O código de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="b1023-114">The return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1023-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1023-115">Requirements</span></span>



| <span data-ttu-id="b1023-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1023-116">Requirement</span></span> | <span data-ttu-id="b1023-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b1023-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1023-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1023-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b1023-119">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b1023-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b1023-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1023-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b1023-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b1023-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b1023-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b1023-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1023-123"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1023-123"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1023-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1023-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1023-125">Visão geral</span><span class="sxs-lookup"><span data-stu-id="b1023-125">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="b1023-126">Notificações</span><span class="sxs-lookup"><span data-stu-id="b1023-126">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="b1023-127">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="b1023-127">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="b1023-128">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="b1023-128">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="b1023-129">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="b1023-129">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




