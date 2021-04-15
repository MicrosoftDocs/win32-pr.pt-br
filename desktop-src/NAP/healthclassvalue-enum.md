---
title: Enumeração HealthClassValue (NapProtocol. h)
description: Indica o valor do TLV da classe de integridade.
ms.assetid: af80c27a-a686-494b-8795-73eb366deaa0
keywords:
- HealthClassValue de enumeração de NAP
topic_type:
- apiref
api_name:
- HealthClassValue
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ade44b74d03a69d6ccf410a042adf3819b8cc782
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454597"
---
# <a name="healthclassvalue-enumeration"></a><span data-ttu-id="b227d-104">Enumeração HealthClassValue</span><span class="sxs-lookup"><span data-stu-id="b227d-104">HealthClassValue enumeration</span></span>

> [!Note]  
> <span data-ttu-id="b227d-105">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="b227d-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b227d-106">O tipo de enumeração **HealthClassValue** indica o valor do TLV da classe de integridade.</span><span class="sxs-lookup"><span data-stu-id="b227d-106">The **HealthClassValue** enumeration type indicates the value of the health class TLV.</span></span>

## <a name="syntax"></a><span data-ttu-id="b227d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b227d-107">Syntax</span></span>


```C++
typedef enum tagHealthClassValue { 
  healthClassFirewall        = 0,
  healthClassPatchLevel      = 1,
  healthClassAntiVirus       = 2,
  healthClassCriticalUpdate  = 3,
  healthClassReserved        = 128
} HealthClassValue;
```



## <a name="constants"></a><span data-ttu-id="b227d-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="b227d-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b227d-109"><span id="healthClassFirewall"></span><span id="healthclassfirewall"></span><span id="HEALTHCLASSFIREWALL"></span>**healthClassFirewall**</span><span class="sxs-lookup"><span data-stu-id="b227d-109"><span id="healthClassFirewall"></span><span id="healthclassfirewall"></span><span id="HEALTHCLASSFIREWALL"></span>**healthClassFirewall**</span></span>
</dt> <dd>

<span data-ttu-id="b227d-110">O TLV de classe de integridade é o firewall.</span><span class="sxs-lookup"><span data-stu-id="b227d-110">The health class TLV is firewall.</span></span>

</dd> <dt>

<span data-ttu-id="b227d-111"><span id="healthClassPatchLevel"></span><span id="healthclasspatchlevel"></span><span id="HEALTHCLASSPATCHLEVEL"></span>**healthClassPatchLevel**</span><span class="sxs-lookup"><span data-stu-id="b227d-111"><span id="healthClassPatchLevel"></span><span id="healthclasspatchlevel"></span><span id="HEALTHCLASSPATCHLEVEL"></span>**healthClassPatchLevel**</span></span>
</dt> <dd>

<span data-ttu-id="b227d-112">O TLV da classe de integridade é o nível de patch.</span><span class="sxs-lookup"><span data-stu-id="b227d-112">The health class TLV is patch level.</span></span>

</dd> <dt>

<span data-ttu-id="b227d-113"><span id="healthClassAntiVirus"></span><span id="healthclassantivirus"></span><span id="HEALTHCLASSANTIVIRUS"></span>**healthClassAntiVirus**</span><span class="sxs-lookup"><span data-stu-id="b227d-113"><span id="healthClassAntiVirus"></span><span id="healthclassantivirus"></span><span id="HEALTHCLASSANTIVIRUS"></span>**healthClassAntiVirus**</span></span>
</dt> <dd>

<span data-ttu-id="b227d-114">O TLV da classe de integridade é o antivírus.</span><span class="sxs-lookup"><span data-stu-id="b227d-114">The health class TLV is antivirus.</span></span>

</dd> <dt>

<span data-ttu-id="b227d-115"><span id="healthClassCriticalUpdate"></span><span id="healthclasscriticalupdate"></span><span id="HEALTHCLASSCRITICALUPDATE"></span>**healthClassCriticalUpdate**</span><span class="sxs-lookup"><span data-stu-id="b227d-115"><span id="healthClassCriticalUpdate"></span><span id="healthclasscriticalupdate"></span><span id="HEALTHCLASSCRITICALUPDATE"></span>**healthClassCriticalUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="b227d-116">O TLV da classe de integridade é atualização crítica.</span><span class="sxs-lookup"><span data-stu-id="b227d-116">The health class TLV is critical update.</span></span>

</dd> <dt>

<span data-ttu-id="b227d-117"><span id="healthClassReserved"></span><span id="healthclassreserved"></span><span id="HEALTHCLASSRESERVED"></span>**healthClassReserved**</span><span class="sxs-lookup"><span data-stu-id="b227d-117"><span id="healthClassReserved"></span><span id="healthclassreserved"></span><span id="HEALTHCLASSRESERVED"></span>**healthClassReserved**</span></span>
</dt> <dd>

<span data-ttu-id="b227d-118">Reservado somente para uso do sistema.</span><span class="sxs-lookup"><span data-stu-id="b227d-118">Reserved for system use only.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b227d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b227d-119">Requirements</span></span>



| <span data-ttu-id="b227d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b227d-120">Requirement</span></span> | <span data-ttu-id="b227d-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b227d-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b227d-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b227d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b227d-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b227d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b227d-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b227d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b227d-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b227d-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b227d-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b227d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b227d-127"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="b227d-127"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="b227d-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="b227d-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b227d-129"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b227d-129"><dt>NapProtocol.idl</dt></span></span> </dl> |



 

 





