---
description: Simula um clique do botão de dispositivo especificado.
ms.assetid: 77CFA2E9-E422-464C-B124-6F7D3D56BA4C
title: Método ClickButton da classe Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.ClickButton
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ffaded2a5e9a8e4e37a158e3aa91b27520dff2b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782816"
---
# <a name="clickbutton-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="32a21-103">Método ClickButton da \_ classe Ps2Mouse Msvm</span><span class="sxs-lookup"><span data-stu-id="32a21-103">ClickButton method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="32a21-104">Simula um clique do botão de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="32a21-104">Simulates a click of the specified device button.</span></span> <span data-ttu-id="32a21-105">Isso é equivalente a chamar [**Setbuttonstate**](setbuttonstate-msvm-syntheticmouse.md) duas vezes, primeiro para pressionar o botão e novamente para liberá-lo.</span><span class="sxs-lookup"><span data-stu-id="32a21-105">This is equivalent to calling [**SetButtonState**](setbuttonstate-msvm-syntheticmouse.md) twice, first to press the button, and again to release it.</span></span>

## <a name="syntax"></a><span data-ttu-id="32a21-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32a21-106">Syntax</span></span>


```mof
uint32 ClickButton(
  [in] uint32 buttonIndex
);
```



## <a name="parameters"></a><span data-ttu-id="32a21-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32a21-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32a21-108">*buttonIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="32a21-108">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32a21-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="32a21-109">Type: **uint32**</span></span>

<span data-ttu-id="32a21-110">O índice de base 1 do botão.</span><span class="sxs-lookup"><span data-stu-id="32a21-110">The 1-based index of the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32a21-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="32a21-111">Return value</span></span>

<span data-ttu-id="32a21-112">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="32a21-112">Type: **uint32**</span></span>

<span data-ttu-id="32a21-113">Um valor de retorno igual A zero indica êxito.</span><span class="sxs-lookup"><span data-stu-id="32a21-113">A return value of zero indicates success.</span></span> <span data-ttu-id="32a21-114">Um valor diferente de zero indica uma falha ao modificar o estado do botão.</span><span class="sxs-lookup"><span data-stu-id="32a21-114">A nonzero value indicates a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="32a21-115">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="32a21-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="32a21-116">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="32a21-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="32a21-117">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="32a21-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="32a21-118">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="32a21-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="32a21-119">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="32a21-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="32a21-120">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="32a21-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="32a21-121">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="32a21-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="32a21-122">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="32a21-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="32a21-123">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="32a21-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="32a21-124">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="32a21-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="32a21-125">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="32a21-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="32a21-126">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="32a21-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="32a21-127">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="32a21-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="32a21-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="32a21-128">Remarks</span></span>

<span data-ttu-id="32a21-129">O acesso à classe [**Msvm \_ Ps2Mouse**](msvm-ps2mouse.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="32a21-129">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="32a21-130">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="32a21-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="32a21-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32a21-131">Requirements</span></span>



| <span data-ttu-id="32a21-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="32a21-132">Requirement</span></span> | <span data-ttu-id="32a21-133">Valor</span><span class="sxs-lookup"><span data-stu-id="32a21-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32a21-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32a21-134">Minimum supported client</span></span><br/> | <span data-ttu-id="32a21-135">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="32a21-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="32a21-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32a21-136">Minimum supported server</span></span><br/> | <span data-ttu-id="32a21-137">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="32a21-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="32a21-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="32a21-138">Namespace</span></span><br/>                | <span data-ttu-id="32a21-139">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="32a21-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="32a21-140">MOF</span><span class="sxs-lookup"><span data-stu-id="32a21-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32a21-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32a21-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="32a21-142">DLL</span><span class="sxs-lookup"><span data-stu-id="32a21-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32a21-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="32a21-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="32a21-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="32a21-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32a21-145">**Msvm \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="32a21-145">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

