---
description: A \_ notificação SPFILENOTIFY RENAMEERROR será enviada para a rotina de retorno de chamada se ocorrer um erro durante uma operação de renomeação de arquivo.
ms.assetid: b7016cbe-2987-477f-958b-52b7a31c54c2
title: Mensagem de SPFILENOTIFY_RENAMEERROR (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a45658153980d7cfd5cb99b76fb344fcdb4bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297098"
---
# <a name="spfilenotify_renameerror-message"></a><span data-ttu-id="ca034-103">\_Mensagem SPFILENOTIFY RENAMEERROR</span><span class="sxs-lookup"><span data-stu-id="ca034-103">SPFILENOTIFY\_RENAMEERROR message</span></span>

<span data-ttu-id="ca034-104">A notificação **SPFILENOTIFY \_ RENAMEERROR** será enviada para a rotina de retorno de chamada se ocorrer um erro durante uma operação de renomeação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="ca034-104">The **SPFILENOTIFY\_RENAMEERROR** notification is sent to the callback routine if an error occurs during a file rename operation.</span></span>


```C++
SPFILENOTIFY_RENAMEERROR
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="ca034-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca034-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca034-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="ca034-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="ca034-107">Ponteiro para uma estrutura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="ca034-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="ca034-108">O membro **Win32Error** da estrutura **filePaths** especifica o erro que ocorreu durante a operação de renomeação.</span><span class="sxs-lookup"><span data-stu-id="ca034-108">The **Win32Error** member of the **FILEPATHS** structure specifies the error that occurred during the rename operation.</span></span>

</dd> <dt>

<span data-ttu-id="ca034-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="ca034-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="ca034-110">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="ca034-110">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca034-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ca034-111">Return value</span></span>

<span data-ttu-id="ca034-112">A rotina de retorno de chamada deve retornar um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="ca034-112">The callback routine should return one of the following.</span></span>



| <span data-ttu-id="ca034-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ca034-113">Return code</span></span>                                                                                  | <span data-ttu-id="ca034-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca034-114">Description</span></span>                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ca034-115"><dt>**repetição de FILEOP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ca034-115"><dt>**FILEOP\_RETRY**</dt></span></span> </dl> | <span data-ttu-id="ca034-116">O usuário optou por tentar a operação de renomeação novamente.</span><span class="sxs-lookup"><span data-stu-id="ca034-116">The user chose to attempt the rename operation again.</span></span><br/>                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="ca034-117"><dt>**FILEOP \_ ignorar**</dt></span><span class="sxs-lookup"><span data-stu-id="ca034-117"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>  | <span data-ttu-id="ca034-118">O usuário optou por ignorar a operação de renomeação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="ca034-118">The user chose to skip the file rename operation.</span></span><br/>                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="ca034-119"><dt>**\_anular FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="ca034-119"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="ca034-120">Pare a confirmação da fila.</span><span class="sxs-lookup"><span data-stu-id="ca034-120">Stop the queue commit.</span></span> <span data-ttu-id="ca034-121">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retorna **false**.</span><span class="sxs-lookup"><span data-stu-id="ca034-121">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns **FALSE**.</span></span> <span data-ttu-id="ca034-122">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna informações de erro estendidas, como \_ o erro cancelado (se o usuário cancelou) ou o erro \_ não tem \_ memória suficiente \_ .</span><span class="sxs-lookup"><span data-stu-id="ca034-122">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns extended error information such as ERROR\_CANCELLED (if the user canceled) or ERROR\_NOT\_ENOUGH\_MEMORY.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ca034-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca034-123">Requirements</span></span>



| <span data-ttu-id="ca034-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca034-124">Requirement</span></span> | <span data-ttu-id="ca034-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ca034-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca034-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca034-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ca034-127">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ca034-127">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ca034-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca034-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ca034-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ca034-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ca034-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ca034-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca034-131"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca034-131"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca034-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca034-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca034-133">Visão geral</span><span class="sxs-lookup"><span data-stu-id="ca034-133">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="ca034-134">Notificações</span><span class="sxs-lookup"><span data-stu-id="ca034-134">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="ca034-135">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="ca034-135">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="ca034-136">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="ca034-136">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="ca034-137">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="ca034-137">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

