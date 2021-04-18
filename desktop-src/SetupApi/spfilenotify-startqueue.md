---
description: A \_ notificação SPFILENOTIFY STARTQUEUE é enviada para a rotina de retorno de chamada quando o processo de compromisso de fila é iniciado.
ms.assetid: 682c2ce0-0c82-402c-a487-db5f2c377f3f
title: Mensagem de SPFILENOTIFY_STARTQUEUE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090e3f97dceb1843d75934dd99cca500e6f93086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756137"
---
# <a name="spfilenotify_startqueue-message"></a><span data-ttu-id="d3a80-103">\_Mensagem SPFILENOTIFY STARTQUEUE</span><span class="sxs-lookup"><span data-stu-id="d3a80-103">SPFILENOTIFY\_STARTQUEUE message</span></span>

<span data-ttu-id="d3a80-104">A notificação **SPFILENOTIFY \_ STARTQUEUE** é enviada para a rotina de retorno de chamada quando o processo de compromisso de fila é iniciado.</span><span class="sxs-lookup"><span data-stu-id="d3a80-104">The **SPFILENOTIFY\_STARTQUEUE** notification is sent to the callback routine when the queue commitment process starts.</span></span>


```C++
SPFILENOTIFY_STARTQUEUE
  Param1 = (UINT) OwnerWindow;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="d3a80-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3a80-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3a80-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="d3a80-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="d3a80-107">Manipule a janela que é proprietária das caixas de diálogo geradas pela rotina de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="d3a80-107">Handle to the window that is to own the dialog boxes that the callback routine generates.</span></span>

</dd> <dt>

<span data-ttu-id="d3a80-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="d3a80-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="d3a80-109">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="d3a80-109">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3a80-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d3a80-110">Return value</span></span>

<span data-ttu-id="d3a80-111">Se ocorrer um erro, a rotina de retorno de chamada deverá chamar [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), especificando o erro e, em seguida, retornará zero.</span><span class="sxs-lookup"><span data-stu-id="d3a80-111">If an error occurs, the callback routine should call [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), specifying the error, and then return zero.</span></span> <span data-ttu-id="d3a80-112">A função [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retornará **false** e uma chamada subsequente para [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o código de erro definido pela rotina de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="d3a80-112">The [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function will return **FALSE** and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the error code set by the callback routine.</span></span>

<span data-ttu-id="d3a80-113">Se nenhum erro ocorrer, a rotina de retorno de chamada deverá retornar um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="d3a80-113">If no error occurs, the callback routine should return a nonzero value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3a80-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3a80-114">Requirements</span></span>



| <span data-ttu-id="d3a80-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3a80-115">Requirement</span></span> | <span data-ttu-id="d3a80-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d3a80-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d3a80-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3a80-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d3a80-118">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d3a80-118">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d3a80-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3a80-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d3a80-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d3a80-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d3a80-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d3a80-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3a80-122"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3a80-122"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3a80-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3a80-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3a80-124">Visão geral</span><span class="sxs-lookup"><span data-stu-id="d3a80-124">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="d3a80-125">Notificações</span><span class="sxs-lookup"><span data-stu-id="d3a80-125">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="d3a80-126">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="d3a80-126">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="d3a80-127">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="d3a80-127">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

