---
description: Define a posição horizontal e vertical do cursor do mouse.
ms.assetid: 7845E10A-7F61-4134-BF81-AED5483F36AD
title: Método SetAbsolutePosition da classe Msvm_SyntheticMouse (Dbdao. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.SetAbsolutePosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4b8ffb3a4d415f76dedf30acba5869b4cc585eb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828274"
---
# <a name="setabsoluteposition-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="e6070-103">Método SetAbsolutePosition da \_ classe SyntheticMouse Msvm</span><span class="sxs-lookup"><span data-stu-id="e6070-103">SetAbsolutePosition method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="e6070-104">Define a posição horizontal e vertical do cursor do mouse.</span><span class="sxs-lookup"><span data-stu-id="e6070-104">Sets the horizontal and vertical position of the mouse cursor.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6070-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6070-105">Syntax</span></span>


```mof
uint32 SetAbsolutePosition(
  [in] sint32 horizontalPosition,
  [in] sint32 verticalPosition
);
```



## <a name="parameters"></a><span data-ttu-id="e6070-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6070-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6070-107">*horizontalPosition* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6070-107">*horizontalPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6070-108">Tipo: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e6070-108">Type: **sint32**</span></span>

<span data-ttu-id="e6070-109">A nova posição horizontal do cursor do mouse, em pixels.</span><span class="sxs-lookup"><span data-stu-id="e6070-109">The new horizontal position of the mouse cursor, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="e6070-110">*verticalPosition* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6070-110">*verticalPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6070-111">Tipo: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e6070-111">Type: **sint32**</span></span>

<span data-ttu-id="e6070-112">A nova posição vertical do cursor do mouse, em pixels.</span><span class="sxs-lookup"><span data-stu-id="e6070-112">The new vertical position of the mouse cursor, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6070-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e6070-113">Return value</span></span>

<span data-ttu-id="e6070-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e6070-114">Type: **uint32**</span></span>

<span data-ttu-id="e6070-115">Um valor de retorno igual A zero indica êxito.</span><span class="sxs-lookup"><span data-stu-id="e6070-115">A return value of zero indicates success.</span></span> <span data-ttu-id="e6070-116">Um valor diferente de zero indica uma falha ao alterar a posição de rolagem.</span><span class="sxs-lookup"><span data-stu-id="e6070-116">A nonzero value indicates a failure to alter the scroll position.</span></span>

<dl> <dt>

<span data-ttu-id="e6070-117">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="e6070-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e6070-118">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="e6070-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e6070-119">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="e6070-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e6070-120">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="e6070-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e6070-121">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="e6070-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e6070-122">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="e6070-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e6070-123">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="e6070-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e6070-124">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="e6070-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e6070-125">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="e6070-125">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e6070-126">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="e6070-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e6070-127">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="e6070-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e6070-128">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="e6070-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e6070-129">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="e6070-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="e6070-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6070-130">Remarks</span></span>

<span data-ttu-id="e6070-131">O acesso à classe [**Msvm \_ SyntheticMouse**](msvm-syntheticmouse.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="e6070-131">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e6070-132">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e6070-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6070-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6070-133">Requirements</span></span>



| <span data-ttu-id="e6070-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6070-134">Requirement</span></span> | <span data-ttu-id="e6070-135">Valor</span><span class="sxs-lookup"><span data-stu-id="e6070-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6070-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6070-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e6070-137">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e6070-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e6070-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6070-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e6070-139">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e6070-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e6070-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="e6070-140">Namespace</span></span><br/>                | <span data-ttu-id="e6070-141">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e6070-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e6070-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e6070-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6070-143"><dt>Dbdao. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6070-143"><dt>Dbdao.h</dt></span></span> </dl>                      |
| <span data-ttu-id="e6070-144">MOF</span><span class="sxs-lookup"><span data-stu-id="e6070-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6070-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e6070-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6070-146">DLL</span><span class="sxs-lookup"><span data-stu-id="e6070-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6070-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e6070-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e6070-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6070-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6070-149">**Msvm \_ SyntheticMouse**</span><span class="sxs-lookup"><span data-stu-id="e6070-149">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

