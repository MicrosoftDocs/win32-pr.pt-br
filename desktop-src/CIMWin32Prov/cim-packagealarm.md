---
description: A \_ associação CIM PackageAlarm representa a relação na qual um dispositivo de alarme é instalado como parte de um pacote. A instalação indica problemas com o ambiente do pacote&\# 8212; seu estado de segurança ou sua integridade geral.
ms.assetid: 4911502a-de9c-46b4-91f6-a042c69fd052
ms.tgt_platform: multiple
title: Classe CIM_PackageAlarm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageAlarm
- CIM_PackageAlarm.Dependent
- CIM_PackageAlarm.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 29aae3a2c1093e026356ea7a096f8b673673f67d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088986"
---
# <a name="cim_packagealarm-class"></a><span data-ttu-id="0167d-104">\_Classe CIM PackageAlarm</span><span class="sxs-lookup"><span data-stu-id="0167d-104">CIM\_PackageAlarm class</span></span>

<span data-ttu-id="0167d-105">A associação [**CIM \_ PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) representa a relação na qual um dispositivo de alarme é instalado como parte de um pacote.</span><span class="sxs-lookup"><span data-stu-id="0167d-105">The [**CIM\_PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) association represents the relationship in which an alarm device is installed as part of a package.</span></span> <span data-ttu-id="0167d-106">A instalação indica problemas com o ambiente do pacote seu estado de segurança ou sua integridade geral.</span><span class="sxs-lookup"><span data-stu-id="0167d-106">The installation indicates issues with the package's environment its security state or its overall health.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0167d-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="0167d-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0167d-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0167d-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0167d-109">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0167d-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="0167d-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="0167d-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0167d-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0167d-111">Syntax</span></span>

``` syntax
[Abstract, Aggregation, UUID("{FAF76B90-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageAlarm : CIM_Dependency
{
  CIM_PhysicalPackage REF Dependent;
  CIM_AlarmDevice     REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="0167d-112">Membros</span><span class="sxs-lookup"><span data-stu-id="0167d-112">Members</span></span>

<span data-ttu-id="0167d-113">A classe **CIM \_ PackageAlarm** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0167d-113">The **CIM\_PackageAlarm** class has these types of members:</span></span>

-   [<span data-ttu-id="0167d-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0167d-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0167d-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0167d-115">Properties</span></span>

<span data-ttu-id="0167d-116">A classe **CIM \_ PackageAlarm** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0167d-116">The **CIM\_PackageAlarm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0167d-117">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="0167d-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0167d-118">Tipo de dados: **CIM \_ AlarmDevice**</span><span class="sxs-lookup"><span data-stu-id="0167d-118">Data type: **CIM\_AlarmDevice**</span></span>
</dt> <dt>

<span data-ttu-id="0167d-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0167d-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0167d-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="0167d-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="0167d-121">Um [**\_ AlarmDevice CIM**](cim-alarmdevice.md) que descreve o dispositivo de alarme para o pacote.</span><span class="sxs-lookup"><span data-stu-id="0167d-121">A [**CIM\_AlarmDevice**](cim-alarmdevice.md) that describes the alarm device for the package.</span></span>

</dd> <dt>

<span data-ttu-id="0167d-122">**Depende**</span><span class="sxs-lookup"><span data-stu-id="0167d-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0167d-123">Tipo de dados: **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="0167d-123">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="0167d-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0167d-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0167d-125">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="0167d-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="0167d-126">Um [**\_ PhysicalPackage CIM**](cim-physicalpackage.md) que descreve o pacote físico cuja integridade, segurança, ambiente etc. é alarmante.</span><span class="sxs-lookup"><span data-stu-id="0167d-126">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) describing the physical package whose health, security, environment, etc. is alarmed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0167d-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="0167d-127">Remarks</span></span>

<span data-ttu-id="0167d-128">**CIM \_ PackageAlarm** é derivado da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="0167d-128">**CIM\_PackageAlarm** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="0167d-129">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="0167d-129">WMI does not implement this class.</span></span>

<span data-ttu-id="0167d-130">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="0167d-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0167d-131">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="0167d-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0167d-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0167d-132">Requirements</span></span>



| <span data-ttu-id="0167d-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="0167d-133">Requirement</span></span> | <span data-ttu-id="0167d-134">Valor</span><span class="sxs-lookup"><span data-stu-id="0167d-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0167d-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0167d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0167d-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0167d-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0167d-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0167d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0167d-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0167d-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0167d-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="0167d-139">Namespace</span></span><br/>                | <span data-ttu-id="0167d-140">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0167d-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0167d-141">MOF</span><span class="sxs-lookup"><span data-stu-id="0167d-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0167d-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0167d-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0167d-143">DLL</span><span class="sxs-lookup"><span data-stu-id="0167d-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0167d-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0167d-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0167d-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="0167d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0167d-146">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="0167d-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

