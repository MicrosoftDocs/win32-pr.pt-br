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
# <a name="registering-a-provider"></a>Registrando um provedor

Antes de implementar seu provedor, primeiro você deve registrar seu provedor com o WMI. O registro do provedor define o tipo do provedor e as classes que o provedor suporta. O WMI só pode acessar provedores registrados.

> [!Note]  
> Para obter mais informações sobre como registrar um provedor de MI, consulte [como registrar um provedor de mi](/previous-versions/windows/desktop/wmi_v2/how-to-register-an-mi-provider).

 

Você pode escrever o código do provedor antes de registrar o provedor. No entanto, é muito difícil depurar um provedor que não esteja registrado com o WMI. Determinar as interfaces do seu provedor também ajuda a descrever a finalidade e a estrutura de um provedor. Portanto, registrar seu provedor ajuda você a projetar seu provedor.

Somente os administradores podem registrar ou excluir um provedor.

Um provedor deve ser registrado para todos os diferentes tipos de funções de provedor que ele executa. Quase todos os provedores fornecem instâncias de classes que eles definem, mas também podem fornecer dados de propriedade, métodos, eventos ou classes. O provedor também pode ser registrado como um provedor de consumidor de eventos ou um provedor de contador de desempenho. É recomendável que você combine toda a funcionalidade do provedor em um provedor em vez de ter muitos provedores separados para cada tipo. Um exemplo é o [provedor de registro do sistema](/previous-versions/windows/desktop/regprov/system-registry-provider), que fornece métodos e instâncias, e o [provedor de cota de disco](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider), que fornece instâncias, métodos e eventos.

Um provedor deve ser registrado para todos os diferentes tipos de funções de provedor que ele executa. Quase todos os provedores fornecem instâncias de classes que eles definem, mas também podem fornecer dados de propriedade, métodos, eventos ou classes. O provedor também pode ser registrado como um provedor de consumidor de eventos ou um provedor de contador de desempenho.

A mesma instância do [**\_ \_ Win32Provider**](--win32provider.md) é usada para cada tipo de registro:

-   [Registrando um provedor de instância](registering-an-instance-provider.md)
-   [Registrando um provedor de classe](registering-a-class-provider.md)
-   [Registrando um provedor de métodos](registering-a-method-provider.md)
-   [Registrando um provedor de eventos](registering-an-event-provider.md)
-   [Registrando um provedor de consumidor de eventos](registering-an-event-consumer-provider.md)
-   [Criando um provedor de instância em um provedor de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)

## <a name="example-creating-and-registering-an-instance-of-a-provider"></a>Exemplo: Criando e registrando uma instância de um provedor

O exemplo a seguir mostra um arquivo MOF que cria e registra uma instância do [provedor de registro do sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) no \\ namespace raiz cimv2. Ele atribui o alias $Reg ao provedor para evitar o nome de caminho longo necessário nos registros de instância e método. Para obter mais informações, consulte [criando um alias](creating-an-alias.md).

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

## <a name="example-registering-a-provider"></a>Exemplo: registrando um provedor

O procedimento a seguir descreve como registrar um provedor.

**Para registrar um provedor**

1.  Registre o provedor como um servidor COM.

    Se necessário, talvez seja necessário criar entradas do registro. Esse processo se aplica a todos os servidores COM e não está relacionado ao WMI. Para obter mais informações, consulte a seção COM na documentação do SDK (Software Development Kit) do Microsoft Windows.

2.  Crie um arquivo MOF que contém instâncias do [**\_ \_ Win32Provider**](--win32provider.md) e uma instância de uma classe derivada direta ou indiretamente de [**\_ \_ ProviderRegistration**](--providerregistration.md), como [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md). Somente os administradores podem registrar ou excluir um provedor criando instâncias de classes derivadas de **\_ \_ Win32Provider** ou [**\_ \_ ProviderRegistration**](--providerregistration.md).
3.  Defina o [**HostingModel**](--win32provider.md) na instância do **\_ \_ Win32Provider** de acordo com os valores em [modelos de hospedagem](provider-hosting-and-security.md).

    > [!Note]  
    > A menos que o provedor exija os altos privilégios da conta LocalSystem, a propriedade [**\_ \_ Win32Provider. HostingModel**](--win32provider.md) deverá ser definida como "NetworkServiceHost". Para obter mais informações, consulte [provedor de hospedagem e segurança](provider-hosting-and-security.md).

     

    O exemplo de MOF a seguir do exemplo completo mostra o código que cria uma instância do [**\_ \_ Win32Provider**](--win32provider.md).

    ```mof
    instance of __Win32Provider as $Reg
    {
    Name = "RegProv";        
    CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
    HostingModel = "NetworkServiceHost:LocalServiceHost";
    };
    ```

    

4.  Uma instância de uma classe derivada direta ou indiretamente de [**\_ \_ ProviderRegistration**](--providerregistration.md), para descrever a implementação lógica do provedor. Um provedor pode ser registrado para vários tipos diferentes de funcionalidade. O exemplo acima registra RegProv como um provedor de método e instância. Mas se o RegProv der suporte à funcionalidade, ele também poderá ser registrado como um provedor de eventos ou propriedade. A tabela a seguir lista as classes que registram a funcionalidade do provedor.

    

    | Classes de registro do provedor                                                        | Descrição                                                                         |
    |--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
    | [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md)           | Registra um [provedor de instância](registering-an-instance-provider.md).             |
    | [**\_\_EventProviderRegistration**](--eventproviderregistration.md)                 | Registra um [provedor de eventos](registering-an-event-provider.md).                   |
    | [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) | Registra um [provedor de consumidor de eventos](registering-an-event-consumer-provider.md). |
    | [**\_\_MethodProviderRegistration**](--methodproviderregistration.md)               | Registra um [provedor de método](registering-an-event-consumer-provider.md).          |
    | [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md)           | Registra um [provedor de propriedades](registering-a-property-provider.md).               |

    

     

5.  Coloque o arquivo MOF em um diretório permanente.

    Normalmente, você deve posicionar o arquivo no diretório de instalação do provedor.

6.  Compile o arquivo MOF usando [Mofcomp](mofcomp.md) ou a interface [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .

    Para obter mais informações, consulte [compilando arquivos MOF](compiling-mof-files.md).

    **Windows 8 e Windows Server 2012:** Ao instalar provedores, tanto o [**Mofcomp**](mofcomp.md) quanto a interface [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) tratam os \[ qualificadores de chave \] e \[ estáticos \] como verdadeiros se estiverem presentes, independentemente de seus valores reais. Outros qualificadores são tratados como false se estiverem presentes, mas não definidos explicitamente como true.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvendo um provedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Configurando descritores de segurança namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Protegendo seu provedor](securing-your-provider.md)
</dt> </dl>

 

 
