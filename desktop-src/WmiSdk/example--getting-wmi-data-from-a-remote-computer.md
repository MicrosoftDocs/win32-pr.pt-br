---
description: Você pode usar os exemplos de procedimento e código neste tópico para criar um aplicativo cliente WMI completo que executa inicialização COM, conecta-se ao WMI em um computador remoto, obtém dados semisynchronously e, em seguida, limpa.
ms.assetid: 30e65b9e-9372-46d1-843a-bda0d6ec1c69
ms.tgt_platform: multiple
title: 'Exemplo: obtendo dados WMI de um computador remoto'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c3375bd25073defa92358f697ee4165ddb57793
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811601"
---
# <a name="example-getting-wmi-data-from-a-remote-computer"></a><span data-ttu-id="0b05e-103">Exemplo: obtendo dados WMI de um computador remoto</span><span class="sxs-lookup"><span data-stu-id="0b05e-103">Example: Getting WMI Data from a Remote Computer</span></span>

<span data-ttu-id="0b05e-104">Você pode usar os exemplos de procedimento e código neste tópico para criar um aplicativo cliente WMI completo que executa inicialização COM, conecta-se ao WMI em um computador remoto, obtém dados semisynchronously e, em seguida, limpa.</span><span class="sxs-lookup"><span data-stu-id="0b05e-104">You can use the procedure and code examples in this topic to create a complete WMI client application that performs COM initialization, connects to WMI on a remote computer, gets data semisynchronously, and then cleans up.</span></span> <span data-ttu-id="0b05e-105">Para obter mais informações sobre como obter dados do computador local, consulte [exemplo: obtendo dados WMI do computador local](example--getting-wmi-data-from-the-local-computer.md).</span><span class="sxs-lookup"><span data-stu-id="0b05e-105">For more information about how to get data from the local computer, see [Example: Getting WMI Data from the Local Computer](example--getting-wmi-data-from-the-local-computer.md).</span></span> <span data-ttu-id="0b05e-106">Para obter mais informações sobre como obter os dados de forma assíncrona, consulte [exemplo: obtendo dados do WMI do computador local de forma assíncrona](example--getting-wmi-data-from-the-local-computer-asynchronously.md).</span><span class="sxs-lookup"><span data-stu-id="0b05e-106">For more information about how to get the data asynchronously, see [Example: Getting WMI Data from the Local Computer Asynchronously](example--getting-wmi-data-from-the-local-computer-asynchronously.md).</span></span>

> [!Note]  
> <span data-ttu-id="0b05e-107">Se você estiver tentando se conectar a um computador remoto, consulte as informações em[conectando-se ao WMI remotamente](connecting-to-wmi-remotely-starting-with-vista.md).</span><span class="sxs-lookup"><span data-stu-id="0b05e-107">If you are trying to connect to a remote computer refer to the information in[Connecting to WMI Remotely](connecting-to-wmi-remotely-starting-with-vista.md).</span></span>

 

<span data-ttu-id="0b05e-108">O procedimento a seguir mostra como executar o aplicativo WMI.</span><span class="sxs-lookup"><span data-stu-id="0b05e-108">The following procedure shows how to execute the WMI application.</span></span> <span data-ttu-id="0b05e-109">As etapas de 1 a 5 contêm todas as etapas necessárias para configurar e conectar-se ao WMI, e as etapas 6 e 7 são onde os dados são consultados e recebidos.</span><span class="sxs-lookup"><span data-stu-id="0b05e-109">Steps 1 through 5 contain all of the steps required to set up and connect to WMI, and steps 6 and 7 are where data is queried and received.</span></span>

<span data-ttu-id="0b05e-110">**Para obter dados WMI de um computador remoto**</span><span class="sxs-lookup"><span data-stu-id="0b05e-110">**To get WMI data from a remote computer**</span></span>

