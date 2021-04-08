---
description: A \_ classe CIM BootOSFromFS associa o sistema operacional e os sistemas de arquivos dos quais o sistema operacional é carregado.
ms.assetid: c5697e9c-9031-4787-a03d-cf713c961cdf
ms.tgt_platform: multiple
title: Classe CIM_BootOSFromFS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootOSFromFS
- CIM_BootOSFromFS.Dependent
- CIM_BootOSFromFS.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 993ee7a66ef9f8b0cbb47285e38b78e4fd4dd61b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920439"
---
# <a name="cim_bootosfromfs-class"></a><span data-ttu-id="4cedb-103">\_Classe CIM BootOSFromFS</span><span class="sxs-lookup"><span data-stu-id="4cedb-103">CIM\_BootOSFromFS class</span></span>

<span data-ttu-id="4cedb-104">A classe **CIM \_ BootOSFromFS** associa o sistema operacional e os sistemas de arquivos dos quais o sistema operacional é carregado.</span><span class="sxs-lookup"><span data-stu-id="4cedb-104">The **CIM\_BootOSFromFS** class associates the operating system and the file systems from which the operating system is loaded.</span></span> <span data-ttu-id="4cedb-105">A associação é muitos-para-muitos; um sistema operacional distribuído pode depender de vários sistemas de arquivos para serem carregados de forma correta e completa.</span><span class="sxs-lookup"><span data-stu-id="4cedb-105">The association is many-to-many; a distributed operating system can depend on several file systems to load correctly and completely.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4cedb-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="4cedb-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4cedb-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4cedb-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4cedb-108">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="4cedb-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4cedb-109">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="4cedb-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cedb-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4cedb-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{5F5B101E-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_BootOSFromFS : CIM_Dependency
{
  CIM_OperatingSystem REF Dependent;
  CIM_FileSystem      REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="4cedb-111">Membros</span><span class="sxs-lookup"><span data-stu-id="4cedb-111">Members</span></span>

<span data-ttu-id="4cedb-112">A classe **CIM \_ BootOSFromFS** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4cedb-112">The **CIM\_BootOSFromFS** class has these types of members:</span></span>

-   [<span data-ttu-id="4cedb-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4cedb-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4cedb-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4cedb-114">Properties</span></span>

<span data-ttu-id="4cedb-115">A classe **CIM \_ BootOSFromFS** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4cedb-115">The **CIM\_BootOSFromFS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4cedb-116">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="4cedb-116">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cedb-117">Tipo de dados **: \_ sistema de arquivos CIM**</span><span class="sxs-lookup"><span data-stu-id="4cedb-117">Data type: **CIM\_FileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="4cedb-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4cedb-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4cedb-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="4cedb-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="4cedb-120">O sistema de arquivos do qual o sistema operacional é carregado.</span><span class="sxs-lookup"><span data-stu-id="4cedb-120">The file system from which the operating system is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="4cedb-121">**Depende**</span><span class="sxs-lookup"><span data-stu-id="4cedb-121">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cedb-122">Tipo de dados: sistema **\_ operacional CIM**</span><span class="sxs-lookup"><span data-stu-id="4cedb-122">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="4cedb-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4cedb-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4cedb-124">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="4cedb-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4cedb-125">O sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4cedb-125">The operating system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4cedb-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="4cedb-126">Remarks</span></span>

<span data-ttu-id="4cedb-127">A classe **CIM \_ BootOSFromFS** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="4cedb-127">The **CIM\_BootOSFromFS** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="4cedb-128">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="4cedb-128">WMI does not implement this class.</span></span>

<span data-ttu-id="4cedb-129">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="4cedb-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4cedb-130">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="4cedb-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cedb-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cedb-131">Requirements</span></span>



| <span data-ttu-id="4cedb-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cedb-132">Requirement</span></span> | <span data-ttu-id="4cedb-133">Valor</span><span class="sxs-lookup"><span data-stu-id="4cedb-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4cedb-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4cedb-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4cedb-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4cedb-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4cedb-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4cedb-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4cedb-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4cedb-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4cedb-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="4cedb-138">Namespace</span></span><br/>                | <span data-ttu-id="4cedb-139">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4cedb-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4cedb-140">MOF</span><span class="sxs-lookup"><span data-stu-id="4cedb-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4cedb-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4cedb-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4cedb-142">DLL</span><span class="sxs-lookup"><span data-stu-id="4cedb-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cedb-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cedb-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cedb-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="4cedb-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cedb-145">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="4cedb-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

