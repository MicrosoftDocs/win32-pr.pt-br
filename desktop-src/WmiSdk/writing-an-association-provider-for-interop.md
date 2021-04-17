---
description: Um provedor de associação fornece um mecanismo para registrar perfis e associá-los a perfis que são implementados em namespaces diferentes.
ms.assetid: e6aab944-4ed8-4678-ad35-426f7b4f9a35
ms.tgt_platform: multiple
title: Escrevendo um provedor de associação para interoperabilidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f38f09a5c5771fe7fd04909f8247834b646ad1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105812379"
---
# <a name="writing-an-association-provider-for-interop"></a><span data-ttu-id="20564-103">Escrevendo um provedor de associação para interoperabilidade</span><span class="sxs-lookup"><span data-stu-id="20564-103">Writing an Association Provider for Interop</span></span>

<span data-ttu-id="20564-104">Um provedor de associação fornece um mecanismo para registrar perfis e associá-los a perfis que são implementados em namespaces diferentes.</span><span class="sxs-lookup"><span data-stu-id="20564-104">An association provider provides a mechanism to register profiles and associate them with profiles that are implemented in different namespaces.</span></span>

<span data-ttu-id="20564-105">Provedores de associação são usados para expor perfis padrão, como um perfil de energia.</span><span class="sxs-lookup"><span data-stu-id="20564-105">Association providers are used to expose standard profiles, like a power profile.</span></span> <span data-ttu-id="20564-106">Isso é feito escrevendo um provedor de associação no namespace root/Interop que expõe instâncias de associação implementando uma classe, que é derivada do [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="20564-106">This is accomplished by writing an association provider in the root/interop namespace that exposes association instances by implementing a class, which is derived from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span> <span data-ttu-id="20564-107">O provedor deve ser registrado tanto na raiz/na interoperabilidade quanto na raiz/ <implemented> namespace para dar suporte à passagem entre namespaces.</span><span class="sxs-lookup"><span data-stu-id="20564-107">The provider must be registered in both the root/interop and the root/<implemented> namespace to support cross namespace traversal.</span></span>

<span data-ttu-id="20564-108">Instrumentação de Gerenciamento do Windows (WMI) carrega o provedor de associação sempre que uma consulta de associação é executada no namespace root/Interop.</span><span class="sxs-lookup"><span data-stu-id="20564-108">Windows Management Instrumentation (WMI) loads the association provider whenever an association query is run in the root/interop namespace.</span></span>

<span data-ttu-id="20564-109">**Para implementar um provedor de associação para interoperabilidade**</span><span class="sxs-lookup"><span data-stu-id="20564-109">**To implement an association provider for interop**</span></span>

1.  <span data-ttu-id="20564-110">Derive uma classe do [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) e crie uma instância estática dessa classe derivada no namespace root \\ Interop.</span><span class="sxs-lookup"><span data-stu-id="20564-110">Derive a class from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) and create a static instance of this derived class in the root\\interop namespace.</span></span> <span data-ttu-id="20564-111">No mínimo, as seguintes propriedades devem ser propagadas com valores válidos:</span><span class="sxs-lookup"><span data-stu-id="20564-111">At a minimum, the following properties must be propagated with valid values:</span></span>

    -   <span data-ttu-id="20564-112">[**InstanceID**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="20564-112">[**InstanceID**](/previous-versions//ee309375(v=vs.85))</span></span>
    -   <span data-ttu-id="20564-113">[**Registeredname**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="20564-113">[**RegisteredName**](/previous-versions//ee309375(v=vs.85))</span></span>
    -   <span data-ttu-id="20564-114">[**RegisteredOrganization**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="20564-114">[**RegisteredOrganization**](/previous-versions//ee309375(v=vs.85))</span></span>
    -   <span data-ttu-id="20564-115">[**RegisteredVersion**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="20564-115">[**RegisteredVersion**](/previous-versions//ee309375(v=vs.85))</span></span>

    <span data-ttu-id="20564-116">Embora [**InstanceId**](/previous-versions//ee309375(v=vs.85)) defina exclusivamente a instância do **\_ RegisteredProfile CIM**, a combinação de **registeredname**, **RegisteredOrganization** e **RegisteredVersion** deve identificar exclusivamente o perfil registrado no escopo da organização.</span><span class="sxs-lookup"><span data-stu-id="20564-116">Even though [**InstanceID**](/previous-versions//ee309375(v=vs.85)) uniquely defines the instance of the **CIM\_RegisteredProfile**, the combination of **RegisteredName**, **RegisteredOrganization**, and **RegisteredVersion** must uniquely identify the registered profile within the scope of the organization.</span></span> <span data-ttu-id="20564-117">Para obter mais informações sobre as propriedades individuais, consulte [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="20564-117">For more information about the individual properties, see [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

    <span data-ttu-id="20564-118">O exemplo de código a seguir descreve a sintaxe para derivar a classe **ProcessProfile** de [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) e preencher a instância estática.</span><span class="sxs-lookup"><span data-stu-id="20564-118">The following code example describes the syntax for deriving the **ProcessProfile** class from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) and populating the static instance.</span></span>

    ```syntax
    class ProcessProfile : CIM_RegisteredProfile
    {
    };

    instance of ProcessProfile as $PP
    {
         InstanceID = "Process";
         RegisteredName = "Process";
         RegisteredOrganization = "1"; // Set to "Other"
         OtherRegisteredOrganization = "Microsoft";
         RegisteredVersion = "1.0";
    };
    ```

    > [!Note]  
    > <span data-ttu-id="20564-119">Para clientes Windows, a propriedade **RegisteredOrganization** deve ser definida como 1 e a propriedade **OtherRegisteredOrganization** definida como "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="20564-119">For Windows clients, the **RegisteredOrganization** property must be set to 1 and the **OtherRegisteredOrganization** property set to "Microsoft".</span></span>

     

2.  <span data-ttu-id="20564-120">Crie um provedor que retorne instâncias de associação do [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile).</span><span class="sxs-lookup"><span data-stu-id="20564-120">Create a provider that returns association instances of [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile).</span></span> <span data-ttu-id="20564-121">Esse é um processo de duas etapas.</span><span class="sxs-lookup"><span data-stu-id="20564-121">This is a two-step process.</span></span>

    1.  <span data-ttu-id="20564-122">Crie uma classe que seja derivada do [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) nos namespaces de interoperabilidade e implementação.</span><span class="sxs-lookup"><span data-stu-id="20564-122">Create a class that is derived from [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) in both the interop and implementation namespaces.</span></span> <span data-ttu-id="20564-123">Como o mesmo perfil pode ser implementado por diferentes fornecedores, o nome da classe deve ser exclusivo.</span><span class="sxs-lookup"><span data-stu-id="20564-123">Because the same profile can be implemented by different vendors, the name of the class should be unique.</span></span> <span data-ttu-id="20564-124">A Convenção de nomenclatura recomendada é " <Organization> \_ <ProductName> \_ <ClassName> \_ <Version> ".</span><span class="sxs-lookup"><span data-stu-id="20564-124">The recommended naming convention is "<Organization>\_<ProductName>\_<ClassName>\_<Version>".</span></span> <span data-ttu-id="20564-125">A propriedade **ConformantStandard** ou **managedelement** deve especificar o qualificador **\_ targetNamespace de MSFT** que contém o namespace ao qual essa classe pertence.</span><span class="sxs-lookup"><span data-stu-id="20564-125">Either the **ConformantStandard** or the **ManagedElement** property must specify the **MSFT\_TargetNamespace** qualifier that contains the namespace to which this class belongs.</span></span>

        <span data-ttu-id="20564-126">O exemplo de código a seguir descreve a sintaxe para derivar \_ a \_ classe Microsoft Process ElementConformsToProfile \_ v1 do [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) no \\ namespace root Interop.</span><span class="sxs-lookup"><span data-stu-id="20564-126">The following code example describes the syntax for deriving the Microsoft\_Process\_ElementConformsToProfile\_v1 class from [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) in the root\\interop namespace.</span></span> <span data-ttu-id="20564-127">Neste exemplo, o \_ elemento gerenciado pelo processo Win32 faz referência ao \\ namespace raiz cimv2 usando o qualificador **\_ targetNamespace do MSFT** .</span><span class="sxs-lookup"><span data-stu-id="20564-127">In this example, the Win32\_Process managed element references the root\\cimv2 namespace by using the **MSFT\_TargetNamespace** qualifier.</span></span>

        ```syntax
        #pragma namespace("\\\\.\\root\\interop")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             CIM_RegisteredProfile ref ConformantStandard = $PP;
             [MSFT_TargetNamespace("root\\cimv2")]Win32_process ref ManagedElement = null;
        };
        ```

        <span data-ttu-id="20564-128">O exemplo de código a seguir descreve a sintaxe para derivar \_ a \_ classe Microsoft Process ElementConformsToProfile \_ v1 do [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) no \\ namespace root cimv2.</span><span class="sxs-lookup"><span data-stu-id="20564-128">The following code example describes the syntax for deriving the Microsoft\_Process\_ElementConformsToProfile\_v1 class from [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) in the root\\cimv2 namespace.</span></span> <span data-ttu-id="20564-129">Neste exemplo, o padrão de conformidade do [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) faz referência ao \\ namespace de interoperabilidade de raiz usando o qualificador **\_ targetNamespace do MSFT** .</span><span class="sxs-lookup"><span data-stu-id="20564-129">In this example, the [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) conformant standard references the root\\interop namespace by using the **MSFT\_TargetNamespace** qualifier.</span></span>

        ```syntax
        #pragma namespace("\\\\.\\root\\cimv2")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             [MSFT_TargetNamespace("root\\interop")] CIM_RegisteredProfile ref ConformantStandard = $PP;
             Win32_process ref ManagedElement = null;
        };
        ```

        <span data-ttu-id="20564-130">Se o qualificador **\_ targetNamespace do MSFT** não for especificado na propriedade que faz referência ao namespace implementado, o filtro **ResultClass** da instrução "ASSOCIATORS of" não funcionará.</span><span class="sxs-lookup"><span data-stu-id="20564-130">If the **MSFT\_TargetNamespace** qualifier is not specified on the property that is referencing the implemented namespace, the **ResultClass** filter of "Associators of" statement will not work.</span></span> <span data-ttu-id="20564-131">Por exemplo, se o qualificador de **\_ targetNamespace do MSFT** não for especificado, a seguinte linha de comando do Windows PowerShell não retornará um objeto: **Get-WmiObject-Query "ASSOCIADORES de {ProcessProfile. InstanceId = ' Process '}, em que ResultClass = ' Win32 \_ Process '"**.</span><span class="sxs-lookup"><span data-stu-id="20564-131">For example, if the **MSFT\_TargetNamespace** qualifier is not specified, the following Windows PowerShell command-line will not return an object: **get-wmiobject -query "associators of {ProcessProfile.InstanceID='Process'} where resultclass='Win32\_Process'"**.</span></span>

        <span data-ttu-id="20564-132">O qualificador de **\_ targetNamespace do MSFT** não pode apontar para um namespace em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="20564-132">The **MSFT\_TargetNamespace** qualifier cannot point to a namespace on a remote computer.</span></span> <span data-ttu-id="20564-133">Por exemplo, não há suporte para o namespace a seguir: MSFT \_ targetNamespace ( \\ \\ \\ \\ <RemoteMachine> \\ \\ \\ \\ interoperabilidade raiz).</span><span class="sxs-lookup"><span data-stu-id="20564-133">For example, the following namespace is not supported: MSFT\_TargetNamespace(\\\\\\\\<RemoteMachine>\\\\root\\\\interop).</span></span>

    2.  <span data-ttu-id="20564-134">Escreva um provedor que retorne instâncias da classe derivada criada.</span><span class="sxs-lookup"><span data-stu-id="20564-134">Write a provider that returns instances of the created derived class.</span></span> <span data-ttu-id="20564-135">Para obter mais informações, consulte [escrevendo um provedor de instância](writing-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="20564-135">For more information, see [Writing an Instance Provider](writing-an-instance-provider.md).</span></span> <span data-ttu-id="20564-136">Ao acessar instâncias de namespace cruzado, talvez seja necessário acessar os níveis de segurança do cliente.</span><span class="sxs-lookup"><span data-stu-id="20564-136">When you access cross-namespace instances, you might have to access the security levels for the client.</span></span> <span data-ttu-id="20564-137">Para obter mais informações, consulte [representando um cliente](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="20564-137">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

        <span data-ttu-id="20564-138">O provedor de associação deve implementar os métodos [**IWbemServices. CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) e [**IWbemServices. GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .</span><span class="sxs-lookup"><span data-stu-id="20564-138">The association provider should implement both the [**IWbemServices.CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) and [**IWbemServices.GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) methods.</span></span> <span data-ttu-id="20564-139">A implementação do método [**IWbemServices.ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) é opcional.</span><span class="sxs-lookup"><span data-stu-id="20564-139">Implementing the [**IWbemServices.ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method is optional.</span></span> <span data-ttu-id="20564-140">Como esse provedor pode ser acessado de ambos os \\ namespaces de interoperabilidade raiz e raiz \\ <implemented> , não deve haver uma dependência explícita em um namespace dentro do provedor.</span><span class="sxs-lookup"><span data-stu-id="20564-140">Because this provider can be accessed from both the root\\interop and the root\\<implemented> namespaces, there should not be an explicit dependency on a namespace inside the provider.</span></span>

3.  <span data-ttu-id="20564-141">Registre o provedor de associação nos \\ namespaces de interoperabilidade raiz e raiz \\ <implemented> .</span><span class="sxs-lookup"><span data-stu-id="20564-141">Register the association provider in both the root\\interop and the root\\<implemented> namespaces.</span></span> <span data-ttu-id="20564-142">Para obter mais informações, consulte [registrando um provedor de instância](registering-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="20564-142">For more information, see [Registering an Instance Provider](registering-an-instance-provider.md).</span></span>

    <span data-ttu-id="20564-143">O exemplo de código a seguir descreve a sintaxe para registrar o provedor de associação no \\ namespace de interoperabilidade raiz.</span><span class="sxs-lookup"><span data-stu-id="20564-143">The following code example describes the syntax to register the association provider in the root\\interop namespace.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root\\interop")
    instance of __Win32Provider as $P
    {
        Name    = "ProcessAssociation" ;
        ClsId   = "{DA13393B-A2D5-4BAC-9BD2-30B092E9EBB8}";
    } ;

    instance of __InstanceProviderRegistration
    {
        Provider = $P;
        SupportsPut = false;
        SupportsGet = TRUE;
        SupportsDelete = false;
        SupportsEnumeration = TRUE;
    };
    ```

    <span data-ttu-id="20564-144">O exemplo de código a seguir descreve a sintaxe para registrar o provedor de associação no \\ namespace raiz cimv2.</span><span class="sxs-lookup"><span data-stu-id="20564-144">The following code example describes the syntax to register the association provider in the root\\cimv2 namespace.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root\\cimv2")
    instance of __Win32Provider as $R
    {
        Name    = "ProcessAssociation" ;
        ClsId   = "{DA13393B-A2D5-4BAC-9BD2-30B092E9EBB8}";
    } ;

    instance of __InstanceProviderRegistration
    {
        Provider = $R;
        SupportsPut = false;
        SupportsGet = TRUE;
        SupportsDelete = false;
        SupportsEnumeration = TRUE;
    };
    ```

4.  <span data-ttu-id="20564-145">Coloque o esquema para o [**\_ ElementConformsToProfile CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) no namespace implementado.</span><span class="sxs-lookup"><span data-stu-id="20564-145">Place the schema for the [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) into the implemented namespace.</span></span> <span data-ttu-id="20564-146">Para clientes Windows, esse é o arquivo Interop. mof localizado na pasta% SystemRoot% \\ System32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="20564-146">For Windows clients this is the interop.mof file that is located in the %systemroot%\\system32\\wbem folder.</span></span>
5.  <span data-ttu-id="20564-147">Implemente a interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para seu provedor.</span><span class="sxs-lookup"><span data-stu-id="20564-147">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    <span data-ttu-id="20564-148">O WMI usa [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para carregar e inicializar um provedor.</span><span class="sxs-lookup"><span data-stu-id="20564-148">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="20564-149">O método [**tialize deIWbemProviderInit.Ini**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) deve ser implementado de forma que permita que ele seja chamado para dois namespaces diferentes.</span><span class="sxs-lookup"><span data-stu-id="20564-149">The [**IWbemProviderInit.Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) method should be implemented in a way that allows it to be called for two different namespaces.</span></span> <span data-ttu-id="20564-150">Para obter mais informações, consulte [inicializando um provedor](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="20564-150">For more information, see [Initializing a Provider](initializing-a-provider.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="20564-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="20564-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20564-152">**\_ELEMENTCONFORMSTOPROFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="20564-152">**CIM\_ElementConformsToProfile**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

<span data-ttu-id="20564-153">[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="20564-153">[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="20564-154">Gravando um provedor de instância</span><span class="sxs-lookup"><span data-stu-id="20564-154">Writing an Instance Provider</span></span>](writing-an-instance-provider.md)
</dt> <dt>

[<span data-ttu-id="20564-155">Registrando um provedor de instância</span><span class="sxs-lookup"><span data-stu-id="20564-155">Registering an Instance Provider</span></span>](registering-an-instance-provider.md)
</dt> </dl>

 

 
