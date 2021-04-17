---
description: Antes de implementar seu provedor, primeiro você deve registrar seu provedor com o WMI. O registro do provedor define o tipo do provedor e as classes que o provedor suporta. O WMI só pode acessar provedores registrados.
ms.assetid: b0a1a11c-a8e8-4bc1-b286-fb9243667976
ms.tgt_platform: multiple
title: Registrando um provedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53592ecb452de1b6071cbb8f59cfaaef42b57f1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763934"
---
# <a name="registering-a-provider"></a><span data-ttu-id="df894-105">Registrando um provedor</span><span class="sxs-lookup"><span data-stu-id="df894-105">Registering a Provider</span></span>

<span data-ttu-id="df894-106">Antes de implementar seu provedor, primeiro você deve registrar seu provedor com o WMI.</span><span class="sxs-lookup"><span data-stu-id="df894-106">Before implementing your provider, you should first register your provider with WMI.</span></span> <span data-ttu-id="df894-107">O registro do provedor define o tipo do provedor e as classes que o provedor suporta.</span><span class="sxs-lookup"><span data-stu-id="df894-107">Registering the provider defines the type of the provider and the classes that the provider supports.</span></span> <span data-ttu-id="df894-108">O WMI só pode acessar provedores registrados.</span><span class="sxs-lookup"><span data-stu-id="df894-108">WMI can only access registered providers.</span></span>

> [!Note]  
> <span data-ttu-id="df894-109">Para obter mais informações sobre como registrar um provedor de MI, consulte [como registrar um provedor de mi](/previous-versions/windows/desktop/wmi_v2/how-to-register-an-mi-provider).</span><span class="sxs-lookup"><span data-stu-id="df894-109">For more information on registering an MI provider, see [How to: Register an MI Provider](/previous-versions/windows/desktop/wmi_v2/how-to-register-an-mi-provider).</span></span>

 

<span data-ttu-id="df894-110">Você pode escrever o código do provedor antes de registrar o provedor.</span><span class="sxs-lookup"><span data-stu-id="df894-110">You can write your provider code before you register the provider.</span></span> <span data-ttu-id="df894-111">No entanto, é muito difícil depurar um provedor que não esteja registrado com o WMI.</span><span class="sxs-lookup"><span data-stu-id="df894-111">However, it is very difficult to debug a provider that is not registered with WMI.</span></span> <span data-ttu-id="df894-112">Determinar as interfaces do seu provedor também ajuda a descrever a finalidade e a estrutura de um provedor.</span><span class="sxs-lookup"><span data-stu-id="df894-112">Determining the interfaces for your provider also helps to outline the purpose and structure of a provider.</span></span> <span data-ttu-id="df894-113">Portanto, registrar seu provedor ajuda você a projetar seu provedor.</span><span class="sxs-lookup"><span data-stu-id="df894-113">Therefore, registering your provider helps you design your provider.</span></span>

<span data-ttu-id="df894-114">Somente os administradores podem registrar ou excluir um provedor.</span><span class="sxs-lookup"><span data-stu-id="df894-114">Only administrators can register or delete a provider.</span></span>

<span data-ttu-id="df894-115">Um provedor deve ser registrado para todos os diferentes tipos de funções de provedor que ele executa.</span><span class="sxs-lookup"><span data-stu-id="df894-115">A provider must be registered for all the different types of provider functions that it performs.</span></span> <span data-ttu-id="df894-116">Quase todos os provedores fornecem instâncias de classes que eles definem, mas também podem fornecer dados de propriedade, métodos, eventos ou classes.</span><span class="sxs-lookup"><span data-stu-id="df894-116">Nearly all providers supply instances of classes they define, but they may also provide property data, methods, events, or classes.</span></span> <span data-ttu-id="df894-117">O provedor também pode ser registrado como um provedor de consumidor de eventos ou um provedor de contador de desempenho.</span><span class="sxs-lookup"><span data-stu-id="df894-117">The provider may also be registered as an event consumer provider or a performance counter provider.</span></span> <span data-ttu-id="df894-118">É recomendável que você combine toda a funcionalidade do provedor em um provedor em vez de ter muitos provedores separados para cada tipo.</span><span class="sxs-lookup"><span data-stu-id="df894-118">It is recommended that you combine all provider functionality in one provider rather than having many separate providers for each type.</span></span> <span data-ttu-id="df894-119">Um exemplo é o [provedor de registro do sistema](/previous-versions/windows/desktop/regprov/system-registry-provider), que fornece métodos e instâncias, e o [provedor de cota de disco](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider), que fornece instâncias, métodos e eventos.</span><span class="sxs-lookup"><span data-stu-id="df894-119">An example is the [System Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider), which provides methods and instances, and the [Disk Quota provider](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider), which supplies instances, methods, and events.</span></span>

