---
title: Enumeração de MP_FASTPATH_TYPE (MpClient. h)
description: Tipo de FastPath.
ms.assetid: BD72228F-DCC0-435E-A408-BD7FB02E55E1
keywords:
- Recursos do ambiente Windows herdado de enumeração de MP_FASTPATH_TYPE
- PMP_FASTPATH_TYPE recursos de ambiente herdados do ponteiro de enumeração do Windows
topic_type:
- apiref
api_name:
- MP_FASTPATH_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e89db79c54b166a833369ff52e47473463e0a2b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086255"
---
# <a name="mp_fastpath_type-enumeration"></a><span data-ttu-id="e2ce9-105">\_Enumeração de \_ tipo MP FASTPATH</span><span class="sxs-lookup"><span data-stu-id="e2ce9-105">MP\_FASTPATH\_TYPE enumeration</span></span>

<span data-ttu-id="e2ce9-106">Tipo de FastPath.</span><span class="sxs-lookup"><span data-stu-id="e2ce9-106">FastPath type.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2ce9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2ce9-107">Syntax</span></span>


```C++
typedef enum tagMP_FASTPATH_TYPE { 
  MP_FASTPATH_UNKNOWN   = 0,
  MP_FASTPATH_VDM       = 1,
  MP_FASTPATH_DISABLED  = 2
} MP_FASTPATH_TYPE, *PMP_FASTPATH_TYPE;
```



## <a name="constants"></a><span data-ttu-id="e2ce9-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="e2ce9-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e2ce9-109"><span id="MP_FASTPATH_UNKNOWN"></span><span id="mp_fastpath_unknown"></span>**MP \_ FASTPATH \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="e2ce9-109"><span id="MP_FASTPATH_UNKNOWN"></span><span id="mp_fastpath_unknown"></span>**MP\_FASTPATH\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="e2ce9-110">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="e2ce9-110">Unknown.</span></span>

</dd> <dt>

<span data-ttu-id="e2ce9-111"><span id="MP_FASTPATH_VDM"></span><span id="mp_fastpath_vdm"></span>**\_FASTPATH \_ VDM MP**</span><span class="sxs-lookup"><span data-stu-id="e2ce9-111"><span id="MP_FASTPATH_VDM"></span><span id="mp_fastpath_vdm"></span>**MP\_FASTPATH\_VDM**</span></span>
</dt> <dd>

<span data-ttu-id="e2ce9-112">Atualização do VDM.</span><span class="sxs-lookup"><span data-stu-id="e2ce9-112">VDM update.</span></span>

</dd> <dt>

<span data-ttu-id="e2ce9-113"><span id="MP_FASTPATH_DISABLED"></span><span id="mp_fastpath_disabled"></span>**\_FASTPATH MP \_ desabilitado**</span><span class="sxs-lookup"><span data-stu-id="e2ce9-113"><span id="MP_FASTPATH_DISABLED"></span><span id="mp_fastpath_disabled"></span>**MP\_FASTPATH\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="e2ce9-114">Notificação de desabilitação de assinatura.</span><span class="sxs-lookup"><span data-stu-id="e2ce9-114">Signature disable notification.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e2ce9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2ce9-115">Requirements</span></span>



| <span data-ttu-id="e2ce9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2ce9-116">Requirement</span></span> | <span data-ttu-id="e2ce9-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e2ce9-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2ce9-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2ce9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e2ce9-119">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e2ce9-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e2ce9-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2ce9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e2ce9-121">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e2ce9-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e2ce9-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e2ce9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2ce9-123"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2ce9-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





