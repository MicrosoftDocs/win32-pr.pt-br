---
description: A \_ classe CIM LogicalIdentity é uma associação abstrata e genérica que indica que dois elementos lógicos representam diferentes aspectos da mesma entidade subjacente.
ms.assetid: 624a52bf-001d-4f18-af77-87a5d1cfa1ff
ms.tgt_platform: multiple
title: Classe CIM_LogicalIdentity (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalIdentity
- CIM_LogicalIdentity.SameElement
- CIM_LogicalIdentity.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 52780144a48cbb424ee037f71a56e238bb864311
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920228"
---
# <a name="cim_logicalidentity-class-cimwin32-wmi-providers"></a><span data-ttu-id="424af-103">Classe CIM_LogicalIdentity (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="424af-103">CIM_LogicalIdentity class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="424af-104">A classe **CIM \_ LogicalIdentity** é uma associação abstrata e genérica que indica que dois elementos lógicos representam diferentes aspectos da mesma entidade subjacente.</span><span class="sxs-lookup"><span data-stu-id="424af-104">The **CIM\_LogicalIdentity** class is an abstract and generic association that indicates that two logical elements represent different aspects of the same underlying entity.</span></span> <span data-ttu-id="424af-105">A associação transmite o que pode ser definido com várias heranças e é restrito aos aspectos lógicos de um elemento do sistema gerenciado.</span><span class="sxs-lookup"><span data-stu-id="424af-105">The association conveys what can be defined with multiple inheritance and is restricted to the logical aspects of a managed system element.</span></span> <span data-ttu-id="424af-106">Na maioria dos cenários, a relação de identidade é determinada pela equivalência de chaves ou algumas outras propriedades de identificação dos elementos relacionados.</span><span class="sxs-lookup"><span data-stu-id="424af-106">In most scenarios, the identity relationship is determined by the equivalence of keys, or some other identifying properties of the related elements.</span></span>

<span data-ttu-id="424af-107">A associação só deve ser usada em cenários que são bem compreendidos, permitindo uma definição mais concreta e esclarecimento em subclasses.</span><span class="sxs-lookup"><span data-stu-id="424af-107">The association should only be used in scenarios that are well understood, allowing more concrete definition and clarification in subclasses.</span></span> <span data-ttu-id="424af-108">Um cenário em que a relação é razoável, por exemplo, representa um dispositivo que é uma entidade de barramento e uma entidade funcional em que o dispositivo é uma entidade USB (barramento) e teclado (funcional).</span><span class="sxs-lookup"><span data-stu-id="424af-108">A scenario where the relationship is reasonable, for example, represents a device that is both a bus entity and a functional entity where the device is a USB (bus) and keyboard (functional) entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="424af-109">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="424af-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="424af-110">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="424af-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="424af-111">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="424af-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="424af-112">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="424af-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="424af-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="424af-113">Syntax</span></span>

``` syntax
class CIM_LogicalIdentity
{
  CIM_LogicalElement REF SameElement;
  CIM_LogicalElement REF SystemElement;
};
```

## <a name="members"></a><span data-ttu-id="424af-114">Membros</span><span class="sxs-lookup"><span data-stu-id="424af-114">Members</span></span>

<span data-ttu-id="424af-115">A classe **CIM \_ LogicalIdentity** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="424af-115">The **CIM\_LogicalIdentity** class has these types of members:</span></span>

-   [<span data-ttu-id="424af-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="424af-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="424af-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="424af-117">Properties</span></span>

<span data-ttu-id="424af-118">A classe **CIM \_ LogicalIdentity** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="424af-118">The **CIM\_LogicalIdentity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="424af-119">**Mesmoelement**</span><span class="sxs-lookup"><span data-stu-id="424af-119">**SameElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="424af-120">Tipo de dados: **CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="424af-120">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="424af-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="424af-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="424af-122">Referência a um aspecto alternativo da entidade do sistema.</span><span class="sxs-lookup"><span data-stu-id="424af-122">Reference to an alternate aspect of the system entity.</span></span>

</dd> <dt>

<span data-ttu-id="424af-123">**Sistema de**</span><span class="sxs-lookup"><span data-stu-id="424af-123">**SystemElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="424af-124">Tipo de dados: **CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="424af-124">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="424af-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="424af-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="424af-126">Referência a um aspecto do elemento lógico.</span><span class="sxs-lookup"><span data-stu-id="424af-126">Reference to one aspect of the logical element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="424af-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="424af-127">Remarks</span></span>

<span data-ttu-id="424af-128">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="424af-128">WMI does not implement this class.</span></span> <span data-ttu-id="424af-129">Para classes derivadas do **CIM \_ LogicalIdentity**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="424af-129">For classes derived from **CIM\_LogicalIdentity**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="424af-130">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="424af-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="424af-131">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="424af-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="424af-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="424af-132">Requirements</span></span>



| <span data-ttu-id="424af-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="424af-133">Requirement</span></span> | <span data-ttu-id="424af-134">Valor</span><span class="sxs-lookup"><span data-stu-id="424af-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="424af-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="424af-135">Minimum supported client</span></span><br/> | <span data-ttu-id="424af-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="424af-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="424af-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="424af-137">Minimum supported server</span></span><br/> | <span data-ttu-id="424af-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="424af-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="424af-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="424af-139">Namespace</span></span><br/>                | <span data-ttu-id="424af-140">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="424af-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="424af-141">MOF</span><span class="sxs-lookup"><span data-stu-id="424af-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="424af-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="424af-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="424af-143">DLL</span><span class="sxs-lookup"><span data-stu-id="424af-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="424af-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="424af-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




