---
description: A \_ notificação SPFILENOTIFY QUEUESCAN \_ SIGNERINFO é enviada a uma rotina de retorno de chamada por SetupScanFileQueue para cada nó na subfila de cópia da fila de arquivos.
ms.assetid: 5b22e8ba-9a18-461b-bad7-b2d76f83d7f3
title: Mensagem de SPFILENOTIFY_QUEUESCAN_SIGNERINFO (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29bf9e9c7e0ab76303d8c2fb21a0109ec60358f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922093"
---
# <a name="spfilenotify_queuescan_signerinfo-message"></a><span data-ttu-id="a12e9-103">SPFILENOTIFY \_ QUEUESCAN \_ SIGNERINFO Message</span><span class="sxs-lookup"><span data-stu-id="a12e9-103">SPFILENOTIFY\_QUEUESCAN\_SIGNERINFO message</span></span>

<span data-ttu-id="a12e9-104">A notificação **SPFILENOTIFY \_ QUEUESCAN \_ SIGNERINFO** é enviada a uma rotina de retorno de chamada por [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) para cada nó na subfila de cópia da fila de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a12e9-104">The **SPFILENOTIFY\_QUEUESCAN\_SIGNERINFO** notification is sent to a callback routine by [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) for each node in the copy subqueue of the file queue.</span></span> <span data-ttu-id="a12e9-105">Isso só ocorrerá se a função **SetupScanFileQueue** for chamada especificando o sinalizador SPQ de \_ verificação \_ usar \_ retorno de chamada \_ SIGNERINFO.</span><span class="sxs-lookup"><span data-stu-id="a12e9-105">This only occurs if the **SetupScanFileQueue** function was called specifying the flag SPQ\_SCAN\_USE\_CALLBACK\_SIGNERINFO.</span></span> <span data-ttu-id="a12e9-106">Disponível a partir do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a12e9-106">Available starting with Windows XP.</span></span>


```C++
SPFILENOTIFY_QUEUESCAN_SIGNERINFO
  Param1 = (PFILEPATHS_SIGNERINFO) Filepaths;
            
```



## <a name="parameters"></a><span data-ttu-id="a12e9-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a12e9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a12e9-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="a12e9-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="a12e9-109">Ponteiro para uma estrutura de [**\_ SIGNERINFO de caminho**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_signerinfo_a) .</span><span class="sxs-lookup"><span data-stu-id="a12e9-109">Pointer to a [**FILEPATHS\_SIGNERINFO**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_signerinfo_a) structure.</span></span> <span data-ttu-id="a12e9-110">O membro de **destino** é o nome do arquivo de destino no sistema.</span><span class="sxs-lookup"><span data-stu-id="a12e9-110">The **Target** member is the filename of the target file on the system.</span></span> <span data-ttu-id="a12e9-111">O membro de **origem** é o caminho esperado do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="a12e9-111">The **Source** member is the expected path of the source file.</span></span> <span data-ttu-id="a12e9-112">O membro **Win32Error** é o erro de assinatura.</span><span class="sxs-lookup"><span data-stu-id="a12e9-112">The **Win32Error** member is the signing error.</span></span> <span data-ttu-id="a12e9-113">As informações de assinatura serão retornadas se a rotina de retorno de chamada retornar **Win32Error**= = sem \_ erro.</span><span class="sxs-lookup"><span data-stu-id="a12e9-113">Signature information is returned if the callback routine returns **Win32Error**==NO\_ERROR.</span></span> <span data-ttu-id="a12e9-114">O membro **DigitalSigner** é o signatário digital.</span><span class="sxs-lookup"><span data-stu-id="a12e9-114">The **DigitalSigner** member is the digital signer.</span></span> <span data-ttu-id="a12e9-115">O membro da **versão** é a versão.</span><span class="sxs-lookup"><span data-stu-id="a12e9-115">The **Version** member is the version.</span></span> <span data-ttu-id="a12e9-116">O **catálogofile** é o arquivo de catálogo.</span><span class="sxs-lookup"><span data-stu-id="a12e9-116">The **CatalogFile** is the catalog file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a12e9-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a12e9-117">Return value</span></span>

<span data-ttu-id="a12e9-118">A rotina de retorno de chamada deve retornar um [código de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="a12e9-118">The callback routine should return a [system error code](/windows/desktop/Debug/system-error-codes).</span></span>

<span data-ttu-id="a12e9-119">Se a rotina de retorno de chamada não retornar nenhum \_ erro, a verificação de fila continuará e retornará se a rotina retornar qualquer outro código de erro, a verificação de fila aborta e [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="a12e9-119">If the callback routine returns NO\_ERROR, the queue scan continues, and returns If the routine returns any other error code, the queue scan aborts and [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) returns **FALSE**.</span></span>

> [!Note]  
> <span data-ttu-id="a12e9-120">Essa notificação não é tratada pela função [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) .</span><span class="sxs-lookup"><span data-stu-id="a12e9-120">This notification is not handled by the [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) function.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a12e9-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a12e9-121">Requirements</span></span>



| <span data-ttu-id="a12e9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a12e9-122">Requirement</span></span> | <span data-ttu-id="a12e9-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a12e9-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a12e9-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a12e9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a12e9-125">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a12e9-125">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a12e9-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a12e9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a12e9-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a12e9-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a12e9-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a12e9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a12e9-129"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a12e9-129"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a12e9-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a12e9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a12e9-131">Visão geral</span><span class="sxs-lookup"><span data-stu-id="a12e9-131">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="a12e9-132">Notificações</span><span class="sxs-lookup"><span data-stu-id="a12e9-132">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="a12e9-133">**SetupScanFileQueue**</span><span class="sxs-lookup"><span data-stu-id="a12e9-133">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

