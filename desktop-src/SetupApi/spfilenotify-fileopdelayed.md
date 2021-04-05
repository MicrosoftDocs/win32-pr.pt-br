---
description: A \_ notificação SPFILENOTIFY FILEOPDELAYED é enviada por SetupInstallFileEx ou SetupCommitFileQueue para uma rotina de retorno de chamada quando uma operação de arquivo foi atrasada porque o arquivo estava em uso. A operação será processada na próxima vez em que o sistema for reinicializado.
ms.assetid: a0b38e2b-2390-49e5-b288-77c31636e696
title: Mensagem de SPFILENOTIFY_FILEOPDELAYED (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38975506ff998ec09c4549ec95d9ddb620466cf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827926"
---
# <a name="spfilenotify_fileopdelayed-message"></a><span data-ttu-id="da9b8-104">\_Mensagem SPFILENOTIFY FILEOPDELAYED</span><span class="sxs-lookup"><span data-stu-id="da9b8-104">SPFILENOTIFY\_FILEOPDELAYED message</span></span>

<span data-ttu-id="da9b8-105">A notificação **SPFILENOTIFY \_ FILEOPDELAYED** é enviada por [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) ou [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) para uma rotina de retorno de chamada quando uma operação de arquivo foi atrasada porque o arquivo estava em uso.</span><span class="sxs-lookup"><span data-stu-id="da9b8-105">The **SPFILENOTIFY\_FILEOPDELAYED** notification is sent by [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) or [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) to a callback routine when a file operation was delayed because the file was in use.</span></span> <span data-ttu-id="da9b8-106">A operação será processada na próxima vez em que o sistema for reinicializado.</span><span class="sxs-lookup"><span data-stu-id="da9b8-106">The operation will be processed the next time the system is rebooted.</span></span>


```C++
SPFILENOTIFY_FILEOPDELAYED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="da9b8-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="da9b8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da9b8-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="da9b8-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="da9b8-109">Ponteiro para uma estrutura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="da9b8-109">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

<span data-ttu-id="da9b8-110">Se a operação atrasada for uma operação de cópia de arquivo, a estrutura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) conterá as informações a seguir.</span><span class="sxs-lookup"><span data-stu-id="da9b8-110">If the delayed operation is a file copy operation, the [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure contains the following information.</span></span>



| <span data-ttu-id="da9b8-111">Membro filePaths</span><span class="sxs-lookup"><span data-stu-id="da9b8-111">FILEPATHS member</span></span> | <span data-ttu-id="da9b8-112">Valor</span><span class="sxs-lookup"><span data-stu-id="da9b8-112">Value</span></span>                                |
|------------------|--------------------------------------|
| <span data-ttu-id="da9b8-113">**Win32Error**</span><span class="sxs-lookup"><span data-stu-id="da9b8-113">**Win32Error**</span></span>   | <span data-ttu-id="da9b8-114">SEM \_ erros</span><span class="sxs-lookup"><span data-stu-id="da9b8-114">NO\_ERROR</span></span>                            |
| <span data-ttu-id="da9b8-115">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="da9b8-115">**Flags**</span></span>        | <span data-ttu-id="da9b8-116">\_cópia FILEOP</span><span class="sxs-lookup"><span data-stu-id="da9b8-116">FILEOP\_COPY</span></span>                         |
| <span data-ttu-id="da9b8-117">**Origem**</span><span class="sxs-lookup"><span data-stu-id="da9b8-117">**Source**</span></span>       | <span data-ttu-id="da9b8-118">Caminho completo do arquivo temporário.</span><span class="sxs-lookup"><span data-stu-id="da9b8-118">Full path of the temporary file.</span></span>     |
| <span data-ttu-id="da9b8-119">**Target (destino)**</span><span class="sxs-lookup"><span data-stu-id="da9b8-119">**Target**</span></span>       | <span data-ttu-id="da9b8-120">Caminho completo do arquivo de destino real.</span><span class="sxs-lookup"><span data-stu-id="da9b8-120">Full path of the actual target file.</span></span> |



 

<span data-ttu-id="da9b8-121">Esse arquivo temporário será copiado para o diretório de destino quando o sistema for reinicializado.</span><span class="sxs-lookup"><span data-stu-id="da9b8-121">This temporary file will be copied to the target directory when the system is rebooted.</span></span> <span data-ttu-id="da9b8-122">As funções de instalação geram automaticamente um caminho para o arquivo temporário.</span><span class="sxs-lookup"><span data-stu-id="da9b8-122">The setup functions automatically generate a path for the temporary file.</span></span>

<span data-ttu-id="da9b8-123">Se a operação atrasada for uma operação de exclusão de arquivo, a estrutura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) conterá as informações a seguir.</span><span class="sxs-lookup"><span data-stu-id="da9b8-123">If the delayed operation is a file delete operation, the [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure contains the following information.</span></span>



| <span data-ttu-id="da9b8-124">Membro filePaths</span><span class="sxs-lookup"><span data-stu-id="da9b8-124">FILEPATHS member</span></span> | <span data-ttu-id="da9b8-125">Valor</span><span class="sxs-lookup"><span data-stu-id="da9b8-125">Value</span></span>                                |
|------------------|--------------------------------------|
| <span data-ttu-id="da9b8-126">**Win32Error**</span><span class="sxs-lookup"><span data-stu-id="da9b8-126">**Win32Error**</span></span>   | <span data-ttu-id="da9b8-127">SEM \_ erros</span><span class="sxs-lookup"><span data-stu-id="da9b8-127">NO\_ERROR</span></span>                            |
| <span data-ttu-id="da9b8-128">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="da9b8-128">**Flags**</span></span>        | <span data-ttu-id="da9b8-129">FILEOP \_ excluir</span><span class="sxs-lookup"><span data-stu-id="da9b8-129">FILEOP\_DELETE</span></span>                       |
| <span data-ttu-id="da9b8-130">**Origem**</span><span class="sxs-lookup"><span data-stu-id="da9b8-130">**Source**</span></span>       | <span data-ttu-id="da9b8-131">NULO</span><span class="sxs-lookup"><span data-stu-id="da9b8-131">NULL</span></span>                                 |
| <span data-ttu-id="da9b8-132">**Target (destino)**</span><span class="sxs-lookup"><span data-stu-id="da9b8-132">**Target**</span></span>       | <span data-ttu-id="da9b8-133">Caminho completo do arquivo a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="da9b8-133">Full path of the file to be deleted.</span></span> |



 

</dd> <dt>

<span data-ttu-id="da9b8-134">*Param2*</span><span class="sxs-lookup"><span data-stu-id="da9b8-134">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="da9b8-135">Não é usado.</span><span class="sxs-lookup"><span data-stu-id="da9b8-135">Is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da9b8-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="da9b8-136">Return value</span></span>

<span data-ttu-id="da9b8-137">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="da9b8-137">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="da9b8-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da9b8-138">Requirements</span></span>



| <span data-ttu-id="da9b8-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="da9b8-139">Requirement</span></span> | <span data-ttu-id="da9b8-140">Valor</span><span class="sxs-lookup"><span data-stu-id="da9b8-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da9b8-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da9b8-141">Minimum supported client</span></span><br/> | <span data-ttu-id="da9b8-142">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="da9b8-142">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="da9b8-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da9b8-143">Minimum supported server</span></span><br/> | <span data-ttu-id="da9b8-144">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="da9b8-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="da9b8-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="da9b8-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="da9b8-146"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="da9b8-146"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da9b8-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="da9b8-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da9b8-148">Visão geral</span><span class="sxs-lookup"><span data-stu-id="da9b8-148">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="da9b8-149">Notificações</span><span class="sxs-lookup"><span data-stu-id="da9b8-149">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="da9b8-150">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="da9b8-150">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="da9b8-151">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="da9b8-151">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="da9b8-152">**SetupInstallFile**</span><span class="sxs-lookup"><span data-stu-id="da9b8-152">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[<span data-ttu-id="da9b8-153">**SetupInstallFileEx**</span><span class="sxs-lookup"><span data-stu-id="da9b8-153">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[<span data-ttu-id="da9b8-154">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="da9b8-154">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




