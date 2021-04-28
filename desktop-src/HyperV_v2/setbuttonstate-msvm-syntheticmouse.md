---
description: Método setbuttonstate da classe Msvm_SyntheticMouse – define o estado atual do botão do dispositivo especificado.
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
ms.openlocfilehash: 161520ac1b7e9dba1a084a8fb3c623155aa135fe
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109204"
---
# <a name="setbuttonstate-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="94b2a-103">Método setbuttonstate da classe Msvm \_ SyntheticMouse</span><span class="sxs-lookup"><span data-stu-id="94b2a-103">SetButtonState method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="94b2a-104">Define o estado atual do botão de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="94b2a-104">Sets the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="94b2a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94b2a-105">Syntax</span></span>


```mof
uint32 SetButtonState(
  [in] uint32  buttonIndex,
  [in] boolean isDown
);
```



## <a name="parameters"></a><span data-ttu-id="94b2a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94b2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94b2a-107">*buttonIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="94b2a-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94b2a-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="94b2a-108">Type: **uint32**</span></span>

<span data-ttu-id="94b2a-109">O índice de base 1 do botão a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="94b2a-109">The 1-based index of the button to modify.</span></span>

</dd> <dt>

<span data-ttu-id="94b2a-110">*IsDown* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="94b2a-110">*isDown* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94b2a-111">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="94b2a-111">Type: **boolean**</span></span>

<span data-ttu-id="94b2a-112">O novo estado para baixo do botão.</span><span class="sxs-lookup"><span data-stu-id="94b2a-112">The new down state of the button.</span></span> <span data-ttu-id="94b2a-113">Um valor **verdadeiro** significa que o botão está inoperante.</span><span class="sxs-lookup"><span data-stu-id="94b2a-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94b2a-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="94b2a-114">Return value</span></span>

<span data-ttu-id="94b2a-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="94b2a-115">Type: **uint32**</span></span>

<span data-ttu-id="94b2a-116">Valores não zero indicam uma falha ao modificar o estado do botão.</span><span class="sxs-lookup"><span data-stu-id="94b2a-116">Non zero values indicate a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="94b2a-117">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="94b2a-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="94b2a-118">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="94b2a-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="94b2a-119">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="94b2a-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="94b2a-120">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="94b2a-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="94b2a-121">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="94b2a-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="94b2a-122">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="94b2a-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="94b2a-123">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="94b2a-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="94b2a-124">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="94b2a-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="94b2a-125">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="94b2a-125">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="94b2a-126">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="94b2a-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="94b2a-127">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="94b2a-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="94b2a-128">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="94b2a-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="94b2a-129">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="94b2a-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="94b2a-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="94b2a-130">Remarks</span></span>

<span data-ttu-id="94b2a-131">O acesso à classe [**Msvm \_ SyntheticMouse**](msvm-syntheticmouse.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="94b2a-131">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="94b2a-132">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="94b2a-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="94b2a-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94b2a-133">Requirements</span></span>



| <span data-ttu-id="94b2a-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="94b2a-134">Requirement</span></span> | <span data-ttu-id="94b2a-135">Valor</span><span class="sxs-lookup"><span data-stu-id="94b2a-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94b2a-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94b2a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="94b2a-137">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="94b2a-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="94b2a-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94b2a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="94b2a-139">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="94b2a-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="94b2a-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="94b2a-140">Namespace</span></span><br/>                | <span data-ttu-id="94b2a-141">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="94b2a-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="94b2a-142">MOF</span><span class="sxs-lookup"><span data-stu-id="94b2a-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94b2a-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94b2a-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="94b2a-144">DLL</span><span class="sxs-lookup"><span data-stu-id="94b2a-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94b2a-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="94b2a-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="94b2a-146">Consulte também</span><span class="sxs-lookup"><span data-stu-id="94b2a-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94b2a-147">**Msvm \_ SyntheticMouse**</span><span class="sxs-lookup"><span data-stu-id="94b2a-147">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

