---
description: A \_ classe CIM StorageError representa blocos de mídia ou espaço de memória que são mapeados fora de uso devido a erros. A chave da classe é a propriedade StartingAddress dos bytes em erro.
ms.assetid: e786aa39-4718-416b-b659-bf4b8d3e2851
ms.tgt_platform: multiple
title: Classe CIM_StorageError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageError
- CIM_StorageError.DeviceCreationClassName
- CIM_StorageError.DeviceID
- CIM_StorageError.EndingAddress
- CIM_StorageError.StartingAddress
- CIM_StorageError.SystemCreationClassName
- CIM_StorageError.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6f5b197a5c82e61e054f5875fad466cac808ec38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762767"
---
# <a name="cim_storageerror-class"></a><span data-ttu-id="8d1ef-104">\_Classe CIM StorageError</span><span class="sxs-lookup"><span data-stu-id="8d1ef-104">CIM\_StorageError class</span></span>

<span data-ttu-id="8d1ef-105">A classe **CIM \_ StorageError** representa blocos de mídia ou espaço de memória que são mapeados fora de uso devido a erros.</span><span class="sxs-lookup"><span data-stu-id="8d1ef-105">The **CIM\_StorageError** class represents blocks of media or memory space that are mapped out-of-use due to errors.</span></span> <span data-ttu-id="8d1ef-106">A chave da classe é a propriedade **StartingAddress** dos bytes em erro.</span><span class="sxs-lookup"><span data-stu-id="8d1ef-106">The key of the class is the **StartingAddress** property of the bytes in error.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8d1ef-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="8d1ef-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8d1ef-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8d1ef-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8d1ef-109">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8d1ef-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="8d1ef-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="8d1ef-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d1ef-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8d1ef-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{71312AB6-DB31-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_StorageError
{
  string DeviceCreationClassName;
  string DeviceID;
  uint64 EndingAddress;
  uint64 StartingAddress;
  string SystemCreationClassName;
  string SystemName;
};
```

## <a name="members"></a><span data-ttu-id="8d1ef-112">Membros</span><span class="sxs-lookup"><span data-stu-id="8d1ef-112">Members</span></span>

<span data-ttu-id="8d1ef-113">A classe **CIM \_ StorageError** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8d1ef-113">The **CIM\_StorageError** class has these types of members:</span></span>

-   [<span data-ttu-id="8d1ef-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8d1ef-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8d1ef-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8d1ef-115">Properties</span></span>

<span data-ttu-id="8d1ef-116">A classe **CIM \_ StorageError** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8d1ef-116">The **CIM\_StorageError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8d1ef-117">**DeviceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8d1ef-117">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d1ef-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8d1ef-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d1ef-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d1ef-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d1ef-120">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="8d1ef-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageExtent**](cim-storageextent.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="8d1ef-121">Nome da classe de criação da extensão de armazenamento de escopo.</span><span class="sxs-lookup"><span data-stu-id="8d1ef-121">Scoping storage extent's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="8d1ef-122">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="8d1ef-122">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d1ef-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8d1ef-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d1ef-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d1ef-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d1ef-125">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**DeviceID**")</span><span class="sxs-lookup"><span data-stu-id="8d1ef-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageExtent**](cim-storageextent.md).**DeviceID**")</span></span>
</dt> </dl>

<span data-ttu-id="8d1ef-126">Identificador de dispositivo da extensão de armazenamento de escopo.</span><span class="sxs-lookup"><span data-stu-id="8d1ef-126">Scoping storage extent's device identifier.</span></span>

</dd> <dt>

<span data-ttu-id="8d1ef-127">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="8d1ef-127">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d1ef-128">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8d1ef-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8d1ef-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d1ef-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d1ef-130">Endereço final do erro de bytes.</span><span class="sxs-lookup"><span data-stu-id="8d1ef-130">Ending address of the bytes in error.</span></span>

<span data-ttu-id="8d1ef-131">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8d1ef-131">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8d1ef-132">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="8d1ef-132">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d1ef-133">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8d1ef-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8d1ef-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d1ef-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d1ef-135">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8d1ef-135">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8d1ef-136">Endereço inicial do erro de bytes.</span><span class="sxs-lookup"><span data-stu-id="8d1ef-136">Starting address of the bytes in error.</span></span>

<span data-ttu-id="8d1ef-137">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8d1ef-137">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8d1ef-138">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8d1ef-138">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d1ef-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8d1ef-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d1ef-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d1ef-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d1ef-141">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**SystemCreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="8d1ef-141">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageExtent**](cim-storageextent.md).**SystemCreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="8d1ef-142">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="8d1ef-142">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="8d1ef-143">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8d1ef-143">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d1ef-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8d1ef-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d1ef-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d1ef-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d1ef-146">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**SystemName**")</span><span class="sxs-lookup"><span data-stu-id="8d1ef-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageExtent**](cim-storageextent.md).**SystemName**")</span></span>
</dt> </dl>

<span data-ttu-id="8d1ef-147">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="8d1ef-147">Scoping system's name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d1ef-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d1ef-148">Remarks</span></span>

<span data-ttu-id="8d1ef-149">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="8d1ef-149">WMI does not implement this class.</span></span>

<span data-ttu-id="8d1ef-150">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="8d1ef-150">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8d1ef-151">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="8d1ef-151">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d1ef-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d1ef-152">Requirements</span></span>



| <span data-ttu-id="8d1ef-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d1ef-153">Requirement</span></span> | <span data-ttu-id="8d1ef-154">Valor</span><span class="sxs-lookup"><span data-stu-id="8d1ef-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d1ef-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d1ef-155">Minimum supported client</span></span><br/> | <span data-ttu-id="8d1ef-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8d1ef-156">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8d1ef-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d1ef-157">Minimum supported server</span></span><br/> | <span data-ttu-id="8d1ef-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d1ef-158">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8d1ef-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="8d1ef-159">Namespace</span></span><br/>                | <span data-ttu-id="8d1ef-160">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8d1ef-160">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8d1ef-161">MOF</span><span class="sxs-lookup"><span data-stu-id="8d1ef-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d1ef-162"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d1ef-162"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8d1ef-163">DLL</span><span class="sxs-lookup"><span data-stu-id="8d1ef-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d1ef-164"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d1ef-164"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

