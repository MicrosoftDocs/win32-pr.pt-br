---
description: Um provedor de associação fornece um mecanismo para registrar perfis e associá-los a perfis implementados em namespaces diferentes.
ms.assetid: e6aab944-4ed8-4678-ad35-426f7b4f9a35
ms.tgt_platform: multiple
title: Escrevendo um provedor de associação para interop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ef4e73c35c942e56b2636b7fced4c7e468e120
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887435"
---
# <a name="writing-an-association-provider-for-interop"></a>Escrevendo um provedor de associação para interop

Um provedor de associação fornece um mecanismo para registrar perfis e associá-los a perfis implementados em namespaces diferentes.

Provedores de associação são usados para expor perfis padrão, como um perfil de energia. Isso é feito escrevendo um provedor de associação no namespace raiz/de interop que expõe instâncias de associação implementando uma classe , que é derivada de [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)). O provedor deve ser registrado na raiz/interop e no namespace raiz/implementado para dar suporte à travessia entre &lt; &gt; namespaces.

Windows A Instrumentação de Gerenciamento (WMI) carrega o provedor de associação sempre que uma consulta de associação é executado no namespace raiz/de interop.

**Para implementar um provedor de associação para interop**

1.  Derive uma classe de [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) e crie uma instância estática dessa classe derivada no namespace de \\ interop raiz. No mínimo, as seguintes propriedades devem ser propagadas com valores válidos:

    -   [**Instanceid**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredName**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredOrganization**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredVersion**](/previous-versions//ee309375(v=vs.85))

    Embora [**InstanceID**](/previous-versions//ee309375(v=vs.85)) defina exclusivamente a instância do **CIM \_ RegisteredProfile,** a combinação de **RegisteredName,** **RegisteredOrganization** e **RegisteredVersion** deve identificar exclusivamente o perfil registrado dentro do escopo da organização. Para obter mais informações sobre as propriedades individuais, consulte [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).

    O exemplo de código a seguir descreve a sintaxe para derivar a **classe ProcessProfile** de [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) e popular a instância estática.

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
    > Para Windows clientes, a propriedade **RegisteredOrganization** deve ser definida como 1 e a propriedade **OtherRegisteredOrganization** definida como "Microsoft".

     

2.  Crie um provedor que retorna instâncias de associação de [**\_ ElementConformsToProfile do CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) Esse é um processo de duas etapas.

    1.  Crie uma classe derivada de [**\_ ElementConformsToProfile do CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) nos namespaces de interop e implementação. Como o mesmo perfil pode ser implementado por fornecedores diferentes, o nome da classe deve ser exclusivo. A convenção de nomen efetivação recomendada é " &lt; Organization &gt; \_ &lt; ProductName &gt; \_ &lt; ClassName &gt; \_ &lt; Version &gt; ". A propriedade **ConformantStandard** ou **ManagedElement** deve especificar o qualificador **MSFT \_ TargetNamespace** que contém o namespace ao qual essa classe pertence.

        O exemplo de código a seguir descreve a sintaxe para derivar a classe \_ \_ ElementConformsToProfile v1 do \_ [**\_ ElementConformsToProfile do CIM ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) no namespace de \\ interop raiz. Neste exemplo, o elemento gerenciado processo Win32 faz referência ao namespace raiz cimv2 usando o \_ \\ qualificador **MSFT \_ TargetNamespace.**

        ```syntax
        #pragma namespace("\\\\.\\root\\interop")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             CIM_RegisteredProfile ref ConformantStandard = $PP;
             [MSFT_TargetNamespace("root\\cimv2")]Win32_process ref ManagedElement = null;
        };
        ```

        O exemplo de código a seguir descreve a sintaxe para derivar a classe \_ \_ ElementConformsToProfile v1 do \_ [**\_ ElementConformsToProfile do CIM ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) no \\ namespace raiz cimv2. Neste exemplo, o padrão compatível com [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) faz referência ao namespace de interop raiz usando o \\ qualificador **MSFT \_ TargetNamespace.**

        ```syntax
        #pragma namespace("\\\\.\\root\\cimv2")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             [MSFT_TargetNamespace("root\\interop")] CIM_RegisteredProfile ref ConformantStandard = $PP;
             Win32_process ref ManagedElement = null;
        };
        ```

        Se o qualificador **\_ MSFT TargetNamespace** não for especificado na propriedade que está referenciando o namespace implementado, o filtro **ResultClass** da instrução "Associatores de" não funcionará. Por exemplo, se o qualificador **MSFT \_ TargetNamespace** não for especificado, a seguinte linha de comando do Windows PowerShell não retornará um objeto: **get-wmiobject -query "associators de {ProcessProfile.InstanceID='Process'} em que resultclass='Win32 \_ Process'"**.

        O **qualificador \_ MSFT TargetNamespace** não pode apontar para um namespace em um computador remoto. Por exemplo, não há suporte para o namespace a seguir: MSFT \_ TargetNamespace( \\ \\ \\ \\ &lt; interop raiz RemoteMachine). &gt; \\ \\ \\ \\

    2.  Escreva um provedor que retorna instâncias da classe derivada criada. Para obter mais informações, consulte [Escrevendo um provedor de instância](writing-an-instance-provider.md). Ao acessar instâncias entre namespaces, talvez seja preciso acessar os níveis de segurança do cliente. Para obter mais informações, consulte [Representando um cliente](impersonating-a-client.md).

        O provedor de associação deve implementar os métodos [**IWbemServices.CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) e [**IWbemServices.GetObjectAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) Implementar o método [**IWbemServices.ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) é opcional. Como esse provedor pode ser acessado da interop raiz e dos \\ \\ &lt; namespaces implementados por raiz, não deve haver uma dependência explícita em um namespace dentro &gt; do provedor.

3.  Registre o provedor de associação na \\ interop raiz e nos \\ &lt; &gt; namespaces implementados por raiz. Para obter mais informações, consulte [Registrando um provedor de instância](registering-an-instance-provider.md).

    O exemplo de código a seguir descreve a sintaxe para registrar o provedor de associação no namespace de \\ interop raiz.

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

4.  Coloque o esquema para o [**\_ ElementConformsToProfile do CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) no namespace implementado. Para Windows clientes, esse é o arquivo interop.mof localizado na pasta %systemroot% \\ system32 \\ wbem.
5.  Implemente a interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para seu provedor.

    O WMI [**usa IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para carregar e inicializar um provedor. O [**IWbemProviderInit.Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) deve ser implementado de uma maneira que permita que ele seja chamado para dois namespaces diferentes. Para obter mais informações, consulte [Inicializando um provedor](initializing-a-provider.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Elemento \_ CIMConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

[**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))
</dt> <dt>

[Escrevendo um provedor de instância](writing-an-instance-provider.md)
</dt> <dt>

[Registrando um provedor de instância](registering-an-instance-provider.md)
</dt> </dl>

 

 
