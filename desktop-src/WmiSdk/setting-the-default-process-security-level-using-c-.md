---
description: Quando um aplicativo cliente faz logon no Instrumentação de Gerenciamento do Windows (WMI) pela primeira vez, ele deve definir o nível de segurança do processo padrão com uma chamada para CoInitializeSecurity.
ms.assetid: 4248fd1b-0867-40d8-8c9c-541156212df8
ms.tgt_platform: multiple
title: Definindo o nível de segurança do processo padrão usando C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33bb51deb2c228f0958209c774e7526b4eeed958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506221"
---
# <a name="setting-the-default-process-security-level-using-c"></a>Definindo o nível de segurança do processo padrão usando C++

Quando um aplicativo cliente faz logon no Instrumentação de Gerenciamento do Windows (WMI) pela primeira vez, ele deve definir o nível de segurança do processo padrão com uma chamada para [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). COM usa as informações na chamada para determinar a quantidade de segurança que outro processo deve ter para acessar o processo do aplicativo cliente.

As seções a seguir são discutidas neste tópico:

-   [Alterando as credenciais de autenticação padrão usando C++](#changing-the-default-authentication-credentials-using-c)
-   [Alterando os níveis de representação padrão usando C++](#changing-the-default-impersonation-levels-using-c)

Para a maioria dos aplicativos cliente, os argumentos mostrados no exemplo a seguir definem a segurança padrão para o WMI.


```C++
HRESULT hr = NULL;
hr = CoInitializeSecurity(
        NULL,                       // security descriptor
       -1,                          // use this simple setting
       NULL,                        // use this simple setting
       NULL,                        // reserved
       RPC_C_AUTHN_LEVEL_DEFAULT,   // authentication level  
       RPC_C_IMP_LEVEL_IMPERSONATE, // impersonation level
       NULL,                        // use this simple setting
       EOAC_NONE,                   // no special capabilities
       NULL);                          // reserved

if (FAILED(hr))
{
  CoUninitialize();
  cout << "Failed to initialize security. Error code = 0x"
       << hex << hr << endl;
  return;
}
```



O código requer as referências a seguir e \# inclui instruções para compilar corretamente.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")
```



Definir o nível de autenticação para o **\_ padrão de \_ \_ nível \_ da autenticação RPC C** permite que o DCOM negocie o nível de autenticação para corresponder às demandas de segurança do computador de destino. Para obter mais informações, consulte [alterando as credenciais de autenticação padrão usando c++](#changing-the-default-authentication-credentials-using-c) e [alterando as configurações de representação padrão usando c++](#changing-the-default-impersonation-levels-using-c).

## <a name="changing-the-default-authentication-credentials-using-c"></a>Alterando as credenciais de autenticação padrão usando C++

As credenciais de autenticação padrão funcionam para a maioria das situações, mas talvez seja necessário usar credenciais de autenticação diferentes em situações diferentes. Por exemplo, talvez você queira adicionar criptografia aos procedimentos de autenticação.

A tabela a seguir lista e descreve os diferentes níveis de autenticação.



| Nível de autenticação                 | Descrição                                                                           |
|--------------------------------------|---------------------------------------------------------------------------------------|
| \_padrão de \_ nível de autenticação RPC C \_ \_        | Autenticação de segurança padrão.                                                      |
| RPC \_ C \_ Authn \_ nível \_ nenhum           | Sem autenticação.                                                                    |
| \_conexão em \_ nível de autenticação RPC C \_ \_        | Autenticação somente quando o cliente cria uma relação com o servidor.           |
| \_chamada de \_ nível de autenticação RPC C \_ \_           | Autenticação toda vez que o servidor recebe um RPC.                                  |
| \_PCT do \_ nível de autenticação RPC C \_ \_            | Autenticação toda vez que o servidor recebe dados de um cliente.                      |
| \_integridade de \_ pkt do \_ nível \_ de \_ autenticação RPC C | Autenticação que nenhum dado do pacote foi modificado.                        |
| \_privacidade do \_ PCT do \_ nível \_ de \_ autenticação RPC C   | Inclui todos os níveis de autenticação anteriores e criptografa o valor de cada chamada RPC. |



 

Você pode especificar as credenciais de autenticação padrão para vários usuários usando uma estrutura de **\_ \_ lista de autenticação exclusiva** no parâmetro *pAuthList* de [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

O exemplo de código a seguir mostra como alterar as credenciais de autenticação.


```C++
// Auth Identity structure
SEC_WINNT_AUTH_IDENTITY_W        authidentity;
SecureZeroMemory( &authidentity, sizeof(authidentity) );

authidentity.User = L"MyUser";
authidentity.UserLength = wcslen( authidentity.User );
authidentity.Domain = L"MyDomain ";
authidentity.DomainLength = wcslen( authidentity.Domain );
authidentity.Password = L"";
authidentity.PasswordLength = wcslen( authidentity.Password );
authidentity.Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;

SecureZeroMemory( authninfo, sizeof(SOLE_AUTHENTICATION_INFO)*2 );

// NTLM Settings
authninfo[0].dwAuthnSvc = RPC_C_AUTHN_WINNT;
authninfo[0].dwAuthzSvc = RPC_C_AUTHZ_NONE;
authninfo[0].pAuthInfo = &authidentity;

// Kerberos Settings
authninfo[1].dwAuthnSvc = RPC_C_AUTHN_GSS_KERBEROS ;
authninfo[1].dwAuthzSvc = RPC_C_AUTHZ_NONE;
authninfo[1].pAuthInfo = &authidentity;

SOLE_AUTHENTICATION_LIST    authentlist;

authentlist.cAuthInfo = 2;
authentlist.aAuthInfo = authninfo;

CoInitializeSecurity( 
  NULL, 
  -1, 
  NULL, 
  NULL, 
  RPC_C_AUTHN_LEVEL_CALL, 
  RPC_C_IMP_LEVEL_IMPERSONATE,
  &authentlist, 
  EOAC_NONE,
  NULL);
```



## <a name="changing-the-default-impersonation-levels-using-c"></a>Alterando os níveis de representação padrão usando C++

O COM fornece níveis de segurança padrão lidos no registro do sistema. No entanto, a menos que seja especificamente modificado, as configurações do registro definem o nível de representação muito baixo para que o WMI funcione. Normalmente, o nível de representação padrão é a **identificação do nível de imp do RPC \_ c \_ \_ \_**, mas o WMI precisa de pelo menos a representação de **nível de imp do RPC \_ c \_ \_ \_** para funcionar com a maioria dos provedores, e você pode encontrar uma situação em que você precisa definir um nível mais alto de representação. Para obter mais informações, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md). A tabela a seguir lista os diferentes níveis de representação.



| Nível                           | Descrição                                                                                                   |
|---------------------------------|---------------------------------------------------------------------------------------------------------------|
| \_padrão de \_ nível de imp \_ \_ de RPC C     | O sistema operacional escolhe o nível de representação.                                                      |
| nível de imp do RPC \_ C- \_ \_ \_ anônimo   | O servidor pode representar o cliente, mas o token de representação não pode ser usado para nada.               |
| \_identificação de \_ nível de imp \_ \_ de RPC C    | O servidor pode obter a identidade do cliente e representar o cliente para verificação de ACL.                 |
| \_representação de \_ nível de imp \_ \_ do RPC C | O servidor pode representar o cliente em um limite de computador.                                           |
| \_delegado de \_ nível de imp \_ \_ de RPC C    | O servidor pode representar o cliente entre vários limites e pode fazer chamadas em nome do cliente. |



 

 

 
