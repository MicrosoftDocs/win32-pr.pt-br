---
description: A \_ classe WMI de associação DriverForDevice do Win32 relaciona uma instância de impressora a uma instância de driver de impressora.
ms.assetid: 56ff74b2-31ba-4d8e-b389-9f962932aa03
ms.tgt_platform: multiple
title: Classe Win32_DriverForDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DriverForDevice
- Win32_DriverForDevice.Antecedent
- Win32_DriverForDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5fb384eed80c6a614af448477c50be3204d3080
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750951"
---
# <a name="win32_driverfordevice-class"></a><span data-ttu-id="1bddb-103">\_Classe Win32 DriverForDevice</span><span class="sxs-lookup"><span data-stu-id="1bddb-103">Win32\_DriverForDevice class</span></span>

<span data-ttu-id="1bddb-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ DriverForDevice do Win32** relaciona uma instância de impressora a uma instância de driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="1bddb-104">The **Win32\_DriverForDevice** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a printer instance to a printer driver instance.</span></span>

<span data-ttu-id="1bddb-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1bddb-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1bddb-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="1bddb-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bddb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1bddb-107">Syntax</span></span>

``` syntax
class Win32_DriverForDevice : CIM_Dependency
{
  Win32_Printer       REF Antecedent;
  Win32_PrinterDriver REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="1bddb-108">Membros</span><span class="sxs-lookup"><span data-stu-id="1bddb-108">Members</span></span>

<span data-ttu-id="1bddb-109">A classe **Win32 \_ DriverForDevice** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1bddb-109">The **Win32\_DriverForDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="1bddb-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1bddb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1bddb-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1bddb-111">Properties</span></span>

<span data-ttu-id="1bddb-112">A classe **Win32 \_ DriverForDevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1bddb-112">The **Win32\_DriverForDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1bddb-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="1bddb-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bddb-114">Tipo de dados **: \_ impressora Win32**</span><span class="sxs-lookup"><span data-stu-id="1bddb-114">Data type: **Win32\_Printer**</span></span>
</dt> <dt>

<span data-ttu-id="1bddb-115">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1bddb-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1bddb-116">Referência à instância [**de \_ impressora do Win32**](win32-printer.md) que representa a impressora.</span><span class="sxs-lookup"><span data-stu-id="1bddb-116">Reference to the [**Win32\_Printer**](win32-printer.md) instance that represents the printer.</span></span>

<span data-ttu-id="1bddb-117">Essa propriedade é herdada [**da \_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="1bddb-117">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="1bddb-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="1bddb-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bddb-119">Tipo de dados: **Win32 \_ PrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="1bddb-119">Data type: **Win32\_PrinterDriver**</span></span>
</dt> <dt>

<span data-ttu-id="1bddb-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1bddb-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bddb-121">Referência à instância do [**Win32 \_ PrinterDriver**](win32-printerdriver.md) que representa o driver de impressora para a impressora.</span><span class="sxs-lookup"><span data-stu-id="1bddb-121">Reference to the [**Win32\_PrinterDriver**](win32-printerdriver.md) instance that represents the printer driver for the printer.</span></span>

<span data-ttu-id="1bddb-122">Essa propriedade é herdada [**da \_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="1bddb-122">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1bddb-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="1bddb-123">Remarks</span></span>

<span data-ttu-id="1bddb-124">A classe **Win32 \_ DriverForDevice** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="1bddb-124">The **Win32\_DriverForDevice** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1bddb-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bddb-125">Requirements</span></span>



| <span data-ttu-id="1bddb-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bddb-126">Requirement</span></span> | <span data-ttu-id="1bddb-127">Valor</span><span class="sxs-lookup"><span data-stu-id="1bddb-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bddb-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bddb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1bddb-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1bddb-129">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="1bddb-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bddb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1bddb-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1bddb-131">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="1bddb-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="1bddb-132">Namespace</span></span><br/>                | <span data-ttu-id="1bddb-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1bddb-133">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="1bddb-134">MOF</span><span class="sxs-lookup"><span data-stu-id="1bddb-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1bddb-135"><dt>\_Impressora. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="1bddb-135"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="1bddb-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1bddb-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bddb-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1bddb-137"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="1bddb-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="1bddb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bddb-139">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="1bddb-139">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

