---
description: A \_ notificação SPFILENOTIFY NEEDMEDIA é enviada para a rotina de retorno de chamada quando uma nova mídia ou um novo arquivo de gabinete é necessário.
ms.assetid: 6a7947de-1bb3-46e0-9334-405684e58e98
title: Mensagem de SPFILENOTIFY_NEEDMEDIA (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b856a95f3c2e200d1d81cfa00c05ef592c1759
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105762885"
---
# <a name="spfilenotify_needmedia-message"></a><span data-ttu-id="67000-103">\_Mensagem SPFILENOTIFY NEEDMEDIA</span><span class="sxs-lookup"><span data-stu-id="67000-103">SPFILENOTIFY\_NEEDMEDIA message</span></span>

<span data-ttu-id="67000-104">A notificação **SPFILENOTIFY \_ NEEDMEDIA** é enviada para a rotina de retorno de chamada quando uma nova mídia ou um novo arquivo de gabinete é necessário.</span><span class="sxs-lookup"><span data-stu-id="67000-104">The **SPFILENOTIFY\_NEEDMEDIA** notification is sent to the callback routine when new media or a new cabinet file is required.</span></span>


```C++
SPFILENOTIFY_NEEDMEDIA
  Param1 = (UINT) SourceMediaInfo;
  Param2 = (UINT) NewPathInfo;
            
```



## <a name="parameters"></a><span data-ttu-id="67000-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67000-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67000-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="67000-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="67000-107">Ponteiro para uma estrutura de [**\_ mídia de origem**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) .</span><span class="sxs-lookup"><span data-stu-id="67000-107">Pointer to a [**SOURCE\_MEDIA**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="67000-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="67000-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="67000-109">Ponteiro para uma matriz de caracteres para armazenar novas informações de caminho fornecidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="67000-109">Pointer to a character array to store new path information supplied by the user.</span></span> <span data-ttu-id="67000-110">O tamanho do buffer é uma matriz **TCHAR** de máximo de \_ elementos Path.</span><span class="sxs-lookup"><span data-stu-id="67000-110">The buffer size is a **TCHAR** array of MAX\_PATH elements.</span></span> <span data-ttu-id="67000-111">As informações de caminho retornadas pelo seu aplicativo de instalação não devem exceder esse tamanho.</span><span class="sxs-lookup"><span data-stu-id="67000-111">The path information returned by your setup application should not exceed this size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67000-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="67000-112">Return value</span></span>

<span data-ttu-id="67000-113">A rotina de retorno de chamada deve retornar um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="67000-113">The callback routine should return one of the following.</span></span>



| <span data-ttu-id="67000-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="67000-114">Return code</span></span>                                                                                    | <span data-ttu-id="67000-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="67000-115">Description</span></span>                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="67000-116"><dt>**FILEOP \_ NEWPATH**</dt></span><span class="sxs-lookup"><span data-stu-id="67000-116"><dt>**FILEOP\_NEWPATH**</dt></span></span> </dl> | <span data-ttu-id="67000-117">A mídia está presente e o arquivo solicitado está disponível no caminho especificado no buffer apontado por *param2*.</span><span class="sxs-lookup"><span data-stu-id="67000-117">The media is present and the requested file is available at the path specified in the buffer pointed to by *Param2*.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="67000-118"><dt>**FILEOP \_ ignorar**</dt></span><span class="sxs-lookup"><span data-stu-id="67000-118"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="67000-119">Ignorar o arquivo solicitado</span><span class="sxs-lookup"><span data-stu-id="67000-119">Skip the requested file</span></span><br/>                                                                                                                                                                                      |
| <dl> <span data-ttu-id="67000-120"><dt>**\_anular FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="67000-120"><dt>**FILEOP\_ABORT**</dt></span></span> </dl>   | <span data-ttu-id="67000-121">Anular o processamento da fila.</span><span class="sxs-lookup"><span data-stu-id="67000-121">Abort queue processing.</span></span> <span data-ttu-id="67000-122">A função [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retorna **false**.</span><span class="sxs-lookup"><span data-stu-id="67000-122">The [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function returns **FALSE**.</span></span> <span data-ttu-id="67000-123">GetLastError retorna informações de erro estendidas, como erro \_ cancelado se o usuário cancelou.</span><span class="sxs-lookup"><span data-stu-id="67000-123">GetLastError returns extended error information, such as ERROR\_CANCELLED if the user canceled.</span></span><br/> |
| <dl> <span data-ttu-id="67000-124"><dt>**FILEOP-DOIT**</dt></span><span class="sxs-lookup"><span data-stu-id="67000-124"><dt>**FILEOP-DOIT**</dt></span></span> </dl>     | <span data-ttu-id="67000-125">A mídia está disponível.</span><span class="sxs-lookup"><span data-stu-id="67000-125">The media is available.</span></span><br/>                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="67000-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67000-126">Requirements</span></span>



| <span data-ttu-id="67000-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="67000-127">Requirement</span></span> | <span data-ttu-id="67000-128">Valor</span><span class="sxs-lookup"><span data-stu-id="67000-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67000-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67000-129">Minimum supported client</span></span><br/> | <span data-ttu-id="67000-130">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="67000-130">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="67000-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67000-131">Minimum supported server</span></span><br/> | <span data-ttu-id="67000-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="67000-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="67000-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="67000-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="67000-134"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="67000-134"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67000-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="67000-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67000-136">Visão geral</span><span class="sxs-lookup"><span data-stu-id="67000-136">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="67000-137">Notificações</span><span class="sxs-lookup"><span data-stu-id="67000-137">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="67000-138">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="67000-138">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="67000-139">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="67000-139">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[<span data-ttu-id="67000-140">**mídia de origem \_**</span><span class="sxs-lookup"><span data-stu-id="67000-140">**SOURCE\_MEDIA**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a)
</dt> </dl>

 

 




