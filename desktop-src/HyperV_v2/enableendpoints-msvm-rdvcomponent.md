---
description: Solicita que o dispositivo virtual Serviços de Área de Trabalho Remota inicie uma conexão de pipe com a máquina virtual.
ms.assetid: e53238ee-8264-416b-8855-193c28089cfa
title: Método EnableEndPoints da classe Msvm_RdvComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponent.EnableEndPoints
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a668e6a2605a52c7021f630145d6e4897e1c76ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164624"
---
# <a name="enableendpoints-method-of-the-msvm_rdvcomponent-class"></a><span data-ttu-id="1f459-103">Método EnableEndPoints da \_ classe RdvComponent Msvm</span><span class="sxs-lookup"><span data-stu-id="1f459-103">EnableEndPoints method of the Msvm\_RdvComponent class</span></span>

<span data-ttu-id="1f459-104">Solicita que o dispositivo virtual Serviços de Área de Trabalho Remota inicie uma conexão de pipe com a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1f459-104">Requests the Remote Desktop Services virtual device to start a pipe connection with the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f459-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f459-105">Syntax</span></span>


```mof
uint32 EnableEndPoints();
```



## <a name="parameters"></a><span data-ttu-id="1f459-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f459-106">Parameters</span></span>

<span data-ttu-id="1f459-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1f459-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1f459-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1f459-108">Return value</span></span>

<span data-ttu-id="1f459-109">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1f459-109">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="1f459-110">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="1f459-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1f459-111">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="1f459-111">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1f459-112">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="1f459-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="1f459-113">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="1f459-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="1f459-114">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="1f459-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="1f459-115">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="1f459-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="1f459-116">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="1f459-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="1f459-117">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="1f459-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="1f459-118">**Memória insuficiente** (32774)</span><span class="sxs-lookup"><span data-stu-id="1f459-118">**Out of memory** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="1f459-119">**Arquivo não encontrado** (32775)</span><span class="sxs-lookup"><span data-stu-id="1f459-119">**File not found** (32775)</span></span>
</dt> <dt>

 <span data-ttu-id="1f459-120">(32776)</span><span class="sxs-lookup"><span data-stu-id="1f459-120">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="1f459-121">(32777)</span><span class="sxs-lookup"><span data-stu-id="1f459-121">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="1f459-122">(32778)</span><span class="sxs-lookup"><span data-stu-id="1f459-122">(32778)</span></span>
</dt> <dt>

 <span data-ttu-id="1f459-123">(32779)</span><span class="sxs-lookup"><span data-stu-id="1f459-123">(32779)</span></span>
</dt> <dt>

 <span data-ttu-id="1f459-124">(32780)</span><span class="sxs-lookup"><span data-stu-id="1f459-124">(32780)</span></span>
</dt> <dt>

 <span data-ttu-id="1f459-125">(32781)</span><span class="sxs-lookup"><span data-stu-id="1f459-125">(32781)</span></span>
</dt> <dt>

 <span data-ttu-id="1f459-126">(32782)</span><span class="sxs-lookup"><span data-stu-id="1f459-126">(32782)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1f459-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f459-127">Requirements</span></span>



| <span data-ttu-id="1f459-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f459-128">Requirement</span></span> | <span data-ttu-id="1f459-129">Valor</span><span class="sxs-lookup"><span data-stu-id="1f459-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f459-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f459-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1f459-131">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1f459-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1f459-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f459-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1f459-133">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1f459-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1f459-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="1f459-134">Namespace</span></span><br/>                | <span data-ttu-id="1f459-135">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="1f459-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1f459-136">MOF</span><span class="sxs-lookup"><span data-stu-id="1f459-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f459-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1f459-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1f459-138">DLL</span><span class="sxs-lookup"><span data-stu-id="1f459-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f459-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1f459-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1f459-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f459-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f459-141">**Msvm \_ RdvComponent**</span><span class="sxs-lookup"><span data-stu-id="1f459-141">**Msvm\_RdvComponent**</span></span>](msvm-rdvcomponent.md)
</dt> </dl>

 

 




