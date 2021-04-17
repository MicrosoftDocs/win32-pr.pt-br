---
description: A \_ notificação SPFILENOTIFY STARTSUBQUEUE é enviada para a função de retorno de chamada quando a fila começa a processar as operações na subfila excluir, renomear ou copiar.
ms.assetid: 4f971549-8f79-4995-9796-1177c3a3c416
title: Mensagem de SPFILENOTIFY_STARTSUBQUEUE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30e4f20440c12e7fcd1900cd9762a504a26b907f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755305"
---
# <a name="spfilenotify_startsubqueue-message"></a><span data-ttu-id="e14a7-103">\_Mensagem SPFILENOTIFY STARTSUBQUEUE</span><span class="sxs-lookup"><span data-stu-id="e14a7-103">SPFILENOTIFY\_STARTSUBQUEUE message</span></span>

<span data-ttu-id="e14a7-104">A notificação **SPFILENOTIFY \_ STARTSUBQUEUE** é enviada para a função de retorno de chamada quando a fila começa a processar as operações na subfila excluir, renomear ou copiar.</span><span class="sxs-lookup"><span data-stu-id="e14a7-104">The **SPFILENOTIFY\_STARTSUBQUEUE** notification is sent to the callback function when the queue starts to process the operations in the delete, rename, or copy subqueue.</span></span>


```C++
SPFILENOTIFY_STARTSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) NumOperations;
            
```



## <a name="parameters"></a><span data-ttu-id="e14a7-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e14a7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e14a7-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="e14a7-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="e14a7-107">Subfila que foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="e14a7-107">Subqueue that has been started.</span></span> <span data-ttu-id="e14a7-108">Esse parâmetro pode ser qualquer um dos valores FILEOP \_ excluir, FILEOP \_ Rename ou FILEOP \_ Copy.</span><span class="sxs-lookup"><span data-stu-id="e14a7-108">This parameter can be any one of the values FILEOP\_DELETE, FILEOP\_RENAME, or FILEOP\_COPY.</span></span>

</dd> <dt>

<span data-ttu-id="e14a7-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="e14a7-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="e14a7-110">Número de operações de cópia, renomeação ou exclusão de arquivo na subfila.</span><span class="sxs-lookup"><span data-stu-id="e14a7-110">Number of file copy, rename, or delete operations in the subqueue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e14a7-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e14a7-111">Return value</span></span>

<span data-ttu-id="e14a7-112">Se ocorrer um erro, a rotina de retorno de chamada deverá chamar [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), especificando o erro e, em seguida, retornará zero.</span><span class="sxs-lookup"><span data-stu-id="e14a7-112">If an error occurs, the callback routine should call [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), specifying the error, and then return zero.</span></span> <span data-ttu-id="e14a7-113">A função [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retornará **false** e uma chamada subsequente para [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o código de erro definido pela rotina de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e14a7-113">The [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function will return **FALSE** and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the error code set by the callback routine.</span></span>

<span data-ttu-id="e14a7-114">Se nenhum erro ocorrer, a rotina de retorno de chamada deverá retornar um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="e14a7-114">If no error occurs, the callback routine should return a nonzero value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e14a7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e14a7-115">Requirements</span></span>



| <span data-ttu-id="e14a7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e14a7-116">Requirement</span></span> | <span data-ttu-id="e14a7-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e14a7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e14a7-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e14a7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e14a7-119">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e14a7-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e14a7-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e14a7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e14a7-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e14a7-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e14a7-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e14a7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e14a7-123"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e14a7-123"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e14a7-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="e14a7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e14a7-125">Visão geral</span><span class="sxs-lookup"><span data-stu-id="e14a7-125">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="e14a7-126">Notificações</span><span class="sxs-lookup"><span data-stu-id="e14a7-126">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="e14a7-127">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="e14a7-127">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="e14a7-128">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="e14a7-128">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

