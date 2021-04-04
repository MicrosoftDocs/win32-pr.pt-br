---
description: Simula uma sequência de chaves usando códigos de verificação.
ms.assetid: F67D2FBA-3CE0-4135-9043-FAB59381DE3C
title: Método TypeScancodes da classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeScancodes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 97479a1a0926894f72472b7459f77cd9325ac6fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647364"
---
# <a name="typescancodes-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="e7888-103">Método TypeScancodes da classe de \_ teclado Msvm</span><span class="sxs-lookup"><span data-stu-id="e7888-103">TypeScancodes method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="e7888-104">Simula uma sequência de chaves usando códigos de verificação.</span><span class="sxs-lookup"><span data-stu-id="e7888-104">Simulates a key sequence using scan codes.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7888-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e7888-105">Syntax</span></span>


```mof
uint32 TypeScancodes(
  [in] uint8 Scancodes[]
);
```



## <a name="parameters"></a><span data-ttu-id="e7888-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7888-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7888-107">*Scancodes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7888-107">*Scancodes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7888-108">Tipo: **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="e7888-108">Type: **uint8\[\]**</span></span>

<span data-ttu-id="e7888-109">Uma matriz que contém os códigos de verificação a serem digitados.</span><span class="sxs-lookup"><span data-stu-id="e7888-109">An array that contains the scan codes to type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7888-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e7888-110">Return value</span></span>

<span data-ttu-id="e7888-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e7888-111">Type: **uint32**</span></span>

<span data-ttu-id="e7888-112">Esse método retornará 0 se tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="e7888-112">This method returns 0 if it succeeds.</span></span> <span data-ttu-id="e7888-113">Qualquer outro valor de retorno indica um erro.</span><span class="sxs-lookup"><span data-stu-id="e7888-113">Any other return value indicates an error.</span></span> <span data-ttu-id="e7888-114">O valor de retorno pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e7888-114">The return value can be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e7888-115">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="e7888-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e7888-116">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="e7888-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e7888-117">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="e7888-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e7888-118">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="e7888-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e7888-119">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="e7888-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e7888-120">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="e7888-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e7888-121">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="e7888-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e7888-122">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="e7888-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e7888-123">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="e7888-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e7888-124">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="e7888-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e7888-125">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="e7888-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e7888-126">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="e7888-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e7888-127">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="e7888-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="e7888-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7888-128">Remarks</span></span>

<span data-ttu-id="e7888-129">O acesso à classe de [**\_ teclado Msvm**](msvm-keyboard.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="e7888-129">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e7888-130">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e7888-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7888-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7888-131">Requirements</span></span>



| <span data-ttu-id="e7888-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7888-132">Requirement</span></span> | <span data-ttu-id="e7888-133">Valor</span><span class="sxs-lookup"><span data-stu-id="e7888-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7888-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7888-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e7888-135">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e7888-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e7888-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7888-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e7888-137">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e7888-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e7888-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="e7888-138">Namespace</span></span><br/>                | <span data-ttu-id="e7888-139">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e7888-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e7888-140">MOF</span><span class="sxs-lookup"><span data-stu-id="e7888-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7888-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7888-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7888-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e7888-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7888-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e7888-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e7888-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7888-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7888-145">**\_Teclado Msvm**</span><span class="sxs-lookup"><span data-stu-id="e7888-145">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

