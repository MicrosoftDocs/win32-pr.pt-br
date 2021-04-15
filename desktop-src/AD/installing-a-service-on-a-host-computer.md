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
# <a name="installing-a-service-on-a-host-computer"></a><span data-ttu-id="3cfb6-103">Instalando um serviço em um computador host</span><span class="sxs-lookup"><span data-stu-id="3cfb6-103">Installing a Service on a Host Computer</span></span>

<span data-ttu-id="3cfb6-104">O exemplo de código a seguir mostra as etapas básicas de instalação de um serviço habilitado para diretório em um computador host.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-104">The following code example shows the basic steps of installing a directory-enabled service on a host computer.</span></span> <span data-ttu-id="3cfb6-105">Ele executa as seguintes operações:</span><span class="sxs-lookup"><span data-stu-id="3cfb6-105">It performs the following operations:</span></span>

1.  <span data-ttu-id="3cfb6-106">Chama a função [**OpenSCManager**](/windows/desktop/api/winsvc/nf-winsvc-openscmanagera) para abrir um identificador para o SCM (Gerenciador de controle de serviço) no computador local.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-106">Calls the [**OpenSCManager**](/windows/desktop/api/winsvc/nf-winsvc-openscmanagera) function to open a handle to the service control manager (SCM) on the local computer.</span></span>
2.  <span data-ttu-id="3cfb6-107">Chama a função [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) para instalar o serviço no banco de dados SCM.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-107">Calls the [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) function to install the service in the SCM database.</span></span> <span data-ttu-id="3cfb6-108">Essa chamada especifica a conta e a senha de logon do serviço, bem como o executável do serviço e outras informações sobre o serviço.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-108">This call specifies the service's logon account and password, as well as the service's executable and other information about the service.</span></span> <span data-ttu-id="3cfb6-109">O **CreateService** falhará se a conta de logon especificada for inválida.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-109">**CreateService** fails if the specified logon account is invalid.</span></span> <span data-ttu-id="3cfb6-110">No entanto, o **CreateService** não verifica a validade da senha.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-110">However, **CreateService** does not check the validity of the password.</span></span> <span data-ttu-id="3cfb6-111">Ele também não verifica se a conta tem o direito de logon como um serviço no computador local.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-111">It also does not verify that the account has the logon as a service right on the local computer.</span></span> <span data-ttu-id="3cfb6-112">Para obter mais informações, consulte [concedendo logon como serviço diretamente no computador host](granting-logon-as-service-right-on-the-host-computer.md).</span><span class="sxs-lookup"><span data-stu-id="3cfb6-112">For more information, see [Granting Logon as Service Right on the Host Computer](granting-logon-as-service-right-on-the-host-computer.md).</span></span>
3.  <span data-ttu-id="3cfb6-113">Chama a sub-rotina **ScpCreate** do serviço que cria um SCP (objeto de ponto de conexão de serviço) no diretório para publicar o local dessa instância do serviço.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-113">Calls the service's **ScpCreate** subroutine that creates a service connection point object (SCP) in the directory to publish the location of this instance of the service.</span></span> <span data-ttu-id="3cfb6-114">Para obter mais informações, consulte [como os clientes encontram e usam um ponto de conexão de serviço](how-clients-find-and-use-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="3cfb6-114">For more information, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span> <span data-ttu-id="3cfb6-115">Essa rotina também armazena as informações de associação do serviço no SCP, define uma ACE no SCP para que o serviço possa acessá-lo em tempo de execução, armazena em cache o nome distinto do SCP no registro local e retorna o nome distinto do novo SCP.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-115">This routine also stores the service's binding information in the SCP, sets an ACE on the SCP so the service can access it at run time, caches the distinguished name of the SCP in the local registry, and returns the distinguished name of the new SCP.</span></span>
4.  <span data-ttu-id="3cfb6-116">Chama a sub-rotina **SpnCompose** do serviço que usa a cadeia de caracteres de classe do serviço e o nome distinto do scp para compor um SPN (nome da entidade de serviço).</span><span class="sxs-lookup"><span data-stu-id="3cfb6-116">Calls the service's **SpnCompose** subroutine that uses the service's class string and the distinguished name of the SCP to compose a service principal name (SPN).</span></span> <span data-ttu-id="3cfb6-117">Para obter mais informações, consulte [redigindo os SPNs para um serviço com um SCP](composing-the-spns-for-a-service-with-an-scp.md).</span><span class="sxs-lookup"><span data-stu-id="3cfb6-117">For more information, see [Composing the SPNs for a Service with an SCP](composing-the-spns-for-a-service-with-an-scp.md).</span></span> <span data-ttu-id="3cfb6-118">O SPN identifica exclusivamente essa instância do serviço.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-118">The SPN uniquely identifies this instance of the service.</span></span>
5.  <span data-ttu-id="3cfb6-119">Chama a sub-rotina **SpnRegister** do serviço que registra o SPN no objeto de conta associado à conta de logon do serviço.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-119">Calls the service's **SpnRegister** subroutine that registers the SPN on the account object associated with service's logon account.</span></span> <span data-ttu-id="3cfb6-120">Para obter mais informações, consulte [registrando os SPNs para um serviço](registering-the-spns-for-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="3cfb6-120">For more information, see [Registering the SPNs for a Service](registering-the-spns-for-a-service.md).</span></span> <span data-ttu-id="3cfb6-121">O registro do SPN permite que os aplicativos cliente autentiquem o serviço.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-121">Registration of the SPN enables client applications to authenticate the service.</span></span>