<span data-ttu-id="df894-120">Um provedor deve ser registrado para todos os diferentes tipos de funções de provedor que ele executa.</span><span class="sxs-lookup"><span data-stu-id="df894-120">A provider must be registered for all the different types of provider functions that it performs.</span></span> <span data-ttu-id="df894-121">Quase todos os provedores fornecem instâncias de classes que eles definem, mas também podem fornecer dados de propriedade, métodos, eventos ou classes.</span><span class="sxs-lookup"><span data-stu-id="df894-121">Nearly all providers supply instances of classes they define, but they may also provide property data, methods, events, or classes.</span></span> <span data-ttu-id="df894-122">O provedor também pode ser registrado como um provedor de consumidor de eventos ou um provedor de contador de desempenho.</span><span class="sxs-lookup"><span data-stu-id="df894-122">The provider may also be registered as an event consumer provider or a performance counter provider.</span></span>

<span data-ttu-id="df894-123">A mesma instância do [**\_ \_ Win32Provider**](--win32provider.md) é usada para cada tipo de registro:</span><span class="sxs-lookup"><span data-stu-id="df894-123">The same instance of [**\_\_Win32Provider**](--win32provider.md) is used for each type of registration:</span></span>

-   [<span data-ttu-id="df894-124">Registrando um provedor de instância</span><span class="sxs-lookup"><span data-stu-id="df894-124">Registering an Instance Provider</span></span>](registering-an-instance-provider.md)
-   [<span data-ttu-id="df894-125">Registrando um provedor de classe</span><span class="sxs-lookup"><span data-stu-id="df894-125">Registering a Class Provider</span></span>](registering-a-class-provider.md)
-   [<span data-ttu-id="df894-126">Registrando um provedor de métodos</span><span class="sxs-lookup"><span data-stu-id="df894-126">Registering a Method Provider</span></span>](registering-a-method-provider.md)
-   [<span data-ttu-id="df894-127">Registrando um provedor de eventos</span><span class="sxs-lookup"><span data-stu-id="df894-127">Registering an Event Provider</span></span>](registering-an-event-provider.md)
-   [<span data-ttu-id="df894-128">Registrando um provedor de consumidor de eventos</span><span class="sxs-lookup"><span data-stu-id="df894-128">Registering an Event Consumer Provider</span></span>](registering-an-event-consumer-provider.md)
-   [<span data-ttu-id="df894-129">Criando um provedor de instância em um provedor de High-Performance</span><span class="sxs-lookup"><span data-stu-id="df894-129">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)

## <a name="example-creating-and-registering-an-instance-of-a-provider"></a><span data-ttu-id="df894-130">Exemplo: Criando e registrando uma instância de um provedor</span><span class="sxs-lookup"><span data-stu-id="df894-130">Example: Creating and Registering an Instance of a Provider</span></span>

<span data-ttu-id="df894-131">O exemplo a seguir mostra um arquivo MOF que cria e registra uma instância do [provedor de registro do sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) no \\ namespace raiz cimv2.</span><span class="sxs-lookup"><span data-stu-id="df894-131">The following example shows a MOF file that creates and registers an instance of the [System Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider) in the root\\cimv2 namespace.</span></span> <span data-ttu-id="df894-132">Ele atribui o alias $Reg ao provedor para evitar o nome de caminho longo necessário nos registros de instância e método.</span><span class="sxs-lookup"><span data-stu-id="df894-132">It assigns the alias $Reg to the provider to avoid the long pathname required in the instance and method registrations.</span></span> <span data-ttu-id="df894-133">Para obter mais informações, consulte [criando um alias](creating-an-alias.md).</span><span class="sxs-lookup"><span data-stu-id="df894-133">For more information, see [Creating an Alias](creating-an-alias.md).</span></span>

