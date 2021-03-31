---
description: Quando um aplicativo de usuário solicita dados de objetos no sistema por meio de um provedor WMI, a representação significa que o provedor apresenta credenciais que representam o nível de segurança dos clientes em vez dos provedores.
ms.assetid: 6d54f234-45aa-445b-ad50-7d5a9946c134
ms.tgt_platform: multiple
title: Representando um cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 162857d90c8bddb70d90eb2e10efbc08537299d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829274"
---
# <a name="impersonating-a-client"></a>Representando um cliente

Quando um aplicativo de usuário solicita dados de objetos no sistema por meio de um provedor WMI, a representação significa que o provedor apresenta as credenciais que representam o nível de segurança do cliente, em vez do provedor. A representação impede que um cliente obtenha acesso não autorizado às informações no sistema.

As seções a seguir são discutidas neste tópico:

-   [Registrando um provedor para representação](#registering-a-provider-for-impersonation)
-   [Definindo níveis de representação dentro de um provedor](#setting-impersonation-levels-within-a-provider)
-   [Mantendo níveis de segurança em um provedor](#maintaining-security-levels-in-a-provider)
-   [Manipulando mensagens de acesso negado em um provedor](#handling-access-denied-messages-in-a-provider)
-   [Relatórios de instâncias parciais](#reporting-partial-instances)
-   [Relatando enumerações parciais](#reporting-partial-enumerations)
-   [Depurando seu código de acesso negado](#debugging-your-access-denied-code)
-   [Tópicos relacionados](#related-topics)

Normalmente, o WMI é executado como um serviço administrativo em um nível de segurança alto, usando o contexto de segurança LocalServer. O uso de um serviço administrativo fornece ao WMI o meio de acessar informações privilegiadas. Ao chamar um provedor para obter informações, o WMI passa seu SID (identificador de segurança) para o provedor, permitindo que o provedor acesse as informações no mesmo nível de segurança alto.

Durante o processo de inicialização do aplicativo WMI, o sistema operacional Windows fornece ao aplicativo WMI o contexto de segurança do usuário que iniciou o processo. O contexto de segurança do usuário normalmente é um nível de segurança mais baixo do que LocalServer, portanto, o usuário pode não ter permissão para acessar todas as informações disponíveis para o WMI. Quando o aplicativo do usuário solicita informações dinâmicas, o WMI passa o SID do usuário para o provedor correspondente. Se for escrito adequadamente, o provedor tentará acessar informações com o SID do usuário, em vez do SID do provedor.

Para que o provedor represente com êxito o aplicativo cliente, o aplicativo cliente e o provedor devem atender aos seguintes critérios:

-   O aplicativo cliente deve chamar o WMI com um nível de segurança de conexão COM do destino de nível de **IMP do RPC \_ c \_ \_ \_** ou o delegado de nível de **IMP do RPC \_ c \_ \_ \_**. Para obter mais informações, consulte [mantendo a segurança do WMI](maintaining-wmi-security.md).
-   O provedor deve se registrar no WMI como um provedor de representação. Para obter mais informações, consulte [registrando um provedor para representação](#registering-a-provider-for-impersonation).
-   O provedor deve alternar para o nível de segurança do aplicativo cliente antes de acessar informações privilegiadas. Para obter mais informações, consulte [definindo níveis de representação em um provedor](#setting-impersonation-levels-within-a-provider).
-   O provedor deve lidar corretamente com condições de erro se o acesso a essas informações for negado. Para obter mais informações, consulte [manipulando mensagens de acesso negado em um provedor](#handling-access-denied-messages-in-a-provider).

## <a name="registering-a-provider-for-impersonation"></a>Registrando um provedor para representação

O WMI só passa o SID de um aplicativo cliente para provedores que se registraram como provedores de representação. A habilitação de um provedor para executar a representação requer que você modifique o processo de registro do provedor.

O procedimento a seguir descreve como registrar um provedor para representação. O procedimento pressupõe que você já entendeu o processo de registro. Para obter mais informações sobre o processo de registro, consulte [registrando um provedor](registering-a-provider.md).

**Para registrar um provedor para representação**

1.  Defina a propriedade [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) da classe [**\_ \_ Win32Provider**](--win32provider.md) que representa seu provedor como 1.

    A propriedade [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) documenta se o provedor oferece suporte à representação ou não. Definir **ImpersonationLevel** como 0 indica que o provedor não representa o cliente e executa todas as operações solicitadas no mesmo contexto de usuário que o WMI. Definir **ImpersonationLevel** como 1 indica que o provedor usa chamadas de representação para verificar as operações executadas em nome do cliente.

2.  Defina a propriedade **PerUserInitialization** da mesma classe [**\_ \_ Win32Provider**](--win32provider.md) como **true**.

> [!Note]  
> Se você registrar um provedor com a propriedade [**\_ \_ Win32Provider**](--win32provider.md) **InitializeAsAdminFirst** definida como **true**, o provedor usará o token de segurança de thread de nível de administração somente durante a fase de inicialização. Embora uma chamada para [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) não falhe, o provedor usa o contexto de segurança do WMI e não do cliente.

 

O exemplo de código a seguir mostra como registrar um provedor para representação.

``` syntax
instance of __Win32Provider
{
    CLSID = "{FD4F53E0-65DC-11d1-AB64-00C04FD9159E}";
    ImpersonationLevel = 1;
    Name = "MS_NT_EVENTLOG_PROVIDER";
    PerUserInitialization = TRUE;
};
```

## <a name="setting-impersonation-levels-within-a-provider"></a>Definindo níveis de representação dentro de um provedor

Se você registrar um provedor com a propriedade de classe [**\_ \_ Win32Provider**](--win32provider.md) [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) definida como 1, o WMI chamará seu provedor para representar vários clientes. Para lidar com essas chamadas, use as funções com [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) e [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) em sua implementação da interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .

A função [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) permite que um servidor represente o cliente que fez a chamada. Ao fazer uma chamada para **CoImpersonateClient** em sua implementação de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), você permite que seu provedor defina o token de thread do provedor para corresponder ao token de thread do cliente e, portanto, representa o cliente. Se você não chamar **CoImpersonateClient**, seu provedor executará o código em um nível de segurança de administrador, criando assim uma vulnerabilidade de segurança em potencial. Se o seu provedor precisar agir temporariamente como administrador ou executar a verificação de acesso manualmente, chame o [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself).

Em contraste com [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient), o [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) é uma função com que lida com os níveis de representação do thread. Nesse caso, o **CoRevertToSelf** altera o nível de representação de volta para a configuração de representação original. Em geral, o provedor é inicialmente um administrador e alterna entre **CoImpersonateClient** e **CoRevertToSelf** dependendo se ele está fazendo uma chamada que representa o chamador ou suas próprias chamadas. É responsabilidade do provedor fazer essas chamadas corretamente para não expor uma brecha de segurança para o usuário final. Por exemplo, o provedor deve chamar apenas funções nativas do Windows dentro da sequência de código representada.

> [!Note]  
> A finalidade de [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) e [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) é definir a segurança de um provedor. Se você determinar que sua representação falhou, deverá retornar um código de conclusão apropriado para WMI por meio de [**IWbemObjectSink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus). Para obter mais informações, consulte [manipulando mensagens de acesso negado em um provedor](#handling-access-denied-messages-in-a-provider).

 

## <a name="maintaining-security-levels-in-a-provider"></a>Mantendo níveis de segurança em um provedor

Os provedores não podem chamar [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) uma vez em uma implementação de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) e supõem que as credenciais de representação permaneçam em vigor durante o provedor. Em vez disso, chame **CoImpersonateClient** várias vezes durante o curso de uma implementação para impedir que o WMI altere as credenciais.

A principal preocupação de definir a representação de um provedor é a reentrância. Nesse contexto, a reentrância é quando um provedor faz uma chamada ao WMI para obter informações e aguarda até que o WMI chame de volta para o provedor. Em essência, o thread de execução deixa o código do provedor, apenas para reinserir o código em uma data posterior. A reentrada faz parte do design do COM e geralmente não é uma preocupação. No entanto, quando o thread de execução entra em WMI, o thread assume os níveis de representação do WMI. Quando o thread retorna ao provedor, você deve redefinir os níveis de representação com outra chamada para [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient).

Para se proteger de brechas de segurança em seu provedor, você deve fazer chamadas reentrantes no WMI somente ao mesmo tempo que representa o cliente. Ou seja, as chamadas para o WMI devem ser feitas depois que você chamar [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) e antes de chamar o [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself). Como o **CoRevertToSelf** faz com que a representação seja definida para o WMI de nível de usuário em execução, em geral, as chamadas reentrante para o WMI após chamar o **CoRevertToSelf** podem fornecer ao usuário e a todos os provedores chamados, muito mais recursos do que deveriam ter.

> [!Note]  
> Se você chamar uma função do sistema ou outro método de interface, não haverá garantia de que o contexto de chamada seja mantido.

 

## <a name="handling-access-denied-messages-in-a-provider"></a>Manipulando mensagens de acesso negado em um provedor

A maioria das mensagens de erro de acesso negado aparece quando um cliente solicita uma classe ou informações às quais eles não têm acesso. Se o provedor retornar uma mensagem de erro de acesso negado ao WMI e o WMI passarem por isso para o cliente, o cliente poderá inferir que as informações existem. Em algumas situações, isso pode ser uma violação de segurança. Portanto, o provedor não deve propagar a mensagem para o cliente. Em vez disso, o conjunto de classes que o provedor forneceu não deve ser exposto. Da mesma forma, um provedor de instância dinâmica deve chamar a fonte de dados subjacente para determinar como lidar com mensagens de acesso negado. É responsabilidade do provedor replicar essa filosofia no ambiente WMI. Para obter mais informações, consulte [relatar instâncias parciais](#reporting-partial-instances) e [relatar enumerações parciais](#reporting-partial-enumerations).

Ao determinar como seu provedor deve lidar com mensagens de acesso negado, você deve escrever e depurar seu código. Durante a depuração, geralmente é conveniente distinguir entre uma negação devido à baixa representação e a uma negação devido a um erro em seu código. Você pode usar um teste simples em seu código para determinar a diferença. Para obter mais informações, consulte [Depurando seu código de acesso negado](#debugging-your-access-denied-code).

## <a name="reporting-partial-instances"></a>Relatórios de instâncias parciais

Uma ocorrência comum de uma mensagem de acesso negado é quando o WMI não pode fornecer todas as informações para preencher uma instância. Por exemplo, um cliente pode ter autoridade para exibir um objeto de unidade de disco rígido, mas pode não ter autoridade para ver quanto espaço está disponível na própria unidade de disco rígido. Seu provedor deve determinar como lidar com qualquer situação quando o provedor não puder preencher completamente uma instância com propriedades devido a uma violação de acesso.

O WMI não requer uma única resposta para clientes que têm acesso parcial a uma instância. Em vez disso, o WMI versão 1. x permite ao provedor uma das seguintes opções:

-   Reprovar toda a operação com **acesso de WBEM e \_ \_ \_ negado** e não retornar nenhuma instância.

    Retornar um objeto de erro junto com o **WBEM \_ E \_ acesso \_ negado**, para descrever o motivo da negação.

-   Retornar todas as propriedades disponíveis e preencher as propriedades não disponíveis com **NULL**.

> [!Note]  
> Certifique-se de que o retorno de **WBEM \_ E \_ acesso \_ negado** não crie uma brecha de segurança em sua empresa.

 

## <a name="reporting-partial-enumerations"></a>Relatando enumerações parciais

Outra ocorrência comum de uma violação de acesso é quando o WMI não pode retornar todas as enumerações. Por exemplo, um cliente pode ter acesso para exibir todos os objetos de computador de rede local, mas pode não ter acesso para exibir objetos de computador fora do seu domínio. Seu provedor deve determinar como lidar com qualquer situação quando uma enumeração não puder ser concluída devido a uma violação de acesso.

Assim como com um provedor de instância, o WMI não requer uma única resposta a uma enumeração parcial. Em vez disso, o WMI versão 1. x permite que um provedor seja uma das seguintes opções:

-   Retornar **WBEM \_ S \_ sem \_ erro** para todas as instâncias que o provedor pode acessar.

    Se você usar essa opção, o usuário não saberá que algumas instâncias não estavam disponíveis. Vários provedores, como aqueles que usam o linguagem SQL (SQL) com segurança em nível de linha, retornam resultados parciais com êxito usando o nível de segurança do chamador para definir o conjunto de resultados.

-   Reprovar toda a operação com **acesso de WBEM e \_ \_ \_ negado** e não retornar nenhuma instância.

    O provedor pode opcionalmente incluir um objeto de erro que descreve a situação para o cliente. Observe que alguns provedores podem acessar fontes de dados em série e podem não encontrar negações até MSRC durante por meio da enumeração.

-   Retornar todas as instâncias que podem ser acessadas, mas também retornar o código de status não-erro **WBEM \_ \_ acesso \_ negado**.

    O provedor deve observar a negação durante a enumeração e pode continuar fornecendo instâncias, concluindo com o código de status não-erro. O provedor também pode optar por encerrar a enumeração na primeira negação. A justificativa para essa opção é que provedores diferentes têm paradigmas de recuperação diferentes. Um provedor pode já ter entregue instâncias antes de descobrir uma violação de acesso. Alguns provedores podem optar por continuar fornecendo outras instâncias e outras talvez queiram encerrar.

Devido à estrutura de COM, não é possível realizar marshaling de todas as informações durante um erro, exceto para um objeto de erro. Portanto, você não pode retornar as informações e um código de erro. Se você optar por retornar informações, deverá usar um código de status de não erro.

## <a name="debugging-your-access-denied-code"></a>Depurando seu código de acesso negado

Alguns aplicativos podem usar níveis de representação inferiores à representação de **nível de imp do RPC \_ \_ \_ \_ C**. Nesse caso, a maioria das chamadas de representação feitas pelo provedor para o aplicativo cliente falhará. Para projetar e implementar um provedor com êxito, você deve ter essa ideia em mente.

Por padrão, o único outro nível de representação que pode acessar um provedor é **a \_ \_ identificação do \_ nível \_ de imp do RPC C**. Nos casos em que um aplicativo cliente usa a **identificação de nível de Imp de RPC \_ C \_ \_ \_**, [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) não retorna um código de erro. Em vez disso, o provedor representa o cliente apenas para fins de identificação. Portanto, a maioria dos métodos do Windows chamados pelo provedor retornará uma mensagem de acesso negado. Isso é inofensivo na prática, pois os usuários não terão permissão para fazer nada inadequado. No entanto, pode ser útil durante o desenvolvimento do provedor saber se o cliente foi realmente representado ou não.

O código requer as referências a seguir e \# inclui instruções para compilar corretamente.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
```



O exemplo de código a seguir mostra como determinar se um provedor representou com êxito um aplicativo cliente.


```C++
DWORD dwImp = 0;
HANDLE hThreadTok;
DWORD dwBytesReturned;
BOOL bRes;

// You must call this before trying to open a thread token!
CoImpersonateClient();

bRes = OpenThreadToken(
    GetCurrentThread(),
    TOKEN_QUERY,
    TRUE,
    &hThreadTok
);

if (bRes == FALSE)
{
    printf("Unable to read thread token (%d)\n", GetLastError());
    return 0;
}

bRes = GetTokenInformation(
    hThreadTok,
    TokenImpersonationLevel, 
    &dwImp,
    sizeof(DWORD),
    &dwBytesReturned
);

if (!bRes)
{
    printf("Unable to read impersonation level\n");
    CloseHandle(hThreadTok);
    return 0;
}

switch (dwImp)
{
case SecurityAnonymous:
    printf("SecurityAnonymous\n");
    break;

case SecurityIdentification:
    printf("SecurityIdentification\n");
    break;

case SecurityImpersonation:
    printf("SecurityImpersonation\n");
    break;

case SecurityDelegation:
    printf("SecurityDelegation\n");
    break;

default:
    printf("Error. Unable to determine impersonation level\n");
    break;
}

CloseHandle(hThreadTok);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvendo um provedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Configurando descritores de segurança namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Protegendo seu provedor](securing-your-provider.md)
</dt> </dl>

 

 
