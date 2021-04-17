---
description: A \_ notificação SPFILENOTIFY STARTCOPY é enviada para a função de retorno de chamada quando a fila inicia uma operação de cópia de arquivo.
ms.assetid: 01a7d9d4-b548-4e72-b1c9-7116e67c023b
title: Mensagem de SPFILENOTIFY_STARTCOPY (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6693938a2f67530e7e3c906c5105d2c98a915a32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755545"
---
# <a name="spfilenotify_startcopy-message"></a><span data-ttu-id="8e941-103">\_Mensagem SPFILENOTIFY STARTCOPY</span><span class="sxs-lookup"><span data-stu-id="8e941-103">SPFILENOTIFY\_STARTCOPY message</span></span>

<span data-ttu-id="8e941-104">A notificação **SPFILENOTIFY \_ STARTCOPY** é enviada para a função de retorno de chamada quando a fila inicia uma operação de cópia de arquivo.</span><span class="sxs-lookup"><span data-stu-id="8e941-104">The **SPFILENOTIFY\_STARTCOPY** notification is sent to the callback function when the queue starts a file copy operation.</span></span>


```C++
SPFILENOTIFY_STARTCOPY
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) Operation;
            
```



## <a name="parameters"></a><span data-ttu-id="8e941-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e941-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e941-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="8e941-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="8e941-107">Ponteiro para uma estrutura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="8e941-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8e941-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="8e941-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="8e941-109">Sempre tem o valor FILEOP \_ Copy.</span><span class="sxs-lookup"><span data-stu-id="8e941-109">Always has the value FILEOP\_COPY.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e941-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8e941-110">Return value</span></span>

<span data-ttu-id="8e941-111">A rotina de retorno de chamada deve retornar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8e941-111">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="8e941-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8e941-112">Return code</span></span>                                                                                  | <span data-ttu-id="8e941-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e941-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8e941-114"><dt>**\_anular FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="8e941-114"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="8e941-115">Anule o processo de confirmação da fila.</span><span class="sxs-lookup"><span data-stu-id="8e941-115">Abort the queue commit process.</span></span> <span data-ttu-id="8e941-116">A rotina de retorno de chamada deve chamar [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) para indicar o motivo do encerramento.</span><span class="sxs-lookup"><span data-stu-id="8e941-116">The callback routine should call [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to indicate the reason for termination.</span></span> <span data-ttu-id="8e941-117">A função [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retorna **false** e uma chamada subsequente para [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna o código de erro definido pela rotina de retorno de chamada durante a chamada para **SetLastError**.</span><span class="sxs-lookup"><span data-stu-id="8e941-117">The [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function returns **FALSE** and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code set by the callback routine during the call to **SetLastError**.</span></span><br/> |
| <dl> <span data-ttu-id="8e941-118"><dt>**FILEOP \_ doit**</dt></span><span class="sxs-lookup"><span data-stu-id="8e941-118"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="8e941-119">Execute a operação de cópia de arquivo.</span><span class="sxs-lookup"><span data-stu-id="8e941-119">Perform the file copy operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="8e941-120"><dt>**FILEOP \_ ignorar**</dt></span><span class="sxs-lookup"><span data-stu-id="8e941-120"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>  | <span data-ttu-id="8e941-121">Ignore a operação de cópia atual.</span><span class="sxs-lookup"><span data-stu-id="8e941-121">Skip the current copy operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="8e941-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e941-122">Requirements</span></span>



| <span data-ttu-id="8e941-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e941-123">Requirement</span></span> | <span data-ttu-id="8e941-124">Valor</span><span class="sxs-lookup"><span data-stu-id="8e941-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e941-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e941-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8e941-126">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8e941-126">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8e941-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e941-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8e941-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8e941-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8e941-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8e941-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e941-130"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e941-130"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e941-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e941-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e941-132">Visão geral</span><span class="sxs-lookup"><span data-stu-id="8e941-132">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="8e941-133">Notificações</span><span class="sxs-lookup"><span data-stu-id="8e941-133">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="8e941-134">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="8e941-134">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="8e941-135">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="8e941-135">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="8e941-136">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="8e941-136">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