``` syntax
// Place the Registry provider in the root\cimv2 namespace
#pragma namespace("\\\\.\\ROOT\\cimv2")

// Create an instance of __Win32Provider
instance of __Win32Provider as $Reg
{
Name = "RegProv";        
CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
HostingModel = "NetworkServiceHost:LocalServiceHost";
};

// Register as an instance provider by
// creating an instance
// of __InstanceProviderRegistration
instance of __InstanceProviderRegistration
{
 provider = $Reg;
 SupportsDelete = FALSE;
 SupportsEnumeration = TRUE;
 SupportsGet = TRUE;
 SupportsPut = TRUE;
};

// Register as a method provider by
// creating an instance
// of __MethodProviderRegistration
instance of __MethodProviderRegistration
{
 provider = $Reg;
};

// Define the StdRegProv class
[dynamic: ToInstance, provider("RegProv")]
class StdRegProv
{
[implemented, static] uint32 CreateKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName);
[implemented, static] uint32 DeleteKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName);
[implemented, static] uint32 EnumKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [OUT] string sNames[]);
[implemented, static] uint32 EnumValues(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [OUT] string sNames[], 
 [OUT] sint32 Types[]);
[implemented, static] uint32 DeleteValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName);
 [implemented, static] uint32 SetDWORDValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] uint32 uValue = 3);
[implemented, static] uint32 GetDWORDValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] uint32 uValue);
[implemented, static] uint32 SetStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue = "hello");
[implemented, static] uint32 GetStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [in] string sValueName, 
 [OUT] string sValue);
[implemented, static] uint32 SetMultiStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue[] = {"hello", "there"});
[implemented, static] uint32 GetMultiStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] string sValue[]);
[implemented, static] uint32 SetExpandedStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue = "%path%");
[implemented, static] uint32 GetExpandedStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] string sValue);
[implemented, static] uint32 SetBinaryValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [in] string sValueName, 
 [in] uint8 uValue[] = {1, 2});
[implemented, static] uint32 GetBinaryValue(
 {IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] uint8 uValue[]);
[implemented, static] uint32 CheckAccess(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] uint32 uRequired = 3, 
 [OUT] boolean bGranted);
};
```

## <a name="example-registering-a-provider"></a><span data-ttu-id="df894-134">Exemplo: registrando um provedor</span><span class="sxs-lookup"><span data-stu-id="df894-134">Example: Registering a Provider</span></span>

<span data-ttu-id="df894-135">O procedimento a seguir descreve como registrar um provedor.</span><span class="sxs-lookup"><span data-stu-id="df894-135">The following procedure describes how to register a provider.</span></span>

<span data-ttu-id="df894-136">**Para registrar um provedor**</span><span class="sxs-lookup"><span data-stu-id="df894-136">**To register a provider**</span></span>

1.  <span data-ttu-id="df894-137">Registre o provedor como um servidor COM.</span><span class="sxs-lookup"><span data-stu-id="df894-137">Register the provider as a COM server.</span></span>

    <span data-ttu-id="df894-138">Se necessário, talvez seja necessário criar entradas do registro.</span><span class="sxs-lookup"><span data-stu-id="df894-138">If necessary, you may need to create registry entries.</span></span> <span data-ttu-id="df894-139">Esse processo se aplica a todos os servidores COM e não está relacionado ao WMI.</span><span class="sxs-lookup"><span data-stu-id="df894-139">This process applies to all COM servers and is unrelated to WMI.</span></span> <span data-ttu-id="df894-140">Para obter mais informações, consulte a seção COM na documentação do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="df894-140">For more information, see the COM section in the Microsoft Windows Software Development Kit (SDK) documentation.</span></span>

