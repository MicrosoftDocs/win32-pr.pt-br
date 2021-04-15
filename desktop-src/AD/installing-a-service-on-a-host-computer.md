---
title: Instalando um serviço em um computador host
description: O exemplo de código a seguir mostra as etapas básicas de instalação de um serviço habilitado para diretório em um computador host.
ms.assetid: 35a3b261-d499-4154-a022-1e33a9ef7ba8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d687bbbfadb4d1ccb789e9d5f1051ebfbb4484d7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104453917"
---
# <a name="installing-a-service-on-a-host-computer"></a>Instalando um serviço em um computador host

O exemplo de código a seguir mostra as etapas básicas de instalação de um serviço habilitado para diretório em um computador host. Ele executa as seguintes operações:

1.  Chama a função [**OpenSCManager**](/windows/desktop/api/winsvc/nf-winsvc-openscmanagera) para abrir um identificador para o SCM (Gerenciador de controle de serviço) no computador local.
2.  Chama a função [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) para instalar o serviço no banco de dados SCM. Essa chamada especifica a conta e a senha de logon do serviço, bem como o executável do serviço e outras informações sobre o serviço. O **CreateService** falhará se a conta de logon especificada for inválida. No entanto, o **CreateService** não verifica a validade da senha. Ele também não verifica se a conta tem o direito de logon como um serviço no computador local. Para obter mais informações, consulte [concedendo logon como serviço diretamente no computador host](granting-logon-as-service-right-on-the-host-computer.md).
3.  Chama a sub-rotina **ScpCreate** do serviço que cria um SCP (objeto de ponto de conexão de serviço) no diretório para publicar o local dessa instância do serviço. Para obter mais informações, consulte [como os clientes encontram e usam um ponto de conexão de serviço](how-clients-find-and-use-a-service-connection-point.md). Essa rotina também armazena as informações de associação do serviço no SCP, define uma ACE no SCP para que o serviço possa acessá-lo em tempo de execução, armazena em cache o nome distinto do SCP no registro local e retorna o nome distinto do novo SCP.
4.  Chama a sub-rotina **SpnCompose** do serviço que usa a cadeia de caracteres de classe do serviço e o nome distinto do scp para compor um SPN (nome da entidade de serviço). Para obter mais informações, consulte [redigindo os SPNs para um serviço com um SCP](composing-the-spns-for-a-service-with-an-scp.md). O SPN identifica exclusivamente essa instância do serviço.
5.  Chama a sub-rotina **SpnRegister** do serviço que registra o SPN no objeto de conta associado à conta de logon do serviço. Para obter mais informações, consulte [registrando os SPNs para um serviço](registering-the-spns-for-a-service.md). O registro do SPN permite que os aplicativos cliente autentiquem o serviço.

Este exemplo de código funciona corretamente independentemente de a conta de logon ser uma conta de usuário local ou de domínio ou a conta LocalSystem. Para uma conta de usuário de domínio, o parâmetro *szServiceAccountSAM* contém o nome de usuário de *domínio ***\\**** da conta e o parâmetro *szServiceAccountDN* contém o nome distinto do objeto de conta de usuário no diretório. Para a conta LocalSystem, *szServiceAccountSAM* e *szPassword* são **nulas** e *szServiceAccountSN* é o nome distinto do objeto de conta do computador local no diretório. Se *szServiceAccountSAM* especificar uma conta de usuário local (o formato de nome é ". \\ *Username*"), o exemplo de código ignora o registro de SPN porque a autenticação mútua não tem suporte para contas de usuário local.

Lembre-se de que a configuração de segurança padrão permite apenas que os administradores de domínio executem esse código.

Além disso, lembre-se de que esse exemplo de código, conforme escrito, deve ser executado no computador em que o serviço está sendo instalado. Consequentemente, ele geralmente está em um executável de instalação separado do seu código de instalação do serviço, se houver, que estende o esquema, estende a interface do usuário ou configura a diretiva de grupo. Essas operações instalam componentes de serviço para uma floresta inteira, enquanto esse código instala o serviço em um único computador.


