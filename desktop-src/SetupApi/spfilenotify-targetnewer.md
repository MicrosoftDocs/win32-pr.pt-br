---
description: A notificação de SPFILENOTIFY \_ TARGETNEWER será enviada para a rotina de retorno de chamada se o arquivo a ser copiado tiver sido colocado na fila com a cópia do SP \_ \_ mais recente ou a \_ cópia \_ do SP Force os \_ sinalizadores mais recentes especificados e uma versão mais recente do arquivo já existir no diretório de destino.
ms.assetid: 93bcd610-f75d-4900-841c-f67946af5c4a
title: Mensagem de SPFILENOTIFY_TARGETNEWER (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c432515a5ce0e9a1eddb8ea6e92f7376c318b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748379"
---
# <a name="spfilenotify_targetnewer-message"></a><span data-ttu-id="4547d-103">\_Mensagem SPFILENOTIFY TARGETNEWER</span><span class="sxs-lookup"><span data-stu-id="4547d-103">SPFILENOTIFY\_TARGETNEWER message</span></span>

<span data-ttu-id="4547d-104">A notificação de **SPFILENOTIFY \_ TARGETNEWER** será enviada para a rotina de retorno de chamada se o arquivo a ser copiado tiver sido colocado na fila com a cópia do SP \_ \_ mais recente ou a \_ cópia \_ do SP Force os \_ sinalizadores mais recentes especificados e uma versão mais recente do arquivo já existir no diretório de destino.</span><span class="sxs-lookup"><span data-stu-id="4547d-104">The **SPFILENOTIFY\_TARGETNEWER** notification is sent to the callback routine if the file to be copied was queued with the SP\_COPY\_NEWER or SP\_COPY\_FORCE\_NEWER flags specified and a newer version of the file already exists in the target directory.</span></span> <span data-ttu-id="4547d-105">Ele pode ser enviado para a rotina de retorno de chamada sozinha ou vinculada com [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) e/ou [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md).</span><span class="sxs-lookup"><span data-stu-id="4547d-105">It can be sent to the callback routine alone or ORed together with [**SPFILENOTIFY\_LANGMISMATCH**](spfilenotify-langmismatch.md) and/or [**SPFILENOTIFY\_TARGETEXISTS**](spfilenotify-targetexists.md).</span></span>


```C++
SPFILENOTIFY_TARGETNEWER
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="4547d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4547d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4547d-107">*Param1*</span><span class="sxs-lookup"><span data-stu-id="4547d-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="4547d-108">Ponteiro para uma estrutura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) que contém informações sobre os caminhos para arquivos de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="4547d-108">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure that contains information about the paths for source and target files.</span></span>

</dd> <dt>

<span data-ttu-id="4547d-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="4547d-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="4547d-110">Esse parâmetro não é usado a menos que essa notificação seja combinada, usando o operador OR, com [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md).</span><span class="sxs-lookup"><span data-stu-id="4547d-110">This parameter is not used unless this notification is combined, by using the OR operator, with [**SPFILENOTIFY\_LANGMISMATCH**](spfilenotify-langmismatch.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4547d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4547d-111">Return value</span></span>

<span data-ttu-id="4547d-112">A rotina de retorno de chamada deve retornar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="4547d-112">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="4547d-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4547d-113">Return code</span></span>                                                                          | <span data-ttu-id="4547d-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="4547d-114">Description</span></span>                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="4547d-115"><dt>**TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="4547d-115"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="4547d-116">Substitua o arquivo no diretório de destino.</span><span class="sxs-lookup"><span data-stu-id="4547d-116">Overwrite the file in the target directory.</span></span><br/> |
| <dl> <span data-ttu-id="4547d-117"><dt>**FOR**</dt></span><span class="sxs-lookup"><span data-stu-id="4547d-117"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="4547d-118">Ignore a operação de cópia atual.</span><span class="sxs-lookup"><span data-stu-id="4547d-118">Skip the current copy operation.</span></span><br/>            |



 

## <a name="requirements"></a><span data-ttu-id="4547d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4547d-119">Requirements</span></span>



| <span data-ttu-id="4547d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4547d-120">Requirement</span></span> | <span data-ttu-id="4547d-121">Valor</span><span class="sxs-lookup"><span data-stu-id="4547d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4547d-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4547d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4547d-123">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4547d-123">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4547d-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4547d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4547d-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4547d-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4547d-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4547d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4547d-127"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4547d-127"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4547d-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="4547d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4547d-129">Visão geral</span><span class="sxs-lookup"><span data-stu-id="4547d-129">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="4547d-130">Notificações</span><span class="sxs-lookup"><span data-stu-id="4547d-130">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="4547d-131">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="4547d-131">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="4547d-132">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="4547d-132">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="4547d-133">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="4547d-133">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[<span data-ttu-id="4547d-134">**SetupInstallFile**</span><span class="sxs-lookup"><span data-stu-id="4547d-134">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[<span data-ttu-id="4547d-135">**SetupInstallFileEx**</span><span class="sxs-lookup"><span data-stu-id="4547d-135">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[<span data-ttu-id="4547d-136">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="4547d-136">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




