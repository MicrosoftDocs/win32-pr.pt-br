---
description: Quando um aplicativo cliente faz logon no WMI (Instrumentação de Gerenciamento de Windows) pela primeira vez, ele deve definir o nível de segurança do processo padrão com uma chamada para CoInitializeSecurity.
ms.assetid: 4248fd1b-0867-40d8-8c9c-541156212df8
ms.tgt_platform: multiple
title: Definindo o nível de segurança do processo padrão usando C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcaec4ebbcd39c8cee9ee8aae002621a4a5a1853d1e4cfd4282194115c15ce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050284"
---
# <a name="setting-the-default-process-security-level-using-c"></a>Definindo o nível de segurança do processo padrão usando C++

Quando um aplicativo cliente faz logon no WMI (Instrumentação de Gerenciamento de Windows) pela primeira vez, ele deve definir o nível de segurança do processo padrão com uma chamada para [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). O COM usa as informações na chamada para determinar a segurança que outro processo deve ter para acessar o processo do aplicativo cliente.

As seções a seguir são discutidas neste tópico:

-   [Alterando as credenciais de autenticação padrão usando C++](#changing-the-default-authentication-credentials-using-c)
-   [Alterando os níveis de representação padrão usando C++](#changing-the-default-impersonation-levels-using-c)

Para a maioria dos aplicativos cliente, os argumentos mostrados no exemplo a seguir configuram a segurança padrão para WMI.


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



O código requer as seguintes referências e instruções \# include para compilar corretamente.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")
```



Definir o nível de autenticação como **RPC \_ C \_ AUTHN \_ LEVEL \_ DEFAULT** permite que o DCOM negocie o nível de autenticação para corresponder às demandas de segurança do computador de destino. Para obter mais informações, consulte Alterando as credenciais de autenticação padrão usando [C++](#changing-the-default-authentication-credentials-using-c) e Alterando a representação padrão Configurações [usando C++.](#changing-the-default-impersonation-levels-using-c)

## <a name="changing-the-default-authentication-credentials-using-c"></a>Alterando as credenciais de autenticação padrão usando C++

As credenciais de autenticação padrão funcionam para a maioria das situações, mas talvez seja necessário usar credenciais de autenticação diferentes em situações diferentes. Por exemplo, talvez você queira adicionar criptografia aos procedimentos de autenticação.

A tabela a seguir lista e descreve os diferentes níveis de autenticação.



| Nível de autenticação                 | Descrição                                                                           |
|--------------------------------------|---------------------------------------------------------------------------------------|
| RPC \_ C \_ AUTHN \_ LEVEL \_ DEFAULT        | Autenticação de segurança padrão.                                                      |
| RPC \_ C \_ AUTHN \_ LEVEL \_ NONE           | Sem autenticação.                                                                    |
| RPC \_ C \_ AUTHN \_ LEVEL \_ CONNECT        | Autenticação somente quando o cliente cria uma relação com o servidor.           |
| RPC C CHAMADA DE NÍVEL \_ \_ AUTHN \_ \_           | Autenticação sempre que o servidor recebe um RPC.                                  |
| RPC \_ C \_ AUTHN \_ LEVEL \_ PKT            | Autenticação sempre que o servidor recebe dados de um cliente.                      |
| INTEGRIDADE \_ PKT NO NÍVEL DE \_ AUTHN \_ \_ RPC C \_ | Autenticação de que nenhum dado do pacote foi modificado.                        |
| RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY   | Inclui todos os níveis de autenticação anteriores e criptografa o valor de cada chamada RPC. |



 

Você pode especificar as credenciais de autenticação padrão para vários usuários usando uma estrutura **SOLE \_ AUTHENTICATION \_ LIST** no parâmetro *pAuthList* de [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

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

O COM fornece níveis de segurança padrão lidos do registro do sistema. No entanto, a menos que especificamente modificadas, as configurações do Registro definirão o nível de representação muito baixo para que o WMI funcione. Normalmente, o nível de representação padrão é **RPC \_ C IMP LEVEL \_ \_ \_ IDENTIFY**, mas o WMI precisa de pelo menos **RPC C IMP LEVEL \_ \_ \_ \_ IMPERSONATE** para funcionar com a maioria dos provedores, e você pode encontrar uma situação em que você precisa definir um nível mais alto de representação. Para obter mais informações, [consulte Conectando-se ao WMI em um computador remoto.](connecting-to-wmi-on-a-remote-computer.md) A tabela a seguir lista os diferentes níveis de representação.



| Nível                           | Descrição                                                                                                   |
|---------------------------------|---------------------------------------------------------------------------------------------------------------|
| RPC \_ C \_ IMP \_ LEVEL \_ DEFAULT     | O sistema operacional escolhe o nível de representação.                                                      |
| RPC \_ C \_ IMP \_ LEVEL \_ ANONYMOUS   | O servidor pode representar o cliente, mas o token de representação não pode ser usado para nada.               |
| RPC \_ C \_ IMP \_ LEVEL \_ IDENTIFY    | O servidor pode obter a identidade do cliente e representar o cliente para verificação de ACL.                 |
| REPRESENTAÇÃO NO NÍVEL DE IMP DO RPC \_ C \_ \_ \_ | O servidor pode representar o cliente em um limite de computador.                                           |
| DELEGADO DE NÍVEL DE IMP DO RPC \_ C \_ \_ \_    | O servidor pode representar o cliente em vários limites e pode fazer chamadas em nome do cliente. |



 

 

 
