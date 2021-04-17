---
description: A \_ classe CIM ElementSetting representa a associação entre os elementos do sistema gerenciado e a classe de configuração definida para eles.
ms.assetid: e9b7c43f-7539-48c3-8679-568fb4b036bb
ms.tgt_platform: multiple
title: Classe CIM_ElementSetting (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementSetting
- CIM_ElementSetting.Element
- CIM_ElementSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2c1ea52648728397e811cfae35e7a83e272ab8d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749100"
---
# <a name="cim_elementsetting-class-cimwin32-wmi-providers"></a><span data-ttu-id="ba4e1-103">Classe CIM_ElementSetting (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="ba4e1-103">CIM_ElementSetting class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="ba4e1-104">A classe **CIM \_ ElementSetting** representa a associação entre os elementos do sistema gerenciado e a classe de configuração definida para eles.</span><span class="sxs-lookup"><span data-stu-id="ba4e1-104">The **CIM\_ElementSetting** class represents the association between managed system elements and the setting class defined for them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ba4e1-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="ba4e1-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ba4e1-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ba4e1-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ba4e1-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ba4e1-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ba4e1-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="ba4e1-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba4e1-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba4e1-109">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{8502C577-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ElementSetting
{
  CIM_ManagedSystemElement REF Element;
  CIM_Setting              REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="ba4e1-110">Membros</span><span class="sxs-lookup"><span data-stu-id="ba4e1-110">Members</span></span>

<span data-ttu-id="ba4e1-111">A classe **CIM \_ ElementSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ba4e1-111">The **CIM\_ElementSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="ba4e1-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ba4e1-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ba4e1-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ba4e1-113">Properties</span></span>

<span data-ttu-id="ba4e1-114">A classe **CIM \_ ElementSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ba4e1-114">The **CIM\_ElementSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ba4e1-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="ba4e1-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba4e1-116">Tipo de dados: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="ba4e1-116">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="ba4e1-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ba4e1-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba4e1-118">Referência à função do objeto [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) da Associação ElementSetting do **CIM \_** .</span><span class="sxs-lookup"><span data-stu-id="ba4e1-118">Reference to the role of the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) object of the **CIM\_ElementSetting** association.</span></span> <span data-ttu-id="ba4e1-119">O elemento de sistema gerenciado associado fornece o elemento que implementa a configuração do elemento.</span><span class="sxs-lookup"><span data-stu-id="ba4e1-119">The associated managed system element provides the element that implements the element setting.</span></span>

</dd> <dt>

<span data-ttu-id="ba4e1-120">**Configuração**</span><span class="sxs-lookup"><span data-stu-id="ba4e1-120">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba4e1-121">Tipo de dados **: \_ configuração de CIM**</span><span class="sxs-lookup"><span data-stu-id="ba4e1-121">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="ba4e1-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ba4e1-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba4e1-123">Referência à função do objeto de [**\_ configuração CIM**](cim-setting.md) da Associação **\_ ElementSetting do CIM** .</span><span class="sxs-lookup"><span data-stu-id="ba4e1-123">Reference to the role of the [**CIM\_Setting**](cim-setting.md) object of the **CIM\_ElementSetting** association.</span></span> <span data-ttu-id="ba4e1-124">A configuração associada fornece a configuração que implementa a configuração do elemento.</span><span class="sxs-lookup"><span data-stu-id="ba4e1-124">The associated setting provides the setting that implements the element setting.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba4e1-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba4e1-125">Remarks</span></span>

<span data-ttu-id="ba4e1-126">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="ba4e1-126">WMI does not implement this class.</span></span> <span data-ttu-id="ba4e1-127">Para classes derivadas do **CIM \_ ElementSetting**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ba4e1-127">For classes derived from **CIM\_ElementSetting**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="ba4e1-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="ba4e1-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ba4e1-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="ba4e1-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba4e1-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba4e1-130">Requirements</span></span>



| <span data-ttu-id="ba4e1-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba4e1-131">Requirement</span></span> | <span data-ttu-id="ba4e1-132">Valor</span><span class="sxs-lookup"><span data-stu-id="ba4e1-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba4e1-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba4e1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ba4e1-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ba4e1-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ba4e1-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba4e1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ba4e1-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba4e1-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ba4e1-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="ba4e1-137">Namespace</span></span><br/>                | <span data-ttu-id="ba4e1-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ba4e1-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ba4e1-139">MOF</span><span class="sxs-lookup"><span data-stu-id="ba4e1-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba4e1-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba4e1-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba4e1-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ba4e1-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba4e1-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba4e1-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