```C++
void InstallServiceOnLocalComputer(
            LPTSTR szServiceAccountDN,  // Distinguished name of logon account.
            LPTSTR szServiceAccountSAM, // SAM name of logon account.
            LPTSTR szPassword)          // Password of logon account.
{
SC_HANDLE   schService = NULL;
SC_HANDLE   schSCManager = NULL;
TCHAR szPath[512];
LPTSTR lpFilePart;
TCHAR szDNofSCP[MAX_PATH];
TCHAR szServiceClass[]=TEXT("ADSockAuth");
 
DWORD dwStatus;
TCHAR **pspn=NULL;
ULONG ulSpn=1;
 
// Get the full path of the service's executable.
// The code example assumes that the executable is in the current directory.
dwStatus = GetFullPathName(TEXT("service.exe"), 512, szPath, &lpFilePart);
if (dwStatus == 0) {
    _tprintf(TEXT("Unable to install %s - %s\n"), 
            TEXT(SZSERVICEDISPLAYNAME), GetLastErrorText(szErr, 256));
    return;
}
_tprintf(TEXT("path of service.exe: %s\n"), szPath);
 
// Open the Service Control Manager on the local computer.
schSCManager = OpenSCManager(
                NULL,                   // Computer (NULL == local)
                NULL,                   // Database (NULL == default)
                SC_MANAGER_ALL_ACCESS   // Access required
                );
if (! schSCManager) {
    _tprintf(TEXT("OpenSCManager failed - %s\n"), 
                   GetLastErrorText(szErr,256));
    goto cleanup;
}
        
// Install the service in the SCM database.
schService = CreateService(
            schSCManager,               // SCManager database
            TEXT(SZSERVICENAME),        // Name of service
            TEXT(SZSERVICEDISPLAYNAME), // Name to display
            SERVICE_ALL_ACCESS,         // Desired access
            SERVICE_WIN32_OWN_PROCESS,  // Service type
            SERVICE_DEMAND_START,       // Start type
            SERVICE_ERROR_NORMAL,       // Error control type
            szPath,                     // Service binary
            NULL,                       // No load ordering group
            NULL,                       // No tag identifier
            TEXT(SZDEPENDENCIES),       // Dependencies
            szServiceAccountSAM,        // Service account
            szPassword);                // Account password
if (! schService) {
    _tprintf(TEXT("CreateService failed - %s\n"), 
                   GetLastErrorText(szErr,256));
    goto cleanup;
}
 
_tprintf(TEXT("%s installed.\n"), TEXT(SZSERVICEDISPLAYNAME) );
 
// Create the service's Service Connection Point (SCP).
dwStatus = ScpCreate(
        2000,                 // Service default port number
        szServiceClass,       // Specifies the service class string
        szServiceAccountSAM,  // SAM name of logon account for ACE
        szDNofSCP             // Buffer returns the DN of the SCP
        );
if (dwStatus != 0) {
    _tprintf(TEXT("ScpCreate failed: %d\n"), dwStatus );
    DeleteService(schService);
    goto cleanup;
}
 
// Compose and register a service principal name for this service.
// This is performed on the install path because this requires elevated
// privileges for updating the directory.
// If a local account of the format ".\user name", skip the SPN.
if ( szServiceAccountSAM[0] == '.' ) 
{
    _tprintf(TEXT("Do not register SPN for a local account.\n"));
    goto cleanup;
}
 
dwStatus = SpnCompose(
        &pspn,            // Receives pointer to the SPN array.
        &ulSpn,           // Receives number of SPNs returned.
        szDNofSCP,        // Input: DN of the SCP.
        szServiceClass);  // Input: the service's class string.
 
if (dwStatus == NO_ERROR) 
    dwStatus = SpnRegister(
        szServiceAccountDN,  // Account on which SPNs are registered.
        pspn,                // Array of SPNs to register.
        ulSpn,               // Number of SPNs in array.
        DS_SPN_ADD_SPN_OP);  // Operation code: Add SPNs.
 
if (dwStatus != NO_ERROR) 
{
    _tprintf(TEXT("Failed to compose SPN: Error was %X\n"), 
                  dwStatus);
    DeleteService(schService);
    ScpDelete(szDNofSCP, szServiceClass, szServiceAccountDN);
    goto cleanup;
}
 
cleanup:
if (schSCManager)
    CloseServiceHandle(schSCManager);
if (schService)
    CloseServiceHandle(schService);
DsFreeSpnArray(ulSpn, pspn);
return;
}
```



Para obter mais informações sobre o exemplo de código anterior, consulte [redigindo os SPNs para um serviço com um SCP](composing-the-spns-for-a-service-with-an-scp.md) e [registrando os SPNs para um serviço](registering-the-spns-for-a-service.md).

 

 