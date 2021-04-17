---
description: A infraestrutura do VSS requer que os processos de gravação sejam capazes de funcionar como clientes COM e como servidores.
ms.assetid: 59bb7a86-e874-45ce-abd6-cafd18802c4d
title: Considerações de segurança para gravadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea6f88243adbd62d928170a86ed57b91cbebe134
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770544"
---
# <a name="security-considerations-for-writers"></a>Considerações de segurança para gravadores

A infraestrutura do VSS requer que os processos de gravação sejam capazes de funcionar como clientes COM e como servidores.

Ao atuar como servidores, gravadores VSS expõem interfaces COM (por exemplo, os manipuladores de eventos do VSS, como [**CVssWriter:: Onidentificate**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)) e recebem chamadas de entrada com de processos VSS (como solicitantes e o serviço VSS) ou chamadas RPC de processos que são externos ao VSS, geralmente quando esses processos geram eventos VSS (por exemplo, quando um solicitante chama [**IVssBackupComponents:**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) Portanto, um gravador VSS precisa gerenciar com segurança quais clientes COM são capazes de fazer chamadas COM de entrada em seu processo.

Da mesma forma, os gravadores VSS também podem atuar como clientes COM, fazendo chamadas COM de saída COM para os retornos de chamada fornecidos pela infraestrutura do VSS ou chamadas RPC para processos que são externos ao VSS. Esses retornos de chamada que são fornecidos por um aplicativo de backup ou pelo serviço VSS permitem que o gravador Execute tarefas como atualizar o documento de componentes de backup por meio da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) . Portanto, as configurações de segurança do VSS devem permitir que os gravadores façam chamadas COM de saída em outros processos VSS.

O mecanismo mais simples para gerenciar problemas de segurança do gravador envolve a seleção adequada da conta de usuário sob a qual ele é executado. Normalmente, um gravador precisa ser executado sob um usuário que seja membro do grupo Administradores ou do grupo operadores de backup ou que ele precise ser executado como a conta sistema local.

Por padrão, quando um gravador está agindo como um cliente COM, se ele não for executado nessas contas, qualquer chamada COM ele será rejeitada automaticamente com **E \_ ACCESSDENIED** sem até mesmo chegar à implementação do método com.

## <a name="disabling-com-exception-handling"></a>Desabilitando a manipulação de exceção COM

Ao desenvolver um gravador, defina o sinalizador COM COMGLB \_ exceção \_ não cercamento \_ manipular opções globais para desabilitar a manipulação de exceções com. É importante fazer isso porque a manipulação de exceção COM pode mascarar erros fatais em um aplicativo VSS. O erro mascarado pode deixar o processo em um estado instável e imprevisível, o que pode levar a corrupções e travamentos. Para obter mais informações sobre esse sinalizador, consulte [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).

## <a name="setting-writer-default-com-access-check-permission"></a>Definindo a permissão de verificação de acesso COM padrão do gravador

Os gravadores precisam estar cientes de que, quando seus processos atuam como um servidor (por exemplo, para manipular eventos VSS), eles devem permitir chamadas de entrada de outros participantes do VSS, como solicitantes ou o serviço VSS.

No entanto, por padrão, um processo permitirá apenas clientes COM que estão em execução na mesma sessão de logon, o SID próprio) ou em execução na conta sistema local. Esse é um problema potencial porque esses padrões não são suficientes para dar suporte à infraestrutura do VSS. Por exemplo, os solicitantes podem ser executados como uma conta de usuário de "operador de backup" que não esteja na mesma sessão de logon que o processo do gravador nem em uma conta do sistema local.

