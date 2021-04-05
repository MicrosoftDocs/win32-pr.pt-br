---
description: A \_ classe WMI de associação PrinterShare do Win32 relaciona uma impressora local e o compartilhamento que a representa, pois ela é exibida em uma rede.
ms.assetid: 9ac99e52-5e8f-4329-960f-7bd1fd229e37
ms.tgt_platform: multiple
title: Classe Win32_PrinterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterShare
- Win32_PrinterShare.Antecedent
- Win32_PrinterShare.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 57bc15fc5d3db78179335b039851d7d3b7cbf8a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826578"
---
# <a name="win32_printershare-class"></a><span data-ttu-id="41bce-103">\_Classe Win32 PrinterShare</span><span class="sxs-lookup"><span data-stu-id="41bce-103">Win32\_PrinterShare class</span></span>

<span data-ttu-id="41bce-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ PrinterShare do Win32** relaciona uma impressora local e o compartilhamento que a representa, pois ela é exibida em uma rede.</span><span class="sxs-lookup"><span data-stu-id="41bce-104">The **Win32\_PrinterShare** association [WMI class](../wmisdk/retrieving-a-class.md) relates a local printer and the share that represents it as it is viewed over a network.</span></span>

<span data-ttu-id="41bce-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="41bce-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="41bce-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="41bce-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="41bce-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41bce-107">Syntax</span></span>

``` syntax
class Win32_PrinterShare : CIM_Dependency
{
  Win32_Printer REF Antecedent;
  Win32_Share   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="41bce-108">Membros</span><span class="sxs-lookup"><span data-stu-id="41bce-108">Members</span></span>

<span data-ttu-id="41bce-109">A classe **Win32 \_ PrinterShare** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="41bce-109">The **Win32\_PrinterShare** class has these types of members:</span></span>

-   [<span data-ttu-id="41bce-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="41bce-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="41bce-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="41bce-111">Properties</span></span>

<span data-ttu-id="41bce-112">A classe **Win32 \_ PrinterShare** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="41bce-112">The **Win32\_PrinterShare** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="41bce-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="41bce-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41bce-114">Tipo de dados **: \_ impressora Win32**</span><span class="sxs-lookup"><span data-stu-id="41bce-114">Data type: **Win32\_Printer**</span></span>
</dt> <dt>

<span data-ttu-id="41bce-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41bce-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41bce-116">Qualificadores: [ **chave**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="41bce-116">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="41bce-117">Referência à instância que representa a impressora local compartilhada nessa associação.</span><span class="sxs-lookup"><span data-stu-id="41bce-117">Reference to the instance representing the local printer shared in this association.</span></span>

</dd> <dt>

<span data-ttu-id="41bce-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="41bce-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41bce-119">Tipo de dados **: \_ compartilhamento do Win32**</span><span class="sxs-lookup"><span data-stu-id="41bce-119">Data type: **Win32\_Share**</span></span>
</dt> <dt>

<span data-ttu-id="41bce-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41bce-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41bce-121">Qualificadores: [ **chave**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="41bce-121">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="41bce-122">Referência à instância que representa o compartilhamento da impressora nessa associação.</span><span class="sxs-lookup"><span data-stu-id="41bce-122">Reference to the instance representing the share of the printer in this association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41bce-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="41bce-123">Remarks</span></span>

<span data-ttu-id="41bce-124">A classe **Win32 \_ PrinterShare** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="41bce-124">The **Win32\_PrinterShare** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="41bce-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41bce-125">Requirements</span></span>



| <span data-ttu-id="41bce-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="41bce-126">Requirement</span></span> | <span data-ttu-id="41bce-127">Valor</span><span class="sxs-lookup"><span data-stu-id="41bce-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="41bce-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41bce-128">Minimum supported client</span></span><br/> | <span data-ttu-id="41bce-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41bce-129">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="41bce-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41bce-130">Minimum supported server</span></span><br/> | <span data-ttu-id="41bce-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41bce-131">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="41bce-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="41bce-132">Namespace</span></span><br/>                | <span data-ttu-id="41bce-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="41bce-133">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="41bce-134">MOF</span><span class="sxs-lookup"><span data-stu-id="41bce-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41bce-135"><dt>\_Impressora. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="41bce-135"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="41bce-136">DLL</span><span class="sxs-lookup"><span data-stu-id="41bce-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41bce-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41bce-137"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="41bce-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="41bce-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41bce-139">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="41bce-139">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
