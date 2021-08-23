---
description: 'No C++, você pode definir a segurança em todo o processo chamando CoInitializeSecurity antes de se conectar ao WMI por meio de IWbemLocator:: ConnectServer.'
ms.assetid: 83c04a96-3829-4c07-91a7-06e5b75b2c12
ms.tgt_platform: multiple
title: Definindo a segurança em IWbemServices e em outros proxies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da997b9d4a8f91cf31e8619af983209d4a07a571932c85304d372379d7f752b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050264"
---
# <a name="setting-the-security-on-iwbemservices-and-other-proxies"></a>Definindo a segurança em IWbemServices e em outros proxies

No C++, você pode definir a segurança em todo o processo chamando [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) antes de se conectar ao WMI por meio de [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver). Você também pode alterar o nível de autenticação, o nível de representação ou o serviço de autenticação em uma chamada que obtém um ponteiro para um proxy WMI, como [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) ou [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult). Chamar [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) também permite que você altere o serviço de autenticação (Kerberos, NTLM ou Negotiate).

Scripts e Visual Basic aplicativos apenas definem a segurança em proxies indiretamente por meio de chamadas para [**SWbemServices**](swbemservices.md) e outros objetos de automação. Para obter mais informações sobre como configurar e alterar a autenticação e a representação em script, consulte [definindo o nível de segurança do processo padrão usando o VBScript](setting-the-default-process-security-level-using-vbscript.md).

A alteração de níveis de segurança ou serviços é principalmente uma preocupação ao se conectar ao WMI em um computador remoto que esteja executando um sistema operacional diferente. Para obter mais informações, consulte [conectando entre diferentes sistemas operacionais](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).

Um aplicativo cliente se conecta a um proxy WMI usando uma identidade. Uma identidade é um objeto de dados que consiste em um nome de usuário, senha e configurações de autoridade. Para um aplicativo cliente WMI, a chamada para a interface [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) cria a identidade inicial. O método [**ConnectServer**](swbemlocator-connectserver.md) usa a identidade em um conjunto de três parâmetros, que você pode definir como **NULL** para indicar o usuário atual. Você também pode especificar um parâmetro não **nulo** para indicar um usuário e domínio específicos. se a chamada for bem-sucedida, **ConnectServer** retornará um ponteiro por meio do qual você pode acessar uma variedade de processos remotos, como um serviço WMI ou o sistema operacional Windows diretamente.

Como muitas interfaces COM, [**ConnectServer**](swbemlocator-connectserver.md) retorna um ponteiro para um proxy. Um proxy é um objeto de dados que representa um processo remoto, como WMI ou um provedor remoto. O COM usa um proxy para permitir que os desenvolvedores acessem dados remotos como se os dados fossem locais.

As seguintes interfaces WMI usam proxies:

-   [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) (objeto de script [**SWbemServices**](swbemservices.md) )
-   [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)
-   [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)
-   [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) (objeto de script [**SWbemRefresher**](swbemrefresher.md) )

    O atualizador WMI é um caso especial porque é passado para um ponteiro de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , cujas configurações de segurança devem ser definidas corretamente. Para obter mais informações sobre como usar objetos de atualizador, consulte [acessando dados de desempenho em C++](accessing-performance-data-in-c--.md).

Depois de receber um ponteiro para um processo remoto, você pode fazer uma das duas coisas. Se você souber o que o processo faz, poderá optar por definir a segurança no ponteiro e acessar o processo normalmente. Esse é o caso com a maioria dos ponteiros para um serviço WMI. Para obter mais informações, consulte [definindo os níveis de segurança em uma conexão WMI](setting-the-security-levels-on-a-wmi-connection.md). Como alternativa, você precisa acessar uma interface COM diferente no proxy, como [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release), por meio de uma chamada para a interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) no proxy.

## <a name="defaults-and-recommendations"></a>padrões e Recomendações

A versão distribuída do Component Object Model (DCOM) negocia o serviço de autenticação padrão (Kerberos, NTLM ou Negotiate) e você não pode especificar o serviço de autenticação padrão usando [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). A especificação do **\_ padrão RPC C \_ Authn \_** no parâmetro serviço de autenticação de [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) permite que o DCOM selecione o serviço apropriado. Para conexões remotas, o serviço padrão é Negotiate, que é o serviço recomendado para aplicativos que funcionam em domínios Kerberos e não Kerberos. Para conexões locais, o serviço de autenticação padrão é NT LAN Manager (NTLM).

O exemplo de código a seguir mostra o serviço de autenticação padrão que está sendo usado.


```C++
// The pWbemServices variable is of type IWbemServices*

HRESULT hr = CoSetProxyBlanket(
     pWbemServices,                //Proxy
     RPC_C_AUTHN_DEFAULT,          //Authentication service 
     RPC_C_AUTHZ_DEFAULT,          //Authorization service 
     COLE_DEFAULT_PRINCIPAL,       //Server principal name used 
                                       // by authentication service
     RPC_C_AUTHN_LEVEL_DEFAULT,    //Authentication level
     RPC_C_IMP_LEVEL_IMPERSONATE,  //Impersonation level
     COLE_DEFAULT_AUTHINFO,       //Client identity
     EOAC_DEFAULT                  //Capability flags
     );
```



O exemplo de código neste tópico requer a referência a seguir e as \# instruções include.


```C++
#define _WIN32_DCOM
#include <wbemidl.h>
#include <comdef.h>

#pragma comment(lib, "wbemuuid.lib")
```



Para scripts, é recomendável que você use os padrões que o DCOM seleciona para chamadas remotas. No computador local, você não pode especificar um serviço de autenticação para chamadas ao WMI. Para obter mais informações, consulte [definindo o serviço de autenticação usando o VBScript](setting-the-authentication-service-using-vbscript.md) e [construindo uma cadeia de caracteres de moniker](constructing-a-moniker-string.md).

 

 
