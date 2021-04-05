---
description: A \_ classe CIM CollectionSetting representa a associação entre um CIM \_ CollectionOfMSEs e a classe de configuração definida para eles.
ms.assetid: f09bd656-5fdd-4ab1-8ef9-52d431a5117d
ms.tgt_platform: multiple
title: Classe CIM_CollectionSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionSetting
- CIM_CollectionSetting.Collection
- CIM_CollectionSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c290225ee38008f0345b695af794e57f311f2998
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826500"
---
# <a name="cim_collectionsetting-class"></a><span data-ttu-id="d865c-103">\_Classe CIM CollectionSetting</span><span class="sxs-lookup"><span data-stu-id="d865c-103">CIM\_CollectionSetting class</span></span>

<span data-ttu-id="d865c-104">A classe **CIM \_ CollectionSetting** representa a associação entre um [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) e a classe de configuração definida para eles.</span><span class="sxs-lookup"><span data-stu-id="d865c-104">The **CIM\_CollectionSetting** class represents the association between a [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) and the setting class defined for them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d865c-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="d865c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d865c-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d865c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d865c-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d865c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d865c-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="d865c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d865c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d865c-109">Syntax</span></span>

``` syntax
class CIM_CollectionSetting
{
  CIM_CollectionOfMSEs REF Collection;
  CIM_Setting          REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="d865c-110">Membros</span><span class="sxs-lookup"><span data-stu-id="d865c-110">Members</span></span>

<span data-ttu-id="d865c-111">A classe **CIM \_ CollectionSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d865c-111">The **CIM\_CollectionSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="d865c-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d865c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d865c-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d865c-113">Properties</span></span>

<span data-ttu-id="d865c-114">A classe **CIM \_ CollectionSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d865c-114">The **CIM\_CollectionSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d865c-115">**Coleção**</span><span class="sxs-lookup"><span data-stu-id="d865c-115">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d865c-116">Tipo de dados: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="d865c-116">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="d865c-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d865c-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d865c-118">Referência à classe [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="d865c-118">Reference to the [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="d865c-119">**Configuração**</span><span class="sxs-lookup"><span data-stu-id="d865c-119">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d865c-120">Tipo de dados **: \_ configuração de CIM**</span><span class="sxs-lookup"><span data-stu-id="d865c-120">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="d865c-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d865c-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d865c-122">Referência ao objeto de **configuração** associado à propriedade de **coleção** .</span><span class="sxs-lookup"><span data-stu-id="d865c-122">Reference to the **Setting** object associated with the **Collection** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d865c-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="d865c-123">Remarks</span></span>

<span data-ttu-id="d865c-124">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="d865c-124">WMI does not implement this class.</span></span> <span data-ttu-id="d865c-125">Para obter mais informações sobre classes WMI derivadas do **CIM \_ CollectionSetting**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d865c-125">For more information about WMI classes derived from **CIM\_CollectionSetting**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="d865c-126">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="d865c-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d865c-127">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="d865c-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d865c-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d865c-128">Requirements</span></span>



| <span data-ttu-id="d865c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d865c-129">Requirement</span></span> | <span data-ttu-id="d865c-130">Valor</span><span class="sxs-lookup"><span data-stu-id="d865c-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d865c-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d865c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d865c-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d865c-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d865c-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d865c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d865c-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d865c-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d865c-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="d865c-135">Namespace</span></span><br/>                | <span data-ttu-id="d865c-136">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d865c-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d865c-137">MOF</span><span class="sxs-lookup"><span data-stu-id="d865c-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d865c-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d865c-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d865c-139">DLL</span><span class="sxs-lookup"><span data-stu-id="d865c-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d865c-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d865c-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




