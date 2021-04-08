---
description: O encerramento&\# 32; O método de classe WMI encerra um processo e todos os seus threads.
ms.assetid: 6c6b27d4-cf9b-42d7-9136-42641ea56ee8
ms.tgt_platform: multiple
title: Método Terminate da classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.Terminate
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 00300ca9656c3b732b9c294aeba9a6c626ac6e2e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920244"
---
# <a name="terminate-method-of-the-win32_process-class"></a><span data-ttu-id="a87ab-103">Método Terminate da classe de \_ processo do Win32</span><span class="sxs-lookup"><span data-stu-id="a87ab-103">Terminate method of the Win32\_Process class</span></span>

<span data-ttu-id="a87ab-104">O método **terminar** da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) encerra um processo e todos os seus threads.</span><span class="sxs-lookup"><span data-stu-id="a87ab-104">The **Terminate** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method terminates a process and all of its threads.</span></span>

<span data-ttu-id="a87ab-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="a87ab-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a87ab-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a87ab-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a87ab-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a87ab-107">Syntax</span></span>


```mof
uint32 Terminate(
  [in] uint32 Reason
);
```



## <a name="parameters"></a><span data-ttu-id="a87ab-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a87ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a87ab-109">*Motivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a87ab-109">*Reason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a87ab-110">Código de saída para o processo e para todos os threads terminados como resultado dessa chamada.</span><span class="sxs-lookup"><span data-stu-id="a87ab-110">Exit code for the process and for all of the threads terminated as a result of this call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a87ab-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a87ab-111">Return value</span></span>

<span data-ttu-id="a87ab-112">Retorna um valor de 0 (zero) se o processo foi encerrado com êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="a87ab-112">Returns a value of 0 (zero) if the process was successfully terminated, and any other number to indicate an error.</span></span> <span data-ttu-id="a87ab-113">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="a87ab-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a87ab-114">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="a87ab-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="a87ab-115">**Conclusão bem-sucedida** (0)</span><span class="sxs-lookup"><span data-stu-id="a87ab-115">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a87ab-116">**Acesso negado** (2)</span><span class="sxs-lookup"><span data-stu-id="a87ab-116">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a87ab-117">**Privilégio insuficiente** (3)</span><span class="sxs-lookup"><span data-stu-id="a87ab-117">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a87ab-118">**Falha desconhecida** (8)</span><span class="sxs-lookup"><span data-stu-id="a87ab-118">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a87ab-119">**Caminho não encontrado** (9)</span><span class="sxs-lookup"><span data-stu-id="a87ab-119">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="a87ab-120">**Parâmetro inválido** (21)</span><span class="sxs-lookup"><span data-stu-id="a87ab-120">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="a87ab-121">**Outro** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="a87ab-121">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="a87ab-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="a87ab-122">Remarks</span></span>

<span data-ttu-id="a87ab-123">**Visão geral**</span><span class="sxs-lookup"><span data-stu-id="a87ab-123">**Overview**</span></span>

<span data-ttu-id="a87ab-124">Problemas de computador geralmente são devido a um processo que não está mais funcionando conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="a87ab-124">Computer problems are often due to a process that is no longer working as expected.</span></span> <span data-ttu-id="a87ab-125">Por exemplo, o processo pode estar vazando memória ou pode ter parado de responder à entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="a87ab-125">For example, the process might be leaking memory, or it might have stopped responding to user input.</span></span> <span data-ttu-id="a87ab-126">Quando ocorrem problemas como esses, o processo deve ser encerrado.</span><span class="sxs-lookup"><span data-stu-id="a87ab-126">When problems such as these occur, the process must be terminated.</span></span> <span data-ttu-id="a87ab-127">Embora isso possa parecer uma tarefa suficientemente simples, o encerramento de um processo pode ser complicado por vários fatores:</span><span class="sxs-lookup"><span data-stu-id="a87ab-127">Although this might seem like a simple enough task, terminating a process can be complicated by several factors:</span></span>

