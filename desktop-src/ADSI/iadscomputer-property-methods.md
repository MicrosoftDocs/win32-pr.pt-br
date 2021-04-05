---
title: Métodos de propriedade IADsComputer (IADs. h)
description: Os métodos de interface IADsComputer lêem e gravam as propriedades descritas neste tópico. Para obter mais informações, consulte interface Property Methods.
ms.assetid: c990b6bb-6256-4216-9435-c85c67db4d13
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsComputer
topic_type:
- apiref
api_name:
- IADsComputer Property Methods
- IADsComputer.ComputerID
- IADsComputer.get_ComputerID
- IADsComputer.Department
- IADsComputer.get_Department
- IADsComputer.put_Department
- IADsComputer.Description
- IADsComputer.get_Description
- IADsComputer.put_Description
- IADsComputer.Division
- IADsComputer.get_Division
- IADsComputer.put_Division
- IADsComputer.Location
- IADsComputer.get_Location
- IADsComputer.put_Location
- IADsComputer.MemorySize
- IADsComputer.get_MemorySize
- IADsComputer.put_MemorySize
- IADsComputer.Model
- IADsComputer.get_Model
- IADsComputer.put_Model
- IADsComputer.NetAddresses
- IADsComputer.get_NetAddresses
- IADsComputer.put_NetAddresses
- IADsComputer.OperatingSystem
- IADsComputer.get_OperatingSystem
- IADsComputer.put_OperatingSystem
- IADsComputer.OperatingSystemVersion
- IADsComputer.get_OperatingSystemVersion
- IADsComputer.put_OperatingSystemVersion
- IADsComputer.Owner
- IADsComputer.get_Owner
- IADsComputer.put_Owner
- IADsComputer.PrimaryUser
- IADsComputer.get_PrimaryUser
- IADsComputer.put_PrimaryUser
- IADsComputer.Processor
- IADsComputer.get_Processor
- IADsComputer.put_Processor
- IADsComputer.ProcessorCount
- IADsComputer.get_ProcessorCount
- IADsComputer.put_ProcessorCount
- IADsComputer.Role
- IADsComputer.get_Role
- IADsComputer.put_Role
- IADsComputer.Site
- IADsComputer.get_Site
- IADsComputer.StorageCapacity
- IADsComputer.get_StorageCapacity
- IADsComputer.put_StorageCapacity
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f2f3c455e2e43436627b62d142781bb6a605bef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824630"
---
# <a name="iadscomputer-property-methods"></a><span data-ttu-id="8ad68-105">Métodos de propriedade IADsComputer</span><span class="sxs-lookup"><span data-stu-id="8ad68-105">IADsComputer Property Methods</span></span>

<span data-ttu-id="8ad68-106">Os métodos de interface [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) lêem e gravam as propriedades descritas neste tópico.</span><span class="sxs-lookup"><span data-stu-id="8ad68-106">The [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) interface methods read and write the properties described in this topic.</span></span> <span data-ttu-id="8ad68-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="8ad68-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="8ad68-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8ad68-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="8ad68-109">**Computadorid**</span><span class="sxs-lookup"><span data-stu-id="8ad68-109">**ComputerID**</span></span>
<span data-ttu-id="8ad68-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8ad68-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="8ad68-111">O identificador global exclusivo atribuído a cada computador.</span><span class="sxs-lookup"><span data-stu-id="8ad68-111">The globally unique identifier assigned to each computer.</span></span>

<dt>

<span data-ttu-id="8ad68-112">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ad68-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ad68-113">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8ad68-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerID(
  [out] BSTR* pbstrComputerID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ad68-114">**Departamento**</span><span class="sxs-lookup"><span data-stu-id="8ad68-114">**Department**</span></span>
<span data-ttu-id="8ad68-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8ad68-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="8ad68-116">A UO (unidade organizacional), como departamento, à qual este computador pertence.</span><span class="sxs-lookup"><span data-stu-id="8ad68-116">The organizational unit (OU), such as department, that this computer belongs to.</span></span>

<dt>

