---
description: Método getbuttonstate da classe Msvm_Ps2Mouse – recupera o estado atual do botão do dispositivo especificado.
ms.assetid: 7772A3AC-1677-44A7-9E5E-D31E90988705
title: Método getbuttonstate da classe Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.GetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 160134a2ae48bb23dc525eeded70b483484e0b71
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112194"
---
# <a name="getbuttonstate-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="a231d-103">Método getbuttonstate da classe Msvm \_ Ps2Mouse</span><span class="sxs-lookup"><span data-stu-id="a231d-103">GetButtonState method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="a231d-104">Recupera o estado atual do botão de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="a231d-104">Retrieves the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="a231d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a231d-105">Syntax</span></span>


```mof
uint32 GetButtonState(
  [in]  uint32  buttonIndex,
  [out] boolean buttonState
);
```



## <a name="parameters"></a><span data-ttu-id="a231d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a231d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a231d-107">*buttonIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a231d-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a231d-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a231d-108">Type: **uint32**</span></span>

<span data-ttu-id="a231d-109">O índice de base 1 do botão a ser consultado.</span><span class="sxs-lookup"><span data-stu-id="a231d-109">The 1-based index of the button to query.</span></span>

</dd> <dt>

<span data-ttu-id="a231d-110">*botão de* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a231d-110">*buttonState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a231d-111">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a231d-111">Type: **boolean**</span></span>

<span data-ttu-id="a231d-112">O estado de inatividade atual do botão.</span><span class="sxs-lookup"><span data-stu-id="a231d-112">The current down state of the button.</span></span> <span data-ttu-id="a231d-113">Um valor **verdadeiro** significa que o botão está inoperante.</span><span class="sxs-lookup"><span data-stu-id="a231d-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a231d-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a231d-114">Return value</span></span>

<span data-ttu-id="a231d-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a231d-115">Type: **uint32**</span></span>

<span data-ttu-id="a231d-116">Um valor de retorno igual A zero indica êxito.</span><span class="sxs-lookup"><span data-stu-id="a231d-116">A return value of zero indicates success.</span></span> <span data-ttu-id="a231d-117">Um valor diferente de zero indica uma falha de consulta.</span><span class="sxs-lookup"><span data-stu-id="a231d-117">A nonzero value indicates a query failure.</span></span>

<dl> <dt>

<span data-ttu-id="a231d-118">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="a231d-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a231d-119">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="a231d-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a231d-120">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="a231d-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a231d-121">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="a231d-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a231d-122">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="a231d-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a231d-123">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="a231d-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a231d-124">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="a231d-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a231d-125">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="a231d-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a231d-126">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="a231d-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a231d-127">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="a231d-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a231d-128">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="a231d-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a231d-129">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="a231d-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a231d-130">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="a231d-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="a231d-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="a231d-131">Remarks</span></span>

<span data-ttu-id="a231d-132">O acesso à classe [**Msvm \_ Ps2Mouse**](msvm-ps2mouse.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="a231d-132">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a231d-133">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a231d-133">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a231d-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a231d-134">Requirements</span></span>



| <span data-ttu-id="a231d-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="a231d-135">Requirement</span></span> | <span data-ttu-id="a231d-136">Valor</span><span class="sxs-lookup"><span data-stu-id="a231d-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a231d-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a231d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="a231d-138">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a231d-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a231d-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a231d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="a231d-140">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a231d-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a231d-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="a231d-141">Namespace</span></span><br/>                | <span data-ttu-id="a231d-142">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="a231d-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a231d-143">MOF</span><span class="sxs-lookup"><span data-stu-id="a231d-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a231d-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a231d-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a231d-145">DLL</span><span class="sxs-lookup"><span data-stu-id="a231d-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a231d-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a231d-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a231d-147">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a231d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a231d-148">**Msvm \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="a231d-148">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

