---
description: Simula uma sequência de teclas de liberação de prensa.
ms.assetid: 4166BA71-315D-41BD-857C-48AFB702911E
title: Método TypeKey da classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1b978da48600cc52472ab8bdec011ddbaa5ff624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922553"
---
# <a name="typekey-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="b4574-103">Método TypeKey da classe de \_ teclado Msvm</span><span class="sxs-lookup"><span data-stu-id="b4574-103">TypeKey method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="b4574-104">Simula uma sequência de teclas de liberação de prensa.</span><span class="sxs-lookup"><span data-stu-id="b4574-104">Simulates a press-release key sequence.</span></span> <span data-ttu-id="b4574-105">Isso é equivalente a chamar [**PressKey**](presskey-msvm-keyboard.md) seguido por [**ReleaseKey**](releasekey-msvm-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="b4574-105">This is equivalent to calling [**PressKey**](presskey-msvm-keyboard.md) followed by [**ReleaseKey**](releasekey-msvm-keyboard.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b4574-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4574-106">Syntax</span></span>


```mof
uint32 TypeKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a><span data-ttu-id="b4574-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4574-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4574-108">*KeyCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b4574-108">*keyCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4574-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4574-109">Type: **uint32**</span></span>

<span data-ttu-id="b4574-110">O código de chave virtual da chave a ser pressionada.</span><span class="sxs-lookup"><span data-stu-id="b4574-110">The virtual key code of the key to press.</span></span> <span data-ttu-id="b4574-111">Para obter a lista de códigos de chave virtual, consulte [**códigos de chave virtual**](../inputdev/virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b4574-111">For the list for virtual-key codes, see [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4574-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b4574-112">Return value</span></span>

<span data-ttu-id="b4574-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4574-113">Type: **uint32**</span></span>

<span data-ttu-id="b4574-114">Um valor de retorno igual A zero indica êxito.</span><span class="sxs-lookup"><span data-stu-id="b4574-114">A return value of zero indicates success.</span></span> <span data-ttu-id="b4574-115">Um valor diferente de zero indica uma falha ao modificar o estado da chave.</span><span class="sxs-lookup"><span data-stu-id="b4574-115">A nonzero value indicates a failure to modify the key state.</span></span>

<dl> <dt>

<span data-ttu-id="b4574-116">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="b4574-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b4574-117">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="b4574-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b4574-118">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="b4574-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b4574-119">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="b4574-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b4574-120">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="b4574-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b4574-121">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="b4574-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b4574-122">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="b4574-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b4574-123">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="b4574-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b4574-124">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="b4574-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b4574-125">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="b4574-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b4574-126">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="b4574-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b4574-127">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="b4574-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b4574-128">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="b4574-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="b4574-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4574-129">Remarks</span></span>

<span data-ttu-id="b4574-130">O acesso à classe de [**\_ teclado Msvm**](msvm-keyboard.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="b4574-130">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b4574-131">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b4574-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4574-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4574-132">Requirements</span></span>



| <span data-ttu-id="b4574-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4574-133">Requirement</span></span> | <span data-ttu-id="b4574-134">Valor</span><span class="sxs-lookup"><span data-stu-id="b4574-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4574-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4574-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b4574-136">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b4574-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b4574-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4574-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b4574-138">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b4574-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b4574-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="b4574-139">Namespace</span></span><br/>                | <span data-ttu-id="b4574-140">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="b4574-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b4574-141">MOF</span><span class="sxs-lookup"><span data-stu-id="b4574-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4574-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b4574-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b4574-143">DLL</span><span class="sxs-lookup"><span data-stu-id="b4574-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4574-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b4574-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b4574-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4574-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4574-146">**\_Teclado Msvm**</span><span class="sxs-lookup"><span data-stu-id="b4574-146">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> <dt>

[<span data-ttu-id="b4574-147">**Códigos de chave virtual**</span><span class="sxs-lookup"><span data-stu-id="b4574-147">**Virtual-Key Codes**</span></span>](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