<span data-ttu-id="3cfb6-122">Este exemplo de código funciona corretamente independentemente de a conta de logon ser uma conta de usuário local ou de domínio ou a conta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-122">This code example works correctly regardless of whether the logon account is a local or domain user account or the LocalSystem account.</span></span> <span data-ttu-id="3cfb6-123">Para uma conta de usuário de domínio, o parâmetro *szServiceAccountSAM* contém o nome de usuário de \*domínio \*\*\*\\*\*\*\* da conta e o parâmetro *szServiceAccountDN* contém o nome distinto do objeto de conta de usuário no diretório.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-123">For a domain user account, the *szServiceAccountSAM* parameter contains the *Domain ***\\*** UserName* name of the account, and the *szServiceAccountDN* parameter contains the distinguished name of the user account object in the directory.</span></span> <span data-ttu-id="3cfb6-124">Para a conta LocalSystem, *szServiceAccountSAM* e *szPassword* são **nulas** e *szServiceAccountSN* é o nome distinto do objeto de conta do computador local no diretório.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-124">For the LocalSystem account, *szServiceAccountSAM* and *szPassword* are **NULL**, and *szServiceAccountSN* is the distinguished name of the local computer's account object in the directory.</span></span> <span data-ttu-id="3cfb6-125">Se *szServiceAccountSAM* especificar uma conta de usuário local (o formato de nome é ". \\ *Username*"), o exemplo de código ignora o registro de SPN porque a autenticação mútua não tem suporte para contas de usuário local.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-125">If *szServiceAccountSAM* specifies a local user account (name format is ".\\*UserName*"), the code example skips the SPN registration because mutual authentication is not supported for local user accounts.</span></span>

<span data-ttu-id="3cfb6-126">Lembre-se de que a configuração de segurança padrão permite apenas que os administradores de domínio executem esse código.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-126">Be aware that the default security configuration allows only domain administrators to execute this code.</span></span>

<span data-ttu-id="3cfb6-127">Além disso, lembre-se de que esse exemplo de código, conforme escrito, deve ser executado no computador em que o serviço está sendo instalado.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-127">Also, be aware that this code example, as written, must be executed on the computer where the service is being installed.</span></span> <span data-ttu-id="3cfb6-128">Consequentemente, ele geralmente está em um executável de instalação separado do seu código de instalação do serviço, se houver, que estende o esquema, estende a interface do usuário ou configura a diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-128">Consequently, it is typically in a separate installation executable from your service installation code, if any, that extends the schema, extends the UI, or sets up group policy.</span></span> <span data-ttu-id="3cfb6-129">Essas operações instalam componentes de serviço para uma floresta inteira, enquanto esse código instala o serviço em um único computador.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-129">Those operations install service components for an entire a forest, whereas this code installs the service on a single computer.</span></span>


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



<span data-ttu-id="3cfb6-130">Para obter mais informações sobre o exemplo de código anterior, consulte [redigindo os SPNs para um serviço com um SCP](composing-the-spns-for-a-service-with-an-scp.md) e [registrando os SPNs para um serviço](registering-the-spns-for-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="3cfb6-130">For more information about the previous code example, see [Composing the SPNs for a Service with an SCP](composing-the-spns-for-a-service-with-an-scp.md) and [Registering the SPNs for a Service](registering-the-spns-for-a-service.md).</span></span>

 

 