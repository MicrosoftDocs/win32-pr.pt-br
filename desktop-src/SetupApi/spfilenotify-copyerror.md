---
description: A \_ notificação SPFILENOTIFY COPYERROR será enviada para a rotina de retorno de chamada se ocorrer um erro durante uma operação de cópia de arquivo.
ms.assetid: d6096954-c6a5-44d4-a358-c1320c50730a
title: Mensagem de SPFILENOTIFY_COPYERROR (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6cd44daabd6a4aed5e61a716bab3df44f35fc0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828687"
---
# <a name="spfilenotify_copyerror-message"></a><span data-ttu-id="355d9-103">\_Mensagem SPFILENOTIFY COPYERROR</span><span class="sxs-lookup"><span data-stu-id="355d9-103">SPFILENOTIFY\_COPYERROR message</span></span>

<span data-ttu-id="355d9-104">A notificação **SPFILENOTIFY \_ COPYERROR** será enviada para a rotina de retorno de chamada se ocorrer um erro durante uma operação de cópia de arquivo.</span><span class="sxs-lookup"><span data-stu-id="355d9-104">The **SPFILENOTIFY\_COPYERROR** notification is sent to the callback routine if an error occurs during a file copy operation.</span></span>


```C++
SPFILENOTIFY_COPYERROR
  Param1 = (UINT_PTR) FilePathInfo;
  Param2 = (UINT_PTR) ReturnBuffer;
            
```



## <a name="parameters"></a><span data-ttu-id="355d9-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="355d9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="355d9-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="355d9-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="355d9-107">Ponteiro para uma estrutura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="355d9-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="355d9-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="355d9-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="355d9-109">Ponteiro para um buffer, de tamanho máximo de \_ caracteres de caminho, que armazena novas informações de caminho especificadas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="355d9-109">Pointer to a buffer, of size MAX\_PATH characters, that stores new path information specified by the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="355d9-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="355d9-110">Return value</span></span>

<span data-ttu-id="355d9-111">O retorno de chamada deve retornar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="355d9-111">The callback should return one of the following values.</span></span>



| <span data-ttu-id="355d9-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="355d9-112">Return code</span></span>                                                                                    | <span data-ttu-id="355d9-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="355d9-113">Description</span></span>                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="355d9-114"><dt>**\_anular FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="355d9-114"><dt>**FILEOP\_ABORT**</dt></span></span> </dl>   | <span data-ttu-id="355d9-115">O processamento da fila deve ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="355d9-115">Queue processing should be canceled.</span></span> <span data-ttu-id="355d9-116">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retorna zero e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna informações de erro ESTENDIdas, como erro \_ cancelado (se o usuário cancelou) ou erro \_ não \_ há \_ memória suficiente.</span><span class="sxs-lookup"><span data-stu-id="355d9-116">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns zero and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns extended error information such as ERROR\_CANCELLED (if the user canceled) or ERROR\_NOT\_ENOUGH\_MEMORY.</span></span><br/> |
| <dl> <span data-ttu-id="355d9-117"><dt>**FILEOP \_ NEWPATH**</dt></span><span class="sxs-lookup"><span data-stu-id="355d9-117"><dt>**FILEOP\_NEWPATH**</dt></span></span> </dl> | <span data-ttu-id="355d9-118">Repita a operação de cópia usando o caminho que a função de retorno de chamada colocou no buffer apontado pelo parâmetro *param2* .</span><span class="sxs-lookup"><span data-stu-id="355d9-118">Retry the copy operation using the path the callback function placed in the buffer pointed to by the *Param2* parameter.</span></span> <span data-ttu-id="355d9-119">A rotina de retorno de chamada deve garantir que o caminho não exceda o tamanho do buffer de uma matriz TCHAR de \_ elementos de caminho máximo.</span><span class="sxs-lookup"><span data-stu-id="355d9-119">The callback routine should ensure that the path does not overflow the buffer size of a TCHAR array of MAX\_PATH elements.</span></span><br/>                |
| <dl> <span data-ttu-id="355d9-120"><dt>**repetição de FILEOP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="355d9-120"><dt>**FILEOP\_RETRY**</dt></span></span> </dl>   | <span data-ttu-id="355d9-121">O usuário está tentando a operação de cópia novamente.</span><span class="sxs-lookup"><span data-stu-id="355d9-121">The user is attempting the copy operation again.</span></span><br/>                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="355d9-122"><dt>**FILEOP \_ ignorar**</dt></span><span class="sxs-lookup"><span data-stu-id="355d9-122"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="355d9-123">O usuário está ignorando a operação de cópia de arquivo.</span><span class="sxs-lookup"><span data-stu-id="355d9-123">The user is skipping the file copy operation.</span></span><br/>                                                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="355d9-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="355d9-124">Requirements</span></span>



| <span data-ttu-id="355d9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="355d9-125">Requirement</span></span> | <span data-ttu-id="355d9-126">Valor</span><span class="sxs-lookup"><span data-stu-id="355d9-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="355d9-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="355d9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="355d9-128">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="355d9-128">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="355d9-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="355d9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="355d9-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="355d9-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="355d9-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="355d9-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="355d9-132"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="355d9-132"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="355d9-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="355d9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="355d9-134">Visão geral</span><span class="sxs-lookup"><span data-stu-id="355d9-134">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="355d9-135">Notificações</span><span class="sxs-lookup"><span data-stu-id="355d9-135">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="355d9-136">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="355d9-136">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="355d9-137">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="355d9-137">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="355d9-138">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="355d9-138">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

