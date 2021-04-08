---
description: O \_ relacionamento CIM DependencyContext associa uma \_ classe de dependência CIM a um ou mais \_ objetos de configuração CIM. Por exemplo, as dependências de um sistema de computador podem ser alteradas com base na rede à qual o sistema está anexado.
ms.assetid: 9f35fc41-1bfa-4018-a54c-64c875c710d4
ms.tgt_platform: multiple
title: Classe CIM_DependencyContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DependencyContext
- CIM_DependencyContext.Context
- CIM_DependencyContext.Dependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 69319a4f4d228d484da62411060ae3fead90bb79
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826465"
---
# <a name="cim_dependencycontext-class"></a><span data-ttu-id="377ce-104">\_Classe CIM DependencyContext</span><span class="sxs-lookup"><span data-stu-id="377ce-104">CIM\_DependencyContext class</span></span>

<span data-ttu-id="377ce-105">O relacionamento **CIM \_ DependencyContext** associa uma classe de [**\_ dependência CIM**](cim-dependency.md) a um ou mais objetos de [**\_ configuração CIM**](cim-configuration.md) .</span><span class="sxs-lookup"><span data-stu-id="377ce-105">The **CIM\_DependencyContext** relationship associates a [**CIM\_Dependency**](cim-dependency.md) class with one or more [**CIM\_Configuration**](cim-configuration.md) objects.</span></span> <span data-ttu-id="377ce-106">Por exemplo, as dependências de um sistema de computador podem ser alteradas com base na rede à qual o sistema está anexado.</span><span class="sxs-lookup"><span data-stu-id="377ce-106">For example, a computer system's dependencies can change based on the network to which the system is attached.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="377ce-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="377ce-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="377ce-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="377ce-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="377ce-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="377ce-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="377ce-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="377ce-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="377ce-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="377ce-111">Syntax</span></span>

``` syntax
[Abstract, Aggregation, Association, UUID("{A228E208-DB22-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DependencyContext
{
  CIM_Configuration REF Context;
  CIM_Dependency    REF Dependency;
};
```

## <a name="members"></a><span data-ttu-id="377ce-112">Membros</span><span class="sxs-lookup"><span data-stu-id="377ce-112">Members</span></span>

<span data-ttu-id="377ce-113">A classe **CIM \_ DependencyContext** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="377ce-113">The **CIM\_DependencyContext** class has these types of members:</span></span>

-   [<span data-ttu-id="377ce-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="377ce-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="377ce-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="377ce-115">Properties</span></span>

<span data-ttu-id="377ce-116">A classe **CIM \_ DependencyContext** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="377ce-116">The **CIM\_DependencyContext** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="377ce-117">**Contexto**</span><span class="sxs-lookup"><span data-stu-id="377ce-117">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377ce-118">Tipo de dados **: \_ configuração de CIM**</span><span class="sxs-lookup"><span data-stu-id="377ce-118">Data type: **CIM\_Configuration**</span></span>
</dt> <dt>

<span data-ttu-id="377ce-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="377ce-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="377ce-120">Qualificadores: [ **agregação**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="377ce-120">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="377ce-121">Referência ao objeto de configuração que agrega a dependência.</span><span class="sxs-lookup"><span data-stu-id="377ce-121">Reference to the configuration object that aggregates the dependency.</span></span>

</dd> <dt>

<span data-ttu-id="377ce-122">**Dependência**</span><span class="sxs-lookup"><span data-stu-id="377ce-122">**Dependency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377ce-123">Tipo de dados **: \_ dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="377ce-123">Data type: **CIM\_Dependency**</span></span>
</dt> <dt>

<span data-ttu-id="377ce-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="377ce-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="377ce-125">Referência a uma dependência agregada.</span><span class="sxs-lookup"><span data-stu-id="377ce-125">Reference to an aggregated dependency.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="377ce-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="377ce-126">Remarks</span></span>

<span data-ttu-id="377ce-127">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="377ce-127">WMI does not implement this class.</span></span>

<span data-ttu-id="377ce-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="377ce-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="377ce-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="377ce-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="377ce-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="377ce-130">Requirements</span></span>



| <span data-ttu-id="377ce-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="377ce-131">Requirement</span></span> | <span data-ttu-id="377ce-132">Valor</span><span class="sxs-lookup"><span data-stu-id="377ce-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="377ce-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="377ce-133">Minimum supported client</span></span><br/> | <span data-ttu-id="377ce-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="377ce-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="377ce-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="377ce-135">Minimum supported server</span></span><br/> | <span data-ttu-id="377ce-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="377ce-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="377ce-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="377ce-137">Namespace</span></span><br/>                | <span data-ttu-id="377ce-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="377ce-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="377ce-139">MOF</span><span class="sxs-lookup"><span data-stu-id="377ce-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="377ce-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="377ce-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="377ce-141">DLL</span><span class="sxs-lookup"><span data-stu-id="377ce-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="377ce-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="377ce-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

