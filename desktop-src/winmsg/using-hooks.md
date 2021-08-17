---
description: 'Saiba mais sobre: Usando ganchos'
ms.assetid: f0ca9e41-a9f7-435f-a601-f0959adcb514
title: Usando ganchos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34539855a30a67964acfe671c29de3cacdf23314cbb51bb80027d4b388e47b5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849626"
---
# <a name="using-hooks"></a>Usando ganchos

Os exemplos de código a seguir demonstram como executar as seguintes tarefas associadas a ganchos:

-   [Instalando e liberando procedimentos de gancho](#installing-and-releasing-hook-procedures)
-   [Monitorando eventos do sistema](#monitoring-system-events)

## <a name="installing-and-releasing-hook-procedures"></a>Instalando e liberando procedimentos de gancho

Você pode instalar um procedimento de gancho chamando a função [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) e especificando o tipo de gancho que chama o procedimento, se o procedimento deve ser associado a todos os threads na mesma área de trabalho que o thread de chamada ou a um thread específico e um ponteiro para o ponto de entrada do procedimento.

Você deve colocar um procedimento de gancho global em uma DLL separada do aplicativo que está instalando o procedimento de gancho. O aplicativo de instalação deve ter o handle para o módulo DLL antes de poder instalar o procedimento de gancho. Para recuperar um handle para o módulo DLL, chame a [**função LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) com o nome da DLL. Depois de obter o handle, você pode chamar a [**função GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para recuperar um ponteiro para o procedimento de gancho. Por fim, use [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) para instalar o endereço do procedimento de gancho na cadeia de gancho apropriada. **SetWindowsHookEx** passa o identificador de módulo, um ponteiro para o ponto de entrada de procedimento de gancho e 0 para o identificador de thread, indicando que o procedimento de gancho deve ser associado a todos os threads na mesma área de trabalho que o thread de chamada. Essa sequência é mostrada no exemplo a seguir.

``` syntax
HOOKPROC hkprcSysMsg;
static HINSTANCE hinstDLL; 
static HHOOK hhookSysMsg; 
 
hinstDLL = LoadLibrary(TEXT("c:\\myapp\\sysmsg.dll")); 
hkprcSysMsg = (HOOKPROC)GetProcAddress(hinstDLL, "SysMessageProc"); 

hhookSysMsg = SetWindowsHookEx( 
                    WH_SYSMSGFILTER,
                    hkprcSysMsg,
                    hinstDLL,
                    0); 
```

Você pode liberar um procedimento de gancho específico de thread (remover seu endereço da cadeia de ganchos) chamando a [**função UnhookWindowsHookEx,**](/windows/win32/api/winuser/nf-winuser-unhookwindowshookex) especificando o alça para o procedimento de gancho a ser liberado. Libere um procedimento de gancho assim que seu aplicativo não precisar mais dele.

Você pode liberar um procedimento de gancho global usando [**UnhookWindowsHookEx,**](/windows/win32/api/winuser/nf-winuser-unhookwindowshookex)mas essa função não libera a DLL que contém o procedimento de gancho. Isso porque os procedimentos de gancho global são chamados no contexto de processo de cada aplicativo na área de trabalho, causando uma chamada implícita para a [**função LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) para todos esses processos. Como uma chamada para a [**função FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) não pode ser feita para outro processo, não há como liberar a DLL. O sistema eventualmente libera a DLL depois que todos os processos explicitamente vinculados à DLL foram encerrados ou chamados **de FreeLibrary** e todos os processos que chamam o procedimento de gancho retomaram o processamento fora da DLL.

Um método alternativo para instalar um procedimento de gancho global é fornecer uma função de instalação na DLL, juntamente com o procedimento de gancho. Com esse método, o aplicativo de instalação não precisa do handle para o módulo DLL. Ao vincular com a DLL, o aplicativo obtém acesso à função de instalação. A função de instalação pode fornecer o handle do módulo DLL e outros detalhes na chamada para [**SetWindowsHookEx.**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) A DLL também pode conter uma função que libera o procedimento de gancho global; o aplicativo pode chamar essa função de liberação de gancho ao encerrar.

## <a name="monitoring-system-events"></a>Monitorando eventos do sistema

O exemplo a seguir usa uma variedade de procedimentos de gancho específicos de thread para monitorar o sistema quanto a eventos que afetam um thread. Ele demonstra como processar eventos para os seguintes tipos de procedimentos de gancho:

-   **WH \_ CALLWNDPROC**
-   **CBT do WH \_**
-   **DEPURAÇÃO \_ DE WH**
-   **WH \_ GETMESSAGE**
-   **TECLADO \_ WH**
-   **WH \_ MOUSE**
-   **WH \_ MSGFILTER**

O usuário pode instalar e remover um procedimento de gancho usando o menu . Quando um procedimento de gancho é instalado e ocorre um evento monitorado pelo procedimento, o procedimento grava informações sobre o evento na área do cliente da janela principal do aplicativo.


```
#include <windows.h>
#include <strsafe.h>
#include "app.h"

#pragma comment( lib, "user32.lib") 
#pragma comment( lib, "gdi32.lib")

#define NUMHOOKS 7 
 
// Global variables 
 
typedef struct _MYHOOKDATA 
{ 
    int nType; 
    HOOKPROC hkprc; 
    HHOOK hhook; 
} MYHOOKDATA; 
 
MYHOOKDATA myhookdata[NUMHOOKS]; 

HWND gh_hwndMain;

// Hook procedures

LRESULT WINAPI CallWndProc(int, WPARAM, LPARAM);
LRESULT WINAPI CBTProc(int, WPARAM, LPARAM);
LRESULT WINAPI DebugProc(int, WPARAM, LPARAM);
LRESULT WINAPI GetMsgProc(int, WPARAM, LPARAM);
LRESULT WINAPI KeyboardProc(int, WPARAM, LPARAM);
LRESULT WINAPI MouseProc(int, WPARAM, LPARAM);
LRESULT WINAPI MessageProc(int, WPARAM, LPARAM);

void LookUpTheMessage(PMSG, LPTSTR);
 
LRESULT WINAPI MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    static BOOL afHooks[NUMHOOKS]; 
    int index; 
    static HMENU hmenu; 
 
    gh_hwndMain = hwndMain;
    
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Save the menu handle
 
            hmenu = GetMenu(hwndMain); 
 
            // Initialize structures with hook data. The menu-item identifiers are 
            // defined as 0 through 6 in the header file app.h. They can be used to 
            // identify array elements both here and during the WM_COMMAND message. 
 
            myhookdata[IDM_CALLWNDPROC].nType = WH_CALLWNDPROC; 
            myhookdata[IDM_CALLWNDPROC].hkprc = CallWndProc; 
            myhookdata[IDM_CBT].nType = WH_CBT; 
            myhookdata[IDM_CBT].hkprc = CBTProc; 
            myhookdata[IDM_DEBUG].nType = WH_DEBUG; 
            myhookdata[IDM_DEBUG].hkprc = DebugProc; 
            myhookdata[IDM_GETMESSAGE].nType = WH_GETMESSAGE; 
            myhookdata[IDM_GETMESSAGE].hkprc = GetMsgProc; 
            myhookdata[IDM_KEYBOARD].nType = WH_KEYBOARD; 
            myhookdata[IDM_KEYBOARD].hkprc = KeyboardProc; 
            myhookdata[IDM_MOUSE].nType = WH_MOUSE; 
            myhookdata[IDM_MOUSE].hkprc = MouseProc; 
            myhookdata[IDM_MSGFILTER].nType = WH_MSGFILTER; 
            myhookdata[IDM_MSGFILTER].hkprc = MessageProc; 
 
            // Initialize all flags in the array to FALSE. 
 
            memset(afHooks, FALSE, sizeof(afHooks)); 
 
            return 0; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                 // The user selected a hook command from the menu. 
 
                case IDM_CALLWNDPROC: 
                case IDM_CBT: 
                case IDM_DEBUG: 
                case IDM_GETMESSAGE: 
                case IDM_KEYBOARD: 
                case IDM_MOUSE: 
                case IDM_MSGFILTER: 
 
                    // Use the menu-item identifier as an index 
                    // into the array of structures with hook data. 
 
                    index = LOWORD(wParam); 
 
                    // If the selected type of hook procedure isn't 
                    // installed yet, install it and check the 
                    // associated menu item. 
 
                    if (!afHooks[index]) 
                    { 
                        myhookdata[index].hhook = SetWindowsHookEx( 
                            myhookdata[index].nType, 
                            myhookdata[index].hkprc, 
                            (HINSTANCE) NULL, GetCurrentThreadId()); 
                        CheckMenuItem(hmenu, index, 
                            MF_BYCOMMAND | MF_CHECKED); 
                        afHooks[index] = TRUE; 
                    } 
 
                    // If the selected type of hook procedure is 
                    // already installed, remove it and remove the 
                    // check mark from the associated menu item. 
 
                    else 
                    { 
                        UnhookWindowsHookEx(myhookdata[index].hhook); 
                        CheckMenuItem(hmenu, index, 
                            MF_BYCOMMAND | MF_UNCHECKED); 
                        afHooks[index] = FALSE; 
                    } 
 
                default: 
                    return (DefWindowProc(hwndMain, uMsg, wParam, 
                        lParam)); 
            } 
            break; 
 
            //
            // Process other messages. 
            //
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
/**************************************************************** 
  WH_CALLWNDPROC hook procedure 
 ****************************************************************/ 
 
LRESULT WINAPI CallWndProc(int nCode, WPARAM wParam, LPARAM lParam) 
{ 
    CHAR szCWPBuf[256]; 
    CHAR szMsg[16]; 
    HDC hdc; 
    static int c = 0; 
    size_t cch;
    HRESULT hResult; 
 
    if (nCode < 0)  // do not process message 
        return CallNextHookEx(myhookdata[IDM_CALLWNDPROC].hhook, nCode, wParam, lParam); 
 
    // Call an application-defined function that converts a message 
    // constant to a string and copies it to a buffer. 
 
    LookUpTheMessage((PMSG) lParam, szMsg); 
 
    hdc = GetDC(gh_hwndMain); 
 
    switch (nCode) 
    { 
        case HC_ACTION:
            hResult = StringCchPrintf(szCWPBuf, 256/sizeof(TCHAR),  
               "CALLWNDPROC - tsk: %ld, msg: %s, %d times   ", 
                wParam, szMsg, c++);
            if (FAILED(hResult))
            {
            // TODO: writer error handler
            }
            hResult = StringCchLength(szCWPBuf, 256/sizeof(TCHAR), &cch);
            if (FAILED(hResult))
            {
            // TODO: write error handler
            } 
            TextOut(hdc, 2, 15, szCWPBuf, cch); 
            break; 
 
        default: 
            break; 
    } 
 
    ReleaseDC(gh_hwndMain, hdc); 
    
    return CallNextHookEx(myhookdata[IDM_CALLWNDPROC].hhook, nCode, wParam, lParam); 
} 
 
/**************************************************************** 
  WH_GETMESSAGE hook procedure 
 ****************************************************************/ 
 
LRESULT CALLBACK GetMsgProc(int nCode, WPARAM wParam, LPARAM lParam) 
{ 
    CHAR szMSGBuf[256]; 
    CHAR szRem[16]; 
    CHAR szMsg[16]; 
    HDC hdc; 
    static int c = 0; 
    size_t cch; 
    HRESULT hResult;
 
    if (nCode < 0) // do not process message 
        return CallNextHookEx(myhookdata[IDM_GETMESSAGE].hhook, nCode, 
            wParam, lParam); 
 
    switch (nCode) 
    { 
        case HC_ACTION: 
            switch (wParam) 
            { 
                case PM_REMOVE:
                    hResult = StringCchCopy(szRem, 16/sizeof(TCHAR), "PM_REMOVE");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
                    break; 
 
                case PM_NOREMOVE:
                    hResult = StringCchCopy(szRem, 16/sizeof(TCHAR), "PM_NOREMOVE");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
                    break; 
 
                default:
                    hResult = StringCchCopy(szRem, 16/sizeof(TCHAR), "Unknown");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
                    break; 
            } 
 
            // Call an application-defined function that converts a 
            // message constant to a string and copies it to a 
            // buffer. 
 
            LookUpTheMessage((PMSG) lParam, szMsg); 
 
            hdc = GetDC(gh_hwndMain);
            hResult = StringCchPrintf(szMSGBuf, 256/sizeof(TCHAR), 
                "GETMESSAGE - wParam: %s, msg: %s, %d times   ", 
                szRem, szMsg, c++);
            if (FAILED(hResult))
            {
            // TODO: write error handler
            }
            hResult = StringCchLength(szMSGBuf, 256/sizeof(TCHAR), &cch);
            if (FAILED(hResult))
            {
            // TODO: write error handler
            } 
            TextOut(hdc, 2, 35, szMSGBuf, cch); 
            break; 
 
        default: 
            break; 
    } 
 
    ReleaseDC(gh_hwndMain, hdc); 
    
    return CallNextHookEx(myhookdata[IDM_GETMESSAGE].hhook, nCode, wParam, lParam); 
} 
 
/**************************************************************** 
  WH_DEBUG hook procedure 
 ****************************************************************/ 
 
LRESULT CALLBACK DebugProc(int nCode, WPARAM wParam, LPARAM lParam) 
{ 
    CHAR szBuf[128]; 
    HDC hdc; 
    static int c = 0; 
    size_t cch; 
    HRESULT hResult;
 
    if (nCode < 0)  // do not process message 
        return CallNextHookEx(myhookdata[IDM_DEBUG].hhook, nCode, 
            wParam, lParam); 
 
    hdc = GetDC(gh_hwndMain); 
 
    switch (nCode) 
    { 
        case HC_ACTION:
            hResult = StringCchPrintf(szBuf, 128/sizeof(TCHAR),   
                "DEBUG - nCode: %d, tsk: %ld, %d times   ", 
                nCode,wParam, c++);
            if (FAILED(hResult))
            {
            // TODO: write error handler
            }
            hResult = StringCchLength(szBuf, 128/sizeof(TCHAR), &cch);
            if (FAILED(hResult))
            {
            // TODO: write error handler
            } 
            TextOut(hdc, 2, 55, szBuf, cch); 
            break; 
 
        default: 
            break; 
    } 
 
    ReleaseDC(gh_hwndMain, hdc); 
    
    return CallNextHookEx(myhookdata[IDM_DEBUG].hhook, nCode, wParam, lParam); 
} 
 
/**************************************************************** 
  WH_CBT hook procedure 
 ****************************************************************/ 
 
LRESULT CALLBACK CBTProc(int nCode, WPARAM wParam, LPARAM lParam) 
{ 
    CHAR szBuf[128]; 
    CHAR szCode[128]; 
    HDC hdc; 
    static int c = 0; 
    size_t cch; 
    HRESULT hResult;
 
    if (nCode < 0)  // do not process message 
        return CallNextHookEx(myhookdata[IDM_CBT].hhook, nCode, wParam, 
            lParam); 
 
    hdc = GetDC(gh_hwndMain); 
 
    switch (nCode) 
    { 
        case HCBT_ACTIVATE:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_ACTIVATE");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_CLICKSKIPPED:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_CLICKSKIPPED");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_CREATEWND:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_CREATEWND");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_DESTROYWND:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_DESTROYWND");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_KEYSKIPPED:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_KEYSKIPPED");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_MINMAX:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_MINMAX");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_MOVESIZE:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_MOVESIZE");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_QS:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_QS");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_SETFOCUS:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_SETFOCUS");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_SYSCOMMAND:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_SYSCOMMAND");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        default:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "Unknown");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
    } 
    hResult = StringCchPrintf(szBuf, 128/sizeof(TCHAR), "CBT -  nCode: %s, tsk: %ld, %d times   ",
        szCode, wParam, c++);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    }
    hResult = StringCchLength(szBuf, 128/sizeof(TCHAR), &cch);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    } 
    TextOut(hdc, 2, 75, szBuf, cch); 
    ReleaseDC(gh_hwndMain, hdc); 
    
    return CallNextHookEx(myhookdata[IDM_CBT].hhook, nCode, wParam, lParam); 
} 
 
/**************************************************************** 
  WH_MOUSE hook procedure 
 ****************************************************************/ 
 
LRESULT CALLBACK MouseProc(int nCode, WPARAM wParam, LPARAM lParam) 
{ 
    CHAR szBuf[128]; 
    CHAR szMsg[16]; 
    HDC hdc; 
    static int c = 0; 
    size_t cch; 
    HRESULT hResult;
 
    if (nCode < 0)  // do not process the message 
        return CallNextHookEx(myhookdata[IDM_MOUSE].hhook, nCode, 
            wParam, lParam); 
 
    // Call an application-defined function that converts a message 
    // constant to a string and copies it to a buffer. 
 
    LookUpTheMessage((PMSG) lParam, szMsg); 
 
    hdc = GetDC(gh_hwndMain);
    hResult = StringCchPrintf(szBuf, 128/sizeof(TCHAR), 
        "MOUSE - nCode: %d, msg: %s, x: %d, y: %d, %d times   ", 
        nCode, szMsg, LOWORD(lParam), HIWORD(lParam), c++); 
    if (FAILED(hResult))
    {
    // TODO: write error handler
    }
    hResult = StringCchLength(szBuf, 128/sizeof(TCHAR), &cch);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    }
    TextOut(hdc, 2, 95, szBuf, cch); 
    ReleaseDC(gh_hwndMain, hdc); 
    
    return CallNextHookEx(myhookdata[IDM_MOUSE].hhook, nCode, wParam, lParam); 
} 
 
/**************************************************************** 
  WH_KEYBOARD hook procedure 
 ****************************************************************/ 
 
LRESULT CALLBACK KeyboardProc(int nCode, WPARAM wParam, LPARAM lParam) 
{ 
    CHAR szBuf[128]; 
    HDC hdc; 
    static int c = 0; 
    size_t cch; 
    HRESULT hResult;
 
    if (nCode < 0)  // do not process message 
        return CallNextHookEx(myhookdata[IDM_KEYBOARD].hhook, nCode, 
            wParam, lParam); 
 
    hdc = GetDC(gh_hwndMain);
    hResult = StringCchPrintf(szBuf, 128/sizeof(TCHAR), "KEYBOARD - nCode: %d, vk: %d, %d times ", nCode, wParam, c++);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    } 
    hResult = StringCchLength(szBuf, 128/sizeof(TCHAR), &cch);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    } 
    TextOut(hdc, 2, 115, szBuf, cch); 
    ReleaseDC(gh_hwndMain, hdc); 
    
    return CallNextHookEx(myhookdata[IDM_KEYBOARD].hhook, nCode, wParam, lParam); 
} 
 
/**************************************************************** 
  WH_MSGFILTER hook procedure 
 ****************************************************************/ 
 
LRESULT CALLBACK MessageProc(int nCode, WPARAM wParam, LPARAM lParam) 
{ 
    CHAR szBuf[128]; 
    CHAR szMsg[16]; 
    CHAR szCode[32]; 
    HDC hdc; 
    static int c = 0; 
    size_t cch; 
    HRESULT hResult;
 
    if (nCode < 0)  // do not process message 
        return CallNextHookEx(myhookdata[IDM_MSGFILTER].hhook, nCode, 
            wParam, lParam); 
 
    switch (nCode) 
    { 
        case MSGF_DIALOGBOX:
            hResult = StringCchCopy(szCode, 32/sizeof(TCHAR), "MSGF_DIALOGBOX");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case MSGF_MENU:
            hResult = StringCchCopy(szCode, 32/sizeof(TCHAR), "MSGF_MENU");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case MSGF_SCROLLBAR:
            hResult = StringCchCopy(szCode, 32/sizeof(TCHAR), "MSGF_SCROLLBAR");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        default:
            hResult = StringCchPrintf(szCode, 128/sizeof(TCHAR), "Unknown: %d", nCode);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    }
            break; 
    } 
 
    // Call an application-defined function that converts a message 
    // constant to a string and copies it to a buffer. 
 
    LookUpTheMessage((PMSG) lParam, szMsg); 
 
    hdc = GetDC(gh_hwndMain);
    hResult = StringCchPrintf(szBuf, 128/sizeof(TCHAR),  
        "MSGFILTER  nCode: %s, msg: %s, %d times    ", 
        szCode, szMsg, c++);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    } 
    hResult = StringCchLength(szBuf, 128/sizeof(TCHAR), &cch);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    } 
    TextOut(hdc, 2, 135, szBuf, cch); 
    ReleaseDC(gh_hwndMain, hdc); 
    
    return CallNextHookEx(myhookdata[IDM_MSGFILTER].hhook, nCode, wParam, lParam); 
}
```



 

 
