---
description: Especifica o modelo de hospedagem do provedor. Definir essa propriedade faz com que o provedor seja carregado em um processo de host compartilhado que tenha um nível de privilégio especificado.
ms.assetid: 1e5c778d-cd29-449b-88e2-fe0c90d0edcd
ms.tgt_platform: multiple
title: Hospedagem e segurança de provedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db6b88a5727f34fbb76baf62dcdf0488e5eb9eb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793220"
---
# <a name="provider-hosting-and-security"></a>Hospedagem e segurança de provedor

A propriedade [**HostingModel**](--win32provider.md) na instância do **\_ \_ Win32Provider** que representa o provedor especifica o modelo de hospedagem do provedor. Definir essa propriedade faz com que o provedor seja carregado em um processo de host compartilhado que tenha um nível de privilégio especificado.

## <a name="shared-provider-host-process"></a>Processo de host do provedor compartilhado

O WMI reside em um host de serviço compartilhado com vários outros serviços. Para evitar a interrupção de todos os serviços quando um provedor falha, os provedores são carregados em um processo de host separado chamado "Wmiprvse.exe". Mais de um processo com esse nome pode estar em execução. Cada um pode ser executado em uma conta diferente com segurança variável. Lembre-se de que, a partir do Windows Vista, use o comando [**winmgmt**](winmgmt.md) para executar o WMI em um processo separado usando uma porta fixa. Para obter mais informações, consulte [conectando-se ao WMI remotamente a partir do vista](connecting-to-wmi-remotely-starting-with-vista.md).

O host compartilhado pode ser executado em uma das seguintes contas de sistema em um processo de host Wmiprvse.exe:

-   [LocalSystem](/windows/desktop/Services/localsystem-account)
-   [NetworkService](/windows/desktop/Services/networkservice-account)
-   [LocalService](/windows/desktop/Services/localservice-account)

Um provedor também pode ser um servidor COM local (. exe) ou auto-hospedado, que não requer um host de provedor WMI.

## <a name="setting-the-hosting-model"></a>Definindo o modelo de hospedagem

Como o LocalSystem é uma conta com privilégios, é recomendável que você defina [**HostingModel**](--win32provider.md) como **NetworkServiceHost** quando um provedor estiver sendo executado em um processo de Wmiprvse.exe. A conta NetworkServiceHost é para serviços que não exigem privilégios extensos, mas precisam se comunicar remotamente com outros sistemas.

Se você não definir um valor para a propriedade [**HostingModel**](--win32provider.md) , o WMI definirá um valor padrão de **NetworkServiceHostOrSelfHost**. Se o valor **HostingModel** for definido como **LocalSystemHost**, o WMI usará o rastreamento para gerar eventos 5603 e 5604 no log de eventos do Windows. Como a conta [LocalSystem](/windows/desktop/Services/localsystem-account) local é altamente privilegiada, essa configuração não é recomendada. Você pode exibir esses eventos no **Visualizador de eventos**. Para obter mais informações, consulte [rastreando a atividade WMI](tracing-wmi-activity.md).