1.  <span data-ttu-id="0b05e-111">Inicialize parâmetros COM com uma chamada para [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="0b05e-111">Initialize COM parameters with a call to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    <span data-ttu-id="0b05e-112">Para obter mais informações, consulte [Inicializando com para um aplicativo WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="0b05e-112">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

2.  <span data-ttu-id="0b05e-113">Inicialize a segurança do processo COM chamando [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="0b05e-113">Initialize COM process security by calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

    <span data-ttu-id="0b05e-114">Para obter mais informações, consulte [definindo o nível de segurança do processo padrão usando C++](setting-the-default-process-security-level-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="0b05e-114">For more information, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md).</span></span>

3.  <span data-ttu-id="0b05e-115">Obtenha o localizador inicial para o WMI chamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="0b05e-115">Obtain the initial locator to WMI by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="0b05e-116">Para obter mais informações, consulte [criando uma conexão com um namespace do WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="0b05e-116">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

4.  <span data-ttu-id="0b05e-117">Obtenha um ponteiro para [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para o \\ \\ \\ namespace raiz cimv2 em um computador remoto chamando [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="0b05e-117">Obtain a pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) for the \\\\root\\cimv2 namespace on a remote computer by calling [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="0b05e-118">Ao se conectar a um computador remoto, você precisa saber o nome do computador, o domínio, o nome de usuário e a senha do computador remoto ao qual você está se conectando.</span><span class="sxs-lookup"><span data-stu-id="0b05e-118">When connecting to a remote computer, you need to know the computer name, domain, user name, and password of the remote computer you are connecting to.</span></span> <span data-ttu-id="0b05e-119">Esses atributos são todos passados para o método **IWbemLocator:: ConnectServer** .</span><span class="sxs-lookup"><span data-stu-id="0b05e-119">These attributes are all passed into the **IWbemLocator::ConnectServer** method.</span></span> <span data-ttu-id="0b05e-120">Além disso, verifique se o nome de usuário no computador que está tentando se conectar ao computador remoto tem os privilégios de acesso corretos no computador remoto.</span><span class="sxs-lookup"><span data-stu-id="0b05e-120">Also, ensure the user name on the computer that is trying to connect to the remote computer has the correct access privileges on the remote computer.</span></span> <span data-ttu-id="0b05e-121">Para obter mais informações, consulte [conectando por meio do firewall do Windows](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span><span class="sxs-lookup"><span data-stu-id="0b05e-121">For more information, see [Connecting Through Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span></span> <span data-ttu-id="0b05e-122">Para se conectar ao computador local, consulte [exemplo: obtendo dados do WMI do computador local](example--getting-wmi-data-from-the-local-computer.md) e [criando uma conexão com um namespace do WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="0b05e-122">To connect to the local computer, see [Example: Getting WMI Data from the Local Computer](example--getting-wmi-data-from-the-local-computer.md) and [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

    <span data-ttu-id="0b05e-123">Ao manipular nomes de usuário e senhas, é recomendável que o usuário seja solicitado a fornecer as informações, use as informações e, em seguida, exclua as informações, para que haja menos chance de que as informações sejam interceptadas por um usuário não autorizado.</span><span class="sxs-lookup"><span data-stu-id="0b05e-123">When handling user names and passwords, it is recommended that the user be prompted for the information, use the information, and then delete the information, so that there is less of a chance of the information being intercepted by an unauthorized user.</span></span> <span data-ttu-id="0b05e-124">A etapa 4 no código de exemplo abaixo usa [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) para obter o nome de usuário e a senha e, em seguida, usa [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) para se livrar das informações depois que ela é usada em [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="0b05e-124">Step 4 in the example code below uses [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) to get the user name and password, and then uses [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) to get rid of the information after it is used in [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="0b05e-125">Para obter mais informações, consulte [manipulando senhas](/windows/desktop/SecBP/handling-passwords) e [solicitando credenciais ao usuário](/windows/desktop/SecBP/asking-the-user-for-credentials) no msdn.</span><span class="sxs-lookup"><span data-stu-id="0b05e-125">For more information, see [Handling Passwords](/windows/desktop/SecBP/handling-passwords) and [Asking the User for Credentials](/windows/desktop/SecBP/asking-the-user-for-credentials) on MSDN.</span></span>

5.  <span data-ttu-id="0b05e-126">Crie uma estrutura [COAUTHIDENTITY](/windows/win32/api/wtypesbase/ns-wtypesbase-coauthidentity) para fornecer credenciais para definir a segurança do proxy.</span><span class="sxs-lookup"><span data-stu-id="0b05e-126">Create a [COAUTHIDENTITY](/windows/win32/api/wtypesbase/ns-wtypesbase-coauthidentity) structure to provide credentials for setting the proxy security.</span></span>
6.  <span data-ttu-id="0b05e-127">Defina a segurança do proxy de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para que o serviço WMI possa representar o cliente chamando [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="0b05e-127">Set [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy security so WMI service can impersonate the client by calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="0b05e-128">Para obter mais informações, consulte [definindo os níveis de segurança em uma conexão WMI](setting-the-security-levels-on-a-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0b05e-128">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

7.  <span data-ttu-id="0b05e-129">Use o ponteiro de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para fazer solicitações do WMI.</span><span class="sxs-lookup"><span data-stu-id="0b05e-129">Use the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer to make requests of WMI.</span></span> <span data-ttu-id="0b05e-130">Uma consulta é executada para obter o nome do sistema operacional e a quantidade de memória física livre chamando [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).</span><span class="sxs-lookup"><span data-stu-id="0b05e-130">A query is executed to obtain the name of the operating system and the amount of free physical memory by calling [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).</span></span>

    <span data-ttu-id="0b05e-131">A consulta WQL a seguir é um dos argumentos do método.</span><span class="sxs-lookup"><span data-stu-id="0b05e-131">The following WQL query is one of the method arguments.</span></span>

    `SELECT * FROM Win32_OperatingSystem`

    <span data-ttu-id="0b05e-132">O resultado dessa consulta é armazenado em um ponteiro [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="0b05e-132">The result of this query is stored in an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) pointer.</span></span> <span data-ttu-id="0b05e-133">Isso permite que os objetos de dados da consulta sejam recuperados semisynchronously com a interface **IEnumWbemClassObject** .</span><span class="sxs-lookup"><span data-stu-id="0b05e-133">This allows the data objects from the query to be retrieved semisynchronously with the **IEnumWbemClassObject** interface.</span></span> <span data-ttu-id="0b05e-134">Para obter mais informações, consulte [enumerando o WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="0b05e-134">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span> <span data-ttu-id="0b05e-135">Para obter os dados de forma assíncrona, consulte [exemplo: obtendo dados do WMI do computador local de forma assíncrona](example--getting-wmi-data-from-the-local-computer-asynchronously.md).</span><span class="sxs-lookup"><span data-stu-id="0b05e-135">For getting the data asynchronously, see [Example: Getting WMI Data from the Local Computer Asynchronously](example--getting-wmi-data-from-the-local-computer-asynchronously.md).</span></span>

    <span data-ttu-id="0b05e-136">Para obter mais informações sobre como fazer solicitações do WMI, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md), [consultando o WMI](querying-wmi.md)e [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="0b05e-136">For more information about making requests of WMI, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Querying WMI](querying-wmi.md), and [Calling a Method](calling-a-method.md).</span></span>

8.  <span data-ttu-id="0b05e-137">Defina a segurança de proxy do enumerador [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="0b05e-137">Set [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) enumerator proxy security.</span></span> <span data-ttu-id="0b05e-138">Certifique-se de apagar as credenciais da memória depois de terminar de usá-las.</span><span class="sxs-lookup"><span data-stu-id="0b05e-138">Make sure to erase the credentials from memory after you have finished using them.</span></span>

    <span data-ttu-id="0b05e-139">Para obter mais informações, consulte [definindo a segurança em IWbemServices e outros proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span><span class="sxs-lookup"><span data-stu-id="0b05e-139">For more information, see [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

9.  <span data-ttu-id="0b05e-140">Obter e exibir os dados da consulta WQL.</span><span class="sxs-lookup"><span data-stu-id="0b05e-140">Get and display the data from the WQL query.</span></span> <span data-ttu-id="0b05e-141">O ponteiro [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) é vinculado aos objetos de dados retornados pela consulta e os objetos de dados podem ser recuperados com o método [**IEnumWbemClassObject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) .</span><span class="sxs-lookup"><span data-stu-id="0b05e-141">The [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) pointer is linked to the data objects that the query returned, and the data objects can be retrieved with the [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) method.</span></span> <span data-ttu-id="0b05e-142">Esse método vincula os objetos de dados a um ponteiro [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) que é passado para o método.</span><span class="sxs-lookup"><span data-stu-id="0b05e-142">This method links the data objects to an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer that is passed into the method.</span></span> <span data-ttu-id="0b05e-143">Use o método [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) para obter as informações desejadas dos objetos de dados.</span><span class="sxs-lookup"><span data-stu-id="0b05e-143">Use the [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) method to get the desired information from the data objects.</span></span>

    <span data-ttu-id="0b05e-144">O exemplo de código a seguir é usado para obter a `Name` Propriedade do objeto de dados, que fornece o nome do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="0b05e-144">The following code example is used to get the `Name` property from the data object, which provides the name of the operating system.</span></span>

    ```C++
    VARIANT vtProp;

    // Get the value of the Name property
    hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
    wcout << " OS Name : " << vtProp.bstrVal << endl;
    ```

    

    <span data-ttu-id="0b05e-145">Depois que o valor da `Name` propriedade é armazenado na variável [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) `vtProp` , ele pode ser exibido para o usuário.</span><span class="sxs-lookup"><span data-stu-id="0b05e-145">Once the value of the `Name` property is stored in the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) variable `vtProp`, it can then be displayed to the user.</span></span>

    <span data-ttu-id="0b05e-146">O exemplo de código a seguir mostra como a variável [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) pode ser usada novamente para armazenar e exibir o valor da quantidade de memória física livre.</span><span class="sxs-lookup"><span data-stu-id="0b05e-146">The following code example shows how the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) variable can be used again to store and display the value of the amount of free physical memory.</span></span>

    ```C++
    hr = pclsObj->Get(L"FreePhysicalMemory",
        0, &vtProp, 0, 0);
    wcout << " Free physical memory (in kilobytes): "
        << vtProp.uintVal << endl;
    ```

    

    <span data-ttu-id="0b05e-147">Para obter mais informações, consulte [enumerando o WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="0b05e-147">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span>

<span data-ttu-id="0b05e-148">O exemplo de código a seguir mostra como obter semisynchronously de dados WMI de um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="0b05e-148">The following code example shows how to get WMI data semisynchronously from a remote computer.</span></span>


```C++
#define _WIN32_DCOM
#define UNICODE
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
#pragma comment(lib, "credui.lib")
#pragma comment(lib, "comsuppw.lib")
#include <wincred.h>
#include <strsafe.h>

int __cdecl main(int argc, char **argv)
{
    HRESULT hres;

    // Step 1: --------------------------------------------------
    // Initialize COM. ------------------------------------------

    hres =  CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hres))
    {
        cout << "Failed to initialize COM library. Error code = 0x" 
            << hex << hres << endl;
        return 1;                  // Program has failed.
    }

    // Step 2: --------------------------------------------------
    // Set general COM security levels --------------------------

    hres =  CoInitializeSecurity(
        NULL, 
        -1,                          // COM authentication
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication 
        RPC_C_IMP_LEVEL_IDENTIFY,    // Default Impersonation  
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities 
        NULL                         // Reserved
        );

                      
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. Error code = 0x" 
            << hex << hres << endl;
        CoUninitialize();
        return 1;                    // Program has failed.
    }
    
    // Step 3: ---------------------------------------------------
    // Obtain the initial locator to WMI -------------------------

    IWbemLocator *pLoc = NULL;

    hres = CoCreateInstance(
        CLSID_WbemLocator,             
        0, 
        CLSCTX_INPROC_SERVER, 
        IID_IWbemLocator, (LPVOID *) &pLoc);
 
    if (FAILED(hres))
    {
        cout << "Failed to create IWbemLocator object."
            << " Err code = 0x"
            << hex << hres << endl;
        CoUninitialize();
        return 1;                 // Program has failed.
    }

    // Step 4: -----------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    IWbemServices *pSvc = NULL;

    // Get the user name and password for the remote computer
    CREDUI_INFO cui;
    bool useToken = false;
    bool useNTLM = true;
    wchar_t pszName[CREDUI_MAX_USERNAME_LENGTH+1] = {0};
    wchar_t pszPwd[CREDUI_MAX_PASSWORD_LENGTH+1] = {0};
    wchar_t pszDomain[CREDUI_MAX_USERNAME_LENGTH+1];
    wchar_t pszUserName[CREDUI_MAX_USERNAME_LENGTH+1];
    wchar_t pszAuthority[CREDUI_MAX_USERNAME_LENGTH+1];
    BOOL fSave;
    DWORD dwErr;

    memset(&cui,0,sizeof(CREDUI_INFO));
    cui.cbSize = sizeof(CREDUI_INFO);
    cui.hwndParent = NULL;
    // Ensure that MessageText and CaptionText identify
    // what credentials to use and which application requires them.
    cui.pszMessageText = TEXT("Press cancel to use process token");
    cui.pszCaptionText = TEXT("Enter Account Information");
    cui.hbmBanner = NULL;
    fSave = FALSE;

    dwErr = CredUIPromptForCredentials( 
        &cui,                             // CREDUI_INFO structure
        TEXT(""),                         // Target for credentials
        NULL,                             // Reserved
        0,                                // Reason
        pszName,                          // User name
        CREDUI_MAX_USERNAME_LENGTH+1,     // Max number for user name
        pszPwd,                           // Password
        CREDUI_MAX_PASSWORD_LENGTH+1,     // Max number for password
        &fSave,                           // State of save check box
        CREDUI_FLAGS_GENERIC_CREDENTIALS |// flags
        CREDUI_FLAGS_ALWAYS_SHOW_UI |
        CREDUI_FLAGS_DO_NOT_PERSIST);  

    if(dwErr == ERROR_CANCELLED)
    {
        useToken = true;
    }
    else if (dwErr)
    {
        cout << "Did not get credentials " << dwErr << endl;
        pLoc->Release();     
        CoUninitialize();
        return 1;      
    }

    // change the computerName strings below to the full computer name
    // of the remote computer
    if(!useNTLM)
    {
        StringCchPrintf(pszAuthority, CREDUI_MAX_USERNAME_LENGTH+1, L"kERBEROS:%s", L"COMPUTERNAME");
    }

    // Connect to the remote root\cimv2 namespace
    // and obtain pointer pSvc to make IWbemServices calls.
    //---------------------------------------------------------
   
    hres = pLoc->ConnectServer(
        _bstr_t(L"\\\\COMPUTERNAME\\root\\cimv2"),
        _bstr_t(useToken?NULL:pszName),    // User name
        _bstr_t(useToken?NULL:pszPwd),     // User password
        NULL,                              // Locale             
        NULL,                              // Security flags
        _bstr_t(useNTLM?NULL:pszAuthority),// Authority        
        NULL,                              // Context object 
        &pSvc                              // IWbemServices proxy
        );
    
    if (FAILED(hres))
    {
        cout << "Could not connect. Error code = 0x" 
             << hex << hres << endl;
        pLoc->Release();     
        CoUninitialize();
        return 1;                // Program has failed.
    }

    cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;


    // step 5: --------------------------------------------------
    // Create COAUTHIDENTITY that can be used for setting security on proxy

    COAUTHIDENTITY *userAcct =  NULL ;
    COAUTHIDENTITY authIdent;

    if( !useToken )
    {
        memset(&authIdent, 0, sizeof(COAUTHIDENTITY));
        authIdent.PasswordLength = wcslen (pszPwd);
        authIdent.Password = (USHORT*)pszPwd;

        LPWSTR slash = wcschr (pszName, L'\\');
        if( slash == NULL )
        {
            cout << "Could not create Auth identity. No domain specified\n" ;
            pSvc->Release();
            pLoc->Release();     
            CoUninitialize();
            return 1;               // Program has failed.
        }

        StringCchCopy(pszUserName, CREDUI_MAX_USERNAME_LENGTH+1, slash+1);
        authIdent.User = (USHORT*)pszUserName;
        authIdent.UserLength = wcslen(pszUserName);

        StringCchCopyN(pszDomain, CREDUI_MAX_USERNAME_LENGTH+1, pszName, slash - pszName);
        authIdent.Domain = (USHORT*)pszDomain;
        authIdent.DomainLength = slash - pszName;
        authIdent.Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;

        userAcct = &authIdent;

    }

    // Step 6: --------------------------------------------------
    // Set security levels on a WMI connection ------------------

    hres = CoSetProxyBlanket(
       pSvc,                           // Indicates the proxy to set
       RPC_C_AUTHN_DEFAULT,            // RPC_C_AUTHN_xxx
       RPC_C_AUTHZ_DEFAULT,            // RPC_C_AUTHZ_xxx
       COLE_DEFAULT_PRINCIPAL,         // Server principal name 
       RPC_C_AUTHN_LEVEL_PKT_PRIVACY,  // RPC_C_AUTHN_LEVEL_xxx 
       RPC_C_IMP_LEVEL_IMPERSONATE,    // RPC_C_IMP_LEVEL_xxx
       userAcct,                       // client identity
       EOAC_NONE                       // proxy capabilities 
    );

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket. Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 7: --------------------------------------------------
    // Use the IWbemServices pointer to make requests of WMI ----

    // For example, get the name of the operating system
    IEnumWbemClassObject* pEnumerator = NULL;
    hres = pSvc->ExecQuery(
        bstr_t("WQL"), 
        bstr_t("Select * from Win32_OperatingSystem"),
        WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
        NULL,
        &pEnumerator);
    
    if (FAILED(hres))
    {
        cout << "Query for operating system name failed."
            << " Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 8: -------------------------------------------------
    // Secure the enumerator proxy
    hres = CoSetProxyBlanket(
        pEnumerator,                    // Indicates the proxy to set
        RPC_C_AUTHN_DEFAULT,            // RPC_C_AUTHN_xxx
        RPC_C_AUTHZ_DEFAULT,            // RPC_C_AUTHZ_xxx
        COLE_DEFAULT_PRINCIPAL,         // Server principal name 
        RPC_C_AUTHN_LEVEL_PKT_PRIVACY,  // RPC_C_AUTHN_LEVEL_xxx 
        RPC_C_IMP_LEVEL_IMPERSONATE,    // RPC_C_IMP_LEVEL_xxx
        userAcct,                       // client identity
        EOAC_NONE                       // proxy capabilities 
        );

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket on enumerator. Error code = 0x" 
             << hex << hres << endl;
        pEnumerator->Release();
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // When you have finished using the credentials,
    // erase them from memory.
    SecureZeroMemory(pszName, sizeof(pszName));
    SecureZeroMemory(pszPwd, sizeof(pszPwd));
    SecureZeroMemory(pszUserName, sizeof(pszUserName));
    SecureZeroMemory(pszDomain, sizeof(pszDomain));


    // Step 9: -------------------------------------------------
    // Get the data from the query in step 7 -------------------
 
    IWbemClassObject *pclsObj = NULL;
    ULONG uReturn = 0;
   
    while (pEnumerator)
    {
        HRESULT hr = pEnumerator->Next(WBEM_INFINITE, 1, 
            &pclsObj, &uReturn);

        if(0 == uReturn)
        {
            break;
        }

        VARIANT vtProp;

        // Get the value of the Name property
        hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
        wcout << " OS Name : " << vtProp.bstrVal << endl;

        // Get the value of the FreePhysicalMemory property
        hr = pclsObj->Get(L"FreePhysicalMemory",
            0, &vtProp, 0, 0);
        wcout << " Free physical memory (in kilobytes): "
            << vtProp.uintVal << endl;
        VariantClear(&vtProp);

        pclsObj->Release();
        pclsObj = NULL;
    }

    // Cleanup
    // ========
    
    pSvc->Release();
    pLoc->Release();
    pEnumerator->Release();
    if( pclsObj )
    {
        pclsObj->Release();
    }
    
    CoUninitialize();

    return 0;   // Program successfully completed.
    
}
```



 

 
