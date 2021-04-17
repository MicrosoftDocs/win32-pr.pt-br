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
# <a name="writing-an-association-provider-for-interop"></a>Escrevendo um provedor de associação para interoperabilidade

Um provedor de associação fornece um mecanismo para registrar perfis e associá-los a perfis que são implementados em namespaces diferentes.

Provedores de associação são usados para expor perfis padrão, como um perfil de energia. Isso é feito escrevendo um provedor de associação no namespace root/Interop que expõe instâncias de associação implementando uma classe, que é derivada do [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)). O provedor deve ser registrado tanto na raiz/na interoperabilidade quanto na raiz/ <implemented> namespace para dar suporte à passagem entre namespaces.

Instrumentação de Gerenciamento do Windows (WMI) carrega o provedor de associação sempre que uma consulta de associação é executada no namespace root/Interop.

**Para implementar um provedor de associação para interoperabilidade**

1.  Derive uma classe do [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) e crie uma instância estática dessa classe derivada no namespace root \\ Interop. No mínimo, as seguintes propriedades devem ser propagadas com valores válidos:

    -   [**InstanceID**](/previous-versions//ee309375(v=vs.85))
    -   [**Registeredname**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredOrganization**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredVersion**](/previous-versions//ee309375(v=vs.85))

    Embora [**InstanceId**](/previous-versions//ee309375(v=vs.85)) defina exclusivamente a instância do **\_ RegisteredProfile CIM**, a combinação de **registeredname**, **RegisteredOrganization** e **RegisteredVersion** deve identificar exclusivamente o perfil registrado no escopo da organização. Para obter mais informações sobre as propriedades individuais, consulte [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).

    O exemplo de código a seguir descreve a sintaxe para derivar a classe **ProcessProfile** de [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) e preencher a instância estática.

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
    > Para clientes Windows, a propriedade **RegisteredOrganization** deve ser definida como 1 e a propriedade **OtherRegisteredOrganization** definida como "Microsoft".

     

2.  Crie um provedor que retorne instâncias de associação do [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile). Esse é um processo de duas etapas.

    1.  Crie uma classe que seja derivada do [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) nos namespaces de interoperabilidade e implementação. Como o mesmo perfil pode ser implementado por diferentes fornecedores, o nome da classe deve ser exclusivo. A Convenção de nomenclatura recomendada é " <Organization> \_ <ProductName> \_ <ClassName> \_ <Version> ". A propriedade **ConformantStandard** ou **managedelement** deve especificar o qualificador **\_ targetNamespace de MSFT** que contém o namespace ao qual essa classe pertence.

        O exemplo de código a seguir descreve a sintaxe para derivar \_ a \_ classe Microsoft Process ElementConformsToProfile \_ v1 do [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) no \\ namespace root Interop. Neste exemplo, o \_ elemento gerenciado pelo processo Win32 faz referência ao \\ namespace raiz cimv2 usando o qualificador **\_ targetNamespace do MSFT** .

        ```syntax
        #pragma namespace("\\\\.\\root\\interop")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             CIM_RegisteredProfile ref ConformantStandard = $PP;
             [MSFT_TargetNamespace("root\\cimv2")]Win32_process ref ManagedElement = null;
        };
        ```

        O exemplo de código a seguir descreve a sintaxe para derivar \_ a \_ classe Microsoft Process ElementConformsToProfile \_ v1 do [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) no \\ namespace root cimv2. Neste exemplo, o padrão de conformidade do [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) faz referência ao \\ namespace de interoperabilidade de raiz usando o qualificador **\_ targetNamespace do MSFT** .

        ```syntax
        #pragma namespace("\\\\.\\root\\cimv2")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             [MSFT_TargetNamespace("root\\interop")] CIM_RegisteredProfile ref ConformantStandard = $PP;
             Win32_process ref ManagedElement = null;
        };
        ```

        Se o qualificador **\_ targetNamespace do MSFT** não for especificado na propriedade que faz referência ao namespace implementado, o filtro **ResultClass** da instrução "ASSOCIATORS of" não funcionará. Por exemplo, se o qualificador de **\_ targetNamespace do MSFT** não for especificado, a seguinte linha de comando do Windows PowerShell não retornará um objeto: **Get-WmiObject-Query "ASSOCIADORES de {ProcessProfile. InstanceId = ' Process '}, em que ResultClass = ' Win32 \_ Process '"**.

        O qualificador de **\_ targetNamespace do MSFT** não pode apontar para um namespace em um computador remoto. Por exemplo, não há suporte para o namespace a seguir: MSFT \_ targetNamespace ( \\ \\ \\ \\ <RemoteMachine> \\ \\ \\ \\ interoperabilidade raiz).

    2.  Escreva um provedor que retorne instâncias da classe derivada criada. Para obter mais informações, consulte [escrevendo um provedor de instância](writing-an-instance-provider.md). Ao acessar instâncias de namespace cruzado, talvez seja necessário acessar os níveis de segurança do cliente. Para obter mais informações, consulte [representando um cliente](impersonating-a-client.md).

        O provedor de associação deve implementar os métodos [**IWbemServices. CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) e [**IWbemServices. GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) . A implementação do método [**IWbemServices.ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) é opcional. Como esse provedor pode ser acessado de ambos os \\ namespaces de interoperabilidade raiz e raiz \\ <implemented> , não deve haver uma dependência explícita em um namespace dentro do provedor.

3.  Registre o provedor de associação nos \\ namespaces de interoperabilidade raiz e raiz \\ <implemented> . Para obter mais informações, consulte [registrando um provedor de instância](registering-an-instance-provider.md).

    O exemplo de código a seguir descreve a sintaxe para registrar o provedor de associação no \\ namespace de interoperabilidade raiz.

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

    O exemplo de código a seguir descreve a sintaxe para registrar o provedor de associação no \\ namespace raiz cimv2.

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

4.  Coloque o esquema para o [**\_ ElementConformsToProfile CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) no namespace implementado. Para clientes Windows, esse é o arquivo Interop. mof localizado na pasta% SystemRoot% \\ System32 \\ WBEM.
5.  Implemente a interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para seu provedor.

    O WMI usa [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para carregar e inicializar um provedor. O método [**tialize deIWbemProviderInit.Ini**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) deve ser implementado de forma que permita que ele seja chamado para dois namespaces diferentes. Para obter mais informações, consulte [inicializando um provedor](initializing-a-provider.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**\_ELEMENTCONFORMSTOPROFILE CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))
</dt> <dt>

[Gravando um provedor de instância](writing-an-instance-provider.md)
</dt> <dt>

[Registrando um provedor de instância](registering-an-instance-provider.md)
</dt> </dl>

 

 
