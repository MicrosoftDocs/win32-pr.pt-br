---
description: A infraestrutura do VSS requer que os solicitantes VSS, como aplicativos de backup, possam funcionar como clientes COM e como um servidor.
ms.assetid: b01145c6-76ba-4a81-bca6-59c4ca488dac
title: Considerações de segurança para solicitantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e989793dbf5a5dd1fac3224cf6f06958564de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296651"
---
# <a name="security-considerations-for-requesters"></a>Considerações de segurança para solicitantes

A infraestrutura do VSS requer que os solicitantes VSS, como aplicativos de backup, possam funcionar como clientes COM e como um servidor.

Ao atuar como um servidor, um solicitante expõe um conjunto de interfaces de retorno de chamada COM que pode ser invocado a partir de processos externos (como gravadores ou o serviço VSS). Portanto, os solicitantes precisam gerenciar com segurança quais clientes COM são capazes de fazer chamadas COM de entrada em seu processo.

Da mesma forma, os solicitantes podem atuar como um cliente COM para as APIs COM fornecidas por um gravador VSS ou pelo serviço VSS. As configurações de segurança específicas do solicitante devem permitir chamadas COM de saída do solicitante para esses outros processos.

O mecanismo mais simples para gerenciar os problemas de segurança de um solicitante envolve a seleção adequada da conta de usuário sob a qual ele é executado.

Normalmente, um solicitante precisa ser executado sob um usuário que seja membro do grupo Administradores ou do grupo operadores de backup ou seja executado como a conta sistema local.

Por padrão, quando um solicitante estiver agindo como um cliente COM, se ele não for executado nessas contas, qualquer chamada COM será rejeitada automaticamente com **E \_ ACCESSDENIED**, sem até mesmo a implementação do método com.

## <a name="disabling-com-exception-handling"></a>Desabilitando a manipulação de exceção COM

Ao desenvolver um solicitante, defina o sinalizador COM COMGLB \_ exceção \_ não cercamento \_ manipular opções globais para desabilitar a manipulação de exceções com. É importante fazer isso porque a manipulação de exceção COM pode mascarar erros fatais em um aplicativo VSS. O erro mascarado pode deixar o processo em um estado instável e imprevisível, o que pode levar a corrupções e travamentos. Para obter mais informações sobre esse sinalizador, consulte [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).

## <a name="setting-requester-default-com-access-check-permission"></a>Definindo permissão de verificação de acesso COM COM padrão do solicitante

Os solicitantes precisam estar cientes de que, quando o processo atua como um servidor (por exemplo, permitindo que os gravadores modifiquem o documento de componentes de backup), eles devem permitir chamadas de entrada de outros participantes do VSS, como gravadores ou o serviço VSS.

No entanto, por padrão, um processo do Windows permitirá apenas clientes COM em execução na mesma sessão de logon (o SID próprio) ou em execução na conta sistema local. Esse é um problema potencial porque esses padrões não são adequados para a infraestrutura do VSS. Por exemplo, os gravadores podem ser executados como uma conta de usuário de "operador de backup" que não esteja na mesma sessão de logon que o processo do solicitante nem uma conta do sistema local.

