---
description: Ajusta a coordenada z do controle de roda do dispositivo apontador.
ms.assetid: FF1929EE-4A2D-4761-8919-488369FAEE1F
title: Método SetScrollPosition da classe Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.SetScrollPosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ffec8e05acf2210c55038edde5def8373e900ed7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829021"
---
# <a name="setscrollposition-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="24f14-103">Método SetScrollPosition da \_ classe Ps2Mouse Msvm</span><span class="sxs-lookup"><span data-stu-id="24f14-103">SetScrollPosition method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="24f14-104">Ajusta a coordenada z do controle de roda do dispositivo apontador.</span><span class="sxs-lookup"><span data-stu-id="24f14-104">Adjusts the z-coordinate of the wheel control of the pointing device.</span></span> <span data-ttu-id="24f14-105">Os valores gravados nessa propriedade são sempre deslocamentos de coordenadas relativos.</span><span class="sxs-lookup"><span data-stu-id="24f14-105">Values written to this property are always relative coordinate offsets.</span></span>

## <a name="syntax"></a><span data-ttu-id="24f14-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24f14-106">Syntax</span></span>


```mof
uint32 SetScrollPosition(
  [in] sint8 scrollPositionDelta
);
```



## <a name="parameters"></a><span data-ttu-id="24f14-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24f14-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24f14-108">*scrollPositionDelta* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="24f14-108">*scrollPositionDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24f14-109">Tipo: **sint8**</span><span class="sxs-lookup"><span data-stu-id="24f14-109">Type: **sint8**</span></span>

<span data-ttu-id="24f14-110">O Delta da posição de rolagem.</span><span class="sxs-lookup"><span data-stu-id="24f14-110">The delta of the scroll position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24f14-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="24f14-111">Return value</span></span>

<span data-ttu-id="24f14-112">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24f14-112">Type: **uint32**</span></span>

<span data-ttu-id="24f14-113">Um valor de retorno igual A zero indica êxito.</span><span class="sxs-lookup"><span data-stu-id="24f14-113">A return value of zero indicates success.</span></span> <span data-ttu-id="24f14-114">Um valor diferente de zero indica uma falha ao alterar a posição de rolagem.</span><span class="sxs-lookup"><span data-stu-id="24f14-114">A nonzero value indicates a failure to alter the scroll position.</span></span>

<dl> <dt>

<span data-ttu-id="24f14-115">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="24f14-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="24f14-116">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="24f14-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="24f14-117">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="24f14-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="24f14-118">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="24f14-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="24f14-119">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="24f14-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="24f14-120">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="24f14-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="24f14-121">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="24f14-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="24f14-122">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="24f14-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="24f14-123">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="24f14-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="24f14-124">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="24f14-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="24f14-125">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="24f14-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="24f14-126">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="24f14-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="24f14-127">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="24f14-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="24f14-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="24f14-128">Remarks</span></span>

<span data-ttu-id="24f14-129">O acesso à classe [**Msvm \_ Ps2Mouse**](msvm-ps2mouse.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="24f14-129">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="24f14-130">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="24f14-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="24f14-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24f14-131">Requirements</span></span>



| <span data-ttu-id="24f14-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="24f14-132">Requirement</span></span> | <span data-ttu-id="24f14-133">Valor</span><span class="sxs-lookup"><span data-stu-id="24f14-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24f14-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24f14-134">Minimum supported client</span></span><br/> | <span data-ttu-id="24f14-135">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="24f14-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="24f14-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24f14-136">Minimum supported server</span></span><br/> | <span data-ttu-id="24f14-137">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="24f14-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="24f14-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="24f14-138">Namespace</span></span><br/>                | <span data-ttu-id="24f14-139">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="24f14-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="24f14-140">MOF</span><span class="sxs-lookup"><span data-stu-id="24f14-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24f14-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="24f14-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="24f14-142">DLL</span><span class="sxs-lookup"><span data-stu-id="24f14-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24f14-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="24f14-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="24f14-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="24f14-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24f14-145">**Msvm \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="24f14-145">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