Para lidar com esse tipo de problema, cada processo de servidor COM pode exercer mais controle sobre se um cliente RPC ou COM tem permissão para executar um método COM no qual o servidor (um gravador, nesse caso) implementa, usando [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para definir uma permissão de verificação de acesso com em todo o processo.

Os gravadores podem fazer o seguinte explicitamente:

-   Permitir que todos os processos acessem para chamar o processo do gravador.

    Essa opção pode ser adequada para muitos gravadores e é usada por outros servidores COM — por exemplo, todos os serviços do Windows baseados em SVCHOST já estão usando essa opção, assim como todos os serviços COM+ por padrão.

    Permitir que todos os processos executem chamadas COM de entrada não é necessariamente uma vulnerabilidade de segurança. Um gravador agindo como um servidor COM, como todos os outros servidores COM, sempre retém a opção de autorizar seus clientes em cada método COM implementado em seu processo.

    Para permitir que todos os processos COM acesso a um gravador, você pode passar um descritor de segurança **nulo** como o primeiro parâmetro de [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). (Observe que **CoInitializeSecurity** deve ser chamado no máximo uma vez para todo o processo. Consulte a documentação COM para obter mais detalhes sobre **CoInitializeSecurity**.)

    Veja a seguir um exemplo de código que inclui uma chamada para [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity):

    ``` syntax
    // Initialize COM security.
    hr = CoInitializeSecurity(
           NULL,                          // PSECURITY_DESCRIPTOR          pSecDesc,
           -1,                            // LONG                          cAuthSvc,
           NULL,                          // SOLE_AUTHENTICATION_SERVICE  *asAuthSvc,
           NULL,                          // void                         *pReserved1,
           RPC_C_AUTHN_LEVEL_PKT_PRIVACY, // DWORD                         dwAuthnLevel,
           RPC_C_IMP_LEVEL_IDENTIFY,      // DWORD                         dwImpLevel,
           NULL,                          // void                         *pAuthList,
           EOAC_NONE,                     // DWORD                         dwCapabilities,
           NULL                           // void                         *pReserved3
        );
    ```

    Ao definir explicitamente a segurança de nível de COM de um gravador com [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), você deve fazer o seguinte:

    -   Defina o nível de autenticação para pelo menos o **RPC \_ C \_ Authn \_ nível \_ Connect**.

        Para obter mais segurança, considere usar a **privacidade do PCT do \_ nível de \_ autenticação \_ \_ \_ RPC C**.

    -   Defina o nível de representação para o **nível de imp do RPC \_ C \_ \_ \_** , a menos que o processo do gravador precise permitir a representação de chamadas RPC ou com específicas que não estejam relacionadas ao VSS.

-   Permitir que somente processos especificados acessem para chamar o processo do gravador.

    Um servidor COM (como um gravador) que está chamando [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) com um descritor de segurança não **nulo** pode usar o descritor para se configurar para aceitar chamadas de entrada somente de usuários que pertencem a um conjunto específico de contas.

    Um gravador deve garantir que clientes COM em execução em usuários válidos estejam autorizados a chamar seu processo. Um gravador que especifica um descritor de segurança no primeiro parâmetro deve permitir que os seguintes usuários executem chamadas de entrada no processo do solicitante:

    -   Sistema Local
    -   Membros do grupo Administradores local
    -   Membros do grupo operadores de backup local
    -   A conta sob a qual o gravador está sendo executado

## <a name="explicitly-controlling-user-account-access-to-a-writer"></a>Controlando explicitamente o acesso de conta de usuário a um gravador

Há casos em que restringir o acesso a um gravador para processos em execução como sistema local ou nos grupos locais de administradores locais ou de operadores de backup locais pode ser muito restritivo.

Por exemplo, um processo de gravação (talvez um gravador que não seja de sistema) pode, normalmente, ser executado em uma conta de administrador ou de operador de backup. Por motivos de segurança, seria melhor não promover artificialmente os privilégios do processo para dar suporte ao VSS.

Nesses casos, a chave de registro **HKEY \_ local \_** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **VSS** \\ **VssAccessControl** deve ser modificada para instruir o VSS de que um usuário especificado é seguro para executar um gravador VSS.

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
                  MyDomain\MyUser = 1<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

Esse mecanismo também pode ser usado para restringir explicitamente um usuário permitido da execução de um gravador VSS. O exemplo a seguir restringirá o acesso da conta "administrador do ThatDomain \\ ":

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

O administrador do ThatDomain do usuário \\ não poderá executar um gravador VSS.

 

 
