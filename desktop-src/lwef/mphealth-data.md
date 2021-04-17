---
title: Estrutura de MPHEALTH_DATA (MpClient. h)
description: Dados de notificação de integridade.
ms.assetid: 37A87F77-386A-4508-B338-ED2151518968
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPHEALTH_DATA
- Ponteiro de estrutura de PMPHEALTH_DATA recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPHEALTH_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e729bdea82b6a885b64e95ecd77f9deae6bff4e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105797907"
---
# <a name="mphealth_data-structure"></a><span data-ttu-id="69d53-105">\_Estrutura de dados MPHEALTH</span><span class="sxs-lookup"><span data-stu-id="69d53-105">MPHEALTH\_DATA structure</span></span>

<span data-ttu-id="69d53-106">Dados de notificação de integridade.</span><span class="sxs-lookup"><span data-stu-id="69d53-106">Health notification data.</span></span>

## <a name="syntax"></a><span data-ttu-id="69d53-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="69d53-107">Syntax</span></span>


```C++
typedef struct tagMPHEALTH_DATA {
  DWORD dwNotificationType;
  DWORD dwNotificationFlag;
} MPHEALTH_DATA, *PMPHEALTH_DATA;
```



## <a name="members"></a><span data-ttu-id="69d53-108">Membros</span><span class="sxs-lookup"><span data-stu-id="69d53-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="69d53-109">**dwNotificationType**</span><span class="sxs-lookup"><span data-stu-id="69d53-109">**dwNotificationType**</span></span>
</dt> <dd>

<span data-ttu-id="69d53-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="69d53-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="69d53-111">Tipo de notificação.</span><span class="sxs-lookup"><span data-stu-id="69d53-111">Type of notification.</span></span>

</dd> <dt>

<span data-ttu-id="69d53-112">**dwNotificationFlag**</span><span class="sxs-lookup"><span data-stu-id="69d53-112">**dwNotificationFlag**</span></span>
</dt> <dd>

<span data-ttu-id="69d53-113">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="69d53-113">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="69d53-114">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="69d53-114">Unused.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="69d53-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69d53-115">Requirements</span></span>



| <span data-ttu-id="69d53-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="69d53-116">Requirement</span></span> | <span data-ttu-id="69d53-117">Valor</span><span class="sxs-lookup"><span data-stu-id="69d53-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69d53-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69d53-118">Minimum supported client</span></span><br/> | <span data-ttu-id="69d53-119">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="69d53-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="69d53-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69d53-120">Minimum supported server</span></span><br/> | <span data-ttu-id="69d53-121">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="69d53-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="69d53-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="69d53-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="69d53-123"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="69d53-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





