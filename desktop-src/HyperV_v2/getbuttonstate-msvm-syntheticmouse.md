---
description: Método getbuttonstate da classe Msvm_SyntheticMouse – recupera o estado atual do botão do dispositivo especificado.
ms.assetid: 66363AF1-E360-478D-8E62-513DE66EF130
title: Método getbuttonstate da classe Msvm_SyntheticMouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.GetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 26839292cf2fb3099e740629b28c7de0fbe3f60f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119384"
---
# <a name="getbuttonstate-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="abccd-103">Método getbuttonstate da classe Msvm \_ SyntheticMouse</span><span class="sxs-lookup"><span data-stu-id="abccd-103">GetButtonState method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="abccd-104">Recupera o estado atual do botão de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="abccd-104">Retrieves the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="abccd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="abccd-105">Syntax</span></span>


```mof
uint32 GetButtonState(
  [in]  uint32  buttonIndex,
  [out] boolean isDown
);
```



## <a name="parameters"></a><span data-ttu-id="abccd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="abccd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abccd-107">*buttonIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="abccd-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abccd-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="abccd-108">Type: **uint32**</span></span>

<span data-ttu-id="abccd-109">O índice de base 1 do botão a ser consultado.</span><span class="sxs-lookup"><span data-stu-id="abccd-109">The 1-based index of the button to query.</span></span>

</dd> <dt>

<span data-ttu-id="abccd-110">*IsDown* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="abccd-110">*isDown* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abccd-111">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="abccd-111">Type: **boolean**</span></span>

<span data-ttu-id="abccd-112">O estado de inatividade atual do botão.</span><span class="sxs-lookup"><span data-stu-id="abccd-112">The current down state of the button.</span></span> <span data-ttu-id="abccd-113">Um valor **verdadeiro** significa que o botão está inoperante.</span><span class="sxs-lookup"><span data-stu-id="abccd-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abccd-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="abccd-114">Return value</span></span>

<span data-ttu-id="abccd-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="abccd-115">Type: **uint32**</span></span>

<span data-ttu-id="abccd-116">Um valor de retorno igual A zero indica êxito.</span><span class="sxs-lookup"><span data-stu-id="abccd-116">A return value of zero indicates success.</span></span> <span data-ttu-id="abccd-117">Um valor diferente de zero indica uma falha de consulta.</span><span class="sxs-lookup"><span data-stu-id="abccd-117">A nonzero value indicates a query failure.</span></span>

<dl> <dt>

<span data-ttu-id="abccd-118">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="abccd-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="abccd-119">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="abccd-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="abccd-120">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="abccd-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="abccd-121">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="abccd-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="abccd-122">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="abccd-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="abccd-123">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="abccd-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="abccd-124">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="abccd-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="abccd-125">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="abccd-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="abccd-126">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="abccd-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="abccd-127">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="abccd-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="abccd-128">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="abccd-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="abccd-129">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="abccd-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="abccd-130">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="abccd-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="abccd-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="abccd-131">Remarks</span></span>

<span data-ttu-id="abccd-132">O acesso à classe [**Msvm \_ SyntheticMouse**](msvm-syntheticmouse.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="abccd-132">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="abccd-133">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="abccd-133">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="abccd-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abccd-134">Requirements</span></span>



| <span data-ttu-id="abccd-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="abccd-135">Requirement</span></span> | <span data-ttu-id="abccd-136">Valor</span><span class="sxs-lookup"><span data-stu-id="abccd-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abccd-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="abccd-137">Minimum supported client</span></span><br/> | <span data-ttu-id="abccd-138">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="abccd-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="abccd-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="abccd-139">Minimum supported server</span></span><br/> | <span data-ttu-id="abccd-140">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="abccd-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="abccd-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="abccd-141">Namespace</span></span><br/>                | <span data-ttu-id="abccd-142">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="abccd-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="abccd-143">MOF</span><span class="sxs-lookup"><span data-stu-id="abccd-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="abccd-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="abccd-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="abccd-145">DLL</span><span class="sxs-lookup"><span data-stu-id="abccd-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abccd-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="abccd-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="abccd-147">Consulte também</span><span class="sxs-lookup"><span data-stu-id="abccd-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abccd-148">**Msvm \_ SyntheticMouse**</span><span class="sxs-lookup"><span data-stu-id="abccd-148">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

