---
description: Representa um produto. Isso inclui software e hardware usado neste sistema de computador.
ms.assetid: 6241e703-4ce9-435f-bf36-4388e38a3ea5
ms.tgt_platform: multiple
title: Classe Win32_ComputerSystemProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystemProduct
- Win32_ComputerSystemProduct.Caption
- Win32_ComputerSystemProduct.Description
- Win32_ComputerSystemProduct.IdentifyingNumber
- Win32_ComputerSystemProduct.Name
- Win32_ComputerSystemProduct.SKUNumber
- Win32_ComputerSystemProduct.Vendor
- Win32_ComputerSystemProduct.Version
- Win32_ComputerSystemProduct.UUID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8cab3dc8679c606076eca2f5cf704867aa9833c9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089025"
---
# <a name="win32_computersystemproduct-class"></a><span data-ttu-id="d29be-104">\_Classe Win32 ComputerSystemProduct</span><span class="sxs-lookup"><span data-stu-id="d29be-104">Win32\_ComputerSystemProduct class</span></span>

<span data-ttu-id="d29be-105">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ ComputerSystemProduct do Win32** representa um produto.</span><span class="sxs-lookup"><span data-stu-id="d29be-105">The **Win32\_ComputerSystemProduct** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a product.</span></span> <span data-ttu-id="d29be-106">Isso inclui software e hardware usado neste sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="d29be-106">This includes software and hardware used on this computer system.</span></span>

