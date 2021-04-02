---
description: Recupera o estado de chave de uma chave.
ms.assetid: 4AEB732D-274E-42BB-AA97-9E4D30B81338
title: Método iskeypressed da classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.IsKeyPressed
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 44af7a3dc82c0d4d20a2e4c6aff21f7a47837490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165008"
---
# <a name="iskeypressed-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="737b8-103">Método iskeypressed da \_ classe Keyboard Msvm</span><span class="sxs-lookup"><span data-stu-id="737b8-103">IsKeyPressed method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="737b8-104">Recupera o estado de chave de uma chave.</span><span class="sxs-lookup"><span data-stu-id="737b8-104">Retrieves the key state of a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="737b8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="737b8-105">Syntax</span></span>


```mof
uint32 IsKeyPressed(
  [in]  uint32  keyCode,
  [out] boolean keyState
);
```



## <a name="parameters"></a><span data-ttu-id="737b8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="737b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="737b8-107">*KeyCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="737b8-107">*keyCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="737b8-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="737b8-108">Type: **uint32**</span></span>

<span data-ttu-id="737b8-109">O código de chave virtual da chave a ser consultada.</span><span class="sxs-lookup"><span data-stu-id="737b8-109">The virtual key code of the key to query.</span></span> <span data-ttu-id="737b8-110">Para obter a lista de códigos de chave virtual, consulte [**códigos de chave virtual**](../inputdev/virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="737b8-110">For the list for virtual-key codes, see [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="737b8-111">*keyState* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="737b8-111">*keyState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="737b8-112">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="737b8-112">Type: **boolean**</span></span>

<span data-ttu-id="737b8-113">O estado de inatividade atual da chave.</span><span class="sxs-lookup"><span data-stu-id="737b8-113">The current down state of the key.</span></span> <span data-ttu-id="737b8-114">Um valor **verdadeiro** significa que a chave está inoperante.</span><span class="sxs-lookup"><span data-stu-id="737b8-114">A **True** value means the key is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="737b8-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="737b8-115">Return value</span></span>

<span data-ttu-id="737b8-116">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="737b8-116">Type: **uint32**</span></span>

<span data-ttu-id="737b8-117">Um valor de retorno igual A zero indica êxito.</span><span class="sxs-lookup"><span data-stu-id="737b8-117">A return value of zero indicates success.</span></span> <span data-ttu-id="737b8-118">Um valor diferente de zero indica uma falha ao consultar o estado da chave.</span><span class="sxs-lookup"><span data-stu-id="737b8-118">A nonzero value indicates a failure to query the key state.</span></span>

<dl> <dt>

<span data-ttu-id="737b8-119">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="737b8-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="737b8-120">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="737b8-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="737b8-121">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="737b8-121">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="737b8-122">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="737b8-122">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="737b8-123">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="737b8-123">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="737b8-124">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="737b8-124">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="737b8-125">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="737b8-125">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="737b8-126">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="737b8-126">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="737b8-127">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="737b8-127">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="737b8-128">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="737b8-128">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="737b8-129">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="737b8-129">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="737b8-130">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="737b8-130">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="737b8-131">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="737b8-131">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="737b8-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="737b8-132">Remarks</span></span>

<span data-ttu-id="737b8-133">O método **Iskeypressd** sempre retornará **false** para o **\_ menu VK** (18), o **\_ controle VK** (17) e o **VK \_ Shift** (16) porque eles não são chaves reais em um teclado.</span><span class="sxs-lookup"><span data-stu-id="737b8-133">The **IsKeyPressed** method will always return **False** for the **VK\_MENU** (18), **VK\_CONTROL** (17), and **VK\_SHIFT** (16) because these are not real keys on a keyboard.</span></span> <span data-ttu-id="737b8-134">Esses códigos de chave virtual sempre são mapeados para **VK \_ LMENU** (164), **VK \_ LCONTROL** (162) e **VK \_ LSHIFT** (160), respectivamente, pelos métodos [**PressKey**](presskey-msvm-keyboard.md) e [**ReleaseKey**](releasekey-msvm-keyboard.md) .</span><span class="sxs-lookup"><span data-stu-id="737b8-134">These virtual key codes are always mapped to **VK\_LMENU** (164), **VK\_LCONTROL** (162), and **VK\_LSHIFT** (160), respectively, by the [**PressKey**](presskey-msvm-keyboard.md) and [**ReleaseKey**](releasekey-msvm-keyboard.md) methods.</span></span>

<span data-ttu-id="737b8-135">O acesso à classe de [**\_ teclado Msvm**](msvm-keyboard.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="737b8-135">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="737b8-136">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="737b8-136">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="737b8-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="737b8-137">Requirements</span></span>



| <span data-ttu-id="737b8-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="737b8-138">Requirement</span></span> | <span data-ttu-id="737b8-139">Valor</span><span class="sxs-lookup"><span data-stu-id="737b8-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="737b8-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="737b8-140">Minimum supported client</span></span><br/> | <span data-ttu-id="737b8-141">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="737b8-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="737b8-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="737b8-142">Minimum supported server</span></span><br/> | <span data-ttu-id="737b8-143">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="737b8-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="737b8-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="737b8-144">Namespace</span></span><br/>                | <span data-ttu-id="737b8-145">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="737b8-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="737b8-146">MOF</span><span class="sxs-lookup"><span data-stu-id="737b8-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="737b8-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="737b8-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="737b8-148">DLL</span><span class="sxs-lookup"><span data-stu-id="737b8-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="737b8-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="737b8-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="737b8-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="737b8-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="737b8-151">**\_Teclado Msvm**</span><span class="sxs-lookup"><span data-stu-id="737b8-151">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> <dt>

[<span data-ttu-id="737b8-152">**Códigos de chave virtual**</span><span class="sxs-lookup"><span data-stu-id="737b8-152">**Virtual-Key Codes**</span></span>](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

