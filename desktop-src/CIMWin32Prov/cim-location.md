---
description: A classe de local do CIM \_ representa a posição e o endereço de um elemento físico.
ms.assetid: c1ec467c-a338-4beb-a8fe-1ebc5b05c754
ms.tgt_platform: multiple
title: Classe CIM_Location
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Location
- CIM_Location.Address
- CIM_Location.Name
- CIM_Location.PhysicalPosition
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd5a1c1c23d07020b45c1c5979a941f01baff0d0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164060"
---
# <a name="cim_location-class"></a><span data-ttu-id="8f3e4-103">\_Classe de local CIM</span><span class="sxs-lookup"><span data-stu-id="8f3e4-103">CIM\_Location class</span></span>

<span data-ttu-id="8f3e4-104">A classe de **\_ local do CIM** representa a posição e o endereço de um elemento físico.</span><span class="sxs-lookup"><span data-stu-id="8f3e4-104">The **CIM\_Location** class represents the position and address of a physical element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8f3e4-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="8f3e4-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8f3e4-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8f3e4-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8f3e4-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8f3e4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8f3e4-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="8f3e4-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f3e4-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f3e4-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B67-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Location
{
  string Address;
  string Name;
  string PhysicalPosition;
};
```

## <a name="members"></a><span data-ttu-id="8f3e4-110">Membros</span><span class="sxs-lookup"><span data-stu-id="8f3e4-110">Members</span></span>

<span data-ttu-id="8f3e4-111">A classe de **\_ local do CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8f3e4-111">The **CIM\_Location** class has these types of members:</span></span>

-   [<span data-ttu-id="8f3e4-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8f3e4-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8f3e4-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8f3e4-113">Properties</span></span>

<span data-ttu-id="8f3e4-114">A classe de **\_ local CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8f3e4-114">The **CIM\_Location** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8f3e4-115">**Endereço**</span><span class="sxs-lookup"><span data-stu-id="8f3e4-115">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3e4-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8f3e4-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f3e4-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f3e4-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f3e4-118">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="8f3e4-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="8f3e4-119">Cadeia de caracteres de forma livre que indica uma rua ou outro tipo de endereço para o local do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="8f3e4-119">Free-form string that indicates a street or other type of address for the physical element's location.</span></span>

</dd> <dt>

<span data-ttu-id="8f3e4-120">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8f3e4-120">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3e4-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8f3e4-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f3e4-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f3e4-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f3e4-123">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8f3e4-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8f3e4-124">Cadeia de caracteres de forma livre que define um rótulo para o local e que faz parte da chave do objeto.</span><span class="sxs-lookup"><span data-stu-id="8f3e4-124">Free-form string that defines a label for the location and is part of the key for the object.</span></span>

</dd> <dt>

<span data-ttu-id="8f3e4-125">**PhysicalPosition**</span><span class="sxs-lookup"><span data-stu-id="8f3e4-125">**PhysicalPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f3e4-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8f3e4-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f3e4-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f3e4-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f3e4-128">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8f3e4-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8f3e4-129">Cadeia de caracteres de forma livre que indica o posicionamento de um elemento físico.</span><span class="sxs-lookup"><span data-stu-id="8f3e4-129">Free-form string that indicates the placement of a physical element.</span></span> <span data-ttu-id="8f3e4-130">Ele pode especificar informações de slot em uma placa de hospedagem, montar um site em um gabinete ou informações de latitude e longitude.</span><span class="sxs-lookup"><span data-stu-id="8f3e4-130">It can specify slot information on a hosting board, mounting site in a cabinet, or latitude and longitude information.</span></span> <span data-ttu-id="8f3e4-131">Ele faz parte da chave do objeto de **\_ local do CIM** .</span><span class="sxs-lookup"><span data-stu-id="8f3e4-131">It is part of the key of the **CIM\_Location** object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f3e4-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f3e4-132">Remarks</span></span>

<span data-ttu-id="8f3e4-133">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="8f3e4-133">WMI does not implement this class.</span></span> <span data-ttu-id="8f3e4-134">Para classes derivadas do **\_ local do CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8f3e4-134">For classes derived from **CIM\_Location**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="8f3e4-135">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="8f3e4-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8f3e4-136">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="8f3e4-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f3e4-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f3e4-137">Requirements</span></span>



| <span data-ttu-id="8f3e4-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f3e4-138">Requirement</span></span> | <span data-ttu-id="8f3e4-139">Valor</span><span class="sxs-lookup"><span data-stu-id="8f3e4-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f3e4-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f3e4-140">Minimum supported client</span></span><br/> | <span data-ttu-id="8f3e4-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f3e4-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8f3e4-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f3e4-142">Minimum supported server</span></span><br/> | <span data-ttu-id="8f3e4-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f3e4-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8f3e4-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="8f3e4-144">Namespace</span></span><br/>                | <span data-ttu-id="8f3e4-145">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8f3e4-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8f3e4-146">MOF</span><span class="sxs-lookup"><span data-stu-id="8f3e4-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f3e4-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f3e4-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f3e4-148">DLL</span><span class="sxs-lookup"><span data-stu-id="8f3e4-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f3e4-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f3e4-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

