---
description: Simula uma sequência de teclas Ctrl + Alt + Del.
ms.assetid: C24C9C42-844F-4560-B8C1-0054F5E913D6
title: Método TypeCtrlAltDel da classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeCtrlAltDel
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 64ebc4bddf8adccd7098cafed1df43d1cf1cb4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297283"
---
# <a name="typectrlaltdel-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="4ca77-103">Método TypeCtrlAltDel da classe de \_ teclado Msvm</span><span class="sxs-lookup"><span data-stu-id="4ca77-103">TypeCtrlAltDel method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="4ca77-104">Simula uma sequência de teclas Ctrl + Alt + Del.</span><span class="sxs-lookup"><span data-stu-id="4ca77-104">Simulates a Ctrl+Alt+Del key sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ca77-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ca77-105">Syntax</span></span>


```mof
uint32 TypeCtrlAltDel();
```



## <a name="parameters"></a><span data-ttu-id="4ca77-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ca77-106">Parameters</span></span>

<span data-ttu-id="4ca77-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4ca77-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4ca77-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4ca77-108">Return value</span></span>

<span data-ttu-id="4ca77-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4ca77-109">Type: **uint32**</span></span>

<span data-ttu-id="4ca77-110">Um valor de retorno igual A zero indica êxito.</span><span class="sxs-lookup"><span data-stu-id="4ca77-110">A return value of zero indicates success.</span></span> <span data-ttu-id="4ca77-111">Um valor diferente de zero indica uma falha ao enviar.</span><span class="sxs-lookup"><span data-stu-id="4ca77-111">A nonzero value indicates a failure to send.</span></span>

<dl> <dt>

<span data-ttu-id="4ca77-112">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="4ca77-112">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4ca77-113">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="4ca77-113">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4ca77-114">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="4ca77-114">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="4ca77-115">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="4ca77-115">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="4ca77-116">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="4ca77-116">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="4ca77-117">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="4ca77-117">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="4ca77-118">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="4ca77-118">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="4ca77-119">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="4ca77-119">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="4ca77-120">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="4ca77-120">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="4ca77-121">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="4ca77-121">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="4ca77-122">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="4ca77-122">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="4ca77-123">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="4ca77-123">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="4ca77-124">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="4ca77-124">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="4ca77-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ca77-125">Remarks</span></span>

<span data-ttu-id="4ca77-126">O acesso à classe de [**\_ teclado Msvm**](msvm-keyboard.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="4ca77-126">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4ca77-127">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="4ca77-127">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ca77-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ca77-128">Requirements</span></span>



| <span data-ttu-id="4ca77-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ca77-129">Requirement</span></span> | <span data-ttu-id="4ca77-130">Valor</span><span class="sxs-lookup"><span data-stu-id="4ca77-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ca77-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ca77-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4ca77-132">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4ca77-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4ca77-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ca77-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4ca77-134">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4ca77-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4ca77-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ca77-135">Namespace</span></span><br/>                | <span data-ttu-id="4ca77-136">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="4ca77-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4ca77-137">MOF</span><span class="sxs-lookup"><span data-stu-id="4ca77-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ca77-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4ca77-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ca77-139">DLL</span><span class="sxs-lookup"><span data-stu-id="4ca77-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ca77-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4ca77-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4ca77-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ca77-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ca77-142">**\_Teclado Msvm**</span><span class="sxs-lookup"><span data-stu-id="4ca77-142">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

