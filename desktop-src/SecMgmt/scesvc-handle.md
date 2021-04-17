---
description: O \_ tipo de dados de identificador SCESVC é um identificador opaco fornecido pelo conjunto de ferramentas de configuração de segurança.
ms.assetid: 478d7d4b-7983-4247-b8be-2e2cd3327533
title: SCESVC_HANDLE (Scesvc. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09fbc115326361e4cbfe1152361a70a36007a302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501542"
---
# <a name="scesvc_handle"></a><span data-ttu-id="fca7d-103">identificador de SCESVC \_</span><span class="sxs-lookup"><span data-stu-id="fca7d-103">SCESVC\_HANDLE</span></span>

<span data-ttu-id="fca7d-104">O tipo de dados de **\_ identificador SCESVC** é um identificador opaco fornecido pelo conjunto de ferramentas de configuração de segurança.</span><span class="sxs-lookup"><span data-stu-id="fca7d-104">The **SCESVC\_HANDLE** data type is an opaque handle provided by the Security Configuration tool set.</span></span> <span data-ttu-id="fca7d-105">Ele é usado por métodos das interfaces [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) e [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) para passar informações entre o snap-in de configuração de segurança e a extensão do snap-in.</span><span class="sxs-lookup"><span data-stu-id="fca7d-105">It is used by methods of the [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) and [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) interfaces to pass information between the Security Configuration snap-in and the snap-in extension.</span></span>


```C++
typedef PVOID SCESVC_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="fca7d-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fca7d-106">Requirements</span></span>



| <span data-ttu-id="fca7d-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="fca7d-107">Requirement</span></span> | <span data-ttu-id="fca7d-108">Valor</span><span class="sxs-lookup"><span data-stu-id="fca7d-108">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fca7d-109">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fca7d-109">Minimum supported client</span></span><br/> | <span data-ttu-id="fca7d-110">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fca7d-110">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fca7d-111">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fca7d-111">Minimum supported server</span></span><br/> | <span data-ttu-id="fca7d-112">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fca7d-112">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fca7d-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fca7d-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="fca7d-114"><dt>Scesvc. h</dt></span><span class="sxs-lookup"><span data-stu-id="fca7d-114"><dt>Scesvc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fca7d-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="fca7d-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fca7d-116">**ISceSvcAttachmentData**</span><span class="sxs-lookup"><span data-stu-id="fca7d-116">**ISceSvcAttachmentData**</span></span>](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)
</dt> <dt>

[<span data-ttu-id="fca7d-117">**ISceSvcAttachmentPersistInfo**</span><span class="sxs-lookup"><span data-stu-id="fca7d-117">**ISceSvcAttachmentPersistInfo**</span></span>](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo)
</dt> </dl>

 

 




