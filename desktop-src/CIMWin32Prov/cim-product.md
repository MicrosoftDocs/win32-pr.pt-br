---
description: A \_ classe de produto CIM é uma classe concreta que representa uma coleção de elementos físicos, recursos de software e outros produtos, adquiridos como uma unidade.
ms.assetid: beb20f61-de39-4221-8d29-4727104518d5
ms.tgt_platform: multiple
title: Classe CIM_Product
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Product
- CIM_Product.Caption
- CIM_Product.Description
- CIM_Product.IdentifyingNumber
- CIM_Product.Name
- CIM_Product.SKUNumber
- CIM_Product.Vendor
- CIM_Product.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 16c8541a18185d721bbdcbf23acaeb67adf508c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646276"
---
# <a name="cim_product-class"></a><span data-ttu-id="6b787-103">\_Classe de produto CIM</span><span class="sxs-lookup"><span data-stu-id="6b787-103">CIM\_Product class</span></span>

<span data-ttu-id="6b787-104">A classe de **\_ produto CIM** é uma classe concreta que representa uma coleção de elementos físicos, recursos de software e outros produtos, adquiridos como uma unidade.</span><span class="sxs-lookup"><span data-stu-id="6b787-104">The **CIM\_Product** class is a concrete class that represents a collection of physical elements, software features and, other products, acquired as a unit.</span></span> <span data-ttu-id="6b787-105">A aquisição implica um contrato entre o fornecedor e o consumidor, o que pode ter implicações no licenciamento, suporte e garantia do produto.</span><span class="sxs-lookup"><span data-stu-id="6b787-105">Acquisition implies an agreement between the supplier and consumer, which can have implications on product licensing, support, and warranty.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b787-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="6b787-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6b787-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6b787-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6b787-108">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="6b787-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="6b787-109">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="6b787-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b787-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6b787-110">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B63-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Product
{
  string Caption;
  string Description;
  string IdentifyingNumber;
  string Name;
  string SKUNumber;
  string Vendor;
  string Version;
};
```

## <a name="members"></a><span data-ttu-id="6b787-111">Membros</span><span class="sxs-lookup"><span data-stu-id="6b787-111">Members</span></span>

<span data-ttu-id="6b787-112">A classe de **\_ produto CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6b787-112">The **CIM\_Product** class has these types of members:</span></span>

-   [<span data-ttu-id="6b787-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6b787-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6b787-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6b787-114">Properties</span></span>

<span data-ttu-id="6b787-115">A classe de **\_ produto CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6b787-115">The **CIM\_Product** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6b787-116">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="6b787-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b787-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6b787-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b787-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6b787-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b787-119">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6b787-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6b787-120">Breve descrição textual do produto.</span><span class="sxs-lookup"><span data-stu-id="6b787-120">Short textual description for the product.</span></span>

</dd> <dt>

<span data-ttu-id="6b787-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6b787-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b787-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6b787-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b787-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6b787-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b787-124">Descrição textual do produto.</span><span class="sxs-lookup"><span data-stu-id="6b787-124">Textual description of the product.</span></span>

</dd> <dt>

<span data-ttu-id="6b787-125">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="6b787-125">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b787-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6b787-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b787-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6b787-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b787-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,4 ")</span><span class="sxs-lookup"><span data-stu-id="6b787-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="6b787-129">Identificação do produto, como um número de série em software, um número de dado em um chip de hardware ou (para produtos comerciais) um número de projeto.</span><span class="sxs-lookup"><span data-stu-id="6b787-129">Product identification, such as a serial number on software, a die number on a hardware chip, or (for noncommercial products) a project number.</span></span>

</dd> <dt>

<span data-ttu-id="6b787-130">**Nome**</span><span class="sxs-lookup"><span data-stu-id="6b787-130">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b787-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6b787-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b787-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6b787-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b787-133">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,2 ")</span><span class="sxs-lookup"><span data-stu-id="6b787-133">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="6b787-134">Nome do produto usado normalmente.</span><span class="sxs-lookup"><span data-stu-id="6b787-134">Commonly used product name.</span></span>

</dd> <dt>

<span data-ttu-id="6b787-135">**SKUNumber**</span><span class="sxs-lookup"><span data-stu-id="6b787-135">**SKUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b787-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6b787-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b787-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6b787-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b787-138">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6b787-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6b787-139">Informações de SKU (unidade de manutenção de estoque) do produto.</span><span class="sxs-lookup"><span data-stu-id="6b787-139">Product's stock-keeping unit (SKU) information.</span></span>

</dd> <dt>

<span data-ttu-id="6b787-140">**Fornecedor**</span><span class="sxs-lookup"><span data-stu-id="6b787-140">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b787-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6b787-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b787-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6b787-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b787-143">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,1 ")</span><span class="sxs-lookup"><span data-stu-id="6b787-143">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="6b787-144">Nome do fornecedor do produto ou a entidade que vende o produto (fabricante, revendedor, OEM e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="6b787-144">Name of the product's supplier, or the entity selling the product (the manufacturer, reseller, OEM, and so on).</span></span>

</dd> <dt>

<span data-ttu-id="6b787-145">**Versão**</span><span class="sxs-lookup"><span data-stu-id="6b787-145">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b787-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6b787-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b787-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6b787-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b787-148">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="6b787-148">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="6b787-149">Informações de versão do produto.</span><span class="sxs-lookup"><span data-stu-id="6b787-149">Product version information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b787-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b787-150">Remarks</span></span>

<span data-ttu-id="6b787-151">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="6b787-151">WMI does not implement this class.</span></span> <span data-ttu-id="6b787-152">Para classes WMI derivadas do **\_ produto CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6b787-152">For WMI classes that are derived from **CIM\_Product**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="6b787-153">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="6b787-153">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6b787-154">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="6b787-154">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b787-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b787-155">Requirements</span></span>



| <span data-ttu-id="6b787-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b787-156">Requirement</span></span> | <span data-ttu-id="6b787-157">Valor</span><span class="sxs-lookup"><span data-stu-id="6b787-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b787-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b787-158">Minimum supported client</span></span><br/> | <span data-ttu-id="6b787-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b787-159">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6b787-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b787-160">Minimum supported server</span></span><br/> | <span data-ttu-id="6b787-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b787-161">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6b787-162">Namespace</span><span class="sxs-lookup"><span data-stu-id="6b787-162">Namespace</span></span><br/>                | <span data-ttu-id="6b787-163">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6b787-163">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6b787-164">MOF</span><span class="sxs-lookup"><span data-stu-id="6b787-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b787-165"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b787-165"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b787-166">DLL</span><span class="sxs-lookup"><span data-stu-id="6b787-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b787-167"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b787-167"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

