---
description: A classe de FRU do CIM \_ representa uma coleção de produtos e elementos físicos definidos pelo fornecedor que estão associados a uma FRU (unidade de substituição de campo) para oferecer suporte, manutenção ou atualização de um produto no local do cliente.
ms.assetid: 4464ec3a-5509-4e15-9020-4abb2edd2570
ms.tgt_platform: multiple
title: Classe CIM_FRU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FRU
- CIM_FRU.Caption
- CIM_FRU.Description
- CIM_FRU.FRUNumber
- CIM_FRU.IdentifyingNumber
- CIM_FRU.Name
- CIM_FRU.RevisionLevel
- CIM_FRU.Vendor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d163c3c223159ad8e09aa6e36d63187ff0aa97f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646391"
---
# <a name="cim_fru-class"></a><span data-ttu-id="6bb04-103">\_Classe de FRU CIM</span><span class="sxs-lookup"><span data-stu-id="6bb04-103">CIM\_FRU class</span></span>

<span data-ttu-id="6bb04-104">A classe de **\_ FRU do CIM** representa uma coleção de produtos e elementos físicos definidos pelo fornecedor que estão associados a uma FRU (unidade de substituição de campo) para oferecer suporte, manutenção ou atualização de um produto no local do cliente.</span><span class="sxs-lookup"><span data-stu-id="6bb04-104">The **CIM\_FRU** class represents a vendor-defined collection of products and physical elements that are associated with a field replaceable unit (FRU) to support, maintain, or upgrade a product at the customer's location.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6bb04-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="6bb04-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6bb04-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6bb04-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6bb04-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="6bb04-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6bb04-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="6bb04-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bb04-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6bb04-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{778C74EE-DB2A-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_FRU
{
  string Caption;
  string Description;
  string FRUNumber;
  string IdentifyingNumber;
  string Name;
  string RevisionLevel;
  string Vendor;
};
```

## <a name="members"></a><span data-ttu-id="6bb04-110">Membros</span><span class="sxs-lookup"><span data-stu-id="6bb04-110">Members</span></span>

<span data-ttu-id="6bb04-111">A classe de **\_ FRU CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6bb04-111">The **CIM\_FRU** class has these types of members:</span></span>

-   [<span data-ttu-id="6bb04-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6bb04-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6bb04-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6bb04-113">Properties</span></span>

<span data-ttu-id="6bb04-114">A classe de **\_ FRU CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6bb04-114">The **CIM\_FRU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6bb04-115">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="6bb04-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb04-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6bb04-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bb04-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6bb04-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bb04-118">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6bb04-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6bb04-119">Breve descrição textual para a FRU.</span><span class="sxs-lookup"><span data-stu-id="6bb04-119">Short textual description for the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="6bb04-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6bb04-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb04-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6bb04-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bb04-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6bb04-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bb04-123">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| FRU \| 2,3 ")</span><span class="sxs-lookup"><span data-stu-id="6bb04-123">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.3")</span></span>
</dt> </dl>

<span data-ttu-id="6bb04-124">Descrição da FRU.</span><span class="sxs-lookup"><span data-stu-id="6bb04-124">Description of the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="6bb04-125">**FRUNumber**</span><span class="sxs-lookup"><span data-stu-id="6bb04-125">**FRUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb04-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6bb04-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bb04-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6bb04-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bb04-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| FRU \| 2,6 "), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6bb04-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.6"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6bb04-129">Informações de pedidos de FRU.</span><span class="sxs-lookup"><span data-stu-id="6bb04-129">FRU ordering information.</span></span>

</dd> <dt>

<span data-ttu-id="6bb04-130">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="6bb04-130">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb04-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6bb04-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bb04-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6bb04-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bb04-133">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| FRU \| 2,7 "), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6bb04-133">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.7"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6bb04-134">Identificação de software, como um número de série, ou um número de dado em um chip de hardware.</span><span class="sxs-lookup"><span data-stu-id="6bb04-134">Identification on software, such as a serial number, or a die number on a hardware chip.</span></span>

</dd> <dt>

<span data-ttu-id="6bb04-135">**Nome**</span><span class="sxs-lookup"><span data-stu-id="6bb04-135">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb04-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6bb04-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bb04-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6bb04-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bb04-138">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6bb04-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6bb04-139">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="6bb04-139">Label by which the object is known.</span></span>

</dd> <dt>

<span data-ttu-id="6bb04-140">**RevisionLevel**</span><span class="sxs-lookup"><span data-stu-id="6bb04-140">**RevisionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb04-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6bb04-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bb04-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6bb04-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bb04-143">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| FRU \| 2,8 "), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6bb04-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.8"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6bb04-144">Nível de revisão da FRU.</span><span class="sxs-lookup"><span data-stu-id="6bb04-144">Revision level of the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="6bb04-145">**Fornecedor**</span><span class="sxs-lookup"><span data-stu-id="6bb04-145">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb04-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6bb04-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bb04-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6bb04-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bb04-148">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| FRU \| 2,4 "), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6bb04-148">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.4"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6bb04-149">Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="6bb04-149">Name of the supplier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6bb04-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="6bb04-150">Remarks</span></span>

<span data-ttu-id="6bb04-151">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="6bb04-151">WMI does not implement this class.</span></span>

<span data-ttu-id="6bb04-152">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="6bb04-152">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6bb04-153">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="6bb04-153">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bb04-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bb04-154">Requirements</span></span>



| <span data-ttu-id="6bb04-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bb04-155">Requirement</span></span> | <span data-ttu-id="6bb04-156">Valor</span><span class="sxs-lookup"><span data-stu-id="6bb04-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6bb04-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6bb04-157">Minimum supported client</span></span><br/> | <span data-ttu-id="6bb04-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6bb04-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6bb04-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6bb04-159">Minimum supported server</span></span><br/> | <span data-ttu-id="6bb04-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6bb04-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6bb04-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="6bb04-161">Namespace</span></span><br/>                | <span data-ttu-id="6bb04-162">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6bb04-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6bb04-163">MOF</span><span class="sxs-lookup"><span data-stu-id="6bb04-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6bb04-164"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6bb04-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6bb04-165">DLL</span><span class="sxs-lookup"><span data-stu-id="6bb04-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6bb04-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bb04-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

