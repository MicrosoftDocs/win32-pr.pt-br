---
description: Identifica o tipo de host do chamador WLDP.
ms.assetid: E8E603CC-9CB2-4C3B-9F06-9B06C7B5D752
title: Enumeração de WLDP_HOST_ID (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_HOST_ID
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: 8914f93ff5936451b71b855473a09cb1d06584b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500768"
---
# <a name="wldp_host_id-enumeration"></a><span data-ttu-id="ded2c-103">Enumeração de ID de \_ host WLDP \_</span><span class="sxs-lookup"><span data-stu-id="ded2c-103">WLDP\_HOST\_ID enumeration</span></span>

<span data-ttu-id="ded2c-104">Identifica o tipo de host do chamador WLDP.</span><span class="sxs-lookup"><span data-stu-id="ded2c-104">Identifies the host type of the WLDP caller.</span></span>

## <a name="syntax"></a><span data-ttu-id="ded2c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ded2c-105">Syntax</span></span>


```C++
typedef enum _WLDP_HOST_ID { 
   WLDP_HOST_ID_UNKNOWN     = 0,
   WLDP_HOST_ID_GLOBAL      = 1,
  WLDP_HOST_ID_VBA          = 2,
   WLDP_HOST_ID_WSH         = 3,
   WLDP_HOST_ID_POWERSHELL  = 4,
   WLDP_HOST_ID_IE          = 5,
   WLDP_HOST_ID_MSI         = 6,
   WLDP_HOST_ID_MAX         = 7
} WLDP_HOST_ID, *PWLDP_HOST_ID;
```



## <a name="constants"></a><span data-ttu-id="ded2c-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="ded2c-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ded2c-107"><span id="_WLDP_HOST_ID_UNKNOWN_"></span><span id="_wldp_host_id_unknown_"></span>**WLDP \_ ID de HOST \_ \_ desconhecida**</span><span class="sxs-lookup"><span data-stu-id="ded2c-107"><span id="_WLDP_HOST_ID_UNKNOWN_"></span><span id="_wldp_host_id_unknown_"></span> **WLDP\_HOST\_ID\_UNKNOWN**</span></span> 
</dt> <dd>

<span data-ttu-id="ded2c-108">O tipo de host é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="ded2c-108">The host type is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="ded2c-109"><span id="_WLDP_HOST_ID_GLOBAL"></span><span id="_wldp_host_id_global"></span>**WLDP \_ ID do HOST \_ \_ global**</span><span class="sxs-lookup"><span data-stu-id="ded2c-109"><span id="_WLDP_HOST_ID_GLOBAL"></span><span id="_wldp_host_id_global"></span> **WLDP\_HOST\_ID\_GLOBAL**</span></span>
</dt> <dd>

<span data-ttu-id="ded2c-110">O tipo de host é política global.</span><span class="sxs-lookup"><span data-stu-id="ded2c-110">The host type is global policy.</span></span>

</dd> <dt>

<span data-ttu-id="ded2c-111"><span id="WLDP_HOST_ID_VBA"></span><span id="wldp_host_id_vba"></span>**WLDP \_ ID do host do \_ \_ VBA**</span><span class="sxs-lookup"><span data-stu-id="ded2c-111"><span id="WLDP_HOST_ID_VBA"></span><span id="wldp_host_id_vba"></span>**WLDP\_HOST\_ID\_VBA**</span></span>
</dt> <dd>

<span data-ttu-id="ded2c-112">O tipo de host é VBScript.</span><span class="sxs-lookup"><span data-stu-id="ded2c-112">The host type is VBScript.</span></span>

</dd> <dt>

<span data-ttu-id="ded2c-113"><span id="_WLDP_HOST_ID_WSH"></span><span id="_wldp_host_id_wsh"></span>**WLDP \_ ID do HOST \_ \_ WSH**</span><span class="sxs-lookup"><span data-stu-id="ded2c-113"><span id="_WLDP_HOST_ID_WSH"></span><span id="_wldp_host_id_wsh"></span> **WLDP\_HOST\_ID\_WSH**</span></span>
</dt> <dd>

<span data-ttu-id="ded2c-114">O tipo de host é Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="ded2c-114">The host type is Windows Script Host.</span></span>

</dd> <dt>

<span data-ttu-id="ded2c-115"><span id="_WLDP_HOST_ID_POWERSHELL"></span><span id="_wldp_host_id_powershell"></span>**WLDP \_ ID do HOST \_ \_ PowerShell**</span><span class="sxs-lookup"><span data-stu-id="ded2c-115"><span id="_WLDP_HOST_ID_POWERSHELL"></span><span id="_wldp_host_id_powershell"></span> **WLDP\_HOST\_ID\_POWERSHELL**</span></span>
</dt> <dd>

<span data-ttu-id="ded2c-116">O tipo de host é o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ded2c-116">The host type is Windows Powershell.</span></span>

</dd> <dt>

<span data-ttu-id="ded2c-117"><span id="_WLDP_HOST_ID_IE"></span><span id="_wldp_host_id_ie"></span>**WLDP \_ ID do HOST \_ \_ IE**</span><span class="sxs-lookup"><span data-stu-id="ded2c-117"><span id="_WLDP_HOST_ID_IE"></span><span id="_wldp_host_id_ie"></span> **WLDP\_HOST\_ID\_IE**</span></span>
</dt> <dd>

<span data-ttu-id="ded2c-118">O tipo de host é o Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="ded2c-118">The host type is Internet Explorer.</span></span>

</dd> <dt>

<span data-ttu-id="ded2c-119"><span id="_WLDP_HOST_ID_MSI"></span><span id="_wldp_host_id_msi"></span>**WLDP \_ \_ \_ MSI da ID do host**</span><span class="sxs-lookup"><span data-stu-id="ded2c-119"><span id="_WLDP_HOST_ID_MSI"></span><span id="_wldp_host_id_msi"></span> **WLDP\_HOST\_ID\_MSI**</span></span>
</dt> <dd>

<span data-ttu-id="ded2c-120">O tipo de host é o Microsoft Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ded2c-120">The host type is the Microsoft Windows Installer.</span></span>

</dd> <dt>

<span data-ttu-id="ded2c-121"><span id="_WLDP_HOST_ID_MAX__"></span><span id="_wldp_host_id_max__"></span>**WLDP \_ ID do HOST \_ \_ máx** .</span><span class="sxs-lookup"><span data-stu-id="ded2c-121"><span id="_WLDP_HOST_ID_MAX__"></span><span id="_wldp_host_id_max__"></span> **WLDP\_HOST\_ID\_MAX**</span></span> 
</dt> <dd>

<span data-ttu-id="ded2c-122">O valor máximo de enumeração.</span><span class="sxs-lookup"><span data-stu-id="ded2c-122">The maximum enumeration value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ded2c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ded2c-123">Requirements</span></span>



| <span data-ttu-id="ded2c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ded2c-124">Requirement</span></span> | <span data-ttu-id="ded2c-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ded2c-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ded2c-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ded2c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ded2c-127">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ded2c-127">Windows 8 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ded2c-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ded2c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ded2c-129">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ded2c-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ded2c-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ded2c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ded2c-131"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ded2c-131"><dt>Wldp.h</dt></span></span> </dl> |



 

 




