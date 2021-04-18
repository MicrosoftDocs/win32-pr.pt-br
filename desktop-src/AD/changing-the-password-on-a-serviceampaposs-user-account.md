---
title: Alterando a senha na conta de usuário de um serviço
description: Para uma instância de serviço que faz logon com uma conta de usuário, em vez da conta LocalSystem, o SCM (Gerenciador de controle de serviço) no computador host armazena a senha da conta, que é usada para fazer logon no serviço quando o serviço é iniciado.
ms.assetid: d9cef772-bd85-4103-901e-3cf786b29163
ms.tgt_platform: multiple
keywords:
- Alterando a senha no AD da conta de usuário de um serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf16b018796979d3710825472a5f9abab72cd24
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104453954"
---
# <a name="changing-the-password-on-a-services-user-account"></a>Alterando a senha na conta de usuário de um serviço

Para uma instância de serviço que faz logon com uma conta de usuário, em vez da conta LocalSystem, o SCM (Gerenciador de controle de serviço) no computador host armazena a senha da conta, que é usada para fazer logon no serviço quando o serviço é iniciado. Assim como ocorre com qualquer conta de usuário, você deve alterar a senha periodicamente para manter a segurança. Quando você alterar a senha em uma conta de serviço, atualize a senha armazenada pelo SCM. O exemplo de código a seguir mostra como fazer ambos.

Os exemplos de código usam [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) para definir a senha da conta. Esse método usa o nome distinto da conta. Em seguida, o exemplo abre um identificador para o serviço instalado no computador host especificado e usa a função [**ChangeServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga) para atualizar a senha armazenada em cache pelo SCM. Essa função usa o nome Sam (" <domain> \\ <username> ") da conta.

> [!Note]  
> Esse código deve ser executado por um administrador de domínio.

 

Para um serviço replicável no qual cada réplica usa uma conta de logon diferente, você pode atualizar as senhas de todas as réplicas enumerando as instâncias de serviço. Para obter mais informações e um exemplo de código, consulte [enumerando as réplicas de um serviço](enumerating-the-replicas-of-a-service.md).


```C++
DWORD UpdateAccountPassword(
    LPTSTR szServerDNS,   // DNS name of host computer
    LPTSTR szAccountDN,   // Distinguished name of service 
                          // logon account
    LPTSTR szServiceName, // Name of the service
    LPTSTR szOldPassword, // Old password
    LPTSTR szNewPassword  // New password
    )
{
SC_HANDLE schService = NULL;
SC_HANDLE schSCManager = NULL;
 
DWORD dwLen = MAX_PATH;
TCHAR szAccountPath[MAX_PATH];
IADsUser *pUser = NULL;
HRESULT hr;
 
DWORD dwStatus = 0;
SC_LOCK sclLock = NULL; 

if( !szServerDNS || 
    !szAccountDN || 
    !szServiceName || 
    !szOldPassword || 
    !szNewPassword)
{
    _tprintf(TEXT("Invalid parameter"));
    goto cleanup;
}
 
// Set the password on the account.
// Use the distinguished name to bind to the account object.
_tcsncpy_s(szAccountPath, TEXT("LDAP://"), MAX_PATH);
_tcscat_s(szAccountPath, 
    szAccountDN, 
    MAX_PATH - _tcslen(szAccountPath));
hr = ADsGetObject(szAccountPath, IID_IADsUser, (void**)&pUser);
if (FAILED(hr)) 
{
    _tprintf(TEXT("Get IADsUser failed - 0x%x\n"), dwStatus = hr);
       goto cleanup;
}
 
// Set the password on the account. 
hr = pUser->ChangePassword(CComBSTR(szOldPassword), 
    CComBSTR(szNewPassword));
if (FAILED(hr)) 
{
    _tprintf(TEXT("ChangePassword failed - 0x%x\n"), 
             dwStatus = hr);
    goto cleanup;
}
 
// Update the account and password in the SCM database.
// Open the Service Control Manager on the specified computer.
schSCManager = OpenSCManager(
                szServerDNS,          // DNS name of host computer
                NULL,                 // database (NULL == default)
                SC_MANAGER_ALL_ACCESS // access required
                        );
if (! schSCManager) 
{
    _tprintf(TEXT("OpenSCManager failed - %d\n"), 
        dwStatus = GetLastError());
    goto cleanup;
}
 
// Open a handle to the service instance.
schService = OpenService(schSCManager, 
    szServiceName, 
    SERVICE_ALL_ACCESS);
if (! schService) 
{
    _tprintf(TEXT("OpenService failed - %d\n"), 
        dwStatus = GetLastError());
    goto cleanup;
}
 
// Get the SCM database lock before changing the password. 
sclLock = LockServiceDatabase(schSCManager); 
if (sclLock == NULL) {
    _tprintf(TEXT("LockServiceDatabase failed - %d\n"), 
        dwStatus = GetLastError());
    goto cleanup;
}
 
// Set the account and password that the service uses at startup.
if (! ChangeServiceConfig( 
        schService,        // Handle of service 
        SERVICE_NO_CHANGE, // Service type: no change 
        SERVICE_NO_CHANGE, // Change service start type 
        SERVICE_NO_CHANGE, // Error control: no change 
        NULL,              // Binary path: no change 
        NULL,              // Load order group: no change 
        NULL,              // Tag ID: no change 
        NULL,              // Dependencies: no change 
        NULL,              // Account name: no change 
        szNewPassword,     // New password 
        NULL) )            // Display name: no change
{
    _tprintf(TEXT("ChangeServiceConfig failed - %d\n"), 
        dwStatus = GetLastError());
    goto cleanup;
}
_tprintf(TEXT("Password changed for service instance on: %s\n"), 
    szServerDNS);

cleanup:
 
if (sclLock)
    UnlockServiceDatabase(sclLock); 
if (schService)
    CloseServiceHandle(schService);
if (schSCManager)
    CloseServiceHandle(schSCManager);
if (pUser)
    pUser->Release();
 
return dwStatus;
}
```



 

 