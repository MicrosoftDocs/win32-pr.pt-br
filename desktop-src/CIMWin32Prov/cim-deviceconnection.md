---
description: A \_ classe de associação CIM DeviceConnection representa dois ou mais dispositivos conectados.
ms.assetid: 82095cd6-1843-4db2-9fe8-3e225611bd3b
ms.tgt_platform: multiple
title: Classe CIM_DeviceConnection (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceConnection
- CIM_DeviceConnection.Dependent
- CIM_DeviceConnection.Antecedent
- CIM_DeviceConnection.NegotiatedDataWidth
- CIM_DeviceConnection.NegotiatedSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b8179287686439ea31c19d700a785de7fff47659
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164071"
---
# <a name="cim_deviceconnection-class-cimwin32-wmi-providers"></a><span data-ttu-id="b37db-103">Classe CIM_DeviceConnection (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="b37db-103">CIM_DeviceConnection class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="b37db-104">A classe de associação **CIM \_ DeviceConnection** representa dois ou mais dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="b37db-104">The **CIM\_DeviceConnection** association class represents two or more connected devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b37db-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="b37db-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b37db-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b37db-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b37db-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b37db-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b37db-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="b37db-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b37db-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b37db-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53C-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DeviceConnection : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_LogicalDevice REF Antecedent;
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
};
```

## <a name="members"></a><span data-ttu-id="b37db-110">Membros</span><span class="sxs-lookup"><span data-stu-id="b37db-110">Members</span></span>

<span data-ttu-id="b37db-111">A classe **CIM \_ DeviceConnection** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b37db-111">The **CIM\_DeviceConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="b37db-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b37db-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b37db-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b37db-113">Properties</span></span>

<span data-ttu-id="b37db-114">A classe **CIM \_ DeviceConnection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b37db-114">The **CIM\_DeviceConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b37db-115">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="b37db-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b37db-116">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="b37db-116">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="b37db-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b37db-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b37db-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="b37db-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="b37db-119">Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que descreve um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b37db-119">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes a logical device.</span></span>

</dd> <dt>

<span data-ttu-id="b37db-120">**Depende**</span><span class="sxs-lookup"><span data-stu-id="b37db-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b37db-121">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="b37db-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="b37db-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b37db-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b37db-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="b37db-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="b37db-124">Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que descreve um segundo dispositivo lógico conectado ao dispositivo Antecedent.</span><span class="sxs-lookup"><span data-stu-id="b37db-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes a second logical device connected to the Antecedent device.</span></span>

</dd> <dt>

<span data-ttu-id="b37db-125">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="b37db-125">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b37db-126">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b37db-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b37db-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b37db-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b37db-128">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="b37db-128">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="b37db-129">Quando várias larguras de dados de barramento ou conexão são possíveis, essa propriedade define a que está em uso entre os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b37db-129">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="b37db-130">A largura dos dados é especificada em bits.</span><span class="sxs-lookup"><span data-stu-id="b37db-130">Data width is specified in bits.</span></span> <span data-ttu-id="b37db-131">Se a largura dos dados não for negociada ou se essas informações não estiverem disponíveis ou importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="b37db-131">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="b37db-132">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="b37db-132">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b37db-133">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b37db-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b37db-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b37db-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b37db-135">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="b37db-135">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="b37db-136">Quando várias velocidades de barramento ou conexão são possíveis, essa propriedade define a que está sendo usada entre os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b37db-136">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="b37db-137">A velocidade é especificada em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="b37db-137">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="b37db-138">Se as velocidades de conexão ou de barramento não forem negociadas ou se essas informações não estiverem disponíveis ou importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="b37db-138">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="b37db-139">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b37db-139">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b37db-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="b37db-140">Remarks</span></span>

<span data-ttu-id="b37db-141">A classe **CIM \_ DeviceConnection** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="b37db-141">The **CIM\_DeviceConnection** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="b37db-142">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="b37db-142">WMI does not implement this class.</span></span> <span data-ttu-id="b37db-143">Para obter mais informações sobre classes derivadas de **CIM \_ DeviceConnection**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b37db-143">For more information about classes derived from **CIM\_DeviceConnection**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="b37db-144">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="b37db-144">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b37db-145">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="b37db-145">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b37db-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b37db-146">Requirements</span></span>



| <span data-ttu-id="b37db-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="b37db-147">Requirement</span></span> | <span data-ttu-id="b37db-148">Valor</span><span class="sxs-lookup"><span data-stu-id="b37db-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b37db-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b37db-149">Minimum supported client</span></span><br/> | <span data-ttu-id="b37db-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b37db-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b37db-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b37db-151">Minimum supported server</span></span><br/> | <span data-ttu-id="b37db-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b37db-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b37db-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="b37db-153">Namespace</span></span><br/>                | <span data-ttu-id="b37db-154">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b37db-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b37db-155">MOF</span><span class="sxs-lookup"><span data-stu-id="b37db-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b37db-156"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b37db-156"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b37db-157">DLL</span><span class="sxs-lookup"><span data-stu-id="b37db-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b37db-158"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b37db-158"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b37db-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="b37db-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b37db-160">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="b37db-160">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

