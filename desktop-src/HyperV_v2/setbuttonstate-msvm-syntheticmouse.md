---
description: Define o estado atual do botão de dispositivo especificado.
ms.assetid: 942DB31C-09A2-43B6-A666-267AF6A84E0E
title: Método setbuttonstate da classe Msvm_SyntheticMouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.SetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c99915fa8ede9cbb405f4483ac10ca9ff8efaf71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169412"
---
# <a name="setbuttonstate-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="ee555-103">Método setbuttonstate da classe Msvm \_ SyntheticMouse</span><span class="sxs-lookup"><span data-stu-id="ee555-103">SetButtonState method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="ee555-104">Define o estado atual do botão de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="ee555-104">Sets the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee555-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee555-105">Syntax</span></span>


```mof
uint32 SetButtonState(
  [in] uint32  buttonIndex,
  [in] boolean isDown
);
```



## <a name="parameters"></a><span data-ttu-id="ee555-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee555-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee555-107">*buttonIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee555-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee555-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ee555-108">Type: **uint32**</span></span>

<span data-ttu-id="ee555-109">O índice de base 1 do botão a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="ee555-109">The 1-based index of the button to modify.</span></span>

</dd> <dt>

<span data-ttu-id="ee555-110">*IsDown* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee555-110">*isDown* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee555-111">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ee555-111">Type: **boolean**</span></span>

<span data-ttu-id="ee555-112">O novo estado para baixo do botão.</span><span class="sxs-lookup"><span data-stu-id="ee555-112">The new down state of the button.</span></span> <span data-ttu-id="ee555-113">Um valor **verdadeiro** significa que o botão está inoperante.</span><span class="sxs-lookup"><span data-stu-id="ee555-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee555-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ee555-114">Return value</span></span>

<span data-ttu-id="ee555-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ee555-115">Type: **uint32**</span></span>

<span data-ttu-id="ee555-116">Valores não zero indicam uma falha ao modificar o estado do botão.</span><span class="sxs-lookup"><span data-stu-id="ee555-116">Non zero values indicate a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="ee555-117">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="ee555-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ee555-118">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="ee555-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ee555-119">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="ee555-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ee555-120">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="ee555-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ee555-121">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="ee555-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ee555-122">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="ee555-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ee555-123">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="ee555-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ee555-124">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="ee555-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ee555-125">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="ee555-125">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ee555-126">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="ee555-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ee555-127">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="ee555-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ee555-128">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="ee555-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ee555-129">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="ee555-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="ee555-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee555-130">Remarks</span></span>

<span data-ttu-id="ee555-131">O acesso à classe [**Msvm \_ SyntheticMouse**](msvm-syntheticmouse.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="ee555-131">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ee555-132">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ee555-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee555-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee555-133">Requirements</span></span>



| <span data-ttu-id="ee555-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee555-134">Requirement</span></span> | <span data-ttu-id="ee555-135">Valor</span><span class="sxs-lookup"><span data-stu-id="ee555-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee555-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee555-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ee555-137">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ee555-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ee555-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee555-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ee555-139">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ee555-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ee555-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="ee555-140">Namespace</span></span><br/>                | <span data-ttu-id="ee555-141">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="ee555-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ee555-142">MOF</span><span class="sxs-lookup"><span data-stu-id="ee555-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee555-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ee555-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ee555-144">DLL</span><span class="sxs-lookup"><span data-stu-id="ee555-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee555-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ee555-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ee555-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee555-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee555-147">**Msvm \_ SyntheticMouse**</span><span class="sxs-lookup"><span data-stu-id="ee555-147">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

