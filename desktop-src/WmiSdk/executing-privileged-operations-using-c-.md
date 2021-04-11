---
description: Aplicativos cliente especiais podem invocar operações privilegiadas.
ms.assetid: e09fcadc-282f-4f07-b69c-b15bfdb07a7d
ms.tgt_platform: multiple
title: Executando operações privilegiadas usando C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fbc0468fef7531586020f55032bff94c977c4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296632"
---
# <a name="executing-privileged-operations-using-c"></a>Executando operações privilegiadas usando C++

Aplicativos cliente especiais podem invocar operações privilegiadas. Por exemplo, um aplicativo pode permitir que um gerente reinicie um computador do Office sem resposta. Usando o Instrumentação de Gerenciamento do Windows (WMI), você pode executar uma operação privilegiada chamando o provedor WMI para a operação privilegiada.

O procedimento a seguir descreve como chamar um provedor para uma operação privilegiada.

**Para chamar um provedor para uma operação privilegiada**

1.  Obtenha permissões para o processo do cliente para executar a operação privilegiada.

    Normalmente, um administrador define as permissões usando as ferramentas administrativas do sistema — antes de executar o processo.

2.  Obtenha a permissão para o processo do provedor para habilitar a operação privilegiada.

    Normalmente, você pode definir permissões de provedor com uma chamada para a função [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) .

3.  Obtenha a permissão para o processo do cliente para habilitar a operação privilegiada.

    Essa etapa será necessária apenas se o provedor for local para o cliente. Se o cliente e o provedor existirem no mesmo computador, o cliente deverá habilitar especificamente a operação privilegiada usando uma das seguintes técnicas:

    -   Se o cliente possuir o processo, o cliente poderá usar [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) para ajustar o token de processo antes de chamar o WMI. Nesse caso, você não precisa mais codificar.
    -   Se o cliente não puder acessar o token do cliente, o cliente poderá usar o procedimento a seguir para criar um token de thread e usar [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) nesse token.

O procedimento a seguir descreve como criar um token de thread e usar [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) nesse token.

**Para criar um token de thread e usar AdjustTokenPrivileges nesse token**

1.  Crie uma cópia do token de processo chamando [**ImpersonateSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateself).
2.  Recupere o token de thread recém-criado chamando [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation).
3.  Habilite a operação privilegiada com uma chamada para [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) no novo token.
4.  Obtenha um ponteiro para [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices).
5.  Encobrir o ponteiro para [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) com uma chamada para [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).
6.  Repita as etapas 1 a 5 em cada chamada para o WMI.

    > [!Note]  
    > Você deve repetir as etapas porque o COM armazena os tokens em cache incorretamente.

     

O exemplo de código neste tópico requer a seguinte \# instrução include para compilação correta.


```C++
#include <wbemidl.h>
```



O exemplo de código a seguir mostra como habilitar privilégios em um computador local.


```C++
// Get the privileges 
// The token has been obtained outside the scope of this code sample
// ================== 
DWORD dwLen;
bool bRes;
HANDLE hToken;

// obtain dwLen
bRes = GetTokenInformation(
  hToken, 
  TokenPrivileges, 
  NULL, 
  0,
  &dwLen
); 

BYTE* pBuffer = new BYTE[dwLen];
if(pBuffer == NULL)
{
  CloseHandle(hToken);
  return WBEM_E_OUT_OF_MEMORY;
} 

bRes = GetTokenInformation(
  hToken, 
  TokenPrivileges, 
  pBuffer,     
  dwLen,        
  &dwLen
);

if (!bRes)
{
  CloseHandle(hToken);
  delete [] pBuffer;
  return WBEM_E_ACCESS_DENIED;
} 

// Iterate through all the privileges and enable them all
// ====================================================== 
TOKEN_PRIVILEGES* pPrivs = (TOKEN_PRIVILEGES*)pBuffer;
for (DWORD i = 0; i < pPrivs->PrivilegeCount; i++)
{
  pPrivs->Privileges[i].Attributes |= SE_PRIVILEGE_ENABLED;
} 
// Store the information back in the token
// ========================================= 
bRes = AdjustTokenPrivileges(
  hToken, 
  FALSE, 
  pPrivs, 
  0, NULL, NULL
);

delete [] pBuffer;
CloseHandle(hToken); 

if (!bRes)
  return WBEM_E_ACCESS_DENIED;
else
  return WBEM_S_NO_ERROR;
```



 

 
