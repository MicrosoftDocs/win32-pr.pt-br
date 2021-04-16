---
description: Representa um par de chave/valor.
ms.assetid: B13E9C5F-5B13-4EE5-AE5F-F51B61BDB9B7
title: Classe Msvm_KvpExchangeDataItem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_KvpExchangeDataItem
- Msvm_KvpExchangeDataItem.InstanceID
- Msvm_KvpExchangeDataItem.Caption
- Msvm_KvpExchangeDataItem.Description
- Msvm_KvpExchangeDataItem.ElementName
- Msvm_KvpExchangeDataItem.Source
- Msvm_KvpExchangeDataItem.Name
- Msvm_KvpExchangeDataItem.Data
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 540c54a694dab1c80a32f9648a90c5b5bf1e48a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757837"
---
# <a name="msvm_kvpexchangedataitem-class"></a><span data-ttu-id="b25aa-103">\_Classe Msvm KvpExchangeDataItem</span><span class="sxs-lookup"><span data-stu-id="b25aa-103">Msvm\_KvpExchangeDataItem class</span></span>

<span data-ttu-id="b25aa-104">Representa um par de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="b25aa-104">Represents a key/value pair.</span></span>

<span data-ttu-id="b25aa-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b25aa-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b25aa-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b25aa-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_KvpExchangeDataItem : CIM_ManagedElement
{
  string InstanceID;
  string Caption = "Key-Value Pair Exchange Data Item";
  string Description = "Microsoft Key-Value Pair Exchange Data Item";
  string ElementName = "Key-Value Pair Exchange Data Item";
  uint16 Source;
  string Name;
  string Data;
};
```

## <a name="members"></a><span data-ttu-id="b25aa-107">Membros</span><span class="sxs-lookup"><span data-stu-id="b25aa-107">Members</span></span>

<span data-ttu-id="b25aa-108">A classe **Msvm \_ KvpExchangeDataItem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b25aa-108">The **Msvm\_KvpExchangeDataItem** class has these types of members:</span></span>

-   [<span data-ttu-id="b25aa-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b25aa-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b25aa-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b25aa-110">Properties</span></span>

<span data-ttu-id="b25aa-111">A classe **Msvm \_ KvpExchangeDataItem** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b25aa-111">The **Msvm\_KvpExchangeDataItem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b25aa-112">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="b25aa-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25aa-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b25aa-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b25aa-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b25aa-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b25aa-115">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="b25aa-115">A short description of the object.</span></span> <span data-ttu-id="b25aa-116">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b25aa-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b25aa-117">**Dados**</span><span class="sxs-lookup"><span data-stu-id="b25aa-117">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25aa-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b25aa-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b25aa-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b25aa-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b25aa-120">Qualificadores: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="b25aa-120">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="b25aa-121">A parte de valor do par chave/valor.</span><span class="sxs-lookup"><span data-stu-id="b25aa-121">The value portion of the key/value pair.</span></span>

</dd> <dt>

<span data-ttu-id="b25aa-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b25aa-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25aa-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b25aa-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b25aa-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b25aa-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b25aa-125">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="b25aa-125">A description of the object.</span></span> <span data-ttu-id="b25aa-126">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b25aa-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b25aa-127">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b25aa-127">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25aa-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b25aa-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b25aa-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b25aa-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b25aa-130">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="b25aa-130">A display name for the object.</span></span> <span data-ttu-id="b25aa-131">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b25aa-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b25aa-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b25aa-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25aa-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b25aa-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b25aa-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b25aa-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b25aa-135">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="b25aa-135">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b25aa-136">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="b25aa-136">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b25aa-137">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b25aa-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b25aa-138">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b25aa-138">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25aa-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b25aa-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b25aa-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b25aa-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b25aa-141">Qualificadores: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="b25aa-141">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="b25aa-142">A parte principal do par chave/valor.</span><span class="sxs-lookup"><span data-stu-id="b25aa-142">The key portion of the key/value pair.</span></span>



| <span data-ttu-id="b25aa-143">Chave</span><span class="sxs-lookup"><span data-stu-id="b25aa-143">Key</span></span>                                                                                                     | <span data-ttu-id="b25aa-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="b25aa-144">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b25aa-145"><dt>"CSDVersion"</dt></span><span class="sxs-lookup"><span data-stu-id="b25aa-145"><dt>"CSDVersion"</dt></span></span> </dl>                 | <span data-ttu-id="b25aa-146">Uma cadeia de caracteres que representa as service pack mais recentes instaladas no sistema convidado.</span><span class="sxs-lookup"><span data-stu-id="b25aa-146">A string that represents the latest service pack installed on the guest system.</span></span> <span data-ttu-id="b25aa-147">Por exemplo, "Service Pack 2".</span><span class="sxs-lookup"><span data-stu-id="b25aa-147">For example, "Service Pack 2".</span></span> <span data-ttu-id="b25aa-148">Se nenhum service pack tiver sido instalado, essa cadeia de caracteres estará vazia.</span><span class="sxs-lookup"><span data-stu-id="b25aa-148">If no service pack has been installed, this string is empty.</span></span><br/>                                                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="b25aa-149"><dt>FullyQualifiedDomainName</dt></span><span class="sxs-lookup"><span data-stu-id="b25aa-149"><dt>"FullyQualifiedDomainName"</dt></span></span> </dl>   | <span data-ttu-id="b25aa-150">Uma cadeia de caracteres que representa o nome DNS totalmente qualificado que identifica exclusivamente o computador local.</span><span class="sxs-lookup"><span data-stu-id="b25aa-150">A string that represents the fully qualified DNS name that uniquely identifies the local computer.</span></span> <span data-ttu-id="b25aa-151">Esse nome é uma combinação do nome do host DNS e do nome de domínio DNS, usando o formato *hostname*. *Nome_do_domínio*.</span><span class="sxs-lookup"><span data-stu-id="b25aa-151">This name is a combination of the DNS host name and the DNS domain name, using the format *HostName*.*DomainName*.</span></span> <span data-ttu-id="b25aa-152">Se o computador local for um nó em um cluster, esse valor será o nome DNS totalmente qualificado do servidor virtual de cluster.</span><span class="sxs-lookup"><span data-stu-id="b25aa-152">If the local computer is a node in a cluster, this value is the fully qualified DNS name of the cluster virtual server.</span></span> <span data-ttu-id="b25aa-153">Esse valor corresponde ao nome retornado pela função [**GetComputerNameEx devia**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) quando o parâmetro *nametype* é "ComputerNameDnsFullyQualified".</span><span class="sxs-lookup"><span data-stu-id="b25aa-153">This value matches the name returned by the [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) function when the *NameType* parameter is "ComputerNameDnsFullyQualified".</span></span><br/> |
| <dl> <span data-ttu-id="b25aa-154"><dt>"IntegrationServicesVersion"</dt></span><span class="sxs-lookup"><span data-stu-id="b25aa-154"><dt>"IntegrationServicesVersion"</dt></span></span> </dl> | <span data-ttu-id="b25aa-155">Uma cadeia de caracteres que representa a versão do Integration Services instalado atualmente na máquina virtual convidada (por exemplo, "6.1.7000.0").</span><span class="sxs-lookup"><span data-stu-id="b25aa-155">A string representing the version of the Integration Services currently installed in the guest virtual machine (for example, "6.1.7000.0").</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="b25aa-156"><dt>"NetworkAddressIPv4"</dt></span><span class="sxs-lookup"><span data-stu-id="b25aa-156"><dt>"NetworkAddressIPv4"</dt></span></span> </dl>         | <span data-ttu-id="b25aa-157">Uma cadeia de caracteres que contém uma lista delimitada por ponto-e-vírgula dos endereços IPv4 atribuídos no momento à máquina virtual convidada.</span><span class="sxs-lookup"><span data-stu-id="b25aa-157">A string that contains a semicolon-delimited list of the IPv4 addresses currently assigned to the guest virtual machine.</span></span> <span data-ttu-id="b25aa-158">A lista é atualizada automaticamente sempre que uma alteração de configuração de TCP/IP ocorre na máquina virtual convidada.</span><span class="sxs-lookup"><span data-stu-id="b25aa-158">The list is automatically updated whenever a TCP/IP configuration change occurs on the guest virtual machine.</span></span> <span data-ttu-id="b25aa-159">Cada endereço é representado na notação de ponto decimal.</span><span class="sxs-lookup"><span data-stu-id="b25aa-159">Each address is represented in dot-decimal notation.</span></span> <br/>                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="b25aa-160"><dt>"NetworkAddressIPv6"</dt></span><span class="sxs-lookup"><span data-stu-id="b25aa-160"><dt>"NetworkAddressIPv6"</dt></span></span> </dl>         | <span data-ttu-id="b25aa-161">Uma cadeia de caracteres que contém uma lista delimitada por ponto-e-vírgula dos endereços IPv6 atribuídos no momento à máquina virtual convidada.</span><span class="sxs-lookup"><span data-stu-id="b25aa-161">A string that contains a semicolon-delimited list of the IPv6 addresses currently assigned to the guest virtual machine.</span></span> <span data-ttu-id="b25aa-162">A lista é atualizada automaticamente sempre que uma alteração de configuração de TCP/IP ocorre na máquina virtual convidada.</span><span class="sxs-lookup"><span data-stu-id="b25aa-162">The list is automatically updated whenever a TCP/IP configuration change occurs on the guest virtual machine.</span></span> <span data-ttu-id="b25aa-163">Cada endereço é representado em notação hexadecimal de dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="b25aa-163">Each address is represented in colon-hexadecimal notation.</span></span> <span data-ttu-id="b25aa-164">As listas IPv4 e IPv6 não têm garantia de serem sincronizadas em todos os momentos.</span><span class="sxs-lookup"><span data-stu-id="b25aa-164">The IPv4 and IPv6 lists are not guaranteed to be in sync at all times.</span></span><br/>                                                                                                                                             |
| <dl> <span data-ttu-id="b25aa-165"><dt>"OSBuildNumber"</dt></span><span class="sxs-lookup"><span data-stu-id="b25aa-165"><dt>"OSBuildNumber"</dt></span></span> </dl>              | <span data-ttu-id="b25aa-166">Uma cadeia de caracteres que representa o número de Build do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b25aa-166">A string that represents the build number of the operating system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="b25aa-167"><dt>"OSEditionId"</dt></span><span class="sxs-lookup"><span data-stu-id="b25aa-167"><dt>"OSEditionId"</dt></span></span> </dl>                | <span data-ttu-id="b25aa-168">Uma cadeia de caracteres que representa a edição (SKU) do sistema operacional da máquina virtual convidada.</span><span class="sxs-lookup"><span data-stu-id="b25aa-168">A string representing the edition (SKU) of the guest virtual machine operating system.</span></span> <span data-ttu-id="b25aa-169">Para obter uma lista de valores possíveis, consulte a função [**GetProductInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getproductinfo) .</span><span class="sxs-lookup"><span data-stu-id="b25aa-169">For a list of possible values, see the [**GetProductInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getproductinfo) function.</span></span><br/>                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="b25aa-170"><dt>OSName</dt></span><span class="sxs-lookup"><span data-stu-id="b25aa-170"><dt>"OSName"</dt></span></span> </dl>                     | <span data-ttu-id="b25aa-171">Uma cadeia de caracteres que representa o nome do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b25aa-171">A string that represents the name of the operating system.</span></span> <span data-ttu-id="b25aa-172">Esse valor vem da seguinte entrada do registro: **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ProductName**</span><span class="sxs-lookup"><span data-stu-id="b25aa-172">This value comes from the following registry entry: **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**ProductName**</span></span><br/> <br/>                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="b25aa-173"><dt>OSMajorVersion</dt></span><span class="sxs-lookup"><span data-stu-id="b25aa-173"><dt>"OSMajorVersion"</dt></span></span> </dl>             | <span data-ttu-id="b25aa-174">Uma cadeia de caracteres que representa o número de versão principal do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b25aa-174">A string that represents the major version number of the operating system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="b25aa-175"><dt>OSMinorVersion</dt></span><span class="sxs-lookup"><span data-stu-id="b25aa-175"><dt>"OSMinorVersion"</dt></span></span> </dl>             | <span data-ttu-id="b25aa-176">Uma cadeia de caracteres que representa o número de versão secundária do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b25aa-176">A string that represents the minor version number of the operating system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="b25aa-177"><dt>"OSPlatformId"</dt></span><span class="sxs-lookup"><span data-stu-id="b25aa-177"><dt>"OSPlatformId"</dt></span></span> </dl>               | <span data-ttu-id="b25aa-178">Uma cadeia de caracteres que representa a plataforma do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b25aa-178">A string that represents the operating system platform.</span></span> <span data-ttu-id="b25aa-179">Os valores possíveis da propriedade **Data** são "1" para indicar um sistema Windows sem suporte e "2" para indicar um sistema Windows com suporte.</span><span class="sxs-lookup"><span data-stu-id="b25aa-179">The possible values of the **Data** property are "1" to indicate an unsupported Windows system and "2" to indicate a supported Windows system.</span></span><br/>                                                                                                                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="b25aa-180"><dt>OSVersion</dt></span><span class="sxs-lookup"><span data-stu-id="b25aa-180"><dt>"OSVersion"</dt></span></span> </dl>                  | <span data-ttu-id="b25aa-181">Uma cadeia de caracteres que representa a versão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b25aa-181">A string that represents the operating system version.</span></span> <span data-ttu-id="b25aa-182">O formato dessa cadeia de caracteres é *MajorVersion*. *MinorVersion*. *BuildNumber*.</span><span class="sxs-lookup"><span data-stu-id="b25aa-182">The format of this string is *MajorVersion*.*MinorVersion*.*BuildNumber*.</span></span> <span data-ttu-id="b25aa-183">Por exemplo, "5.2.3790" para o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b25aa-183">For example, "5.2.3790" for Windows Server 2003.</span></span><br/>                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="b25aa-184"><dt>ProcessorArchitecture</dt></span><span class="sxs-lookup"><span data-stu-id="b25aa-184"><dt>"ProcessorArchitecture"</dt></span></span> </dl>      | <span data-ttu-id="b25aa-185">Uma cadeia de caracteres que representa a arquitetura do processador do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b25aa-185">A string that represents the processor architecture of the operating system.</span></span> <span data-ttu-id="b25aa-186">Para obter uma lista de valores, consulte o membro **wProcessorArchitecture** da estrutura de [**\_ informações do sistema**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) .</span><span class="sxs-lookup"><span data-stu-id="b25aa-186">For a list of values, see the **wProcessorArchitecture** member of the [**SYSTEM\_INFO**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span><br/>                                                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="b25aa-187"><dt>ProductType</dt></span><span class="sxs-lookup"><span data-stu-id="b25aa-187"><dt>"ProductType"</dt></span></span> </dl>                | <span data-ttu-id="b25aa-188">Uma cadeia de caracteres que representa o tipo de produto.</span><span class="sxs-lookup"><span data-stu-id="b25aa-188">A string that represents the product type.</span></span> <span data-ttu-id="b25aa-189">Para obter uma lista de valores, consulte o membro **wProductType** da estrutura [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="b25aa-189">For a list of values, see the **wProductType** member of the [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="b25aa-190"><dt>"RDPAddressIPv4"</dt></span><span class="sxs-lookup"><span data-stu-id="b25aa-190"><dt>"RDPAddressIPv4"</dt></span></span> </dl>             | <span data-ttu-id="b25aa-191">Uma cadeia de caracteres que contém uma lista delimitada por ponto-e-vírgula dos endereços IPv4 que a pilha RDP da máquina virtual convidada está escutando no momento.</span><span class="sxs-lookup"><span data-stu-id="b25aa-191">A string that contains a semicolon-delimited list of the IPv4 addresses that the guest virtual machine RDP stack is currently listening on.</span></span> <span data-ttu-id="b25aa-192">Se a pilha RDP não estiver em execução no momento, a cadeia de caracteres estará vazia.</span><span class="sxs-lookup"><span data-stu-id="b25aa-192">If the RDP stack is not currently running, the string will be empty.</span></span> <span data-ttu-id="b25aa-193">A lista é atualizada automaticamente sempre que uma alteração de configuração de TCP/IP afeta a pilha RDP na máquina virtual convidada.</span><span class="sxs-lookup"><span data-stu-id="b25aa-193">The list is automatically updated whenever a TCP/IP configuration change affects the RDP stack on the guest virtual machine.</span></span> <span data-ttu-id="b25aa-194">Cada endereço é representado na notação de ponto decimal.</span><span class="sxs-lookup"><span data-stu-id="b25aa-194">Each address is represented in dot-decimal notation.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="b25aa-195"><dt>"RDPAddressIPv6"</dt></span><span class="sxs-lookup"><span data-stu-id="b25aa-195"><dt>"RDPAddressIPv6"</dt></span></span> </dl>             | <span data-ttu-id="b25aa-196">Uma cadeia de caracteres que contém uma lista delimitada por ponto-e-vírgula dos endereços IPv6 que a pilha RDP da máquina virtual convidada está escutando no momento.</span><span class="sxs-lookup"><span data-stu-id="b25aa-196">A string that contains a semicolon-delimited list of the IPv6 addresses that the guest virtual machine RDP stack is currently listening on.</span></span> <span data-ttu-id="b25aa-197">Se a pilha RDP não estiver em execução no momento, a cadeia de caracteres estará vazia.</span><span class="sxs-lookup"><span data-stu-id="b25aa-197">If the RDP stack is not currently running, the string will be empty.</span></span> <span data-ttu-id="b25aa-198">A lista é atualizada automaticamente sempre que uma alteração de configuração de TCP/IP afeta a pilha RDP na máquina virtual convidada.</span><span class="sxs-lookup"><span data-stu-id="b25aa-198">The list is automatically updated whenever a TCP/IP configuration change affects the RDP stack on the guest virtual machine.</span></span> <span data-ttu-id="b25aa-199">Cada endereço é representado em notação hexadecimal de dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="b25aa-199">Each address is represented in colon-hexadecimal notation.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="b25aa-200"><dt>"ServicePackMajor"</dt></span><span class="sxs-lookup"><span data-stu-id="b25aa-200"><dt>"ServicePackMajor"</dt></span></span> </dl>           | <span data-ttu-id="b25aa-201">Uma cadeia de caracteres que representa o número de versão principal do service pack mais recente instalado no sistema.</span><span class="sxs-lookup"><span data-stu-id="b25aa-201">A string that represents the major version number of the latest service pack installed on the system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="b25aa-202"><dt>"ServicePackMinor"</dt></span><span class="sxs-lookup"><span data-stu-id="b25aa-202"><dt>"ServicePackMinor"</dt></span></span> </dl>           | <span data-ttu-id="b25aa-203">Uma cadeia de caracteres que representa o número de versão secundária do service pack mais recente instalado no sistema.</span><span class="sxs-lookup"><span data-stu-id="b25aa-203">A string that represents the minor version number of the latest service pack installed on the system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="b25aa-204"><dt>"SuiteMask"</dt></span><span class="sxs-lookup"><span data-stu-id="b25aa-204"><dt>"SuiteMask"</dt></span></span> </dl>                  | <span data-ttu-id="b25aa-205">Uma cadeia de caracteres que representa os pacotes de produto disponíveis no sistema.</span><span class="sxs-lookup"><span data-stu-id="b25aa-205">A string that represents the product suites available on the system.</span></span> <span data-ttu-id="b25aa-206">Essa cadeia de caracteres é uma combinação de qualquer um dos valores do membro **wSuiteMask** da estrutura [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="b25aa-206">This string is a combination of any of the values of the **wSuiteMask** member of the [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span><br/>                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="b25aa-207">**Origem**</span><span class="sxs-lookup"><span data-stu-id="b25aa-207">**Source**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b25aa-208">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b25aa-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b25aa-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b25aa-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b25aa-210">A origem dos dados.</span><span class="sxs-lookup"><span data-stu-id="b25aa-210">The source of the data.</span></span>



| <span data-ttu-id="b25aa-211">Valor</span><span class="sxs-lookup"><span data-stu-id="b25aa-211">Value</span></span>                                                                        | <span data-ttu-id="b25aa-212">Significado</span><span class="sxs-lookup"><span data-stu-id="b25aa-212">Meaning</span></span>                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b25aa-213"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b25aa-213"><dt>0</dt></span></span> </dl> | <span data-ttu-id="b25aa-214">"HostExchangeItems" quando enviado por push pelo host.</span><span class="sxs-lookup"><span data-stu-id="b25aa-214">"HostExchangeItems" when pushed by the host.</span></span><br/>                                                                                                                                                                                      |
| <dl> <span data-ttu-id="b25aa-215"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b25aa-215"><dt>1</dt></span></span> </dl> | <span data-ttu-id="b25aa-216">"GuestExchangeItems" quando enviado por push pela máquina virtual convidada.</span><span class="sxs-lookup"><span data-stu-id="b25aa-216">"GuestExchangeItems" when pushed by the guest virtual machine.</span></span><br/>                                                                                                                                                                    |
| <dl> <span data-ttu-id="b25aa-217"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b25aa-217"><dt>2</dt></span></span> </dl> | <span data-ttu-id="b25aa-218">"GuestIntrinsicExchangeItems" quando preenchido automaticamente pela máquina virtual convidada.</span><span class="sxs-lookup"><span data-stu-id="b25aa-218">"GuestIntrinsicExchangeItems" when automatically populated by the guest virtual machine.</span></span><br/>                                                                                                                                          |
| <dl> <span data-ttu-id="b25aa-219"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b25aa-219"><dt>4</dt></span></span> </dl> | <span data-ttu-id="b25aa-220">Indica que o item é somente host e não compartilhado com a máquina virtual convidada.</span><span class="sxs-lookup"><span data-stu-id="b25aa-220">Indicates that the item is host-only and not shared with the guest virtual machine.</span></span> <span data-ttu-id="b25aa-221">Usado com a propriedade **HostOnlyItems** da classe [**Msvm \_ KvpExchangeComponentSettingData**](msvm-kvpexchangecomponentsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="b25aa-221">Used with the **HostOnlyItems** property of the [**Msvm\_KvpExchangeComponentSettingData**](msvm-kvpexchangecomponentsettingdata.md) class.</span></span> <br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b25aa-222">Comentários</span><span class="sxs-lookup"><span data-stu-id="b25aa-222">Remarks</span></span>

<span data-ttu-id="b25aa-223">O acesso à classe **Msvm \_ KvpExchangeDataItem** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="b25aa-223">Access to the **Msvm\_KvpExchangeDataItem** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b25aa-224">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b25aa-224">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b25aa-225">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b25aa-225">Requirements</span></span>



| <span data-ttu-id="b25aa-226">Requisito</span><span class="sxs-lookup"><span data-stu-id="b25aa-226">Requirement</span></span> | <span data-ttu-id="b25aa-227">Valor</span><span class="sxs-lookup"><span data-stu-id="b25aa-227">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b25aa-228">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b25aa-228">Minimum supported client</span></span><br/> | <span data-ttu-id="b25aa-229">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b25aa-229">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b25aa-230">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b25aa-230">Minimum supported server</span></span><br/> | <span data-ttu-id="b25aa-231">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="b25aa-231">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b25aa-232">Namespace</span><span class="sxs-lookup"><span data-stu-id="b25aa-232">Namespace</span></span><br/>                | <span data-ttu-id="b25aa-233">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="b25aa-233">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b25aa-234">MOF</span><span class="sxs-lookup"><span data-stu-id="b25aa-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b25aa-235"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b25aa-235"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b25aa-236">DLL</span><span class="sxs-lookup"><span data-stu-id="b25aa-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b25aa-237"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b25aa-237"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b25aa-238">Confira também</span><span class="sxs-lookup"><span data-stu-id="b25aa-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b25aa-239">**\_Managedelement do CIM**</span><span class="sxs-lookup"><span data-stu-id="b25aa-239">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> <dt>

[<span data-ttu-id="b25aa-240">**\_Managedelement do CIM**</span><span class="sxs-lookup"><span data-stu-id="b25aa-240">**CIM\_ManagedElement**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)
</dt> </dl>

 

