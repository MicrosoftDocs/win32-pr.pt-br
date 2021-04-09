---
description: A \_ notificação SPFILENOTIFY ENDSUBQUEUE é enviada para a função de retorno de chamada quando a fila conclui todas as operações na subfila excluir, renomear ou copiar.
ms.assetid: 76bd027a-0f00-46e3-b502-0c97827308a8
title: Mensagem de SPFILENOTIFY_ENDSUBQUEUE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7eadc7546487b308313b7cb31088a22420e27af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011758"
---
# <a name="spfilenotify_endsubqueue-message"></a><span data-ttu-id="336bc-103">\_Mensagem SPFILENOTIFY ENDSUBQUEUE</span><span class="sxs-lookup"><span data-stu-id="336bc-103">SPFILENOTIFY\_ENDSUBQUEUE message</span></span>

<span data-ttu-id="336bc-104">A notificação **SPFILENOTIFY \_ ENDSUBQUEUE** é enviada para a função de retorno de chamada quando a fila conclui todas as operações na subfila excluir, renomear ou copiar.</span><span class="sxs-lookup"><span data-stu-id="336bc-104">The **SPFILENOTIFY\_ENDSUBQUEUE** notification is sent to the callback function when the queue completes all the operations in the delete, rename, or copy subqueue.</span></span>


```C++
SPFILENOTIFY_ENDSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="336bc-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="336bc-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="336bc-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="336bc-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="336bc-107">Subfila que foi concluída.</span><span class="sxs-lookup"><span data-stu-id="336bc-107">Subqueue that has been completed.</span></span> <span data-ttu-id="336bc-108">Esse parâmetro pode ser um dos valores a seguir FILEOP \_ excluir, FILEOP \_ Rename ou FILEOP \_ Copy.</span><span class="sxs-lookup"><span data-stu-id="336bc-108">This parameter can be one of the following values FILEOP\_DELETE, FILEOP\_RENAME, or FILEOP\_COPY.</span></span>

</dd> <dt>

<span data-ttu-id="336bc-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="336bc-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="336bc-110">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="336bc-110">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="336bc-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="336bc-111">Return value</span></span>

<span data-ttu-id="336bc-112">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="336bc-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="336bc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="336bc-113">Requirements</span></span>



| <span data-ttu-id="336bc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="336bc-114">Requirement</span></span> | <span data-ttu-id="336bc-115">Valor</span><span class="sxs-lookup"><span data-stu-id="336bc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="336bc-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="336bc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="336bc-117">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="336bc-117">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="336bc-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="336bc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="336bc-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="336bc-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="336bc-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="336bc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="336bc-121"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="336bc-121"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="336bc-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="336bc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="336bc-123">Visão geral</span><span class="sxs-lookup"><span data-stu-id="336bc-123">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="336bc-124">Notificações</span><span class="sxs-lookup"><span data-stu-id="336bc-124">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="336bc-125">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="336bc-125">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="336bc-126">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="336bc-126">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




