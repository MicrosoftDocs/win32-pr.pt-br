---
description: A \_ estrutura informações do trabalho \_ 3 é usada para vincular um conjunto de trabalhos de impressão.
ms.assetid: a110f555-dc33-450c-ae77-ea26f0f69448
title: Estrutura de JOB_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_3
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c76cbb6c019878d9c392d21caa40c604df3a5f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171706"
---
# <a name="job_info_3-structure"></a><span data-ttu-id="b8970-103">Estrutura das informações do trabalho \_ \_ 3</span><span class="sxs-lookup"><span data-stu-id="b8970-103">JOB\_INFO\_3 structure</span></span>

<span data-ttu-id="b8970-104">A **estrutura \_ informações \_ do trabalho 3** é usada para vincular um conjunto de trabalhos de impressão.</span><span class="sxs-lookup"><span data-stu-id="b8970-104">The **JOB\_INFO\_3** structure is used to link together a set of print jobs.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8970-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8970-105">Syntax</span></span>


```C++
typedef struct _JOB_INFO_3 {
  DWORD JobId;
  DWORD NextJobId;
  DWORD Reserved;
} JOB_INFO_3, *PJOB_INFO_3;
```



## <a name="members"></a><span data-ttu-id="b8970-106">Membros</span><span class="sxs-lookup"><span data-stu-id="b8970-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b8970-107">**JobId**</span><span class="sxs-lookup"><span data-stu-id="b8970-107">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="b8970-108">O identificador do trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="b8970-108">The print job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b8970-109">**NextJobId**</span><span class="sxs-lookup"><span data-stu-id="b8970-109">**NextJobId**</span></span>
</dt> <dd>

<span data-ttu-id="b8970-110">O identificador do trabalho de impressão para o próximo trabalho de impressão no conjunto vinculado de trabalhos de impressão.</span><span class="sxs-lookup"><span data-stu-id="b8970-110">The print job identifier for the next print job in the linked set of print jobs.</span></span>

</dd> <dt>

<span data-ttu-id="b8970-111">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="b8970-111">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="b8970-112">Este valor está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="b8970-112">This value is reserved for future use.</span></span> <span data-ttu-id="b8970-113">Você deve defini-lo como zero.</span><span class="sxs-lookup"><span data-stu-id="b8970-113">You must set it to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b8970-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8970-114">Requirements</span></span>



| <span data-ttu-id="b8970-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8970-115">Requirement</span></span> | <span data-ttu-id="b8970-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b8970-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8970-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8970-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b8970-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b8970-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b8970-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8970-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b8970-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b8970-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b8970-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b8970-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8970-122"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8970-122"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8970-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8970-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8970-124">Impressão</span><span class="sxs-lookup"><span data-stu-id="b8970-124">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b8970-125">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="b8970-125">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="b8970-126">**EnumJobs**</span><span class="sxs-lookup"><span data-stu-id="b8970-126">**EnumJobs**</span></span>](enumjobs.md)
</dt> <dt>

[<span data-ttu-id="b8970-127">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="b8970-127">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="b8970-128">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="b8970-128">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

 




