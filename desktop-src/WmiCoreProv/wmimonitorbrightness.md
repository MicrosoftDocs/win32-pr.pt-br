---
description: Representa os parâmetros de brilho de um monitor de computador.
ms.assetid: 01fa3efc-2a1d-4405-989f-2c180842c6b9
title: Classe WmiMonitorBrightness
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightness
- WmiMonitorBrightness.Active
- WmiMonitorBrightness.CurrentBrightness
- WmiMonitorBrightness.InstanceName
- WmiMonitorBrightness.Level
- WmiMonitorBrightness.Levels
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: b8d16c8dc20291a03fb205441c8826c85125970c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760663"
---
# <a name="wmimonitorbrightness-class"></a><span data-ttu-id="af799-103">Classe WmiMonitorBrightness</span><span class="sxs-lookup"><span data-stu-id="af799-103">WmiMonitorBrightness class</span></span>

<span data-ttu-id="af799-104">A classe WMI **WmiMonitorBrightness** representa os parâmetros de brilho de um monitor de computador.</span><span class="sxs-lookup"><span data-stu-id="af799-104">The **WmiMonitorBrightness** WMI class represents the brightness parameters of a computer monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="af799-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af799-105">Syntax</span></span>

``` syntax
class WmiMonitorBrightness : MSMonitorClass
{
  boolean Active;
  uint8   CurrentBrightness;
          InstanceName;
  uint8   Level[];
  uint32  Levels;
};
```

## <a name="members"></a><span data-ttu-id="af799-106">Membros</span><span class="sxs-lookup"><span data-stu-id="af799-106">Members</span></span>

<span data-ttu-id="af799-107">A classe **WmiMonitorBrightness** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="af799-107">The **WmiMonitorBrightness** class has these types of members:</span></span>

-   [<span data-ttu-id="af799-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="af799-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="af799-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="af799-109">Properties</span></span>

<span data-ttu-id="af799-110">A classe **WmiMonitorBrightness** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="af799-110">The **WmiMonitorBrightness** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="af799-111">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="af799-111">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af799-112">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="af799-112">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="af799-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="af799-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af799-114">Indica se o monitor de destino está ativo.</span><span class="sxs-lookup"><span data-stu-id="af799-114">Indicates if the target monitor is active.</span></span>

</dd> <dt>

<span data-ttu-id="af799-115">**CurrentBrightness**</span><span class="sxs-lookup"><span data-stu-id="af799-115">**CurrentBrightness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af799-116">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="af799-116">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="af799-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="af799-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af799-118">Brilho atual.</span><span class="sxs-lookup"><span data-stu-id="af799-118">Current brightness.</span></span> <span data-ttu-id="af799-119">Esse valor deve ser um valor obtido de *níveis*.</span><span class="sxs-lookup"><span data-stu-id="af799-119">This value must be a value taken from *Levels*.</span></span>

<span data-ttu-id="af799-120">Exemplo: 100</span><span class="sxs-lookup"><span data-stu-id="af799-120">Example: 100</span></span>

</dd> <dt>

<span data-ttu-id="af799-121">InstanceName</span><span class="sxs-lookup"><span data-stu-id="af799-121">InstanceName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af799-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="af799-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af799-123">Qualificadores: Chave</span><span class="sxs-lookup"><span data-stu-id="af799-123">Qualifiers: Key</span></span>
</dt> </dl>

<span data-ttu-id="af799-124">Nome da instância de monitor específica.</span><span class="sxs-lookup"><span data-stu-id="af799-124">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="af799-125">**Level**</span><span class="sxs-lookup"><span data-stu-id="af799-125">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af799-126">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="af799-126">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="af799-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="af799-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af799-128">Matriz que contém os níveis de brilho possíveis.</span><span class="sxs-lookup"><span data-stu-id="af799-128">Array containing the possible brightness levels.</span></span>

<span data-ttu-id="af799-129">Exemplo: \[ 0, 1, 2,..., 100 \] .</span><span class="sxs-lookup"><span data-stu-id="af799-129">Example: \[0, 1, 2, ..., 100\].</span></span>

</dd> <dt>

<span data-ttu-id="af799-130">**Níveis**</span><span class="sxs-lookup"><span data-stu-id="af799-130">**Levels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af799-131">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af799-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af799-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="af799-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af799-133">O número total de níveis de brilho aos quais o monitor dá suporte, conforme descrito em *nível*.</span><span class="sxs-lookup"><span data-stu-id="af799-133">The total number of brightness levels the monitor supports, as described in *Level*.</span></span>

<span data-ttu-id="af799-134">Exemplo: 101</span><span class="sxs-lookup"><span data-stu-id="af799-134">Example: 101</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="af799-135">Exemplos</span><span class="sxs-lookup"><span data-stu-id="af799-135">Examples</span></span>

<span data-ttu-id="af799-136">Para obter mais informações e exemplos de código sobre como usar essa classe no PowerShell, consulte [usar o PowerShell para relatar e definir o brilho do monitor](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx).</span><span class="sxs-lookup"><span data-stu-id="af799-136">For more information and code samples on using this class in PowerShell, see [Use PowerShell to Report and Set Monitor Brightness](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx).</span></span>

## <a name="requirements"></a><span data-ttu-id="af799-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af799-137">Requirements</span></span>



| <span data-ttu-id="af799-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="af799-138">Requirement</span></span> | <span data-ttu-id="af799-139">Valor</span><span class="sxs-lookup"><span data-stu-id="af799-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="af799-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af799-140">Minimum supported client</span></span><br/> | <span data-ttu-id="af799-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="af799-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="af799-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af799-142">Minimum supported server</span></span><br/> | <span data-ttu-id="af799-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af799-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="af799-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="af799-144">Namespace</span></span><br/>                | <span data-ttu-id="af799-145">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="af799-145">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="af799-146">MOF</span><span class="sxs-lookup"><span data-stu-id="af799-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af799-147"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="af799-147"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="af799-148">DLL</span><span class="sxs-lookup"><span data-stu-id="af799-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af799-149"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af799-149"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af799-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="af799-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af799-151">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="af799-151">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