<span data-ttu-id="d29be-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d29be-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d29be-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="d29be-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d29be-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d29be-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B96-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_ComputerSystemProduct : CIM_Product
{
  string Caption;
  string Description;
  string IdentifyingNumber;
  string Name;
  string SKUNumber;
  string Vendor;
  string Version;
  string UUID;
};
```

## <a name="members"></a><span data-ttu-id="d29be-110">Membros</span><span class="sxs-lookup"><span data-stu-id="d29be-110">Members</span></span>

<span data-ttu-id="d29be-111">A classe **Win32 \_ ComputerSystemProduct** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d29be-111">The **Win32\_ComputerSystemProduct** class has these types of members:</span></span>

-   [<span data-ttu-id="d29be-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d29be-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d29be-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d29be-113">Properties</span></span>

<span data-ttu-id="d29be-114">A classe **Win32 \_ ComputerSystemProduct** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d29be-114">The **Win32\_ComputerSystemProduct** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d29be-115">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="d29be-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d29be-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d29be-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d29be-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d29be-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d29be-118">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d29be-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d29be-119">Breve descrição textual do produto.</span><span class="sxs-lookup"><span data-stu-id="d29be-119">Short textual description for the product.</span></span>

<span data-ttu-id="d29be-120">Esta propriedade é herdada [**do \_ produto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="d29be-120">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="d29be-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d29be-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d29be-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d29be-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d29be-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d29be-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d29be-124">Descrição textual do produto.</span><span class="sxs-lookup"><span data-stu-id="d29be-124">Textual description of the product.</span></span>

<span data-ttu-id="d29be-125">Esta propriedade é herdada [**do \_ produto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="d29be-125">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="d29be-126">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="d29be-126">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d29be-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d29be-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d29be-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d29be-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d29be-129">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,4 ")</span><span class="sxs-lookup"><span data-stu-id="d29be-129">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="d29be-130">Identificação do produto, como um número de série em software, um número de dado em um chip de hardware ou (para produtos comerciais) um número de projeto.</span><span class="sxs-lookup"><span data-stu-id="d29be-130">Product identification, such as a serial number on software, a die number on a hardware chip, or (for noncommercial products) a project number.</span></span>

<span data-ttu-id="d29be-131">Esta propriedade é herdada [**do \_ produto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="d29be-131">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="d29be-132">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d29be-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d29be-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d29be-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d29be-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d29be-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d29be-135">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,2 ")</span><span class="sxs-lookup"><span data-stu-id="d29be-135">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="d29be-136">Nome do produto usado normalmente.</span><span class="sxs-lookup"><span data-stu-id="d29be-136">Commonly used product name.</span></span>

<span data-ttu-id="d29be-137">Esta propriedade é herdada [**do \_ produto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="d29be-137">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="d29be-138">**SKUNumber**</span><span class="sxs-lookup"><span data-stu-id="d29be-138">**SKUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d29be-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d29be-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d29be-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d29be-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d29be-141">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d29be-141">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d29be-142">Informações de SKU (unidade de manutenção de estoque) do produto.</span><span class="sxs-lookup"><span data-stu-id="d29be-142">Product's stock-keeping unit (SKU) information.</span></span>

<span data-ttu-id="d29be-143">Esta propriedade é herdada [**do \_ produto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="d29be-143">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="d29be-144">**UUID**</span><span class="sxs-lookup"><span data-stu-id="d29be-144">**UUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d29be-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d29be-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d29be-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d29be-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d29be-147">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| UUID do tipo 1 do SMBIOS \| ")</span><span class="sxs-lookup"><span data-stu-id="d29be-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|UUID")</span></span>
</dt> </dl>

<span data-ttu-id="d29be-148">UUID (identificador universal exclusivo) para este produto.</span><span class="sxs-lookup"><span data-stu-id="d29be-148">Universally unique identifier (UUID) for this product.</span></span> <span data-ttu-id="d29be-149">Um UUID é um identificador de 128 bits que é garantido para ser diferente de outros UUIDs gerados.</span><span class="sxs-lookup"><span data-stu-id="d29be-149">A UUID is a 128-bit identifier that is guaranteed to be different from other generated UUIDs.</span></span> <span data-ttu-id="d29be-150">Se um UUID não estiver disponível, um UUID de todos os zeros será usado.</span><span class="sxs-lookup"><span data-stu-id="d29be-150">If a UUID is not available, a UUID of all zeros is used.</span></span>

<span data-ttu-id="d29be-151">Esse valor é proveniente do membro **UUID** da estrutura de **informações do sistema** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d29be-151">This value comes from the **UUID** member of the **System Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="d29be-152">**Fornecedor**</span><span class="sxs-lookup"><span data-stu-id="d29be-152">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d29be-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d29be-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d29be-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d29be-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d29be-155">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,1 ")</span><span class="sxs-lookup"><span data-stu-id="d29be-155">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="d29be-156">Nome do fornecedor do produto ou a entidade que vende o produto (fabricante, revendedor, OEM e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="d29be-156">Name of the product's supplier, or the entity selling the product (the manufacturer, reseller, OEM, and so on).</span></span>

<span data-ttu-id="d29be-157">Esta propriedade é herdada [**do \_ produto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="d29be-157">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="d29be-158">**Versão**</span><span class="sxs-lookup"><span data-stu-id="d29be-158">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d29be-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d29be-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d29be-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d29be-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d29be-161">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="d29be-161">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="d29be-162">Informações de versão do produto.</span><span class="sxs-lookup"><span data-stu-id="d29be-162">Product version information.</span></span>

<span data-ttu-id="d29be-163">Esta propriedade é herdada [**do \_ produto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="d29be-163">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d29be-164">Comentários</span><span class="sxs-lookup"><span data-stu-id="d29be-164">Remarks</span></span>

<span data-ttu-id="d29be-165">A classe **Win32 \_ ComputerSystemProduct** é derivada do [**\_ produto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="d29be-165">The **Win32\_ComputerSystemProduct** class is derived from [**CIM\_Product**](cim-product.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d29be-166">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d29be-166">Examples</span></span>

<span data-ttu-id="d29be-167">A amostra do [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell na galeria do TechNet usa o **Win32 \_ ComputerSystemProduct** para recuperar uma lista de hardwares que não funciona usando o WMI.</span><span class="sxs-lookup"><span data-stu-id="d29be-167">The [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell sample on TechNet Gallery uses to **Win32\_ComputerSystemProduct** to retrieve a list of non-working hardware using WMI.</span></span>

## <a name="requirements"></a><span data-ttu-id="d29be-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d29be-168">Requirements</span></span>



| <span data-ttu-id="d29be-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="d29be-169">Requirement</span></span> | <span data-ttu-id="d29be-170">Valor</span><span class="sxs-lookup"><span data-stu-id="d29be-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d29be-171">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d29be-171">Minimum supported client</span></span><br/> | <span data-ttu-id="d29be-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d29be-172">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d29be-173">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d29be-173">Minimum supported server</span></span><br/> | <span data-ttu-id="d29be-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d29be-174">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d29be-175">Namespace</span><span class="sxs-lookup"><span data-stu-id="d29be-175">Namespace</span></span><br/>                | <span data-ttu-id="d29be-176">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d29be-176">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d29be-177">MOF</span><span class="sxs-lookup"><span data-stu-id="d29be-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d29be-178"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d29be-178"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d29be-179">DLL</span><span class="sxs-lookup"><span data-stu-id="d29be-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d29be-180"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d29be-180"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d29be-181">Confira também</span><span class="sxs-lookup"><span data-stu-id="d29be-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d29be-182">**\_Produto CIM**</span><span class="sxs-lookup"><span data-stu-id="d29be-182">**CIM\_Product**</span></span>](cim-product.md)
</dt> <dt>

<span data-ttu-id="d29be-183">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d29be-183">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

