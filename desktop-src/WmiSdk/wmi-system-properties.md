---
description: Instrumentação de Gerenciamento do Windows (WMI) define um conjunto de propriedades do sistema que estão associadas a todas as classes e instâncias de classes.
ms.assetid: e812c0cb-3e08-4cac-8d05-2cd7abc922d1
ms.tgt_platform: multiple
title: Propriedades do sistema WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ee541d9de0d37c9aa1eae4ded07d3cb70ff1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165318"
---
# <a name="wmi-system-properties"></a><span data-ttu-id="e09a7-103">Propriedades do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="e09a7-103">WMI System Properties</span></span>

<span data-ttu-id="e09a7-104">Instrumentação de Gerenciamento do Windows (WMI) define um conjunto de propriedades do sistema que estão associadas a todas as classes e instâncias de classes.</span><span class="sxs-lookup"><span data-stu-id="e09a7-104">Windows Management Instrumentation (WMI) defines a set of system properties that are associated with all classes and instances of classes.</span></span> <span data-ttu-id="e09a7-105">Assim como acontece com as classes do sistema, os nomes das propriedades do sistema começam com um sublinhado duplo, distinguindo-os das propriedades criadas por aplicativos ou provedores que não devem começar com um sublinhado simples ou duplo.</span><span class="sxs-lookup"><span data-stu-id="e09a7-105">As with system classes, system property names begin with a double underscore, distinguishing them from properties created by applications or providers that must not start with a single or double underscore.</span></span> <span data-ttu-id="e09a7-106">Outra maneira de identificar uma propriedade do sistema é usar o método [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) .</span><span class="sxs-lookup"><span data-stu-id="e09a7-106">Another way to identify a system property is to use the [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) method.</span></span>

<span data-ttu-id="e09a7-107">As propriedades do sistema estão disponíveis a qualquer momento, mas os valores podem ser **nulos**.</span><span class="sxs-lookup"><span data-stu-id="e09a7-107">System properties are available at any time, but values might be **NULL**.</span></span> <span data-ttu-id="e09a7-108">**NULL** indica que uma propriedade não se aplica a um objeto específico.</span><span class="sxs-lookup"><span data-stu-id="e09a7-108">**NULL** indicates a property does not apply to a specific object.</span></span> <span data-ttu-id="e09a7-109">No entanto, as propriedades do sistema podem não estar disponíveis o tempo todo para todas as classes ou instâncias.</span><span class="sxs-lookup"><span data-stu-id="e09a7-109">However, system properties might not be available all the time for all classes or instances.</span></span>

## <a name="system-properties"></a><span data-ttu-id="e09a7-110">Propriedades do Sistema</span><span class="sxs-lookup"><span data-stu-id="e09a7-110">System Properties</span></span>

<span data-ttu-id="e09a7-111">A lista a seguir descreve as propriedades do sistema WMI.</span><span class="sxs-lookup"><span data-stu-id="e09a7-111">The following list describes the WMI system properties.</span></span> <span data-ttu-id="e09a7-112">Os exemplos fornecidos são obtidos das propriedades do sistema da classe [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) , que é descrita na parte inferior deste tópico.</span><span class="sxs-lookup"><span data-stu-id="e09a7-112">The examples given are taken from the system properties of the [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) class, which is described at the bottom of this topic.</span></span>

<dl> <dt>

<span data-ttu-id="e09a7-113"><span id="__Class"></span><span id="__class"></span><span id="__CLASS"></span>**\_\_Classes**</span><span class="sxs-lookup"><span data-stu-id="e09a7-113"><span id="__Class"></span><span id="__class"></span><span id="__CLASS"></span>**\_\_Class**</span></span>
</dt> <dd>

<span data-ttu-id="e09a7-114">Tipo de dados **: \_ cadeia de caracteres CIM**</span><span class="sxs-lookup"><span data-stu-id="e09a7-114">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="e09a7-115">Tipo de acesso: somente leitura para instâncias; leitura/gravação para classes</span><span class="sxs-lookup"><span data-stu-id="e09a7-115">Access type: Read-only for instances; read/write for classes</span></span>

<span data-ttu-id="e09a7-116">O nome da classe.</span><span class="sxs-lookup"><span data-stu-id="e09a7-116">The name of the class.</span></span>

