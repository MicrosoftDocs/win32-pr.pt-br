---
description: A \_ classe WMI de associação PrinterDriverDll do Win32 relaciona uma impressora local e seu arquivo de driver.
ms.assetid: decbd1de-8091-47f7-94a1-42862070b920
ms.tgt_platform: multiple
title: Classe Win32_PrinterDriverDll
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriverDll
- Win32_PrinterDriverDll.Antecedent
- Win32_PrinterDriverDll.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 41484c39d9e1b59efd79d7aee08719b3a241de97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457118"
---
# <a name="win32_printerdriverdll-class"></a><span data-ttu-id="837fb-103">\_Classe Win32 PrinterDriverDll</span><span class="sxs-lookup"><span data-stu-id="837fb-103">Win32\_PrinterDriverDll class</span></span>

<span data-ttu-id="837fb-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ PrinterDriverDll do Win32** relaciona uma impressora local e seu arquivo de driver.</span><span class="sxs-lookup"><span data-stu-id="837fb-104">The **Win32\_PrinterDriverDll** association [WMI class](../wmisdk/retrieving-a-class.md) relates a local printer and its driver file.</span></span>

<span data-ttu-id="837fb-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="837fb-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="837fb-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="837fb-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="837fb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="837fb-107">Syntax</span></span>

``` syntax
class Win32_PrinterDriverDll : CIM_Dependency
{
  CIM_DataFile  REF Antecedent;
  Win32_Printer REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="837fb-108">Membros</span><span class="sxs-lookup"><span data-stu-id="837fb-108">Members</span></span>

<span data-ttu-id="837fb-109">A classe **Win32 \_ PrinterDriverDll** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="837fb-109">The **Win32\_PrinterDriverDll** class has these types of members:</span></span>

-   [<span data-ttu-id="837fb-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="837fb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="837fb-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="837fb-111">Properties</span></span>

<span data-ttu-id="837fb-112">A classe **Win32 \_ PrinterDriverDll** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="837fb-112">The **Win32\_PrinterDriverDll** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="837fb-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="837fb-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="837fb-114">Tipo de dados **: \_ DataFile do CIM**</span><span class="sxs-lookup"><span data-stu-id="837fb-114">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="837fb-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="837fb-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="837fb-116">Qualificadores: [ **chave**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="837fb-116">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="837fb-117">Referência à instância [**de \_ DataFile do CIM**](cim-datafile.md) que representa o arquivo de driver para esta impressora baseada no Windows.</span><span class="sxs-lookup"><span data-stu-id="837fb-117">Reference to the [**CIM\_DataFile**](cim-datafile.md) instance representing the driver file for this Windows-based printer.</span></span>

<span data-ttu-id="837fb-118">Essa propriedade é herdada [**da \_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="837fb-118">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="837fb-119">**Depende**</span><span class="sxs-lookup"><span data-stu-id="837fb-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="837fb-120">Tipo de dados **: \_ impressora Win32**</span><span class="sxs-lookup"><span data-stu-id="837fb-120">Data type: **Win32\_Printer**</span></span>
</dt> <dt>

<span data-ttu-id="837fb-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="837fb-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="837fb-122">Qualificadores: [ **chave**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="837fb-122">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="837fb-123">Referência à instância [**de \_ impressora do Win32**](win32-printer.md) .</span><span class="sxs-lookup"><span data-stu-id="837fb-123">Reference to the [**Win32\_Printer**](win32-printer.md) instance.</span></span>

<span data-ttu-id="837fb-124">Essa propriedade é herdada [**da \_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="837fb-124">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="837fb-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="837fb-125">Remarks</span></span>

<span data-ttu-id="837fb-126">A classe **Win32 \_ PrinterDriverDll** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="837fb-126">The **Win32\_PrinterDriverDll** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="837fb-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="837fb-127">Requirements</span></span>



| <span data-ttu-id="837fb-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="837fb-128">Requirement</span></span> | <span data-ttu-id="837fb-129">Valor</span><span class="sxs-lookup"><span data-stu-id="837fb-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="837fb-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="837fb-130">Minimum supported client</span></span><br/> | <span data-ttu-id="837fb-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="837fb-131">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="837fb-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="837fb-132">Minimum supported server</span></span><br/> | <span data-ttu-id="837fb-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="837fb-133">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="837fb-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="837fb-134">Namespace</span></span><br/>                | <span data-ttu-id="837fb-135">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="837fb-135">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="837fb-136">MOF</span><span class="sxs-lookup"><span data-stu-id="837fb-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="837fb-137"><dt>\_Impressora. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="837fb-137"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="837fb-138">DLL</span><span class="sxs-lookup"><span data-stu-id="837fb-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="837fb-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="837fb-139"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="837fb-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="837fb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="837fb-141">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="837fb-141">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="837fb-142">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="837fb-142">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
