---
description: Contém métodos que gerenciam o brilho do monitor.
ms.assetid: e7e4139e-b985-4163-9c95-03008a2cc8cb
title: Classe WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods
- WmiMonitorBrightnessMethods.Active
- WmiMonitorBrightnessMethods.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 36fe823703d5d5e4f1f6008d02c600828fe2b53f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810206"
---
# <a name="wmimonitorbrightnessmethods-class"></a><span data-ttu-id="78949-103">Classe WmiMonitorBrightnessMethods</span><span class="sxs-lookup"><span data-stu-id="78949-103">WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="78949-104">A classe WMI **WmiMonitorBrightnessMethods** contém métodos que gerenciam o brilho do monitor.</span><span class="sxs-lookup"><span data-stu-id="78949-104">The **WmiMonitorBrightnessMethods** WMI class contains methods that manage monitor brightness.</span></span>

## <a name="syntax"></a><span data-ttu-id="78949-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78949-105">Syntax</span></span>

``` syntax
class WmiMonitorBrightnessMethods
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a><span data-ttu-id="78949-106">Membros</span><span class="sxs-lookup"><span data-stu-id="78949-106">Members</span></span>

<span data-ttu-id="78949-107">A classe **WmiMonitorBrightnessMethods** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="78949-107">The **WmiMonitorBrightnessMethods** class has these types of members:</span></span>

-   [<span data-ttu-id="78949-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="78949-108">Methods</span></span>](#wmimonitorbrightnessmethods-class)
-   [<span data-ttu-id="78949-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="78949-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="78949-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="78949-110">Methods</span></span>

<span data-ttu-id="78949-111">A classe **WmiMonitorBrightnessMethods** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="78949-111">The **WmiMonitorBrightnessMethods** class has these methods.</span></span>



| <span data-ttu-id="78949-112">Método</span><span class="sxs-lookup"><span data-stu-id="78949-112">Method</span></span>                                                                                                         | <span data-ttu-id="78949-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="78949-113">Description</span></span>                                                    |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| [<span data-ttu-id="78949-114">**WmiRevertToPolicyBrightness**</span><span class="sxs-lookup"><span data-stu-id="78949-114">**WmiRevertToPolicyBrightness**</span></span>](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) | <span data-ttu-id="78949-115">Define o brilho de volta para a configuração de política.</span><span class="sxs-lookup"><span data-stu-id="78949-115">Sets the brightness back to the policy setting.</span></span><br/>     |
| [<span data-ttu-id="78949-116">**WmiSetALSBrightness**</span><span class="sxs-lookup"><span data-stu-id="78949-116">**WmiSetALSBrightness**</span></span>](wmisetalsbrightness-method-in-class-wmimonitorbrightnessmethods.md)                 | <span data-ttu-id="78949-117">Define o valor de brilho do sensor de luz ambiente.</span><span class="sxs-lookup"><span data-stu-id="78949-117">Sets the ambient light sensor brightness value.</span></span><br/>     |
| [<span data-ttu-id="78949-118">**WmiSetALSBrightnessState**</span><span class="sxs-lookup"><span data-stu-id="78949-118">**WmiSetALSBrightnessState**</span></span>](wmisetalsbrightnessstate-method-in-class-wmimonitorbrightnessmethods.md)       | <span data-ttu-id="78949-119">Controla o estado de brilho do sensor de luz ambiente.</span><span class="sxs-lookup"><span data-stu-id="78949-119">Controls the ambient light sensor brightness state.</span></span><br/> |
| [<span data-ttu-id="78949-120">**WmiSetBrightness**</span><span class="sxs-lookup"><span data-stu-id="78949-120">**WmiSetBrightness**</span></span>](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md)                       | <span data-ttu-id="78949-121">Define o brilho do monitor.</span><span class="sxs-lookup"><span data-stu-id="78949-121">Sets the monitor brightness.</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="78949-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="78949-122">Properties</span></span>

<span data-ttu-id="78949-123">A classe **WmiMonitorBrightnessMethods** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="78949-123">The **WmiMonitorBrightnessMethods** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="78949-124">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="78949-124">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78949-125">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="78949-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="78949-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78949-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78949-127">Indica o monitor ativo.</span><span class="sxs-lookup"><span data-stu-id="78949-127">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="78949-128">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="78949-128">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78949-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78949-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78949-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="78949-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78949-131">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="78949-131">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="78949-132">Nome da instância de monitor específica.</span><span class="sxs-lookup"><span data-stu-id="78949-132">Name of the specific monitor instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="78949-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78949-133">Requirements</span></span>



| <span data-ttu-id="78949-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="78949-134">Requirement</span></span> | <span data-ttu-id="78949-135">Valor</span><span class="sxs-lookup"><span data-stu-id="78949-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78949-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78949-136">Minimum supported client</span></span><br/> | <span data-ttu-id="78949-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78949-137">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="78949-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78949-138">Minimum supported server</span></span><br/> | <span data-ttu-id="78949-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78949-139">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="78949-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="78949-140">Namespace</span></span><br/>                | <span data-ttu-id="78949-141">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="78949-141">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="78949-142">MOF</span><span class="sxs-lookup"><span data-stu-id="78949-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78949-143"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="78949-143"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="78949-144">DLL</span><span class="sxs-lookup"><span data-stu-id="78949-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78949-145"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78949-145"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78949-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="78949-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78949-147">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="78949-147">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