-   <span data-ttu-id="a87ab-128">O processo pode estar suspenso e, portanto, não responde mais a comandos de menu ou teclado para fechar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a87ab-128">The process might be hung and therefore no longer responds to menu or keyboard commands for closing the application.</span></span> <span data-ttu-id="a87ab-129">Isso torna tudo menos impossível para o usuário típico ignorar o aplicativo e encerrar o processo.</span><span class="sxs-lookup"><span data-stu-id="a87ab-129">This makes it all but impossible for the typical user to dismiss the application and terminate the process.</span></span>
-   <span data-ttu-id="a87ab-130">O processo pode ser órfão.</span><span class="sxs-lookup"><span data-stu-id="a87ab-130">The process might be orphaned.</span></span> <span data-ttu-id="a87ab-131">Por exemplo, um script pode criar uma instância do Word e, em seguida, sair sem destruir essa instância.</span><span class="sxs-lookup"><span data-stu-id="a87ab-131">For example, a script might create an instance of Word and then exit without destroying that instance.</span></span> <span data-ttu-id="a87ab-132">Na verdade, o Word permanece em execução no computador, mesmo que nenhuma interface de usuário esteja visível.</span><span class="sxs-lookup"><span data-stu-id="a87ab-132">In effect, Word remains running on the computer, even though no user interface is visible.</span></span> <span data-ttu-id="a87ab-133">Como não há nenhuma interface do usuário, não há nenhum comando de menu ou de teclado disponível para encerrar o processo.</span><span class="sxs-lookup"><span data-stu-id="a87ab-133">Because there is no user interface, there are no menu or keyboard commands available to terminate the process.</span></span>
-   <span data-ttu-id="a87ab-134">Talvez você não saiba qual processo precisa ser encerrado.</span><span class="sxs-lookup"><span data-stu-id="a87ab-134">You might not know which process needs to be terminated.</span></span> <span data-ttu-id="a87ab-135">Por exemplo, talvez você queira encerrar todos os programas que estão excedendo uma quantidade especificada de memória.</span><span class="sxs-lookup"><span data-stu-id="a87ab-135">For example, you might want to terminate all programs that are exceeding a specified amount of memory.</span></span>
-   <span data-ttu-id="a87ab-136">Como o Gerenciador de tarefas permite que você finalize somente os processos que você criou, talvez não seja possível encerrar um processo, mesmo se você for um administrador no computador.</span><span class="sxs-lookup"><span data-stu-id="a87ab-136">Because Task Manager allows you to terminate only those processes that you created, you might not be able to terminate a process, even if you are an administrator on the computer.</span></span>

<span data-ttu-id="a87ab-137">Os scripts permitem superar todos esses obstáculos potenciais, fornecendo um controle administrativo considerável sobre os computadores.</span><span class="sxs-lookup"><span data-stu-id="a87ab-137">Scripts enable you to overcome all of these potential obstacles, providing you with considerable administrative control over your computers.</span></span> <span data-ttu-id="a87ab-138">Por exemplo, se você suspeitar que os usuários estão jogando em jogos que foram proibidos em sua organização, poderá facilmente escrever um script para se conectar a cada computador, identificar se o jogo está em execução e encerrar imediatamente o processo.</span><span class="sxs-lookup"><span data-stu-id="a87ab-138">For example, if you suspect users are playing games that have been prohibited in your organization, you can easily write a script to connect to each computer, identify whether the game is running, and immediately terminate the process.</span></span>

<span data-ttu-id="a87ab-139">**Usando o método Terminate**</span><span class="sxs-lookup"><span data-stu-id="a87ab-139">**Using the Terminate Method**</span></span>

<span data-ttu-id="a87ab-140">Você pode encerrar um processo da:</span><span class="sxs-lookup"><span data-stu-id="a87ab-140">You can terminate a process by:</span></span>

-   <span data-ttu-id="a87ab-141">Encerrando um processo que está sendo executado no momento.</span><span class="sxs-lookup"><span data-stu-id="a87ab-141">Terminating a process that is currently running.</span></span> <span data-ttu-id="a87ab-142">Por exemplo, talvez seja necessário encerrar um programa de diagnóstico em execução em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="a87ab-142">For example, you might need to terminate a diagnostic program running on a remote computer.</span></span> <span data-ttu-id="a87ab-143">Se não houver nenhuma maneira de controlar o aplicativo remotamente, você poderá simplesmente encerrar o processo para esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a87ab-143">If there is no way to control the application remotely, you can simply terminate the process for that application.</span></span>
-   <span data-ttu-id="a87ab-144">Impedir que um processo seja executado em primeiro lugar.</span><span class="sxs-lookup"><span data-stu-id="a87ab-144">Preventing a process from running in the first place.</span></span> <span data-ttu-id="a87ab-145">Ao monitorar continuamente a criação de processos em um computador, você pode identificar e encerrar instantaneamente qualquer processo assim que ele for iniciado.</span><span class="sxs-lookup"><span data-stu-id="a87ab-145">By continuously monitoring process creation on a computer, you can identify and instantly terminate any process as soon as it starts.</span></span> <span data-ttu-id="a87ab-146">Isso fornece um método para garantir que determinados aplicativos (como programas que baixem arquivos de mídia grandes pela Internet) nunca sejam executados em determinados computadores.</span><span class="sxs-lookup"><span data-stu-id="a87ab-146">This provides one method of ensuring that certain applications (such as programs that download large media files over the Internet) are never run on certain computers.</span></span>