2.  <span data-ttu-id="df894-141">Crie um arquivo MOF que contém instâncias do [**\_ \_ Win32Provider**](--win32provider.md) e uma instância de uma classe derivada direta ou indiretamente de [**\_ \_ ProviderRegistration**](--providerregistration.md), como [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="df894-141">Create a MOF file that contains instances of [**\_\_Win32Provider**](--win32provider.md) and an instance of a class derived either directly or indirectly from [**\_\_ProviderRegistration**](--providerregistration.md), such as [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md).</span></span> <span data-ttu-id="df894-142">Somente os administradores podem registrar ou excluir um provedor criando instâncias de classes derivadas de **\_ \_ Win32Provider** ou [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="df894-142">Only administrators can register or delete a provider by creating instances of classes derived from **\_\_Win32Provider** or [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>
3.  <span data-ttu-id="df894-143">Defina o [**HostingModel**](--win32provider.md) na instância do **\_ \_ Win32Provider** de acordo com os valores em [modelos de hospedagem](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="df894-143">Set the [**HostingModel**](--win32provider.md) in the instance of **\_\_Win32Provider** according to the values in [Hosting models](provider-hosting-and-security.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="df894-144">A menos que o provedor exija os altos privilégios da conta LocalSystem, a propriedade [**\_ \_ Win32Provider. HostingModel**](--win32provider.md) deverá ser definida como "NetworkServiceHost".</span><span class="sxs-lookup"><span data-stu-id="df894-144">Unless the provider requires the high privileges of the LocalSystem account, the [**\_\_Win32Provider.HostingModel**](--win32provider.md) property should be set to "NetworkServiceHost".</span></span> <span data-ttu-id="df894-145">Para obter mais informações, consulte [provedor de hospedagem e segurança](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="df894-145">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

     

    <span data-ttu-id="df894-146">O exemplo de MOF a seguir do exemplo completo mostra o código que cria uma instância do [**\_ \_ Win32Provider**](--win32provider.md).</span><span class="sxs-lookup"><span data-stu-id="df894-146">The following MOF example from the full example shows the code that creates an instance of [**\_\_Win32Provider**](--win32provider.md).</span></span>

    ```mof
    instance of __Win32Provider as $Reg
    {
    Name = "RegProv";        
    CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
    HostingModel = "NetworkServiceHost:LocalServiceHost";
    };
    ```

    

4.  <span data-ttu-id="df894-147">Uma instância de uma classe derivada direta ou indiretamente de [**\_ \_ ProviderRegistration**](--providerregistration.md), para descrever a implementação lógica do provedor.</span><span class="sxs-lookup"><span data-stu-id="df894-147">An instance of a class derived either directly or indirectly from [**\_\_ProviderRegistration**](--providerregistration.md), to describe the logical implementation of the provider.</span></span> <span data-ttu-id="df894-148">Um provedor pode ser registrado para vários tipos diferentes de funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="df894-148">A provider can be registered for several different types of functionality.</span></span> <span data-ttu-id="df894-149">O exemplo acima registra RegProv como um provedor de método e instância.</span><span class="sxs-lookup"><span data-stu-id="df894-149">The example above registers RegProv as an instance and method provider.</span></span> <span data-ttu-id="df894-150">Mas se o RegProv der suporte à funcionalidade, ele também poderá ser registrado como um provedor de eventos ou propriedade.</span><span class="sxs-lookup"><span data-stu-id="df894-150">But if RegProv supports the functionality, it could also be registered as a property or event provider.</span></span> <span data-ttu-id="df894-151">A tabela a seguir lista as classes que registram a funcionalidade do provedor.</span><span class="sxs-lookup"><span data-stu-id="df894-151">The following table lists the classes that register provider functionality.</span></span>

    

    | <span data-ttu-id="df894-152">Classes de registro do provedor</span><span class="sxs-lookup"><span data-stu-id="df894-152">Provider registration classes</span></span>                                                        | <span data-ttu-id="df894-153">Descrição</span><span class="sxs-lookup"><span data-stu-id="df894-153">Description</span></span>                                                                         |
    |--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
    | [<span data-ttu-id="df894-154">**\_\_InstanceProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="df894-154">**\_\_InstanceProviderRegistration**</span></span>](--instanceproviderregistration.md)           | <span data-ttu-id="df894-155">Registra um [provedor de instância](registering-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="df894-155">Registers an [instance provider](registering-an-instance-provider.md).</span></span>             |
    | [<span data-ttu-id="df894-156">**\_\_EventProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="df894-156">**\_\_EventProviderRegistration**</span></span>](--eventproviderregistration.md)                 | <span data-ttu-id="df894-157">Registra um [provedor de eventos](registering-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="df894-157">Registers an [event provider](registering-an-event-provider.md).</span></span>                   |
    | [<span data-ttu-id="df894-158">**\_\_EventConsumerProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="df894-158">**\_\_EventConsumerProviderRegistration**</span></span>](--eventconsumerproviderregistration.md) | <span data-ttu-id="df894-159">Registra um [provedor de consumidor de eventos](registering-an-event-consumer-provider.md).</span><span class="sxs-lookup"><span data-stu-id="df894-159">Registers an [event consumer provider](registering-an-event-consumer-provider.md).</span></span> |
    | [<span data-ttu-id="df894-160">**\_\_MethodProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="df894-160">**\_\_MethodProviderRegistration**</span></span>](--methodproviderregistration.md)               | <span data-ttu-id="df894-161">Registra um [provedor de método](registering-an-event-consumer-provider.md).</span><span class="sxs-lookup"><span data-stu-id="df894-161">Registers a [method provider](registering-an-event-consumer-provider.md).</span></span>          |
    | [<span data-ttu-id="df894-162">**\_\_PropertyProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="df894-162">**\_\_PropertyProviderRegistration**</span></span>](--propertyproviderregistration.md)           | <span data-ttu-id="df894-163">Registra um [provedor de propriedades](registering-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="df894-163">Registers a [property provider](registering-a-property-provider.md).</span></span>               |

    

     

5.  <span data-ttu-id="df894-164">Coloque o arquivo MOF em um diretório permanente.</span><span class="sxs-lookup"><span data-stu-id="df894-164">Place the MOF file into a permanent directory.</span></span>

    <span data-ttu-id="df894-165">Normalmente, você deve posicionar o arquivo no diretório de instalação do provedor.</span><span class="sxs-lookup"><span data-stu-id="df894-165">Typically, you should place the file in the installation directory of the provider.</span></span>

6.  <span data-ttu-id="df894-166">Compile o arquivo MOF usando [Mofcomp](mofcomp.md) ou a interface [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="df894-166">Compile the MOF file using [mofcomp](mofcomp.md) or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span>

    <span data-ttu-id="df894-167">Para obter mais informações, consulte [compilando arquivos MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="df894-167">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

    <span data-ttu-id="df894-168">**Windows 8 e Windows Server 2012:** Ao instalar provedores, tanto o [**Mofcomp**](mofcomp.md) quanto a interface [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) tratam os \[ qualificadores de chave \] e \[ estáticos \] como verdadeiros se estiverem presentes, independentemente de seus valores reais.</span><span class="sxs-lookup"><span data-stu-id="df894-168">**Windows 8 and Windows Server 2012:** When installing providers, both [**mofcomp**](mofcomp.md) and the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface treat the \[Key\] and \[Static\] qualifiers as true if they are present, regardless of their actual values.</span></span> <span data-ttu-id="df894-169">Outros qualificadores são tratados como false se estiverem presentes, mas não definidos explicitamente como true.</span><span class="sxs-lookup"><span data-stu-id="df894-169">Other qualifiers are treated as false if they are present but not explicitly set to true.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df894-170">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="df894-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df894-171">Desenvolvendo um provedor WMI</span><span class="sxs-lookup"><span data-stu-id="df894-171">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="df894-172">Configurando descritores de segurança namepace</span><span class="sxs-lookup"><span data-stu-id="df894-172">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="df894-173">Protegendo seu provedor</span><span class="sxs-lookup"><span data-stu-id="df894-173">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 
