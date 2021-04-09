---
description: A \_ notificação SPFILENOTIFY DELETEERROR será enviada para a rotina de retorno de chamada se ocorrer um erro durante uma operação de exclusão de arquivo.
ms.assetid: b98b62f0-0b59-430e-966d-c1447026b696
title: Mensagem de SPFILENOTIFY_DELETEERROR (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 035b61120bd1343b43c9b6f6d74246eab33cb430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011760"
---
# <a name="spfilenotify_deleteerror-message"></a><span data-ttu-id="b8a96-103">\_Mensagem SPFILENOTIFY DELETEERROR</span><span class="sxs-lookup"><span data-stu-id="b8a96-103">SPFILENOTIFY\_DELETEERROR message</span></span>

<span data-ttu-id="b8a96-104">A notificação **SPFILENOTIFY \_ DELETEERROR** será enviada para a rotina de retorno de chamada se ocorrer um erro durante uma operação de exclusão de arquivo.</span><span class="sxs-lookup"><span data-stu-id="b8a96-104">The **SPFILENOTIFY\_DELETEERROR** notification is sent to the callback routine if an error occurs during a file delete operation.</span></span>


```C++
SPFILENOTIFY_DELETEERROR
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="b8a96-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8a96-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8a96-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="b8a96-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="b8a96-107">Ponteiro para uma estrutura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="b8a96-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b8a96-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="b8a96-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="b8a96-109">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="b8a96-109">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8a96-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b8a96-110">Return value</span></span>

<span data-ttu-id="b8a96-111">A rotina de retorno de chamada deve retornar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b8a96-111">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="b8a96-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b8a96-112">Return code</span></span>                                                                                  | <span data-ttu-id="b8a96-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="b8a96-113">Description</span></span>                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b8a96-114"><dt>**\_anular FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="b8a96-114"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="b8a96-115">O processamento da fila deve ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="b8a96-115">Queue processing should be canceled.</span></span> <span data-ttu-id="b8a96-116">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retorna zero e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna informações de erro ESTENDIdas, como erro \_ cancelado (se o usuário cancelou) ou erro \_ não \_ há \_ memória suficiente.</span><span class="sxs-lookup"><span data-stu-id="b8a96-116">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns zero and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns extended error information such as ERROR\_CANCELLED (if the user canceled) or ERROR\_NOT\_ENOUGH\_MEMORY.</span></span><br/> |
| <dl> <span data-ttu-id="b8a96-117"><dt>**repetição de FILEOP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b8a96-117"><dt>**FILEOP\_RETRY**</dt></span></span> </dl> | <span data-ttu-id="b8a96-118">O usuário está tentando a operação de exclusão novamente.</span><span class="sxs-lookup"><span data-stu-id="b8a96-118">The user is attempting the delete operation again.</span></span><br/>                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="b8a96-119"><dt>**FILEOP \_ ignorar**</dt></span><span class="sxs-lookup"><span data-stu-id="b8a96-119"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>  | <span data-ttu-id="b8a96-120">O usuário está ignorando a operação de exclusão de arquivo.</span><span class="sxs-lookup"><span data-stu-id="b8a96-120">The user is skipping the file delete operation.</span></span><br/>                                                                                                                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="b8a96-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8a96-121">Requirements</span></span>



| <span data-ttu-id="b8a96-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8a96-122">Requirement</span></span> | <span data-ttu-id="b8a96-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b8a96-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8a96-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8a96-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b8a96-125">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b8a96-125">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b8a96-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8a96-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b8a96-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b8a96-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b8a96-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b8a96-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8a96-129"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8a96-129"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8a96-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8a96-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8a96-131">Visão geral</span><span class="sxs-lookup"><span data-stu-id="b8a96-131">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="b8a96-132">Notificações</span><span class="sxs-lookup"><span data-stu-id="b8a96-132">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="b8a96-133">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="b8a96-133">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="b8a96-134">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="b8a96-134">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="b8a96-135">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="b8a96-135">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

