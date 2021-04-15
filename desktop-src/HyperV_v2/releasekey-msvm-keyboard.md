---
description: Simula uma versão de chave.
ms.assetid: EAE84BD5-ECEA-44E7-A7AB-CD18299DF2FE
title: Método ReleaseKey da classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.ReleaseKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2193a4b78128ff3f65e98b4425528a51f6cf5916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506210"
---
# <a name="releasekey-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="daf97-103">Método ReleaseKey da classe de \_ teclado Msvm</span><span class="sxs-lookup"><span data-stu-id="daf97-103">ReleaseKey method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="daf97-104">Simula uma versão de chave.</span><span class="sxs-lookup"><span data-stu-id="daf97-104">Simulates a key release.</span></span> <span data-ttu-id="daf97-105">Quando for bem-sucedido, a chave estará no estado ativo.</span><span class="sxs-lookup"><span data-stu-id="daf97-105">When successful, the key will be in the up state.</span></span>

## <a name="syntax"></a><span data-ttu-id="daf97-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="daf97-106">Syntax</span></span>


```mof
uint32 ReleaseKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a><span data-ttu-id="daf97-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="daf97-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="daf97-108">*KeyCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="daf97-108">*keyCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="daf97-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="daf97-109">Type: **uint32**</span></span>

<span data-ttu-id="daf97-110">O código de chave virtual da chave a ser liberada.</span><span class="sxs-lookup"><span data-stu-id="daf97-110">The virtual key code of the key to release.</span></span> <span data-ttu-id="daf97-111">Para obter a lista de códigos de chave virtual, consulte [**códigos de chave virtual**](../inputdev/virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="daf97-111">For the list for virtual-key codes, see [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="daf97-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="daf97-112">Return value</span></span>

<span data-ttu-id="daf97-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="daf97-113">Type: **uint32**</span></span>

<span data-ttu-id="daf97-114">Um valor de retorno igual A zero indica êxito.</span><span class="sxs-lookup"><span data-stu-id="daf97-114">A return value of zero indicates success.</span></span> <span data-ttu-id="daf97-115">Um valor diferente de zero indica uma falha ao modificar o estado da chave.</span><span class="sxs-lookup"><span data-stu-id="daf97-115">A nonzero value indicates a failure to modify the key state.</span></span>

<dl> <dt>

<span data-ttu-id="daf97-116">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="daf97-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="daf97-117">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="daf97-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="daf97-118">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="daf97-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="daf97-119">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="daf97-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="daf97-120">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="daf97-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="daf97-121">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="daf97-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="daf97-122">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="daf97-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="daf97-123">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="daf97-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="daf97-124">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="daf97-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="daf97-125">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="daf97-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="daf97-126">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="daf97-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="daf97-127">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="daf97-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="daf97-128">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="daf97-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="daf97-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="daf97-129">Remarks</span></span>

<span data-ttu-id="daf97-130">O método **ReleaseKey** mapeia referências ao **\_ menu VK** (18), **\_ controle VK** (17) e **VK \_ Shift** (16) para **VK \_ LMENU** (164), **VK \_ LCONTROL** (162) e **VK \_ LSHIFT** (160), respectivamente, porque os códigos de **\_ menu VK**, **VK \_ Control** e **VK \_ Shift** Virtual Key não representam chaves reais em um teclado.</span><span class="sxs-lookup"><span data-stu-id="daf97-130">The **ReleaseKey** method maps references to the **VK\_MENU** (18), **VK\_CONTROL** (17), and **VK\_SHIFT** (16) to **VK\_LMENU** (164), **VK\_LCONTROL** (162), and **VK\_LSHIFT** (160), respectively, because the **VK\_MENU**, **VK\_CONTROL**, and **VK\_SHIFT** virtual key codes do not represent real keys on a keyboard.</span></span>

<span data-ttu-id="daf97-131">O acesso à classe de [**\_ teclado Msvm**](msvm-keyboard.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="daf97-131">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="daf97-132">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="daf97-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="daf97-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="daf97-133">Requirements</span></span>



| <span data-ttu-id="daf97-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="daf97-134">Requirement</span></span> | <span data-ttu-id="daf97-135">Valor</span><span class="sxs-lookup"><span data-stu-id="daf97-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="daf97-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="daf97-136">Minimum supported client</span></span><br/> | <span data-ttu-id="daf97-137">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="daf97-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="daf97-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="daf97-138">Minimum supported server</span></span><br/> | <span data-ttu-id="daf97-139">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="daf97-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="daf97-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="daf97-140">Namespace</span></span><br/>                | <span data-ttu-id="daf97-141">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="daf97-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="daf97-142">MOF</span><span class="sxs-lookup"><span data-stu-id="daf97-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="daf97-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="daf97-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="daf97-144">DLL</span><span class="sxs-lookup"><span data-stu-id="daf97-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="daf97-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="daf97-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="daf97-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="daf97-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daf97-147">**\_Teclado Msvm**</span><span class="sxs-lookup"><span data-stu-id="daf97-147">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> <dt>

[<span data-ttu-id="daf97-148">**Códigos de chave virtual**</span><span class="sxs-lookup"><span data-stu-id="daf97-148">**Virtual-Key Codes**</span></span>](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