Defina a propriedade [**HostingModel**](--win32provider.md) para provedores dissociados como "dissociado: com". Provedores criados pela adição de classes de instrumentação do [**Microsoft. Management. Infrastructure**](/previous-versions//hh872326(v=vs.85)) no .NET Framework são desacoplados provedores. (Não há mais suporte para **System. Management. instrumentação** .) Para obter mais informações sobre como criar um provedor dissociado, consulte [incorporando um provedor em um aplicativo](incorporating-a-provider-in-an-application.md).

O modelo de hospedagem é especificado na propriedade [**HostingModel**](--win32provider.md) na instância do **\_ \_ Win32Provider** que representa seu provedor.

**Para definir o modelo de hospedagem para um provedor**

1.  No arquivo MOF que define seu provedor, crie uma instância do [**\_ \_ Win32Provider**](--win32provider.md).
2.  Atribua um nome ao provedor na propriedade **Name** e atribua o identificador de classe (CLSID) do objeto com do provedor à propriedade **CLSID** .

    O exemplo de código a seguir atribui um nome à propriedade **Name** e o CSLID do objeto com do provedor à propriedade **CLSID** .

    ``` syntax
    Instance of __Win32Provider as $NewProvider
    {
        Name = "MyProvider";
        Clsid = "{.......}";
    }
    ```

3.  Atribua o valor de host compartilhado apropriado à propriedade [**HostingModel**](--win32provider.md) . Valores de host compartilhados, como "NetworkServiceHost", são definidos na propriedade **HostingSpecification** da classe de [**\_ provedores MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) .

    O exemplo de código a seguir atribui um valor de host compartilhado à propriedade [**HostingModel**](--win32provider.md) .

    ``` syntax
    HostingModel = "NetworkServiceHost";
    ```

O exemplo de código a seguir mostra como registrar um provedor no NetworkServiceHost.

``` syntax
Instance of __Win32Provider as $NewProvider
{
    Name = "MyProvider";
    Clsid = "{.......}";
    HostingModel = "NetworkServiceHost";
}
```

Se você tiver vários provedores, poderá agrupá-los em um host de serviço específico registrando seu provedor para que ele resida na instância específica.

O exemplo de código a seguir também registra um provedor no NetworkServiceHost. A classe de [**\_ provedores de MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) define valores para os dois valores que se combinam para criar a propriedade **HostingModel** do [**\_ \_ Win32Provider**](--win32provider.md) . No exemplo, o valor "NetworkServiceHost" vem da propriedade **HostingSpecification** dos **\_ provedores de MSFT** e "LocalServiceHost" vem da Propriedade do The **Hosting** .

``` syntax
Instance of __Win32Provider as $NewProvider
{
    Name = "MyProvider";
    Clsid = "{.......}";
    HostingModel = "NetworkServiceHost:MySharedHost";
}
```

Existem problemas de desenvolvimento especiais para provedores que não estão desacoplados e são hospedados no processo do WMIPrvSE. Para obter mais informações, consulte [Debugging Providers](debugging-providers.md).

Se você estiver escrevendo um provedor que contém a propriedade ou o registro do provedor de classe, nem todos os modelos de Threading funcionam. Para obter mais informações, consulte [escolhendo o registro correto](choosing-correct-registration.md).

## <a name="hostingmodel-values-for-in-process-providers"></a>Valores de HostingModel para provedores de In-Process

A lista a seguir lista os valores de modelo de Hospedagem de provedor a serem usados na instância [**\_ \_ Win32Provider**](--win32provider.md) para provedores que são executados em um processo de Wmiprvse.exe.



| Valor em [ **\_ \_ Win32Provider. HostingModel**](--win32provider.md) | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SelfHost**                                                       | O provedor é iniciado usando a implementação do servidor local em vez de em processo. O contexto de segurança do processo no qual o provedor é executado determina o contexto de segurança do provedor.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **LocalSystemHost**                                                | O provedor, se implementado como em processo, é carregado em um host de provedor compartilhado em execução no contexto [LocalSystem](/windows/desktop/Services/localsystem-account) . A partir do Windows Vista, o **LocalSystemHost** não será mais o modelo de hospedagem padrão se o [**HostingModel**](--win32provider.md) de um provedor WMI (**\_ \_ Win32Provider**.**** A Propriedade HostingModel) não está especificada. Para obter mais informações, consulte [segurança dos modelos de hospedagem](#provider-hosting-and-security).                                                                                                                                                                                                                                                                               |
| **LocalSystemHostOrSelfHost**                                      | O provedor é auto-hospedado ou carregado no processo de Wmiprvse.exe em execução na conta [LocalSystem](/windows/desktop/Services/localsystem-account) . Como o LocalSystem é uma conta altamente privilegiada, uma entrada é gerada no log de eventos do NT de segurança para notificar os administradores sobre um provedor em execução nesse status confiável.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **NetworkServiceHost**                                             | O provedor, se implementado como em processo, é carregado no processo de Wmiprvse.exe em execução na conta [NetworkService](/windows/desktop/Services/networkservice-account) . A partir do Windows Vista, esse é o modelo de hospedagem padrão se o [**HostingModel**](--win32provider.md) de um provedor WMI (**\_ \_ Win32Provider**.**** A Propriedade HostingModel) não está especificada. Para obter mais informações, consulte [segurança dos modelos de hospedagem](#provider-hosting-and-security).<br/> O **NetworkServiceHost** tem privilégios limitados e, portanto, reduz a possibilidade de um ataque de elevação de privilégio. Se o provedor operar apenas no computador local, defina a propriedade [**HostingModel**](--win32provider.md) como **LocalServiceHost**.<br/> |
| **NetworkServiceHostOrSelfHost**                                   | O provedor é auto-hospedado ou carregado no processo de WmiPrvse.exe em execução na conta [NetworkService](/windows/desktop/Services/networkservice-account) . **NetworkServiceHostOrSelfHost** é a configuração padrão quando a [**Propriedade HostingModel**](--win32provider.md) em **\_ \_ Win32Provider** é **nula**. Como **NetworkServiceHostOrSelfHost** é o padrão, os provedores de sistemas operacionais anteriores podem continuar a funcionar no Windows Vista, no windows Server 2008 e em sistemas operacionais posteriores.                                                                                                                                                                                                                                             |
| **LocalServiceHost**                                               | O provedor, se implementado como em processo, é carregado no processo de Wmiprvse.exe em execução na conta [LocalService](/windows/desktop/Services/localservice-account) . Esse é o modelo de hospedagem recomendado para serviços porque o LocalService tem privilégios limitados.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="hostingmodel-values-for-decoupled-providers"></a>Valores de HostingModel para provedores dissociados

A lista a seguir lista os valores de modelo de Hospedagem de provedor para provedores dissociados.

<dl> <dt>

<span id="Decoupled_Com"></span><span id="decoupled_com"></span><span id="DECOUPLED_COM"></span>**Dissociado: com**
</dt> <dd>

O provedor é um provedor dissociado hospedado em um processo separado que é um cliente do WMI.

O exemplo a seguir mostra o especificador FoldIdentity para a propriedade [**HostingModel**](--win32provider.md) definida como **false**, que permite que o provedor represente o cliente.

``` syntax
Decoupled:Com:FoldIdentity(FALSE)
```

Se FoldIdentity não for especificado, o valor de FoldIdentity será definido como **true** por padrão. Por motivos de segurança, é recomendável que você não especifique FoldIdentity (FALSE), já que um aplicativo não autorizado com representação de delegate pode afetar um domínio inteiro.

O exemplo a seguir mostra a propriedade [**HostingModel**](--win32provider.md) definida da maneira recomendada que é equivalente a definir FOLDIDENTITY (true).

``` syntax
Decoupled:Com
```

</dd> <dt>

<span id="Decoupled_Noncom"></span><span id="decoupled_noncom"></span><span id="DECOUPLED_NONCOM"></span>**Dissociado: noncom**
</dt> <dd>

Somente para uso interno. Não há suporte.

</dd> </dl>

## <a name="security-of-hosting-models"></a>Segurança dos modelos de hospedagem

Na maioria das situações, o **LocalSystem** é desnecessário e o contexto de **NetworkServiceHost** é mais apropriado. A maioria dos provedores de WMI deve representar o contexto do Client Security para executar as operações solicitadas em nome do cliente WMI. A partir do Windows Vista, um provedor WMI que não tem uma definição de modelo de hospedagem e é executado como se fosse executado em **LocalSystem** não será executado corretamente. Para corrigir essa situação, altere o modelo de hospedagem esperado e verifique se o código do provedor WMI executa as operações no contexto do Client Security, representando o cliente WMI. O LocalSystem raramente é um requisito. Se o seu provedor precisar ter esse nível de privilégio, especifique o modelo de hospedagem com a seguinte instrução no arquivo MOF.

``` syntax
HostingModel=LocalSystemHost
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Escolhendo o registro correto](choosing-correct-registration.md)
</dt> <dt>

[Acesso a namespaces WMI](access-to-wmi-namespaces.md)
</dt> <dt>

[Protegendo namespaces WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Configuração do provedor e classes de solução de problemas](provider-configuration-and-troubleshooting-classes.md)
</dt> <dt>

[**Provedores de MSFT \_**](/previous-versions/windows/desktop/wmisystemprov/msft-providers)
</dt> <dt>

[Mantendo a segurança do WMI](maintaining-wmi-security.md)
</dt> </dl>

 