<span data-ttu-id="e09a7-117">Exemplo: Win32 \_ OptionalFeature</span><span class="sxs-lookup"><span data-stu-id="e09a7-117">Example: Win32\_OptionalFeature</span></span>

</dd> <dt>

<span data-ttu-id="e09a7-118"><span id="__Derivation"></span><span id="__derivation"></span><span id="__DERIVATION"></span>**\_\_Derivação**</span><span class="sxs-lookup"><span data-stu-id="e09a7-118"><span id="__Derivation"></span><span id="__derivation"></span><span id="__DERIVATION"></span>**\_\_Derivation**</span></span>
</dt> <dd>

<span data-ttu-id="e09a7-119">Tipo de dados: matriz de **\_ cadeia de caracteres CIM**</span><span class="sxs-lookup"><span data-stu-id="e09a7-119">Data type: **CIM\_STRING** array</span></span>

<span data-ttu-id="e09a7-120">Tipo de acesso: somente leitura para instâncias e classes</span><span class="sxs-lookup"><span data-stu-id="e09a7-120">Access type: Read-only for both instances and classes</span></span>

<span data-ttu-id="e09a7-121">Hierarquia de classes da classe ou instância atual.</span><span class="sxs-lookup"><span data-stu-id="e09a7-121">Class hierarchy of the current class or instance.</span></span> <span data-ttu-id="e09a7-122">O primeiro elemento é a classe pai imediata, o próximo é seu pai e assim por diante; o último elemento é a classe base.</span><span class="sxs-lookup"><span data-stu-id="e09a7-122">The first element is the immediate parent class, the next is its parent, and so on; the last element is the base class.</span></span>

<span data-ttu-id="e09a7-123">Exemplo: {CIM \_ LogicalElement, CIM \_ ManagedSystemElement}</span><span class="sxs-lookup"><span data-stu-id="e09a7-123">Example: {CIM\_LogicalElement, CIM\_ManagedSystemElement}</span></span>

</dd> <dt>

<span data-ttu-id="e09a7-124"><span id="__Dynasty"></span><span id="__dynasty"></span><span id="__DYNASTY"></span>**\_\_Dinastia**</span><span class="sxs-lookup"><span data-stu-id="e09a7-124"><span id="__Dynasty"></span><span id="__dynasty"></span><span id="__DYNASTY"></span>**\_\_Dynasty**</span></span>
</dt> <dd>

<span data-ttu-id="e09a7-125">Tipo de dados **: \_ cadeia de caracteres CIM**</span><span class="sxs-lookup"><span data-stu-id="e09a7-125">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="e09a7-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e09a7-126">Access type: Read-only</span></span>

<span data-ttu-id="e09a7-127">Nome da classe de nível superior da qual a classe ou instância é derivada.</span><span class="sxs-lookup"><span data-stu-id="e09a7-127">Name of the top-level class from which the class or instance is derived.</span></span> <span data-ttu-id="e09a7-128">Quando essa classe ou instância é a classe de nível superior, os valores de **\_ \_ dinastia** e **\_ \_ classe** são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="e09a7-128">When this class or instance is the top-level class, the values of **\_\_Dynasty** and **\_\_Class** are the same.</span></span>

<span data-ttu-id="e09a7-129">Exemplo: CIM \_ ManagedSystemElement</span><span class="sxs-lookup"><span data-stu-id="e09a7-129">Example: CIM\_ManagedSystemElement</span></span>

</dd> <dt>

<span data-ttu-id="e09a7-130"><span id="__Genus"></span><span id="__genus"></span><span id="__GENUS"></span>**\_\_Genus**</span><span class="sxs-lookup"><span data-stu-id="e09a7-130"><span id="__Genus"></span><span id="__genus"></span><span id="__GENUS"></span>**\_\_Genus**</span></span>
</dt> <dd>

<span data-ttu-id="e09a7-131">Tipo de dados: **CIM \_ sint32**</span><span class="sxs-lookup"><span data-stu-id="e09a7-131">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="e09a7-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e09a7-132">Access type: Read-only</span></span>

