---
title: Estrutura de MPSCAN_RESOURCES (MpClient. h)
description: Informações de recurso passadas durante uma operação de verificação.
ms.assetid: D97712A6-547D-44CC-B55D-039A5CCE20BF
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPSCAN_RESOURCES
- Ponteiro de estrutura de PMPSCAN_RESOURCES recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPSCAN_RESOURCES
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ee9ea259bca6bf66eb81fcd17b13d509d5a065
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919176"
---
# <a name="mpscan_resources-structure"></a><span data-ttu-id="db599-105">\_Estrutura de recursos MPSCAN</span><span class="sxs-lookup"><span data-stu-id="db599-105">MPSCAN\_RESOURCES structure</span></span>

<span data-ttu-id="db599-106">Informações de recurso passadas durante uma operação de verificação.</span><span class="sxs-lookup"><span data-stu-id="db599-106">Resource information passed during a scan operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="db599-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db599-107">Syntax</span></span>


```C++
typedef struct tagMPSCAN_RESOURCES {
  DWORD            dwResourceCount;
  PMPRESOURCE_INFO pResourceList;
} MPSCAN_RESOURCES, *PMPSCAN_RESOURCES;
```



## <a name="members"></a><span data-ttu-id="db599-108">Membros</span><span class="sxs-lookup"><span data-stu-id="db599-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="db599-109">**dwResourceCount**</span><span class="sxs-lookup"><span data-stu-id="db599-109">**dwResourceCount**</span></span>
</dt> <dd>

<span data-ttu-id="db599-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="db599-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="db599-111">Contagem de recursos.</span><span class="sxs-lookup"><span data-stu-id="db599-111">Count of resources.</span></span>

</dd> <dt>

<span data-ttu-id="db599-112">**origem**</span><span class="sxs-lookup"><span data-stu-id="db599-112">**pResourceList**</span></span>
</dt> <dd>

<span data-ttu-id="db599-113">Tipo: **\_ informações de PMPRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="db599-113">Type: **PMPRESOURCE\_INFO**</span></span>

</dd> <dd>

<span data-ttu-id="db599-114">Matriz de recursos.</span><span class="sxs-lookup"><span data-stu-id="db599-114">Array of resources.</span></span> <span data-ttu-id="db599-115">Consulte [**MPRESOURCE \_ info**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="db599-115">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="db599-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db599-116">Requirements</span></span>



| <span data-ttu-id="db599-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="db599-117">Requirement</span></span> | <span data-ttu-id="db599-118">Valor</span><span class="sxs-lookup"><span data-stu-id="db599-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db599-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db599-119">Minimum supported client</span></span><br/> | <span data-ttu-id="db599-120">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="db599-120">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="db599-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db599-121">Minimum supported server</span></span><br/> | <span data-ttu-id="db599-122">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="db599-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="db599-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="db599-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="db599-124"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="db599-124"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db599-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="db599-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db599-126">**informações de MPRESOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="db599-126">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> </dl>

 

 





