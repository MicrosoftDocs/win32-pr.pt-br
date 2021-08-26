---
title: Registrando-se para reinicialização do aplicativo
description: Para registrar seu aplicativo a ser reiniciado, chame a função RegisterApplicationRestart.
ms.assetid: 4dfbced7-77db-4042-823f-b4b81b2b27a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe5777d3ed6b99d421f7eba6b5b104b92a1c2c71462c675b2573f18da0ba69f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024566"
---
# <a name="registering-for-application-restart"></a>Registrando-se para reinicialização do aplicativo

Para registrar seu aplicativo a ser reiniciado, chame [**a função RegisterApplicationRestart.**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) [Relatório de Erros do Windows (WER)](/windows/desktop/wer/windows-error-reporting) reiniciará seu aplicativo se ele estiver em execução por pelo menos 60 segundos antes de se tornar sem resposta ou encontrar uma exceção sem resposta.

Você também deve considerar [o registro](registering-for-application-recovery.md)para recuperação , que permite salvar dados e informações de estado que podem ser úteis quando o WER reinicia seu aplicativo. O WER reiniciará o aplicativo após a conclusão do processo de recuperação, se você também se registrar para recuperação.

Depois que o processo de recuperação é concluído, o WER encerra o aplicativo e o reinicia. Para aplicativos de console, o aplicativo é iniciado em uma janela separada do console que é fechada quando o aplicativo é fechado.

**Observação para autores do instalador de aplicativo:** Registrar-se para reinicialização do aplicativo também fará Windows reiniciar automaticamente o aplicativo depois que o computador for reiniciado nos casos em que o computador for reiniciado devido a uma atualização de software. Para que isso funcione, o instalador do aplicativo deve chamar a função [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) com o sinalizador EWX RESTARTAPPS definido ou a função \_ [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) com o sinalizador SHUTDOWN \_ RESTARTAPPS definido.

O exemplo a seguir mostra como registrar para que o WER reinicie seu aplicativo. O exemplo causa uma violação de acesso após o registro para reinicialização do aplicativo. A violação de acesso será escolhida pelo Relatório de Erros do Windows e demonstrará a experiência do usuário de relatório de erros, incluindo a reinicialização do aplicativo. Ele deve ser executado em uma janela do console sem argumentos de linha de comando.