Para lidar com esse tipo de problema, cada processo de servidor COM pode exercer mais controle sobre se um cliente RPC ou COM tem permissão para executar um método COM implementado pelo servidor (um solicitante, nesse caso), usando [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para definir uma "permissão de verificação de acesso com" padrão de todo o processo.

Os solicitantes podem fazer o seguinte explicitamente:

-   Permitir que todos os processos acessem para chamar o processo do solicitante.

    Essa opção pode ser adequada para a grande maioria dos solicitantes e é usada por outros servidores COM — por exemplo, todos os serviços do Windows baseados em SVCHOST já estão usando essa opção, assim como todos os serviços COM+ por padrão.

    Permitir que todos os processos executem chamadas COM de entrada não é necessariamente uma vulnerabilidade de segurança. Um solicitante atuando como um servidor COM, como todos os outros servidores COM, sempre retém a opção de autorizar seus clientes em cada método COM implementado em seu processo.

    Observe que os retornos de chamada COM internos implementados pelo VSS são protegidos por padrão.

    Para permitir que todos os processos acessem COM um solicitante, você pode passar um descritor de segurança **nulo** como o primeiro parâmetro de [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). (Observe que **CoInitializeSecurity** deve ser chamado no máximo uma vez para todo o processo. Consulte a documentação COM ou o MSDN para obter mais informações sobre as chamadas **CoInitializeSecurity** .)

    O exemplo de código a seguir mostra como um solicitante deve chamar [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) no Windows 8 e no windows Server 2012 e posterior para ser compatível com o VSS para compartilhamentos de arquivos remotos (RVSS):

    ``` syntax
    // Initialize COM security.
       hr = CoInitializeSecurity(
            NULL,                          //  PSECURITY_DESCRIPTOR         pSecDesc,
            -1,                            //  LONG                         cAuthSvc,
            NULL,                          //  SOLE_AUTHENTICATION_SERVICE *asAuthSvc,
            NULL,                          //  void                        *pReserved1,
            RPC_C_AUTHN_LEVEL_PKT_PRIVACY, //  DWORD                        dwAuthnLevel,
            RPC_C_IMP_LEVEL_IMPERSONATE,   //  DWORD                        dwImpLevel,
            NULL,                          //  void                        *pAuthList,
            EOAC_STATIC,                   //  DWORD                        dwCapabilities,
            NULL                           //  void                        *pReserved3
            );
    ```

    Ao definir explicitamente a segurança de nível COM de um solicitante com [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), você deve fazer o seguinte:

    -   Defina o nível de autenticação para pelo menos a **integridade de pkt do \_ nível de \_ autenticação \_ \_ \_ RPC C**. Para obter mais segurança, considere usar a **privacidade do PCT do \_ nível de \_ autenticação \_ \_ \_ RPC C**.
    -   Defina o nível de representação para a representação do **nível de imp do RPC \_ \_ \_ \_ C**.
    -   Defina os recursos de segurança de encobrimento como **\_ estático EOAC**. Para obter mais informações sobre a segurança de encobrimento, consulte [encobrindo](../com/cloaking.md).

    O exemplo de código a seguir mostra como um solicitante deve chamar [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) no Windows 7 e no windows Server 2008 R2 e versões anteriores (ou no Windows 8 e no windows Server 2012 e posteriores, se a compatibilidade do RVSS não for necessária):

    ``` syntax
    // Initialize COM security.
       hr = CoInitializeSecurity(
            NULL,                          //  PSECURITY_DESCRIPTOR         pSecDesc,
            -1,                            //  LONG                         cAuthSvc,
            NULL,                          //  SOLE_AUTHENTICATION_SERVICE *asAuthSvc,
            NULL,                          //  void                        *pReserved1,
            RPC_C_AUTHN_LEVEL_PKT_PRIVACY, //  DWORD                        dwAuthnLevel,
            RPC_C_IMP_LEVEL_IDENTIFY,      //  DWORD                        dwImpLevel,
            NULL,                          //  void                        *pAuthList,
            EOAC_NONE,                     //  DWORD                        dwCapabilities,
            NULL                           //  void                        *pReserved3
            );
    ```

    Ao definir explicitamente a segurança de nível COM de um solicitante com [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), você deve fazer o seguinte:

    -   Defina o nível de autenticação para pelo menos o **RPC \_ C \_ Authn \_ nível \_ Connect**. Para obter mais segurança, considere usar a **privacidade do PCT do \_ nível de \_ autenticação \_ \_ \_ RPC C**.
    -   Defina o nível de representação para o **nível de imp do RPC \_ C \_ \_ \_** , a menos que o processo do solicitante precise permitir a representação para chamadas RPC ou com específicas que não estejam relacionadas ao VSS.

-   Permitir que somente processos especificados acessem para chamar o processo do solicitante.

    Um servidor COM (como um solicitante) que está chamando [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) com um descritor de segurança não **nulo** como o primeiro parâmetro pode usar o descritor para se configurar para aceitar chamadas de entrada somente de usuários que pertencem a um conjunto específico de contas.

    Um solicitante deve garantir que clientes COM em execução em usuários válidos estejam autorizados a chamar seu processo. Um solicitante que especifica um descritor de segurança no primeiro parâmetro deve permitir que os seguintes usuários executem chamadas de entrada no processo do solicitante:

    -   Sistema Local
    -   Serviço Local

        **Windows XP:** Não há suporte para esse valor até o Windows Server 2003.

    -   Serviço de Rede

        **Windows XP:** Não há suporte para esse valor até o Windows Server 2003.

    -   Membros do grupo Administradores local
    -   Membros do grupo operadores de backup local
    -   Usuários especiais que são especificados no local do registro abaixo, com "1" como seu valor de REG \_ DWORD

## <a name="explicitly-controlling-user-account-access-to-a-requester"></a>Controlando explicitamente o acesso de conta de usuário a um solicitante

Há casos em que restringir o acesso a um solicitante para processos em execução como sistema local ou nos grupos Administradores locais ou operadores de backup locais pode ser muito restritivo.

Por exemplo, um processo de solicitante especificado pode, normalmente, não precisar ser executado em uma conta de administrador ou de operador de backup. Por motivos de segurança, seria melhor não promover artificialmente os privilégios de processos para dar suporte ao VSS.

Nesses casos, a chave de registro **HKEY \_ \_ local** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **VSS** \\ **VssAccessControl** deve ser modificada para instruir o VSS de que um usuário especificado é seguro para executar um solicitante VSS.

Sob essa chave, você deve criar uma subchave que tenha o mesmo nome que a conta que terá acesso concedido ou negado. Essa subchave deve ser definida como um dos valores na tabela a seguir.

| Valor | Significado                                             |
|-------|-----------------------------------------------------|
| 0     | Negue ao usuário acesso ao seu gravador e solicitante.  |
| 1     | Conceda ao usuário acesso ao seu gravador.               |
| 2     | Conceda ao usuário acesso ao solicitante.            |
| 3     | Conceda ao usuário acesso ao seu gravador e solicitante. |



 

O exemplo a seguir concede acesso à conta "mydomain \\ myuser":

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  MyDomain\MyUser = 2<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

Esse mecanismo também pode ser usado para restringir explicitamente um usuário permitido da execução de um solicitante VSS. O exemplo a seguir restringirá o acesso da conta "administrador do ThatDomain \\ ":

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  ThatDomain\Administrator = 0<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

O administrador do ThatDomain do usuário \\ não poderá executar um solicitante do VSS.

## <a name="performing-a-file-backup-of-the-system-state"></a>Executando um backup de arquivo do estado do sistema

Se um solicitante executar o backup de estado do sistema fazendo backup de arquivos individuais em vez de usar uma imagem de volume para o backup, ele deverá chamar as funções [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) e [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) para enumerar links físicos em arquivos localizados nos seguintes diretórios:

-   Perftrack do Windows \\ System32 \\ WDI \\\\
-   WINSXS do Windows \\\\

Esses diretórios só podem ser acessados por membros do grupo Administradores. Por esse motivo, esse solicitante deve ser executado na conta do sistema ou em uma conta de usuário que seja membro do grupo Administradores.

**Windows XP e Windows Server 2003:** As funções [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) e [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) não têm suporte até o Windows Vista e o Windows Server 2008.

 

 