> [!Note]  
> <span data-ttu-id="a87ab-147">Política de Grupo também pode ser usado para restringir os programas que são executados em um computador.</span><span class="sxs-lookup"><span data-stu-id="a87ab-147">Group Policy can also be used to restrict the programs that run on a computer.</span></span> <span data-ttu-id="a87ab-148">No entanto, Política de Grupo pode restringir apenas os programas executados usando o menu iniciar ou o Windows Explorer; Ele não tem nenhum efeito em programas iniciados usando outros meios, como a linha de comando.</span><span class="sxs-lookup"><span data-stu-id="a87ab-148">However, Group Policy can restrict only the programs run using either the Start menu or Windows Explorer; it has no effect on programs started using other means, such as the command line.</span></span> <span data-ttu-id="a87ab-149">Por outro lado, o WMI pode impedir que um processo seja executado, independentemente de como o processo foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="a87ab-149">By contrast, WMI can prevent a process from running regardless of how the process was started.</span></span>

 

<span data-ttu-id="a87ab-150">**Finalizando um processo que você não possui**</span><span class="sxs-lookup"><span data-stu-id="a87ab-150">**Terminating a Process You Do Not Own**</span></span>

<span data-ttu-id="a87ab-151">Para encerrar um processo que não é de sua propriedade, habilite o privilégio **SeDebugPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="a87ab-151">To terminate a process that you do not own, enable the **SeDebugPrivilege** privilege.</span></span> <span data-ttu-id="a87ab-152">No VBScript, você pode habilitar esse privilégio com as seguintes linhas de código:</span><span class="sxs-lookup"><span data-stu-id="a87ab-152">In VBScript, you can enable this privilege with the following lines of code:</span></span>


```VB
Set objLoc = createobject("wbemscripting.swbemlocator")
objLoc.Security_.privileges.addasstring "sedebugprivilege", true
```



<span data-ttu-id="a87ab-153">Para obter mais informações sobre como habilitar esse privilégio em C++, consulte [Habilitando e desabilitando privilégios em c++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).</span><span class="sxs-lookup"><span data-stu-id="a87ab-153">For more information about enabling this privilege in C++, see [Enabling and Disabling Privileges in C++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).</span></span>

## <a name="examples"></a><span data-ttu-id="a87ab-154">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a87ab-154">Examples</span></span>

<span data-ttu-id="a87ab-155">O exemplo de [encerrar processo em execução em vários servidores](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) do PowerShell no TechNet Gallery encerra um processo em execução em um único ou vários computadores.</span><span class="sxs-lookup"><span data-stu-id="a87ab-155">The [Terminate running process on multiple servers](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) PowerShell code sample on TechNet Gallery terminates a process running on a single or multiple computers.</span></span>

<span data-ttu-id="a87ab-156">O exemplo de VBScript a seguir encerra o processo no qual o aplicativo Diagnose.exe está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="a87ab-156">The following VBScript sample terminates the process in which the application Diagnose.exe is currently running.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Diagnose.exe'")
For Each objProcess in colProcessList
 objProcess.Terminate()
Next
```



<span data-ttu-id="a87ab-157">O exemplo de VBScript a seguir usa um consumidor de evento temporário para encerrar um processo assim que ele é iniciado.</span><span class="sxs-lookup"><span data-stu-id="a87ab-157">The following VBScript sample uses a temporary event consumer to terminate a process as soon as it starts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colMonitoredProcesses = objWMIService.ExecNotificationQuery("SELECT * FROM __InstanceCreationEvent " _
 & " WITHIN 1 WHERE TargetInstance ISA 'Win32_Process'")
i = 0
Do While i = 0
 Set objLatestProcess = colMonitoredProcesses.NextEvent
 If objLatestProcess.TargetInstance.Name = "Download.exe" Then
 objLatestProcess.TargetInstance.Terminate()
 End If
Loop
```



