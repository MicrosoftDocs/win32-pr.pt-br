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
# <a name="terminate-method-of-the-win32_process-class"></a>Método Terminate da classe de \_ processo do Win32

O método **terminar** da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) encerra um processo e todos os seus threads.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Terminate(
  [in] uint32 Reason
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Motivo* \[ no\]
</dt> <dd>

Código de saída para o processo e para todos os threads terminados como resultado dessa chamada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor de 0 (zero) se o processo foi encerrado com êxito e qualquer outro número para indicar um erro. Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Conclusão bem-sucedida** (0)
</dt> <dt>

**Acesso negado** (2)
</dt> <dt>

**Privilégio insuficiente** (3)
</dt> <dt>

**Falha desconhecida** (8)
</dt> <dt>

**Caminho não encontrado** (9)
</dt> <dt>

**Parâmetro inválido** (21)
</dt> <dt>

**Outro** (22 4294967295)
</dt> </dl>

## <a name="remarks"></a>Comentários

**Visão geral**

Problemas de computador geralmente são devido a um processo que não está mais funcionando conforme o esperado. Por exemplo, o processo pode estar vazando memória ou pode ter parado de responder à entrada do usuário. Quando ocorrem problemas como esses, o processo deve ser encerrado. Embora isso possa parecer uma tarefa suficientemente simples, o encerramento de um processo pode ser complicado por vários fatores:

-   O processo pode estar suspenso e, portanto, não responde mais a comandos de menu ou teclado para fechar o aplicativo. Isso torna tudo menos impossível para o usuário típico ignorar o aplicativo e encerrar o processo.
-   O processo pode ser órfão. Por exemplo, um script pode criar uma instância do Word e, em seguida, sair sem destruir essa instância. Na verdade, o Word permanece em execução no computador, mesmo que nenhuma interface de usuário esteja visível. Como não há nenhuma interface do usuário, não há nenhum comando de menu ou de teclado disponível para encerrar o processo.
-   Talvez você não saiba qual processo precisa ser encerrado. Por exemplo, talvez você queira encerrar todos os programas que estão excedendo uma quantidade especificada de memória.
-   Como o Gerenciador de tarefas permite que você finalize somente os processos que você criou, talvez não seja possível encerrar um processo, mesmo se você for um administrador no computador.

Os scripts permitem superar todos esses obstáculos potenciais, fornecendo um controle administrativo considerável sobre os computadores. Por exemplo, se você suspeitar que os usuários estão jogando em jogos que foram proibidos em sua organização, poderá facilmente escrever um script para se conectar a cada computador, identificar se o jogo está em execução e encerrar imediatamente o processo.

**Usando o método Terminate**

Você pode encerrar um processo da:

-   Encerrando um processo que está sendo executado no momento. Por exemplo, talvez seja necessário encerrar um programa de diagnóstico em execução em um computador remoto. Se não houver nenhuma maneira de controlar o aplicativo remotamente, você poderá simplesmente encerrar o processo para esse aplicativo.
-   Impedir que um processo seja executado em primeiro lugar. Ao monitorar continuamente a criação de processos em um computador, você pode identificar e encerrar instantaneamente qualquer processo assim que ele for iniciado. Isso fornece um método para garantir que determinados aplicativos (como programas que baixem arquivos de mídia grandes pela Internet) nunca sejam executados em determinados computadores.

> [!Note]  
> Política de Grupo também pode ser usado para restringir os programas que são executados em um computador. No entanto, Política de Grupo pode restringir apenas os programas executados usando o menu iniciar ou o Windows Explorer; Ele não tem nenhum efeito em programas iniciados usando outros meios, como a linha de comando. Por outro lado, o WMI pode impedir que um processo seja executado, independentemente de como o processo foi iniciado.

 

**Finalizando um processo que você não possui**

Para encerrar um processo que não é de sua propriedade, habilite o privilégio **SeDebugPrivilege** . No VBScript, você pode habilitar esse privilégio com as seguintes linhas de código:


```VB
Set objLoc = createobject("wbemscripting.swbemlocator")
objLoc.Security_.privileges.addasstring "sedebugprivilege", true
```



Para obter mais informações sobre como habilitar esse privilégio em C++, consulte [Habilitando e desabilitando privilégios em c++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).

## <a name="examples"></a>Exemplos

O exemplo de [encerrar processo em execução em vários servidores](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) do PowerShell no TechNet Gallery encerra um processo em execução em um único ou vários computadores.

O exemplo de VBScript a seguir encerra o processo no qual o aplicativo Diagnose.exe está em execução no momento.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Diagnose.exe'")
For Each objProcess in colProcessList
 objProcess.Terminate()
Next
```



O exemplo de VBScript a seguir usa um consumidor de evento temporário para encerrar um processo assim que ele é iniciado.


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



O exemplo de código VBScript a seguir se conecta a um computador remoto e termina Notepad.exe nesse computador.


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



O código C++ a seguir encerra o processo de Notepad.exe no computador local. Especifique um identificador de processo ou (ID do processo) no código para encerrar o processo. Esse valor pode ser encontrado na propriedade Handle na classe [**\_ process do Win32**](win32-process.md) (a propriedade de chave para a classe). Ao especificar um valor para a propriedade Handle, você está fornecendo um caminho para a instância da classe que deseja encerrar. Para obter mais informações sobre como se conectar a um computador remoto, consulte [exemplo: obtendo dados WMI de um computador remoto](/windows/desktop/WmiSdk/example--getting-wmi-data-from-a-remote-computer).


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Processo Win32**](win32-process.md)
</dt> <dt>

[Tarefas do WMI: monitoramento de desempenho](/windows/desktop/WmiSdk/wmi-tasks--performance-monitoring)
</dt> <dt>

[Tarefas do WMI: processos](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 

