---
description: A \_ associação CIM ElementConfiguration relaciona um \_ objeto de configuração CIM a um ou mais elementos do sistema gerenciado. O \_ objeto de configuração CIM representa um determinado comportamento ou um estado funcional desejado para o MANAGEDSYSTEMELEMENT CIM associado \_ .
ms.assetid: 4d2af009-7466-4394-af42-72c8d96e0786
ms.tgt_platform: multiple
title: Classe CIM_ElementConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementConfiguration
- CIM_ElementConfiguration.Configuration
- CIM_ElementConfiguration.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7707338a3c2268cba51146aa8462b3b244b149ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010212"
---
# <a name="cim_elementconfiguration-class"></a><span data-ttu-id="6d802-104">\_Classe CIM ElementConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d802-104">CIM\_ElementConfiguration class</span></span>

<span data-ttu-id="6d802-105">A associação **CIM \_ ElementConfiguration** relaciona um objeto de [**\_ configuração CIM**](cim-configuration.md) a um ou mais elementos do sistema gerenciado.</span><span class="sxs-lookup"><span data-stu-id="6d802-105">The **CIM\_ElementConfiguration** association relates a [**CIM\_Configuration**](cim-configuration.md) object to one or more managed system elements.</span></span> <span data-ttu-id="6d802-106">O objeto de **\_ configuração CIM** representa um determinado comportamento ou um estado funcional desejado para o [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md)associado.</span><span class="sxs-lookup"><span data-stu-id="6d802-106">The **CIM\_Configuration** object represents a certain behavior, or a desired functional state for the associated [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6d802-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="6d802-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6d802-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6d802-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6d802-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="6d802-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6d802-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="6d802-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d802-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d802-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FC049DCE-DB29-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ElementConfiguration
{
  CIM_Configuration        REF Configuration;
  CIM_ManagedSystemElement REF Element;
};
```

## <a name="members"></a><span data-ttu-id="6d802-112">Membros</span><span class="sxs-lookup"><span data-stu-id="6d802-112">Members</span></span>

<span data-ttu-id="6d802-113">A classe **CIM \_ ElementConfiguration** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6d802-113">The **CIM\_ElementConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="6d802-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6d802-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6d802-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6d802-115">Properties</span></span>

<span data-ttu-id="6d802-116">A classe **CIM \_ ElementConfiguration** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6d802-116">The **CIM\_ElementConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6d802-117">**Configuration**</span><span class="sxs-lookup"><span data-stu-id="6d802-117">**Configuration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d802-118">Tipo de dados **: \_ configuração de CIM**</span><span class="sxs-lookup"><span data-stu-id="6d802-118">Data type: **CIM\_Configuration**</span></span>
</dt> <dt>

<span data-ttu-id="6d802-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6d802-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d802-120">Referência ao objeto [**de \_ configuração CIM**](cim-configuration.md) que agrupa as configurações e dependências associadas ao elemento do sistema gerenciado.</span><span class="sxs-lookup"><span data-stu-id="6d802-120">Reference to the [**CIM\_Configuration**](cim-configuration.md) object that groups the settings and dependencies associated with the managed system element.</span></span>

</dd> <dt>

<span data-ttu-id="6d802-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="6d802-121">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d802-122">Tipo de dados: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="6d802-122">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="6d802-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6d802-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d802-124">Referência ao elemento do sistema gerenciado.</span><span class="sxs-lookup"><span data-stu-id="6d802-124">Reference to the managed system element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d802-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d802-125">Remarks</span></span>

<span data-ttu-id="6d802-126">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="6d802-126">WMI does not implement this class.</span></span>

<span data-ttu-id="6d802-127">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="6d802-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6d802-128">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="6d802-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d802-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d802-129">Requirements</span></span>



| <span data-ttu-id="6d802-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d802-130">Requirement</span></span> | <span data-ttu-id="6d802-131">Valor</span><span class="sxs-lookup"><span data-stu-id="6d802-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d802-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d802-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6d802-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6d802-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6d802-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d802-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6d802-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d802-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6d802-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="6d802-136">Namespace</span></span><br/>                | <span data-ttu-id="6d802-137">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6d802-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6d802-138">MOF</span><span class="sxs-lookup"><span data-stu-id="6d802-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d802-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6d802-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6d802-140">DLL</span><span class="sxs-lookup"><span data-stu-id="6d802-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d802-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d802-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