```C++
#include <windows.h>
#include <stdio.h>
#include <strsafe.h>

#define RESTART_SWITCH L"/restart"

void GetRestartInfo(int argc, wchar_t* argv[], BOOL* pfIsRestart, DWORD* pdwRecordId); 
DWORD InitApplication(BOOL fIsRestart, DWORD* pdwRecordId); 
BOOL WINAPI CtrlHandler(DWORD dwControlType);
DWORD WINAPI Recover(PVOID pContext);

// A simple example to show how to use application recovery. For simplicity,
// the state information (record ID) is passed as part of the command line. 
void wmain(int argc, wchar_t* argv[])
{
    HRESULT hr = S_OK;
    DWORD dwRecordId = 0;
    BOOL fIsRestart = FALSE;

    GetRestartInfo(argc, argv, &fIsRestart, &dwRecordId);

    if (FAILED(hr = InitApplication(fIsRestart, &dwRecordId)))
    {
        wprintf(L"Failed to initialize the application.\n");
        goto cleanup;
    }

    // Do work. If you have a lot of state information, you should
    // periodically persist the state information to save time
    // in the recovery process.

    // The application must exist for at least 60 seconds for the
    // application to be restarted. Use Sleep() to mimic 60 seconds
    // worth of work.
    wprintf(L"Sleeping...\n");
    Sleep(62 * 1000);

    // Set the record ID to verify restart value.
    dwRecordId = 10;

    // Generate an access violation to force a restart. If we've already
    // restarted just exit because the example already demonstrated
    // the restart feature.
    if (FALSE == fIsRestart)
    {
        wprintf(L"Causing access violation...\n");
        int* p = NULL;
        *p = 5;
    }

cleanup:

    wprintf(L"Exiting...\n");
}


// Get the restart info from the command line. The command line is 
// of the form, /restart -r <RecordId>. The application 
// is being restarted if the first argument is /restart.
void GetRestartInfo(int argc, wchar_t* argv[], BOOL* pfIsRestart, DWORD* pdwRecordId) 
{
    if (argc > 1)
    {
        if (!wcsncmp(RESTART_SWITCH, argv[1], sizeof(RESTART_SWITCH)))
        {
            *pfIsRestart = TRUE;
            *pdwRecordId = _wtoi(argv[3]);
        }
    }

}

// Initialize the application. If this is a restart, use the state 
// information to reset the state of the application. This example 
// does not fail the initialization process if the process of 
// registering for application recovery and restart failed.
DWORD InitApplication(BOOL fIsRestart, DWORD* pdwRecordId)
{
    DWORD status = ERROR_SUCCESS;  // Set only if the initializing the application fails,
    HRESULT hr = S_OK;             // not if registering for recovery and restart fails.
    WCHAR wsCommandLine[RESTART_MAX_CMD_LINE];

    wprintf(L"Entering InitApplication...\n");

    if (fIsRestart)
    {
        // TODO: Use the record ID to initialize the application.
        wprintf(L"Restart record ID is %lu\n", *pdwRecordId);
    }
    else
    {
        // This is not a restart, so initialize the application accordingly.
    }

    // Register for restart. The command line is updated in the recovery callback.
    RtlZeroMemory(wsCommandLine, sizeof(wsCommandLine));
    StringCchPrintf(wsCommandLine, sizeof(wsCommandLine), L"/restart -r %lu", *pdwRecordId);

    hr = RegisterApplicationRestart(wsCommandLine, RESTART_NO_PATCH | RESTART_NO_REBOOT);
    if (FAILED(hr))
    {
        // Not failing because the registration failed.
        wprintf(L"RegisterApplicationRestart failed with ox%x.\n", hr);
        goto cleanup;
    }

    // Register the callback that handles the control event notifications.
    // Used for recovery when an installer is updating a component of the
    // application.
    if (!SetConsoleCtrlHandler(CtrlHandler, TRUE))
    {
        // Not failing initialization because the registration failed.
        // Consider calling UnregisterApplicationRestart if you must
        // have the latest state information.
        wprintf(L"SetConsoleCtrlHandler failed.\n");
        goto cleanup;
    }

    // Register the callback that handles recovery when the application
    // encounters an unhandled exception or becomes unresponsive.
    hr = RegisterApplicationRecoveryCallback(Recover, pdwRecordId, RECOVERY_DEFAULT_PING_INTERVAL, 0);
    if (FAILED(hr))
    {
        // Not failing initialization because the registration failed.
        // Consider calling UnregisterApplicationRestart if you must
        // have the latest state information.
        wprintf(L"RegisterApplicationRecoveryCallback failed with ox%x.\n", hr);
        goto cleanup;
    }

cleanup:

    return hr;
}


// Implement the callback for handling control character events.
// You'd implement this callback if an installer could update a
// component of your application. The system sends a CTRL_C_EVENT
// notification when an installer needs to shutdown your application
// or restart the computer in order to complete the installation.
// You can use the CTRL_C_EVENT to save final state information or
// data before exiting.
BOOL WINAPI CtrlHandler(DWORD dwControlType)
{
    wprintf(L"Entering CtrlHandler...\n");

    switch (dwControlType)
    {
        case CTRL_C_EVENT:
            wprintf(L"Handling CTRL_C_EVENT\n");
            return FALSE;

        // Other cases go here.

        default: 
            wprintf(L"Other, %ul\n", dwControlType);
            return FALSE;
    }
}


// Implement the recovery callback. This callback lets the application
// save state information or data in the event that the application
// encounters an unhandled exception or becomes unresponsive.
DWORD WINAPI Recover(PVOID pContext)
{
    HRESULT hr = S_OK;
    BOOL bCanceled = FALSE;
    DWORD dwRecordId = *(DWORD*)pContext;
    WCHAR wsCommandLine[RESTART_MAX_CMD_LINE];

    wprintf(L"Entering Recover callback...\n");

    // Do recovery work. 

    // Update the restart command line.
    RtlZeroMemory(wsCommandLine, sizeof(wsCommandLine));
    StringCchPrintf(wsCommandLine, sizeof(wsCommandLine), L"/restart -r %lu", dwRecordId);

    hr = RegisterApplicationRestart(wsCommandLine, RESTART_NO_PATCH | RESTART_NO_REBOOT);
    if (FAILED(hr))
    {
        // Not failing because the registration failed.
        wprintf(L"RegisterApplicationRestart failed with ox%x.\n", hr);
    }

    // You must call the ApplicationRecoveryInProgress function within
    // the specified ping interval or the recovery callback exits.
    // Typically, you would do a block of work, call the function, and repeat.
    hr = ApplicationRecoveryInProgress(&bCanceled);
    if (bCanceled)  
    {
        wprintf(L"Recovery was canceled by the user.\n");
        goto cleanup;
    }

    // Do more recovery work. 
    
    // You could also call the RegisterApplicationRestart function to
    // update the command line used for the restart.

cleanup:

    // Save the state file.

    wprintf(L"Leaving Recover callback...\n");
    ApplicationRecoveryFinished((bCanceled) ? FALSE: TRUE);

    return 0;
}
```



 

 