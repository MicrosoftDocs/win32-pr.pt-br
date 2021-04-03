---
description: Define a coordenada z do controle de roda do dispositivo apontador.
ms.assetid: 02349957-6BAA-42E7-B3D4-F39E748615E6
title: Método SetScrollPosition da classe Msvm_SyntheticMouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.SetScrollPosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6d82ad2cd75b41ca914d0db49d5de4709790ea6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091735"
---
# <a name="setscrollposition-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="12aa0-103">Método SetScrollPosition da \_ classe SyntheticMouse Msvm</span><span class="sxs-lookup"><span data-stu-id="12aa0-103">SetScrollPosition method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="12aa0-104">Define a coordenada z do controle de roda do dispositivo apontador.</span><span class="sxs-lookup"><span data-stu-id="12aa0-104">Sets the z-coordinate of the wheel control of the pointing device.</span></span> <span data-ttu-id="12aa0-105">Os valores gravados nessa propriedade são sempre deslocamentos de coordenadas relativos.</span><span class="sxs-lookup"><span data-stu-id="12aa0-105">Values written to this property are always relative coordinate offsets.</span></span>

## <a name="syntax"></a><span data-ttu-id="12aa0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12aa0-106">Syntax</span></span>


```mof
uint32 SetScrollPosition(
  [in] sint32 scrollPositionDelta
);
```



## <a name="parameters"></a><span data-ttu-id="12aa0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12aa0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12aa0-108">*scrollPositionDelta* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="12aa0-108">*scrollPositionDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12aa0-109">Tipo: **sint32**</span><span class="sxs-lookup"><span data-stu-id="12aa0-109">Type: **sint32**</span></span>

<span data-ttu-id="12aa0-110">O Delta da posição de rolagem.</span><span class="sxs-lookup"><span data-stu-id="12aa0-110">The delta of the scroll position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12aa0-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12aa0-111">Return value</span></span>

<span data-ttu-id="12aa0-112">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="12aa0-112">Type: **uint32**</span></span>

<span data-ttu-id="12aa0-113">Um valor de retorno igual A zero indica êxito.</span><span class="sxs-lookup"><span data-stu-id="12aa0-113">A return value of zero indicates success.</span></span> <span data-ttu-id="12aa0-114">Um valor diferente de zero indica uma falha ao alterar a posição de rolagem.</span><span class="sxs-lookup"><span data-stu-id="12aa0-114">A nonzero value indicates a failure to alter the scroll position.</span></span>

<dl> <dt>

<span data-ttu-id="12aa0-115">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="12aa0-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="12aa0-116">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="12aa0-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="12aa0-117">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="12aa0-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="12aa0-118">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="12aa0-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="12aa0-119">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="12aa0-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="12aa0-120">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="12aa0-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="12aa0-121">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="12aa0-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="12aa0-122">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="12aa0-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="12aa0-123">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="12aa0-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="12aa0-124">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="12aa0-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="12aa0-125">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="12aa0-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="12aa0-126">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="12aa0-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="12aa0-127">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="12aa0-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="12aa0-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="12aa0-128">Remarks</span></span>

<span data-ttu-id="12aa0-129">O acesso à classe [**Msvm \_ SyntheticMouse**](msvm-syntheticmouse.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="12aa0-129">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="12aa0-130">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="12aa0-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="12aa0-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12aa0-131">Requirements</span></span>



| <span data-ttu-id="12aa0-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="12aa0-132">Requirement</span></span> | <span data-ttu-id="12aa0-133">Valor</span><span class="sxs-lookup"><span data-stu-id="12aa0-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12aa0-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12aa0-134">Minimum supported client</span></span><br/> | <span data-ttu-id="12aa0-135">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="12aa0-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="12aa0-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12aa0-136">Minimum supported server</span></span><br/> | <span data-ttu-id="12aa0-137">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="12aa0-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="12aa0-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="12aa0-138">Namespace</span></span><br/>                | <span data-ttu-id="12aa0-139">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="12aa0-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="12aa0-140">MOF</span><span class="sxs-lookup"><span data-stu-id="12aa0-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12aa0-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12aa0-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="12aa0-142">DLL</span><span class="sxs-lookup"><span data-stu-id="12aa0-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12aa0-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="12aa0-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="12aa0-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="12aa0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12aa0-145">**Msvm \_ SyntheticMouse**</span><span class="sxs-lookup"><span data-stu-id="12aa0-145">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