<span data-ttu-id="e09a7-133">Valor que é usado para distinguir entre classes e instâncias.</span><span class="sxs-lookup"><span data-stu-id="e09a7-133">Value that is used to distinguish between classes and instances.</span></span> <span data-ttu-id="e09a7-134">Esse valor é **a \_ \_ classe WBEM genus** (1) para classes e **a \_ \_ instância do WBEM genus** (2) para instâncias e eventos.</span><span class="sxs-lookup"><span data-stu-id="e09a7-134">This value is **WBEM\_GENUS\_CLASS** (1) for classes, and **WBEM\_GENUS\_INSTANCE** (2) for instances and events.</span></span>

<span data-ttu-id="e09a7-135">Exemplo: 2</span><span class="sxs-lookup"><span data-stu-id="e09a7-135">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="e09a7-136"><span id="__Namespace"></span><span id="__namespace"></span><span id="__NAMESPACE"></span>[**\_\_Namespace**](--namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e09a7-136"><span id="__Namespace"></span><span id="__namespace"></span><span id="__NAMESPACE"></span>[**\_\_Namespace**](--namespace.md)</span></span>
</dt> <dd>

<span data-ttu-id="e09a7-137">Tipo de dados **: \_ cadeia de caracteres CIM**</span><span class="sxs-lookup"><span data-stu-id="e09a7-137">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="e09a7-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e09a7-138">Access type: Read-only</span></span>

<span data-ttu-id="e09a7-139">Nome do [*namespace*](gloss-n.md) da classe ou instância.</span><span class="sxs-lookup"><span data-stu-id="e09a7-139">Name of the [*namespace*](gloss-n.md) of the class or instance.</span></span>

<span data-ttu-id="e09a7-140">Exemplo: raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e09a7-140">Example: root\\cimv2</span></span>

</dd> <dt>

<span data-ttu-id="e09a7-141"><span id="__Path"></span><span id="__path"></span><span id="__PATH"></span>**\_\_Multi-Path**</span><span class="sxs-lookup"><span data-stu-id="e09a7-141"><span id="__Path"></span><span id="__path"></span><span id="__PATH"></span>**\_\_Path**</span></span>
</dt> <dd>

<span data-ttu-id="e09a7-142">Tipo de dados **: \_ cadeia de caracteres CIM**</span><span class="sxs-lookup"><span data-stu-id="e09a7-142">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="e09a7-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e09a7-143">Access type: Read-only</span></span>

<span data-ttu-id="e09a7-144">Caminho completo para a classe ou instância — incluindo servidor e namespace.</span><span class="sxs-lookup"><span data-stu-id="e09a7-144">Full path to the class or instance—including server and namespace.</span></span>

<span data-ttu-id="e09a7-145">Exemplo: \\ \\ meuservidor \\ raiz \\ cimv2: Win32 \_ OptionalFeature. Name = "TelnetClient"</span><span class="sxs-lookup"><span data-stu-id="e09a7-145">Example: \\\\MyServer\\root\\cimv2:Win32\_OptionalFeature.Name="TelnetClient"</span></span>

</dd> <dt>

<span data-ttu-id="e09a7-146"><span id="__Property_Count"></span><span id="__property_count"></span><span id="__PROPERTY_COUNT"></span>**\_\_Contagem de propriedades \_**</span><span class="sxs-lookup"><span data-stu-id="e09a7-146"><span id="__Property_Count"></span><span id="__property_count"></span><span id="__PROPERTY_COUNT"></span>**\_\_Property\_Count**</span></span>
</dt> <dd>

<span data-ttu-id="e09a7-147">Tipo de dados: **CIM \_ sint32**</span><span class="sxs-lookup"><span data-stu-id="e09a7-147">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="e09a7-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e09a7-148">Access type: Read-only</span></span>

<span data-ttu-id="e09a7-149">Número de propriedades não do sistema definidas para a classe ou instância.</span><span class="sxs-lookup"><span data-stu-id="e09a7-149">Number of nonsystem properties defined for the class or instance.</span></span>

<span data-ttu-id="e09a7-150">Exemplo: 6</span><span class="sxs-lookup"><span data-stu-id="e09a7-150">Example: 6</span></span>

</dd> <dt>

<span data-ttu-id="e09a7-151"><span id="__Relpath"></span><span id="__relpath"></span><span id="__RELPATH"></span>**\_\_Relpath**</span><span class="sxs-lookup"><span data-stu-id="e09a7-151"><span id="__Relpath"></span><span id="__relpath"></span><span id="__RELPATH"></span>**\_\_Relpath**</span></span>
</dt> <dd>

<span data-ttu-id="e09a7-152">Tipo de dados **: \_ cadeia de caracteres CIM**</span><span class="sxs-lookup"><span data-stu-id="e09a7-152">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="e09a7-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e09a7-153">Access type: Read-only</span></span>

<span data-ttu-id="e09a7-154">Caminho relativo para a classe ou instância.</span><span class="sxs-lookup"><span data-stu-id="e09a7-154">Relative path to the class or instance.</span></span>

<span data-ttu-id="e09a7-155">Exemplo: Win32 \_ OptionalFeature. Name = "TelnetClient"</span><span class="sxs-lookup"><span data-stu-id="e09a7-155">Example: Win32\_OptionalFeature.Name="TelnetClient"</span></span>

</dd> <dt>

<span data-ttu-id="e09a7-156"><span id="__Server"></span><span id="__server"></span><span id="__SERVER"></span>**\_\_Servidor**</span><span class="sxs-lookup"><span data-stu-id="e09a7-156"><span id="__Server"></span><span id="__server"></span><span id="__SERVER"></span>**\_\_Server**</span></span>
</dt> <dd>

<span data-ttu-id="e09a7-157">Tipo de dados **: \_ cadeia de caracteres CIM**</span><span class="sxs-lookup"><span data-stu-id="e09a7-157">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="e09a7-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e09a7-158">Access type: Read-only</span></span>

<span data-ttu-id="e09a7-159">Nome do servidor que fornece a classe ou instância.</span><span class="sxs-lookup"><span data-stu-id="e09a7-159">Name of the server supplying the class or instance.</span></span>

<span data-ttu-id="e09a7-160">Exemplo: meuservidor</span><span class="sxs-lookup"><span data-stu-id="e09a7-160">Example: MyServer</span></span>

</dd> <dt>

<span data-ttu-id="e09a7-161"><span id="__Superclass"></span><span id="__superclass"></span><span id="__SUPERCLASS"></span>**\_\_Super**</span><span class="sxs-lookup"><span data-stu-id="e09a7-161"><span id="__Superclass"></span><span id="__superclass"></span><span id="__SUPERCLASS"></span>**\_\_Superclass**</span></span>
</dt> <dd>

<span data-ttu-id="e09a7-162">Tipo de dados **: \_ cadeia de caracteres CIM**</span><span class="sxs-lookup"><span data-stu-id="e09a7-162">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="e09a7-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e09a7-163">Access type: Read-only</span></span>

<span data-ttu-id="e09a7-164">Nome da classe pai imediata da classe ou instância.</span><span class="sxs-lookup"><span data-stu-id="e09a7-164">Name of the immediate parent class of the class or instance.</span></span>

<span data-ttu-id="e09a7-165">Exemplo: CIM \_ LogicalElement</span><span class="sxs-lookup"><span data-stu-id="e09a7-165">Example: CIM\_LogicalElement</span></span>

</dd> </dl>

<span data-ttu-id="e09a7-166">O código do PowerShell a seguir recupera as propriedades da classe [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) , que inclui as propriedades do sistema.</span><span class="sxs-lookup"><span data-stu-id="e09a7-166">The following PowerShell code retrieves the properties of the [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) class, which includes the system properties.</span></span>


```PowerShell
Get-WmiObject win32_OptionalFeature | Where-Object {$_.name -eq "TelnetClient"}
```



<span data-ttu-id="e09a7-167">O exemplo de código anterior retorna o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e09a7-167">The previous code sample returns the following:</span></span>


```PowerShell
__GENUS          : 2
__CLASS          : Win32_OptionalFeature
__SUPERCLASS     : CIM_LogicalElement
__DYNASTY        : CIM_ManagedSystemElement
__RELPATH        : Win32_OptionalFeature.Name="TelnetClient"
__PROPERTY_COUNT : 6
__DERIVATION     : {CIM_LogicalElement, CIM_ManagedSystemElement}
__SERVER         : myServer
__NAMESPACE      : root\cimv2
__PATH           : \\myServer\root\cimv2:Win32_OptionalFeature.Name="TelnetClient"
Caption          : Telnet Client
Description      : 
InstallDate      : 
InstallState     : 2
Name             : TelnetClient
Status           : 
PSComputerName   : myServer
```



 

 