<span data-ttu-id="a87ab-158">O exemplo de código VBScript a seguir se conecta a um computador remoto e termina Notepad.exe nesse computador.</span><span class="sxs-lookup"><span data-stu-id="a87ab-158">The following VBScript code example connects to a remote computer and terminates Notepad.exe on that computer.</span></span>


```VB
strComputer = "FullComputerName" 
strDomain = "DOMAIN" 
strUser = InputBox("Enter user name") 
strPassword = InputBox("Enter password") 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator") 
Set objWMIService = objSWbemLocator.ConnectServer(strComputer, _ 
    "root\CIMV2", _ 
    strUser, _ 
    strPassword, _ 
    "MS_409", _ 
    "ntlmdomain:" + strDomain) 
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'notepad.exe'")
For Each objProcess in colProcessList
    objProcess.Terminate()
Next
```



<span data-ttu-id="a87ab-159">O código C++ a seguir encerra o processo de Notepad.exe no computador local.</span><span class="sxs-lookup"><span data-stu-id="a87ab-159">The following C++ code terminates the Notepad.exe process on the local computer.</span></span> <span data-ttu-id="a87ab-160">Especifique um identificador de processo ou (ID do processo) no código para encerrar o processo.</span><span class="sxs-lookup"><span data-stu-id="a87ab-160">Specify a or process handle (process id) in the code to terminate the process.</span></span> <span data-ttu-id="a87ab-161">Esse valor pode ser encontrado na propriedade Handle na classe [**\_ process do Win32**](win32-process.md) (a propriedade de chave para a classe).</span><span class="sxs-lookup"><span data-stu-id="a87ab-161">This value can be found in the handle property in the [**Win32\_Process**](win32-process.md) class (the key property for the class).</span></span> <span data-ttu-id="a87ab-162">Ao especificar um valor para a propriedade Handle, você está fornecendo um caminho para a instância da classe que deseja encerrar.</span><span class="sxs-lookup"><span data-stu-id="a87ab-162">By specifying a value for the Handle property, you are supplying a path to the instance of the class that you want to terminate.</span></span> <span data-ttu-id="a87ab-163">Para obter mais informações sobre como se conectar a um computador remoto, consulte [exemplo: obtendo dados WMI de um computador remoto](/windows/desktop/WmiSdk/example--getting-wmi-data-from-a-remote-computer).</span><span class="sxs-lookup"><span data-stu-id="a87ab-163">For more information about connecting to a remote computer, see [Example: Getting WMI Data From a Remote Computer](/windows/desktop/WmiSdk/example--getting-wmi-data-from-a-remote-computer).</span></span>


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

