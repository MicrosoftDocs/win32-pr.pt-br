---
description: Representa um conjunto de componentes que funciona como uma única entidade de alto nível.
ms.assetid: 784cee32-e0ae-4632-8dac-e5110513f5c9
title: Classe CIM_System (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_System
- CIM_System.CreationClassName
- CIM_System.Name
- CIM_System.NameFormat
- CIM_System.PrimaryOwnerName
- CIM_System.PrimaryOwnerContact
- CIM_System.Roles
- CIM_System.OtherIdentifyingInfo
- CIM_System.IdentifyingDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a51e56ad3e8f91200fbe5bc7e09ac2f14c4ee232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750852"
---
# <a name="cim_system-class-hyper-v-management"></a><span data-ttu-id="2ae29-103">Classe CIM_System (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="2ae29-103">CIM_System class (Hyper-V management)</span></span>

<span data-ttu-id="2ae29-104">Representa um conjunto de componentes que funciona como uma única entidade de alto nível.</span><span class="sxs-lookup"><span data-stu-id="2ae29-104">Represents a set of components that function as a single high-level entity.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ae29-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2ae29-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.15.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_System : CIM_EnabledLogicalElement
{
  string CreationClassName;
  string Name;
  string NameFormat;
  string PrimaryOwnerName;
  string PrimaryOwnerContact;
  string Roles[];
  string OtherIdentifyingInfo[];
  string IdentifyingDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="2ae29-106">Membros</span><span class="sxs-lookup"><span data-stu-id="2ae29-106">Members</span></span>

<span data-ttu-id="2ae29-107">A classe de **\_ sistema CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2ae29-107">The **CIM\_System** class has these types of members:</span></span>

-   [<span data-ttu-id="2ae29-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2ae29-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2ae29-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2ae29-109">Properties</span></span>

<span data-ttu-id="2ae29-110">A classe de **\_ sistema CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2ae29-110">The **CIM\_System** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2ae29-111">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2ae29-111">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ae29-112">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2ae29-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ae29-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2ae29-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ae29-114">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2ae29-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2ae29-115">O nome da classe usada para criar uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="2ae29-115">The class name used to create an instance of this class.</span></span> <span data-ttu-id="2ae29-116">**CreationClassName** é combinado com outras propriedades de chave dessa classe para identificar exclusivamente as instâncias dessa classe e suas subclasses.</span><span class="sxs-lookup"><span data-stu-id="2ae29-116">**CreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="2ae29-117">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2ae29-117">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ae29-118">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2ae29-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2ae29-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2ae29-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ae29-120">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ sistema CIM**.**OtherIdentifyingInfo**")</span><span class="sxs-lookup"><span data-stu-id="2ae29-120">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_System**.**OtherIdentifyingInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="2ae29-121">Uma matriz que contém descrições dos valores na propriedade **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="2ae29-121">An array that contains descriptions of the values in the **OtherIdentifyingInfo** property.</span></span> <span data-ttu-id="2ae29-122">Os itens de matriz em **IdentifyingDescriptions** correspondem aos itens na propriedade **IdentifyingDescriptions** .</span><span class="sxs-lookup"><span data-stu-id="2ae29-122">The array items in **IdentifyingDescriptions** correspond to the items in the **IdentifyingDescriptions** property.</span></span>

</dd> <dt>

<span data-ttu-id="2ae29-123">**Nome**</span><span class="sxs-lookup"><span data-stu-id="2ae29-123">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ae29-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2ae29-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ae29-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2ae29-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ae29-126">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2ae29-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2ae29-127">A chave dessa instância em um ambiente corporativo.</span><span class="sxs-lookup"><span data-stu-id="2ae29-127">The key of this instance in an enterprise environment.</span></span>

</dd> <dt>

<span data-ttu-id="2ae29-128">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="2ae29-128">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ae29-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2ae29-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ae29-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2ae29-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ae29-131">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2ae29-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2ae29-132">A Convenção de nomenclatura usada pela propriedade Name para garantir que os valores de **nome** sejam exclusivos.</span><span class="sxs-lookup"><span data-stu-id="2ae29-132">The naming convention used by the Name property to ensure that **Name** values are unique.</span></span>

</dd> <dt>

<span data-ttu-id="2ae29-133">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="2ae29-133">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ae29-134">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2ae29-134">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2ae29-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2ae29-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ae29-136">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ System**.**IdentifyingDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="2ae29-136">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_System**.**IdentifyingDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="2ae29-137">Uma matriz que contém um conjunto de dados adicionais, além das informações de nome do sistema, que podem ser usadas para identificar um sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="2ae29-137">An array that contains a set of additional data, beyond system name information, that could be used to identify a computer system.</span></span>

</dd> <dt>

<span data-ttu-id="2ae29-138">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="2ae29-138">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ae29-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2ae29-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ae29-140">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2ae29-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2ae29-141">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações gerais do DMTF \| 1,4 ")</span><span class="sxs-lookup"><span data-stu-id="2ae29-141">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="2ae29-142">Uma cadeia de caracteres que fornece informações sobre como o proprietário do sistema primário pode ser alcançado (por exemplo, número de telefone, endereço de email e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="2ae29-142">A string that provides information on how the primary system owner can be reached (for example, phone number, e-mail address, and so on).</span></span>

</dd> <dt>

<span data-ttu-id="2ae29-143">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="2ae29-143">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ae29-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2ae29-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ae29-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2ae29-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2ae29-146">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações gerais do DMTF \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="2ae29-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="2ae29-147">O nome do usuário primário do sistema.</span><span class="sxs-lookup"><span data-stu-id="2ae29-147">The name of the primary user of the system.</span></span>

</dd> <dt>

<span data-ttu-id="2ae29-148">**Funções**</span><span class="sxs-lookup"><span data-stu-id="2ae29-148">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ae29-149">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2ae29-149">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2ae29-150">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2ae29-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2ae29-151">Uma matriz que contém as funções executadas pelo sistema em um ambiente corporativo.</span><span class="sxs-lookup"><span data-stu-id="2ae29-151">An array that contains the roles carried out by the system in an enterprise environment.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2ae29-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ae29-152">Requirements</span></span>



| <span data-ttu-id="2ae29-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ae29-153">Requirement</span></span> | <span data-ttu-id="2ae29-154">Valor</span><span class="sxs-lookup"><span data-stu-id="2ae29-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ae29-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ae29-155">Minimum supported client</span></span><br/> | <span data-ttu-id="2ae29-156">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2ae29-156">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="2ae29-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ae29-157">Minimum supported server</span></span><br/> | <span data-ttu-id="2ae29-158">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2ae29-158">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="2ae29-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="2ae29-159">Namespace</span></span><br/>                | <span data-ttu-id="2ae29-160">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="2ae29-160">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2ae29-161">MOF</span><span class="sxs-lookup"><span data-stu-id="2ae29-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2ae29-162"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2ae29-162"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2ae29-163">DLL</span><span class="sxs-lookup"><span data-stu-id="2ae29-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ae29-164"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2ae29-164"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2ae29-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ae29-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ae29-166">**\_ENABLEDLOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="2ae29-166">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