<span data-ttu-id="8ad68-117">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8ad68-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8ad68-118">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8ad68-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Department(
  [out] BSTR* pbstrDepartment
);
HRESULT put_Department(
  [in] BSTR bstrDepartment
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ad68-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8ad68-119">**Description**</span></span>
<span data-ttu-id="8ad68-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8ad68-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="8ad68-121">A descrição deste computador.</span><span class="sxs-lookup"><span data-stu-id="8ad68-121">The description of this computer.</span></span>

<dt>

<span data-ttu-id="8ad68-122">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8ad68-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8ad68-123">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8ad68-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ad68-124">**Divisão**</span><span class="sxs-lookup"><span data-stu-id="8ad68-124">**Division**</span></span>
<span data-ttu-id="8ad68-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8ad68-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="8ad68-126">A divisão, dentro de uma organização, à qual este computador pertence.</span><span class="sxs-lookup"><span data-stu-id="8ad68-126">The division, within an organization, that this computer belongs to.</span></span>

<dt>

<span data-ttu-id="8ad68-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8ad68-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8ad68-128">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8ad68-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Division(
  [out] BSTR* pbstrDivision
);
HRESULT put_Division(
  [in] BSTR bstrDivision
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ad68-129">**Localidade**</span><span class="sxs-lookup"><span data-stu-id="8ad68-129">**Location**</span></span>
<span data-ttu-id="8ad68-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8ad68-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="8ad68-131">O local físico atribuído deste computador.</span><span class="sxs-lookup"><span data-stu-id="8ad68-131">The assigned physical location of this computer.</span></span>

<dt>

<span data-ttu-id="8ad68-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8ad68-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8ad68-133">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8ad68-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Location(
  [out] BSTR* pbstrLocation
);
HRESULT put_Location(
  [in] BSTR bstrLocation
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ad68-134">**Tamanho da memória**</span><span class="sxs-lookup"><span data-stu-id="8ad68-134">**MemorySize**</span></span>
<span data-ttu-id="8ad68-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8ad68-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="8ad68-136">O tamanho, em megabytes, da memória de acesso aleatório para este computador.</span><span class="sxs-lookup"><span data-stu-id="8ad68-136">The size, in megabytes, of random access memory for this computer.</span></span>

<dt>

<span data-ttu-id="8ad68-137">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8ad68-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8ad68-138">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8ad68-138">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MemorySize(
  [out] BSTR* pbstrMemorySize
);
HRESULT put_MemorySize(
  [in] BSTR bstrMemorySize
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ad68-139">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="8ad68-139">**Model**</span></span>
<span data-ttu-id="8ad68-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8ad68-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="8ad68-141">A marca e o modelo deste computador.</span><span class="sxs-lookup"><span data-stu-id="8ad68-141">The make and model of this computer.</span></span>

<dt>

<span data-ttu-id="8ad68-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8ad68-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8ad68-143">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8ad68-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Model(
  [out] BSTR* pbstrModel
);
HRESULT put_Model(
  [in] BSTR bstrModel
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ad68-144">**Endereços de**</span><span class="sxs-lookup"><span data-stu-id="8ad68-144">**NetAddresses**</span></span>
<span data-ttu-id="8ad68-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8ad68-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="8ad68-146">Uma matriz de campos do netaddress que representam os endereços pelos quais esse computador pode ser alcançado.</span><span class="sxs-lookup"><span data-stu-id="8ad68-146">An array of NetAddress fields that represent the addresses by which this computer can be reached.</span></span> <span data-ttu-id="8ad68-147">Netaddress é um **BSTR** específico de provedor composto por duas subcadeias de caracteres separadas por dois-pontos (:).</span><span class="sxs-lookup"><span data-stu-id="8ad68-147">NetAddress is a provider-specific **BSTR** composed of two substrings separated by a colon (:).</span></span> <span data-ttu-id="8ad68-148">A subcadeia de caracteres esquerda indica o tipo de endereço e a subcadeia de caracteres direita é uma representação de cadeia de caracteres de um endereço desse tipo.</span><span class="sxs-lookup"><span data-stu-id="8ad68-148">The left substring indicates the address type, and the right substring is a string representation of an address of that type.</span></span> <span data-ttu-id="8ad68-149">Por exemplo, os endereços TCP/IP estão no formato: IP: 100.201.301.45.</span><span class="sxs-lookup"><span data-stu-id="8ad68-149">For example, TCP/IP addresses are of the form: IP:100.201.301.45.</span></span> <span data-ttu-id="8ad68-150">Os endereços do tipo IPX são do formato: IPX: 10.123456.80.</span><span class="sxs-lookup"><span data-stu-id="8ad68-150">IPX type addresses are of the form: IPX:10.123456.80.</span></span>

<dt>

<span data-ttu-id="8ad68-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8ad68-151">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8ad68-152">Tipo de dados de script: **Variant**</span><span class="sxs-lookup"><span data-stu-id="8ad68-152">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NetAddresses(
  [out] VARIANT* pvNetAddresses
);
HRESULT put_NetAddresses(
  [in] VARIANT vNetAddresses
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ad68-153">**Operacional**</span><span class="sxs-lookup"><span data-stu-id="8ad68-153">**OperatingSystem**</span></span>
<span data-ttu-id="8ad68-154"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8ad68-154"></dt> <dd> <dl></span></span>

<span data-ttu-id="8ad68-155">O sistema operacional usado neste computador.</span><span class="sxs-lookup"><span data-stu-id="8ad68-155">The operating system used on this computer.</span></span>

<dt>

<span data-ttu-id="8ad68-156">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8ad68-156">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8ad68-157">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8ad68-157">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OperatingSystem(
  [out] BSTR* pbstrOperatingSystem
);
HRESULT put_OperatingSystem(
  [in] BSTR bstrOperatingSystem
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ad68-158">**OperatingSystemVersion**</span><span class="sxs-lookup"><span data-stu-id="8ad68-158">**OperatingSystemVersion**</span></span>
<span data-ttu-id="8ad68-159"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8ad68-159"></dt> <dd> <dl></span></span>

<span data-ttu-id="8ad68-160">A versão do sistema operacional usada neste computador.</span><span class="sxs-lookup"><span data-stu-id="8ad68-160">The version of the operating system used on this computer.</span></span>

<dt>

<span data-ttu-id="8ad68-161">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8ad68-161">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8ad68-162">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8ad68-162">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OperatingSystemVersion(
  [out] BSTR* pbstrOperatingSystemVersion
);
HRESULT put_OperatingSystemVersion(
  [in] BSTR bstrOperatingSystemVersion
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ad68-163">**Proprietário**</span><span class="sxs-lookup"><span data-stu-id="8ad68-163">**Owner**</span></span>
<span data-ttu-id="8ad68-164"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8ad68-164"></dt> <dd> <dl></span></span>

<span data-ttu-id="8ad68-165">A pessoa a quem este computador está atribuído.</span><span class="sxs-lookup"><span data-stu-id="8ad68-165">The person to whom this computer is assigned.</span></span> <span data-ttu-id="8ad68-166">Essa pessoa também deve ter uma licença para executar o software instalado.</span><span class="sxs-lookup"><span data-stu-id="8ad68-166">This person should also have a license to run the installed software.</span></span>

<dt>

<span data-ttu-id="8ad68-167">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8ad68-167">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8ad68-168">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8ad68-168">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Owner(
  [out] BSTR* pbstrOwner
);
HRESULT put_Owner(
  [in] BSTR bstrOwner
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ad68-169">**PrimaryUser**</span><span class="sxs-lookup"><span data-stu-id="8ad68-169">**PrimaryUser**</span></span>
<span data-ttu-id="8ad68-170"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8ad68-170"></dt> <dd> <dl></span></span>

<span data-ttu-id="8ad68-171">O nome da pessoa de contato, como um administrador, para este computador.</span><span class="sxs-lookup"><span data-stu-id="8ad68-171">The name of the contact person, such as an administrator, for this computer.</span></span>

<dt>

<span data-ttu-id="8ad68-172">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8ad68-172">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8ad68-173">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8ad68-173">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrimaryUser(
  [out] BSTR* pbstrPrimaryUser
);
HRESULT put_PrimaryUser(
  [in] BSTR bstrPrimaryUser
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ad68-174">**Processador**</span><span class="sxs-lookup"><span data-stu-id="8ad68-174">**Processor**</span></span>
<span data-ttu-id="8ad68-175"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8ad68-175"></dt> <dd> <dl></span></span>

<span data-ttu-id="8ad68-176">O tipo de processador.</span><span class="sxs-lookup"><span data-stu-id="8ad68-176">The processor type.</span></span>

<dt>

<span data-ttu-id="8ad68-177">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8ad68-177">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8ad68-178">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8ad68-178">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Processor(
  [out] BSTR* pbstrProcessor
);
HRESULT put_Processor(
  [in] BSTR bstrProcessor
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ad68-179">**ProcessorCount**</span><span class="sxs-lookup"><span data-stu-id="8ad68-179">**ProcessorCount**</span></span>
<span data-ttu-id="8ad68-180"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8ad68-180"></dt> <dd> <dl></span></span>

<span data-ttu-id="8ad68-181">O número de processadores instalados.</span><span class="sxs-lookup"><span data-stu-id="8ad68-181">The number of installed processors.</span></span>

<dt>

<span data-ttu-id="8ad68-182">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8ad68-182">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8ad68-183">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8ad68-183">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ProcessorCount(
  [out] BSTR* pbstrProcessorCount
);
HRESULT put_ProcessorCount(
  [in] BSTR bstrProcessorCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ad68-184">**Função**</span><span class="sxs-lookup"><span data-stu-id="8ad68-184">**Role**</span></span>
<span data-ttu-id="8ad68-185"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8ad68-185"></dt> <dd> <dl></span></span>

<span data-ttu-id="8ad68-186">A função deste computador, por exemplo, estação de trabalho, servidor ou controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="8ad68-186">The role of this computer, for example, workstation, server, or domain controller.</span></span>

<dt>

<span data-ttu-id="8ad68-187">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8ad68-187">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8ad68-188">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8ad68-188">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Role(
  [out] BSTR* pbstrRole
);
HRESULT put_Role(
  [in] BSTR bstrRole
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ad68-189">**Site**</span><span class="sxs-lookup"><span data-stu-id="8ad68-189">**Site**</span></span>
<span data-ttu-id="8ad68-190"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8ad68-190"></dt> <dd> <dl></span></span>

<span data-ttu-id="8ad68-191">O identificador global exclusivo que identifica o site no qual este computador foi instalado.</span><span class="sxs-lookup"><span data-stu-id="8ad68-191">The globally unique identifier that identifies the site that this computer was installed in.</span></span> <span data-ttu-id="8ad68-192">Um site é uma região física de boa conectividade em uma rede.</span><span class="sxs-lookup"><span data-stu-id="8ad68-192">A site is a physical region of good connectivity in a network.</span></span>

<dt>

<span data-ttu-id="8ad68-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ad68-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ad68-194">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8ad68-194">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Site(
  [out] BSTR* pbstrSite
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ad68-195">**StorageCapacity**</span><span class="sxs-lookup"><span data-stu-id="8ad68-195">**StorageCapacity**</span></span>
<span data-ttu-id="8ad68-196"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8ad68-196"></dt> <dd> <dl></span></span>

<span data-ttu-id="8ad68-197">O tamanho, em megabytes, do disco.</span><span class="sxs-lookup"><span data-stu-id="8ad68-197">The size, in megabytes, of the disk.</span></span>

<dt>

<span data-ttu-id="8ad68-198">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8ad68-198">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8ad68-199">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8ad68-199">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StorageCapacity(
  [out] BSTR* pbstrStorageCapacity
);
HRESULT put_StorageCapacity(
  [in] BSTR bstrStorageCapacity
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="8ad68-200">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ad68-200">Remarks</span></span>

<span data-ttu-id="8ad68-201">Provedores diferentes podem optar por expor propriedades diferentes de um objeto de computador.</span><span class="sxs-lookup"><span data-stu-id="8ad68-201">Different providers may choose to expose different properties of a computer object.</span></span> <span data-ttu-id="8ad68-202">Para obter mais informações, consulte [ADSI System Providers](adsi-system-providers.md).</span><span class="sxs-lookup"><span data-stu-id="8ad68-202">For more information, see [ADSI System Providers](adsi-system-providers.md).</span></span>

<span data-ttu-id="8ad68-203">Você pode descobrir quais propriedades têm suporte inspecionando as propriedades obrigatórias e opcionais por meio de sua classe de esquema.</span><span class="sxs-lookup"><span data-stu-id="8ad68-203">You can discover what properties are supported by inspecting the mandatory and optional properties through its schema class.</span></span> <span data-ttu-id="8ad68-204">Para obter mais informações, consulte a interface [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) .</span><span class="sxs-lookup"><span data-stu-id="8ad68-204">For more information, see the [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface.</span></span>

<span data-ttu-id="8ad68-205">Para examinar o status de um computador ou executar a operação de desligamento na rede, você deve usar a interface [**IADsComputerOperations**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations) .</span><span class="sxs-lookup"><span data-stu-id="8ad68-205">To examine the status of a computer or to perform the shutdown operation across the network, you must use the [**IADsComputerOperations**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="8ad68-206">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8ad68-206">Examples</span></span>

<span data-ttu-id="8ad68-207">O exemplo de código a seguir Visual Basic examina as propriedades do computador com suporte pelo provedor ADSI WinNT.</span><span class="sxs-lookup"><span data-stu-id="8ad68-207">The following Visual Basic code example examines computer properties supported by the ADSI WinNT provider.</span></span>


```VB
Dim obj As IADs
On Error Resume Next

Set obj = GetObject("WinNT://myMachine,computer")
If (obj.Class = "Computer") Then
    MsgBox "Computer owner: " & obj.owner
    MsgBox "Computer division: " & obj.Division
    MsgBox "Computer operatingSystem: " & obj.OperatingSystem
    MsgBox "Computer operating System Version: " & obj.OperatingSystemVersion
    MsgBox "Computer processor: " & obj.Processor
    MsgBox "Computer processor Count: " & obj.ProcessorCount
End If
```



<span data-ttu-id="8ad68-208">O exemplo de código C++ a seguir examina as propriedades do computador com suporte pelo provedor ADSI WinNT.</span><span class="sxs-lookup"><span data-stu-id="8ad68-208">The following C++ code example examines computer properties supported by the ADSI WinNT provider.</span></span>


```C++
IADsComputer *pComp = NULL;
LPWSTR adspath = L"WinNT://jeffsmith1,computer";
HRESULT hr = S_OK;
BSTR bstr = NULL;

hr = ADsGetObject(adspath,IID_IADsComputer,(void**)&pComp);
if(FAILED(hr)) {goto Cleanup;}

hr = pComp->get_Owner(&bstr);
if(FAILED(hr)) {goto Cleanup;}

printf("Computer owner: %S\n",bstr);
SysFreeString(bstr);

hr = pComp->get_OperatingSystem(&bstr);
if(FAILED(hr)) {goto Cleanup;}
printf("Operating System: %S\n",bstr);
SysFreeString(bstr);

Cleanup:
    if(pComp) pComp->Release();
    if(bstr) SysFreeString(bstr);
    return hr;
```



## <a name="requirements"></a><span data-ttu-id="8ad68-209">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ad68-209">Requirements</span></span>



| <span data-ttu-id="8ad68-210">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ad68-210">Requirement</span></span> | <span data-ttu-id="8ad68-211">Valor</span><span class="sxs-lookup"><span data-stu-id="8ad68-211">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ad68-212">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ad68-212">Minimum supported client</span></span><br/> | <span data-ttu-id="8ad68-213">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8ad68-213">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8ad68-214">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ad68-214">Minimum supported server</span></span><br/> | <span data-ttu-id="8ad68-215">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8ad68-215">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8ad68-216">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8ad68-216">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ad68-217"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ad68-217"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="8ad68-218">DLL</span><span class="sxs-lookup"><span data-stu-id="8ad68-218">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ad68-219"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ad68-219"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="8ad68-220">IID</span><span class="sxs-lookup"><span data-stu-id="8ad68-220">IID</span></span><br/>                      | <span data-ttu-id="8ad68-221">IID \_ IADsComputer é definido como EFE3CC70-1D9F-11CF-B1F3-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="8ad68-221">IID\_IADsComputer is defined as EFE3CC70-1D9F-11CF-B1F3-02608C9E7553</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="8ad68-222">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ad68-222">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ad68-223">**IADsComputer**</span><span class="sxs-lookup"><span data-stu-id="8ad68-223">**IADsComputer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscomputer)
</dt> <dt>

[<span data-ttu-id="8ad68-224">Provedores de sistema ADSI</span><span class="sxs-lookup"><span data-stu-id="8ad68-224">ADSI System Providers</span></span>](adsi-system-providers.md)
</dt> <dt>

[<span data-ttu-id="8ad68-225">**IADsClass**</span><span class="sxs-lookup"><span data-stu-id="8ad68-225">**IADsClass**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[<span data-ttu-id="8ad68-226">**IADsComputerOperations**</span><span class="sxs-lookup"><span data-stu-id="8ad68-226">**IADsComputerOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations)
</dt> <dt>

[<span data-ttu-id="8ad68-227">Métodos de propriedade de interface</span><span class="sxs-lookup"><span data-stu-id="8ad68-227">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





