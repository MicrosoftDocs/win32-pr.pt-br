---
title: Estrutura de MPRESERVED_DATA (MpClient. h)
description: Dados de notificação reservados.
ms.assetid: C92206BD-6E56-4B7D-ABB1-DC1149AE141D
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPRESERVED_DATA
- Ponteiro de estrutura de PMPRESERVED_DATA recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPRESERVED_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b1e08184da71fe857cb412ef986c986a0c59baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085845"
---
# <a name="mpreserved_data-structure"></a><span data-ttu-id="2af5d-105">\_Estrutura de dados MPRESERVED</span><span class="sxs-lookup"><span data-stu-id="2af5d-105">MPRESERVED\_DATA structure</span></span>

<span data-ttu-id="2af5d-106">Dados de notificação reservados.</span><span class="sxs-lookup"><span data-stu-id="2af5d-106">Reserved notification data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2af5d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2af5d-107">Syntax</span></span>


```C++
typedef struct tagMPRESERVED_DATA {
  DWORD cbReservedData;
  BYTE  *pbReservedData;
} MPRESERVED_DATA, *PMPRESERVED_DATA;
```



## <a name="members"></a><span data-ttu-id="2af5d-108">Membros</span><span class="sxs-lookup"><span data-stu-id="2af5d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="2af5d-109">**cbReservedData**</span><span class="sxs-lookup"><span data-stu-id="2af5d-109">**cbReservedData**</span></span>
</dt> <dd>

<span data-ttu-id="2af5d-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="2af5d-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="2af5d-111">Tamanho dos dados reservados, em bytes.</span><span class="sxs-lookup"><span data-stu-id="2af5d-111">Size of reserved data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2af5d-112">**pbReservedData**</span><span class="sxs-lookup"><span data-stu-id="2af5d-112">**pbReservedData**</span></span>
</dt> <dd>

<span data-ttu-id="2af5d-113">Tipo: **byte \***</span><span class="sxs-lookup"><span data-stu-id="2af5d-113">Type: **BYTE\***</span></span>

</dd> <dd>

<span data-ttu-id="2af5d-114">Ponteiro para dados reservados.</span><span class="sxs-lookup"><span data-stu-id="2af5d-114">Pointer to reserved data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2af5d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2af5d-115">Requirements</span></span>



| <span data-ttu-id="2af5d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2af5d-116">Requirement</span></span> | <span data-ttu-id="2af5d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="2af5d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2af5d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2af5d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2af5d-119">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2af5d-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2af5d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2af5d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2af5d-121">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2af5d-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2af5d-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2af5d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2af5d-123"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="2af5d-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