int main(int iArgCnt, char ** argv)
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
    // Note: If you are using Windows 2000, specify -
    // the default authentication credentials for a user by using
    // a SOLE_AUTHENTICATION_LIST structure in the pAuthList ----
    // parameter of CoInitializeSecurity ------------------------

    hres =  CoInitializeSecurity(
        NULL, 
        -1,                          // COM negotiates service
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication 
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation  
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities 
        NULL                         // Reserved
        );

                      
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. Error code = 0x" 
             << hex << hres << endl;
        CoUninitialize();
        return 1;                      // Program has failed.
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
        cout << "Failed to create IWbemLocator object. "
             << "Err code = 0x"
             << hex << hres << endl;
        CoUninitialize();
        return 1;                 // Program has failed.
    }

    // Step 4: ---------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    IWbemServices *pSvc = NULL;
 
    // Connect to the local root\cimv2 namespace
    // and obtain pointer pSvc to make IWbemServices calls.
    hres = pLoc->ConnectServer(
        _bstr_t(L"ROOT\\CIMV2"), 
        NULL,
        NULL, 
        0, 
        NULL, 
        0, 
        0, 
        &pSvc
    );
     
    if (FAILED(hres))
    {
        cout << "Could not connect. Error code = 0x" 
             << hex << hres << endl;
        pLoc->Release();
        pSvc->Release();     
        CoUninitialize();
        return 1;                // Program has failed.
    }

    cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;


    // Step 5: --------------------------------------------------
    // Set security levels for the proxy ------------------------

    hres = CoSetProxyBlanket(
        pSvc,                        // Indicates the proxy to set
        RPC_C_AUTHN_WINNT,           // RPC_C_AUTHN_xxx 
        RPC_C_AUTHZ_NONE,            // RPC_C_AUTHZ_xxx 
        NULL,                        // Server principal name 
        RPC_C_AUTHN_LEVEL_CALL,      // RPC_C_AUTHN_LEVEL_xxx 
        RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
        NULL,                        // client identity
        EOAC_NONE                    // proxy capabilities 
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

    // Step 6: --------------------------------------------------
    // Use the IWbemServices pointer to make requests of WMI ----

    // Set up to call the Win32_Process::Create method
    BSTR ClassName = SysAllocString(L"Win32_Process");

    /* YOU NEED TO CHANGE THE NUMBER VALUE OF THE HANDLE 
       (PROCESS ID) TO THE CORRECT VALUE OF THE PROCESS YOU 
       ARE TRYING TO TERMINATE (this provides a path to
       the class instance you are tying to terminate). */
    BSTR ClassNameInstance = SysAllocString(
        L"Win32_Process.Handle=\"3168\"");

    _bstr_t MethodName = (L"Terminate");
    BSTR ParameterName = SysAllocString(L"Reason");

    IWbemClassObject* pClass = NULL;
    hres = pSvc->GetObject(ClassName, 0, NULL, &pClass, NULL);

    IWbemClassObject* pInParamsDefinition = NULL;
    IWbemClassObject* pOutMethod = NULL;
    hres = pClass->GetMethod(MethodName, 0, 
        &pInParamsDefinition, &pOutMethod);

    if (FAILED(hres))
    {
        cout << "Could not get the method. Error code = 0x" 
             << hex << hres << endl;
    }

    IWbemClassObject* pClassInstance = NULL;
    hres = pInParamsDefinition->SpawnInstance(0, &pClassInstance);

    // Create the values for the in parameters
    VARIANT pcVal;
    VariantInit(&pcVal);
    V_VT(&pcVal) = VT_I4;

    // Store the value for the in parameters
    hres = pClassInstance->Put(L"Reason", 0,
        &pcVal, 0);

    // Execute Method
    hres = pSvc->ExecMethod(ClassNameInstance, MethodName, 0,
    NULL, pClassInstance, NULL, NULL);

    if (FAILED(hres))
    {
        cout << "Could not execute method. Error code = 0x" 
             << hex << hres << endl;
        VariantClear(&pcVal);
        SysFreeString(ClassName);
        SysFreeString(MethodName);
        pClass->Release();
        pInParamsDefinition->Release();
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;           // Program has failed.
    }


    // Clean up
    //--------------------------
    VariantClear(&pcVal);
    SysFreeString(ClassName);
    SysFreeString(MethodName);
    pClass->Release();
    pInParamsDefinition->Release();
    pLoc->Release();
    pSvc->Release();
    CoUninitialize();
    return 0;
}
```



## <a name="requirements"></a><span data-ttu-id="a87ab-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a87ab-164">Requirements</span></span>



| <span data-ttu-id="a87ab-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="a87ab-165">Requirement</span></span> | <span data-ttu-id="a87ab-166">Valor</span><span class="sxs-lookup"><span data-stu-id="a87ab-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a87ab-167">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a87ab-167">Minimum supported client</span></span><br/> | <span data-ttu-id="a87ab-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a87ab-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a87ab-169">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a87ab-169">Minimum supported server</span></span><br/> | <span data-ttu-id="a87ab-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a87ab-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a87ab-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="a87ab-171">Namespace</span></span><br/>                | <span data-ttu-id="a87ab-172">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a87ab-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a87ab-173">MOF</span><span class="sxs-lookup"><span data-stu-id="a87ab-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a87ab-174"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a87ab-174"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a87ab-175">DLL</span><span class="sxs-lookup"><span data-stu-id="a87ab-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a87ab-176"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a87ab-176"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a87ab-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="a87ab-177">See also</span></span>

<dl> <dt>

<span data-ttu-id="a87ab-178">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a87ab-178">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a87ab-179">**\_Processo Win32**</span><span class="sxs-lookup"><span data-stu-id="a87ab-179">**Win32\_Process**</span></span>](win32-process.md)
</dt> <dt>

[<span data-ttu-id="a87ab-180">Tarefas do WMI: monitoramento de desempenho</span><span class="sxs-lookup"><span data-stu-id="a87ab-180">WMI Tasks: Performance Monitoring</span></span>](/windows/desktop/WmiSdk/wmi-tasks--performance-monitoring)
</dt> <dt>

[<span data-ttu-id="a87ab-181">Tarefas do WMI: processos</span><span class="sxs-lookup"><span data-stu-id="a87ab-181">WMI Tasks: Processes</span></span>](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 

