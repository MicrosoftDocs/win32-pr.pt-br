---
title: Estrutura de MPNIS_PRIVATE_DATA (MpClient. h)
description: Notificações NIS privadas.
ms.assetid: 19B4928F-BC78-4DEA-A563-1516B6454465
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPNIS_PRIVATE_DATA
- Ponteiro de estrutura de PMPNIS_PRIVATE_DATA recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPNIS_PRIVATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21340665a32b619c42d7909e8cd1b72ca6d09fb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644309"
---
# <a name="mpnis_private_data-structure"></a><span data-ttu-id="5002c-105">\_Estrutura de dados privada do MPNIS \_</span><span class="sxs-lookup"><span data-stu-id="5002c-105">MPNIS\_PRIVATE\_DATA structure</span></span>

<span data-ttu-id="5002c-106">Notificações NIS privadas.</span><span class="sxs-lookup"><span data-stu-id="5002c-106">Private NIS notifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="5002c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5002c-107">Syntax</span></span>


```C++
typedef struct tagMPNIS_PRIVATE_DATA {
  DWORD dwNotificationType;
  DWORD cbDataSize;
  BYTE  *pbData;
} MPNIS_PRIVATE_DATA, *PMPNIS_PRIVATE_DATA;
```



## <a name="members"></a><span data-ttu-id="5002c-108">Membros</span><span class="sxs-lookup"><span data-stu-id="5002c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="5002c-109">**dwNotificationType**</span><span class="sxs-lookup"><span data-stu-id="5002c-109">**dwNotificationType**</span></span>
</dt> <dd>

<span data-ttu-id="5002c-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="5002c-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="5002c-111">Tipo de notificação.</span><span class="sxs-lookup"><span data-stu-id="5002c-111">Type of notification.</span></span>

</dd> <dt>

<span data-ttu-id="5002c-112">**cbDataSize**</span><span class="sxs-lookup"><span data-stu-id="5002c-112">**cbDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="5002c-113">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="5002c-113">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="5002c-114">Tamanho dos dados reservados, em bytes.</span><span class="sxs-lookup"><span data-stu-id="5002c-114">Size of reserved data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="5002c-115">**pbData**</span><span class="sxs-lookup"><span data-stu-id="5002c-115">**pbData**</span></span>
</dt> <dd>

<span data-ttu-id="5002c-116">Tipo: **byte \***</span><span class="sxs-lookup"><span data-stu-id="5002c-116">Type: **BYTE\***</span></span>

</dd> <dd>

<span data-ttu-id="5002c-117">Ponteiro para dados reservados.</span><span class="sxs-lookup"><span data-stu-id="5002c-117">Pointer to reserved data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5002c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5002c-118">Requirements</span></span>



| <span data-ttu-id="5002c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5002c-119">Requirement</span></span> | <span data-ttu-id="5002c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="5002c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5002c-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5002c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5002c-122">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5002c-122">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="5002c-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5002c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5002c-124">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5002c-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5002c-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5002c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5002c-126"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="5002c-126"><dt>MpClient.h</dt></span></span> </dl> |



 

 





