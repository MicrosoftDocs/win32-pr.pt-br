---
title: Estrutura de MPCLEAN_PRECHECK_DATA (MpClient. h)
description: Dados de notificação passados para a função de retorno de chamada de verificação limpa.
ms.assetid: 65B3B116-6E83-46F5-AE2B-92A41AE39480
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPCLEAN_PRECHECK_DATA
- Ponteiro de estrutura de PMPCLEAN_PRECHECK_DATA recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPCLEAN_PRECHECK_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc3d67e0c71c95db49b633feeb3048cc9f104b2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454946"
---
# <a name="mpclean_precheck_data-structure"></a><span data-ttu-id="041eb-105">Estrutura de dados de \_ verificação de MPCLEAN \_</span><span class="sxs-lookup"><span data-stu-id="041eb-105">MPCLEAN\_PRECHECK\_DATA structure</span></span>

<span data-ttu-id="041eb-106">Dados de notificação passados para a função de retorno de chamada de verificação limpa.</span><span class="sxs-lookup"><span data-stu-id="041eb-106">Notification data passed to clean precheck callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="041eb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="041eb-107">Syntax</span></span>


```C++
typedef struct tagMPCLEAN_PRECHECK_DATA {
  PMPRESOURCE_INFO     BlockedResourceInfo;
  BlockingResourceInfo PMPRESOURCE_INFO;
} MPCLEAN_PRECHECK_DATA, *PMPCLEAN_PRECHECK_DATA;
```



## <a name="members"></a><span data-ttu-id="041eb-108">Membros</span><span class="sxs-lookup"><span data-stu-id="041eb-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="041eb-109">**BlockedResourceInfo**</span><span class="sxs-lookup"><span data-stu-id="041eb-109">**BlockedResourceInfo**</span></span>
</dt> <dd>

<span data-ttu-id="041eb-110">Tipo: **\_ informações de PMPRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="041eb-110">Type: **PMPRESOURCE\_INFO**</span></span>

</dd> <dd>

<span data-ttu-id="041eb-111">Informações de recurso sobre o recurso que está sendo bloqueado.</span><span class="sxs-lookup"><span data-stu-id="041eb-111">Resource information about the resource being blocked.</span></span> <span data-ttu-id="041eb-112">Por exemplo, quando o andamento é o **recurso de mpnotify de \_ verificação \_ \_ bloqueado**.</span><span class="sxs-lookup"><span data-stu-id="041eb-112">For example, when progress is **MPNOTIFY\_PRECHECK\_RESOURCE\_BLOCKED**.</span></span> <span data-ttu-id="041eb-113">Consulte [**MPRESOURCE \_ info**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="041eb-113">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="041eb-114">**informações de PMPRESOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="041eb-114">**PMPRESOURCE\_INFO**</span></span>
</dt> <dd>

<span data-ttu-id="041eb-115">Tipo: **BlockingResourceInfo**</span><span class="sxs-lookup"><span data-stu-id="041eb-115">Type: **BlockingResourceInfo**</span></span>

</dd> <dd>

<span data-ttu-id="041eb-116">Informações de recurso sobre o recurso que está bloqueando.</span><span class="sxs-lookup"><span data-stu-id="041eb-116">Resource information about the resource that is blocking.</span></span> <span data-ttu-id="041eb-117">Por exemplo, quando o andamento é o **recurso de mpnotify de \_ verificação \_ \_ bloqueado**.</span><span class="sxs-lookup"><span data-stu-id="041eb-117">For example, when progress is **MPNOTIFY\_PRECHECK\_RESOURCE\_BLOCKED**.</span></span> <span data-ttu-id="041eb-118">Consulte [**MPRESOURCE \_ info**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="041eb-118">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="041eb-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="041eb-119">Requirements</span></span>



| <span data-ttu-id="041eb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="041eb-120">Requirement</span></span> | <span data-ttu-id="041eb-121">Valor</span><span class="sxs-lookup"><span data-stu-id="041eb-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="041eb-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="041eb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="041eb-123">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="041eb-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="041eb-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="041eb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="041eb-125">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="041eb-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="041eb-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="041eb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="041eb-127"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="041eb-127"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="041eb-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="041eb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="041eb-129">**informações de MPRESOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="041eb-129">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> </dl>

 

 





