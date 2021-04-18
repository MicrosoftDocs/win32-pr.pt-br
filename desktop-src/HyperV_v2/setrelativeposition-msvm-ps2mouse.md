---
description: Desloca a posição do ponteiro do mouse pelos deltas horizontais e verticais especificados.
ms.assetid: C74E4BEA-C7E1-44C7-B4FC-8926F23DF1FE
title: Método SetRelativePosition da classe Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.SetRelativePosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b7f4d10f48bce4b33cd4965f08633b85b5a738bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753467"
---
# <a name="setrelativeposition-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="6ec79-103">Método SetRelativePosition da \_ classe Ps2Mouse Msvm</span><span class="sxs-lookup"><span data-stu-id="6ec79-103">SetRelativePosition method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="6ec79-104">Desloca a posição do ponteiro do mouse pelos deltas horizontais e verticais especificados.</span><span class="sxs-lookup"><span data-stu-id="6ec79-104">Offsets the position of the mouse pointer by the specified horizontal and vertical deltas.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ec79-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ec79-105">Syntax</span></span>


```mof
uint32 SetRelativePosition(
  [in] sint8 horizontalDelta,
  [in] sint8 verticalDelta
);
```



## <a name="parameters"></a><span data-ttu-id="6ec79-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ec79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ec79-107">*horizontalDelta* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6ec79-107">*horizontalDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ec79-108">Tipo: **sint8**</span><span class="sxs-lookup"><span data-stu-id="6ec79-108">Type: **sint8**</span></span>

<span data-ttu-id="6ec79-109">A alteração horizontal para a posição do mouse, em pixels.</span><span class="sxs-lookup"><span data-stu-id="6ec79-109">The horizontal change for the mouse position, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="6ec79-110">*verticalDelta* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6ec79-110">*verticalDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ec79-111">Tipo: **sint8**</span><span class="sxs-lookup"><span data-stu-id="6ec79-111">Type: **sint8**</span></span>

<span data-ttu-id="6ec79-112">A alteração vertical da posição do mouse, em pixels.</span><span class="sxs-lookup"><span data-stu-id="6ec79-112">The vertical change for the mouse position, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ec79-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6ec79-113">Return value</span></span>

<span data-ttu-id="6ec79-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ec79-114">Type: **uint32**</span></span>

<span data-ttu-id="6ec79-115">Um valor de retorno igual A zero indica êxito.</span><span class="sxs-lookup"><span data-stu-id="6ec79-115">A return value of zero indicates success.</span></span> <span data-ttu-id="6ec79-116">Um valor diferente de zero indica uma falha ao alterar a posição do mouse.</span><span class="sxs-lookup"><span data-stu-id="6ec79-116">A nonzero value indicates a failure to alter the mouse position.</span></span>

<dl> <dt>

<span data-ttu-id="6ec79-117">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="6ec79-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6ec79-118">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="6ec79-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6ec79-119">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="6ec79-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="6ec79-120">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="6ec79-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6ec79-121">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="6ec79-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="6ec79-122">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="6ec79-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="6ec79-123">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="6ec79-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="6ec79-124">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="6ec79-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6ec79-125">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="6ec79-125">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="6ec79-126">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="6ec79-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="6ec79-127">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="6ec79-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="6ec79-128">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="6ec79-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="6ec79-129">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="6ec79-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="6ec79-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ec79-130">Remarks</span></span>

<span data-ttu-id="6ec79-131">O acesso à classe [**Msvm \_ Ps2Mouse**](msvm-ps2mouse.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="6ec79-131">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="6ec79-132">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="6ec79-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ec79-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ec79-133">Requirements</span></span>



| <span data-ttu-id="6ec79-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ec79-134">Requirement</span></span> | <span data-ttu-id="6ec79-135">Valor</span><span class="sxs-lookup"><span data-stu-id="6ec79-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec79-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ec79-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6ec79-137">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6ec79-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6ec79-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ec79-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6ec79-139">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6ec79-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6ec79-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="6ec79-140">Namespace</span></span><br/>                | <span data-ttu-id="6ec79-141">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="6ec79-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6ec79-142">MOF</span><span class="sxs-lookup"><span data-stu-id="6ec79-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ec79-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ec79-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ec79-144">DLL</span><span class="sxs-lookup"><span data-stu-id="6ec79-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ec79-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6ec79-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6ec79-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ec79-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ec79-147">**Msvm \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="6ec79-147">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

