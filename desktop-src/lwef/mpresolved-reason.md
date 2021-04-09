---
title: Enumeração de MPRESOLVED_REASON (MpClient. h)
description: Possíveis motivos para uma falha de correção ser resolvida.
ms.assetid: 29E875D7-97DA-4129-AB71-B261CD0E682A
keywords:
- Recursos do ambiente Windows herdado de enumeração de MPRESOLVED_REASON
- PMPRESOLVED_REASON recursos de ambiente herdados do ponteiro de enumeração do Windows
topic_type:
- apiref
api_name:
- MPRESOLVED_REASON
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab31fc8b734852ccdf15278f535d916228b43976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009533"
---
# <a name="mpresolved_reason-enumeration"></a><span data-ttu-id="91ec8-105">\_Enumeração de motivo MPRESOLVED</span><span class="sxs-lookup"><span data-stu-id="91ec8-105">MPRESOLVED\_REASON enumeration</span></span>

<span data-ttu-id="91ec8-106">Possíveis motivos para uma falha de correção ser resolvida.</span><span class="sxs-lookup"><span data-stu-id="91ec8-106">Possible reasons for a remediation failure being resolved.</span></span>

## <a name="syntax"></a><span data-ttu-id="91ec8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="91ec8-107">Syntax</span></span>


```C++
typedef enum tagMPRESOLVED_REASON { 
  MPRESOLVED_REASON_UNKNOWN    = 0,
  MPRESOLVED_REASON_FULL_SCAN  = 1,
  MPRESOLVED_REASON_TIMED_OUT  = 2
} MPRESOLVED_REASON, *PMPRESOLVED_REASON;
```



## <a name="constants"></a><span data-ttu-id="91ec8-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="91ec8-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="91ec8-109"><span id="MPRESOLVED_REASON_UNKNOWN"></span><span id="mpresolved_reason_unknown"></span>**\_motivo MPRESOLVED \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="91ec8-109"><span id="MPRESOLVED_REASON_UNKNOWN"></span><span id="mpresolved_reason_unknown"></span>**MPRESOLVED\_REASON\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="91ec8-110">Em um estado de erro.</span><span class="sxs-lookup"><span data-stu-id="91ec8-110">In an error state.</span></span>

</dd> <dt>

<span data-ttu-id="91ec8-111"><span id="MPRESOLVED_REASON_FULL_SCAN"></span><span id="mpresolved_reason_full_scan"></span>**\_ \_ verificação completa do motivo do MPRESOLVED \_**</span><span class="sxs-lookup"><span data-stu-id="91ec8-111"><span id="MPRESOLVED_REASON_FULL_SCAN"></span><span id="mpresolved_reason_full_scan"></span>**MPRESOLVED\_REASON\_FULL\_SCAN**</span></span>
</dt> <dd>

<span data-ttu-id="91ec8-112">Uma verificação completa foi executada.</span><span class="sxs-lookup"><span data-stu-id="91ec8-112">A full scan was performed.</span></span>

</dd> <dt>

<span data-ttu-id="91ec8-113"><span id="MPRESOLVED_REASON_TIMED_OUT"></span><span id="mpresolved_reason_timed_out"></span>**o \_ motivo do MPRESOLVED \_ atingiu o tempo \_ limite**</span><span class="sxs-lookup"><span data-stu-id="91ec8-113"><span id="MPRESOLVED_REASON_TIMED_OUT"></span><span id="mpresolved_reason_timed_out"></span>**MPRESOLVED\_REASON\_TIMED\_OUT**</span></span>
</dt> <dd>

<span data-ttu-id="91ec8-114">Tempo suficiente aprovado.</span><span class="sxs-lookup"><span data-stu-id="91ec8-114">Enough time has passed.</span></span> <span data-ttu-id="91ec8-115">O padrão é uma semana.</span><span class="sxs-lookup"><span data-stu-id="91ec8-115">The default is one week.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="91ec8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91ec8-116">Requirements</span></span>



| <span data-ttu-id="91ec8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="91ec8-117">Requirement</span></span> | <span data-ttu-id="91ec8-118">Valor</span><span class="sxs-lookup"><span data-stu-id="91ec8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91ec8-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91ec8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="91ec8-120">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="91ec8-120">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="91ec8-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91ec8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="91ec8-122">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="91ec8-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="91ec8-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="91ec8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="91ec8-124"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="91ec8-124"><dt>MpClient.h</dt></span></span> </dl> |



 

 





