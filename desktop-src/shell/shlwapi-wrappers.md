---
description: As tabelas neste documento listam invólucros de Shlwapi.dll que fornecem funcionalidade Unicode limitada ao Windows 95, Windows 98 e Windows Millennium Edition (Windows me).
title: Funções de wrapper SHLWAPI
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3c428c89-b650-48c1-9f91-b94f9f8e10e2
api_name:
- SHLWAPI Wrapper Functions
- AppendMenuWrapW
- CallWindowProcWrapW
- CharLowerWrapW
- CharUpperBufWrapW
- CharUpperWrapW
- CompareStringWrapW
- CopyFileWrapW
- CreateEventWrapW
- CreateFileWrapW
- CreateWindowExWrapW
- DefWindowProcWrapW
- DeleteFileWrapW
- DialogBoxParamWrapW
- DispatchMessageWrapW
- DragQueryFileWrapW
- DrawTextExWrapW
- DrawTextWrapW
- ExtTextOutWrapW
- FormatMessageWrapW
- GetClassInfoWrapW
- GetDateFormatW
- GetDateFormatWrapW
- GetDlgItemTextWrapW
- GetFileAttributesWrapW
- GetLocaleInfoWrapW
- GetMenuItemInfoWrapW
- GetModuleFileNameWrapW
- GetModuleHandleWrapW
- GetObjectWrapW
- GetOpenFileNameWrapW
- GetSaveFileNameWrapW
- GetSystemDirectoryWrapW
- GetTimeFormatWrapW
- GetWindowLongWrapW
- GetWindowsDirectoryWrapW
- GetWindowTextLengthWrapW
- GetWindowTextWrapW
- InsertMenuItemWrapW
- IsCharAlphaNumericWrapW
- IsCharAlphaWrapW
- IsCharUpperWrapW
- LoadLibraryWrapW
- LoadStringWrapW
- MessageBoxWrapW
- MLGetUILanguage
- MoveFileWrapW
- OutputDebugStringWrapW
- PeekMessageWrapW
- PostMessageWrapW
- RegCreateKeyExWrapW
- RegisterClassWrapW
- RegOpenKeyExWrapW
- RegQueryValueExW
- RegQueryValueExWrapW
- RegQueryValueWrapW
- RegSetValueExWrapW
- SendMessageWrapW
- SetDlgItemTextWrapW
- SetWindowLongWrapW
- SetWindowTextWrapW
- SHCancelTimerQueueTimer
- SHDeleteTimerQueue
- ShellExecuteExWrapW
- ShellMessageBoxWrapW
- SHGetFileInfoWrapW
- SHGetPathFromIDListWrapW
- SHInterlockedCompareExchange
- SHQueueUserWorkItem
- SHSetTimerQueueTimer
- TranslateAcceleratorWrapW
- UnregisterClassWrapW
api_type:
- NA
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 52e3a5b60a331a74ced1888d5a196348497c5ff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662561"
---
# <a name="shlwapi-wrapper-functions"></a>Funções de wrapper SHLWAPI

\[Essas funções estão disponíveis por meio do Windows XP Service Pack 2 (SP2) e do Windows Server 2003. Eles podem ser alterados ou indisponíveis nas versões subsequentes do Windows.\]

As tabelas neste documento listam invólucros de Shlwapi.dll que fornecem funcionalidade Unicode limitada ao Windows 95, Windows 98 e Windows Millennium Edition (Windows me).

O Windows 95, o Windows 98 e o Windows Millennium Edition (Windows me) são mencionados aqui como "plataformas ANSI nativas". Em plataformas ANSI nativas, essas funções de invólucro convertem os parâmetros de cadeia de caracteres de entrada Unicode para ANSI e chamam as versões ANSI das funções na coluna **encaminhar para** . Por exemplo, **AppendMenuWrapW** chama **AppendMenuA**, que é a versão ANSI do [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua). As outras funções seguem o mesmo padrão. Todas as cadeias de caracteres retornadas pela função ANSI são convertidas em Unicode e retornadas para o aplicativo de chamada. Além das exceções indicadas na coluna **comentários** , a função wrapper tem a mesma sintaxe e fornece a mesma funcionalidade que a função na coluna **encaminhar para** . Você deve consultar essa página de referência para obter informações detalhadas de uso.

**Aviso de segurança:** Várias cadeias de caracteres Unicode podem ser convertidas para a mesma cadeia ANSI. Colisões inesperadas após a conversão podem resultar em um comportamento inesperado. Por exemplo, se **CreateEventWrapW** for usado para criar dois eventos nomeados de forma diferente, cujos nomes correspondem após a conversão de Unicode para ANSI, a segunda chamada retornará um identificador para o mesmo evento que a primeira chamada, mesmo que as cadeias de caracteres Unicode originais fossem diferentes.

Os sistemas operacionais Microsoft Windows NT, Windows 2000, Windows XP, Windows Server 2003 e posteriores são mencionados aqui como "plataformas Unicode nativas". Para a maior parte, em plataformas Unicode nativas, essas funções de wrapper simplesmente encaminham parâmetros de cadeia de caracteres de entrada para a versão Unicode da função na coluna **encaminhar para** . Por exemplo, **AppendMenuWrapW** encaminha para **AppendMenuW**, que é a versão Unicode do [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua). As outras funções seguem o mesmo padrão. Todas as cadeias de caracteres retornadas pela função Unicode são retornadas para o aplicativo de chamada. Além das exceções indicadas na coluna **comentários** , a função wrapper tem a mesma sintaxe e fornece a mesma funcionalidade que a função na coluna **encaminhar para** . Você deve consultar essa página de referência para obter informações detalhadas de uso.

**Aviso de segurança:** Os problemas de segurança indicados para as funções na coluna **encaminhar para** também se aplicam às funções de wrapper correspondentes. Para obter detalhes, consulte a documentação de referência para a função na coluna **encaminhamentos para** .

As funções de wrapper nesta tabela estão todas contidas em Shlwapi.dll. Para chamá-los, você deve usar o ordinal listado na tabela.

> [!Note]  
> Essas funções de wrapper estão disponíveis no Windows XP, mas não fornecem nenhuma funcionalidade de wrapper no Windows XP Service Pack 2 (SP2) e posterior. Eles também não fornecem a funcionalidade de wrapper no Windows Server 2003. Em vez disso, você deve usar as funções listadas na coluna **encaminhar para** .

 



| Função                  | Ordinal | Encaminha para                                             | DLL      | Comentários                                                                                                                             |
|---------------------------|---------|---------------------------------------------------------|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| AppendMenuWrapW           | 36      | [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua)                     | USER32   | [(a)](#shlwapi-wrapper-functions), [(f)](#dragqueryfile), [(menu)](#menu)                                                           |
| CallWindowProcWrapW       | 37      | [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca)             | USER32   | [Encontrei](#shlwapi-wrapper-functions)                                                                                                   |
| CharLowerWrapW            | 38      | [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera)                       | KERNEL32 | [Oriental](#shlwapi-wrapper-functions)                                                                                                   |
| CharUpperBufWrapW         | 44      | [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)               | KERNEL32 | [Oriental](#shlwapi-wrapper-functions)                                                                                                   |
| CharUpperWrapW            | 43      | [**CharUpper**](/windows/win32/api/winuser/nf-winuser-charuppera)                       | KERNEL32 | [Oriental](#shlwapi-wrapper-functions)                                                                                                   |
| CompareStringWrapW        | 45      | [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)                 | KERNEL32 | [CompareString](#comparestring)                                                                                                   |
| CopyFileWrapW             | 112     | [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile)                             | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| CreateEventWrapW          | 51      | [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)                     | KERNEL32 | [um](#shlwapi-wrapper-functions)                                                                                                   |
| CreateFileWrapW           | 52      | [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea)                         | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| CreateWindowExWrapW       | 55      | [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)             | USER32   | [um](#shlwapi-wrapper-functions)                                                                                                   |
| DefWindowProcWrapW        | 56      | [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)               | USER32   | [Encontrei](#shlwapi-wrapper-functions)                                                                                                   |
| DeleteFileWrapW           | 57      | [**DeleteFile**](/windows/win32/api/fileapi/nf-fileapi-deletefilea)                         | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| DialogBoxParamWrapW       | 59      | [**DialogBoxParam**](/windows/win32/api/winuser/nf-winuser-dialogboxparama)             | USER32   | [(f)](#dragqueryfile), [(i)](#shlwapi-wrapper-functions), [(DialogBoxParam)](#dialogboxparam)                                       |
| DispatchMessageWrapW      | 60      | [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)           | USER32   | [Encontrei](#shlwapi-wrapper-functions)                                                                                                   |
| DragQueryFileWrapW        | 318     | [**DragQueryFile**](/windows/win32/api/Shellapi/nf-shellapi-dragqueryfilea)                  | SHELL32  | [(b)](#dialogboxparam), [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(DragQueryFile)](#dragqueryfile)               |
| DrawTextExWrapW           | 301     | [**DrawTextEx**](/windows/win32/api/winuser/nf-winuser-drawtextexa)                        | USER32   | [(a)](#shlwapi-wrapper-functions), [(d)](#shlwapi-wrapper-functions)                                                                |
| DrawTextWrapW             | 61      | [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)                            | USER32   | [um](#shlwapi-wrapper-functions)                                                                                                   |
| ExtTextOutWrapW           | 299     | [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)                        | GDI32    | [(d)](#shlwapi-wrapper-functions), [(f)](#dragqueryfile), [(ExtTextOut)](#exttextout)                                               |
| FormatMessageWrapW        | 68      | [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)                 | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(FormatMessage)](#formatmessage)                                       |
| GetClassInfoWrapW         | 69      | [**GetClassInfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa)                 | USER32   | [(GetClassInfo)](#getclassinfo)                                                                                                     |
| GetDateFormatWrapW        | 311     | [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata)                 | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(DateTime)](#datetime)                                                 |
| GetDlgItemTextWrapW       | 74      | [**GetDlgItemText**](/windows/win32/api/winuser/nf-winuser-getdlgitemtexta)             | USER32   | [m](#compareexchange)                                                                                                             |
| GetFileAttributesWrapW    | 75      | [**GetFileAttributes**](/windows/win32/api/fileapi/nf-fileapi-getfileattributesa)           | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| GetLocaleInfoWrapW        | 77      | [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)                 | KERNEL32 | [m](#compareexchange)                                                                                                             |
| GetMenuItemInfoWrapW      | 302     | [**GetMenuItemInfo**](/windows/win32/api/winuser/nf-winuser-getmenuiteminfoa)           | USER32   | [(f)](#dragqueryfile), [(g)](#compareexchange), [(MenuItemInfo)](#menuiteminfo)                                                     |
| GetModuleFileNameWrapW    | 80      | [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)         | KERNEL32 | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| GetModuleHandleWrapW      | 83      | [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)             | KERNEL32 | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| GetObjectWrapW            | 84      | [**GetObject**](/windows/win32/api/wingdi/nf-wingdi-getobject)                          | GDI32    | [m](#compareexchange)                                                                                                             |
| GetOpenFileNameWrapW      | 403     | [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea)           | COMDLG32 | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(g)](#compareexchange), [(da OPENFILENAME)](#openfilename)                 |
| GetSaveFileNameWrapW      | 389     | [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea)           | COMDLG32 | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(g)](#compareexchange), [(da OPENFILENAME)](#openfilename)                 |
| GetSystemDirectoryWrapW   | 81      | [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)       | KERNEL32 | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| GetTimeFormatWrapW        | 310     | [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata)                 | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(DateTime)](#datetime)                                                 |
| GetWindowLongWrapW        | 94      | [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)               | USER32   | [(WindowLong)](#windowlong)                                                                                                         |
| GetWindowsDirectoryWrapW  | 97      | [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)     | KERNEL32 | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| GetWindowTextLengthWrapW  | 96      | [**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)   | USER32   | [j](#j)                                                                                                                           |
| GetWindowTextWrapW        | 95      | [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)               | USER32   | [(f)](#dragqueryfile), [(g)](#compareexchange)                                                                                      |
| InsertMenuItemWrapW       | 98      | [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema)             | USER32   | [(a)](#shlwapi-wrapper-functions), [(f)](#dragqueryfile), [(menu)](#menu), [(MenuItemInfo)](#menuiteminfo)                          |
| IsCharAlphaWrapW          | 25      | [**IsCharAlpha**](/windows/win32/api/winuser/nf-winuser-ischaralphaa)                   | USER32   | [Oriental](#shlwapi-wrapper-functions)                                                                                                   |
| IsCharAlphaNumericWrapW   | 28      | [**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)     | KERNEL32 | [Oriental](#shlwapi-wrapper-functions)                                                                                                   |
| IsCharUpperWrapW          | 26      | [**IsCharUpper**](/windows/win32/api/winuser/nf-winuser-ischaruppera)                   | USER32   | [Oriental](#shlwapi-wrapper-functions)                                                                                                   |
| LoadLibraryWrapW          | 105     | [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)                     | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| LoadStringWrapW           | 107     | [**Cadeia de caracteres LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)                     | KERNEL32 | [Oriental](#shlwapi-wrapper-functions)                                                                                                   |
| MessageBoxWrapW           | 340     | [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox)                     | USER32   | [um](#shlwapi-wrapper-functions)                                                                                                   |
| MoveFileWrapW             | 113     | [**MoveFile**](/windows/win32/api/winbase/nf-winbase-movefile)                             | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| OutputDebugStringWrapW    | 115     | [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)         | KERNEL32 | [um](#shlwapi-wrapper-functions)                                                                                                   |
| PeekMessageWrapW          | 116     | [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)                   | USER32   | [(PeekMessage e a mensagem)](#peekmessage-and-postmessage)                                                                       |
| PostMessageWrapW          | 117     | [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)                   | USER32   | [(PeekMessage e a mensagem)](#peekmessage-and-postmessage)                                                                       |
| RegCreateKeyExWrapW       | 120     | [**RegCreateKeyEx**](/windows/win32/api/winreg/nf-winreg-regcreatekeyexa)               | ADVAPI32 | [um](#shlwapi-wrapper-functions)                                                                                                   |
| RegisterClassWrapW        | 131     | [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa)               | USER32   | [(a)](#shlwapi-wrapper-functions), [(registerClass)](#registerclass)                                                                |
| RegOpenKeyExWrapW         | 125     | [**Falha em RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)                   | ADVAPI32 | [um](#shlwapi-wrapper-functions)                                                                                                   |
| RegQueryValueExWrapW      | 128     | [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa)             | ADVAPI32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(ValueEx)](#regqueryvalueexw), [(RegQueryValueExW)](#regqueryvalueexw) |
| RegQueryValueWrapW        | 127     | [**RegQueryValue**](/windows/win32/api/winreg/nf-winreg-regqueryvaluea)                 | ADVAPI32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| RegSetValueExWrapW        | 130     | [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvalueexa)                 | ADVAPI32 | [(a)](#shlwapi-wrapper-functions), [(ValueEx)](#regqueryvalueexw)                                                                   |
| SendMessageWrapW          | 136     | [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)                   | USER32   | [SendMessage](#sendmessage)                                                                                                       |
| SetDlgItemTextWrapW       | 138     | [**SetDlgItemText**](/windows/win32/api/winuser/nf-winuser-setdlgitemtexta)             | USER32   | [um](#shlwapi-wrapper-functions)                                                                                                   |
| SetWindowLongWrapW        | 141     | [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)               | USER32   | [(WindowLong)](#windowlong)                                                                                                         |
| SetWindowTextWrapW        | 143     | [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta)               | USER32   | [um](#shlwapi-wrapper-functions)                                                                                                   |
| ShellExecuteExWrapW       | 35      | [**ShellExecuteEx**](/windows/win32/api/Shellapi/nf-shellapi-shellexecuteexa)                | SHELL32  | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(ShellExecuteEx)](#shellexecuteex)                                      |
| ShellMessageBoxWrapW      | 388     | [**ShellMessageBox**](/windows/win32/api/Shellapi/nf-shellapi-shellmessageboxa)              | SHLWAPI  | [(a)](#shlwapi-wrapper-functions), [(FormatMessage)](#formatmessage)                                                                |
| SHGetFileInfoWrapW        | 313     | [**SHGetFileInfo**](/windows/win32/api/Shellapi/nf-shellapi-shgetfileinfoa)                  | SHELL32  | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(g)](#compareexchange)                                                  |
| SHGetPathFromIDListWrapW  | 334     | [**SHGetPathFromIDList**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista)      | USER32   | [m](#compareexchange)                                                                                                             |
| TranslateAcceleratorWrapW | 146     | [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) | USER32   | [Encontrei](#shlwapi-wrapper-functions)                                                                                                   |
| UnregisterClassWrapW      | 147     | [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa)           | USER32   | [um](#shlwapi-wrapper-functions)                                                                                                   |



 

As funções de wrapper na tabela a seguir não executam nenhuma conversão de conjunto de caracteres. Em vez disso, eles fornecem suporte limitado para os recursos do sistema operacional não disponíveis em plataformas anteriores.



| Função                     | Ordinal | Encaminha para                                                                     | DLL      | Comentários                                                                        |
|------------------------------|---------|---------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------|
| MLGetUILanguage              | 376     | [**GetUserDefaultUILanguage**](/windows/win32/api/winnls/nf-winnls-getuserdefaultuilanguage)                   | KERNEL32 | [t](#shlwapi-wrapper-functions)                                              |
| SHCancelTimerQueueTimer      | 265     | [**DeleteTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer)                         | KERNEL32 | [t](#shlwapi-wrapper-functions)                                              |
| SHDeleteTimerQueue           | 262     | [**DeleteTimerQueue**](/windows/win32/api/winbase/nf-winbase-deletetimerqueue)                                   | KERNEL32 | [t](#shlwapi-wrapper-functions)                                              |
| SHInterlockedCompareExchange | 342     | [**InterlockedCompareExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchangepointer) | KERNEL32 | [CompareExchange](#compareexchange)                                          |
| SHQueueUserWorkItem          | 260     | [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem)                                 | KERNEL32 | [(QueueUserWorkItem)](#queueuserworkitem), [(h)](#shlwapi-wrapper-functions)   |
| SHSetTimerQueueTimer         | 263     | [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer)                         | KERNEL32 | [(SetTimerQueueTimer)](#settimerqueuetimer), [(h)](#shlwapi-wrapper-functions) |



 

## <a name="remarks"></a>Comentários

### <a name="a"></a>um

Se a conversão de cadeia de caracteres for necessária, todas as cadeias serão convertidas por meio da \_ página de código CP ACP.

Essas funções empregam os melhores caracteres de ajuste e não executam a verificação padrão ao converter de Unicode em ANSI. Além disso, se a cadeia de caracteres não puder ser convertida de Unicode para ANSI, a função de wrapper passará uma cadeia de caracteres **nula** para a função ANSI subjacente. Isso pode ocorrer, por exemplo, quando não há memória suficiente. A passagem de uma cadeia de caracteres **nula** pode fazer com que algumas funções falhem com um erro de parâmetro inválido, mas outras funções aceitam a cadeia de caracteres **nula** e a tratam como o parâmetro pretendido. Por exemplo, um erro ocorre quando a função **CreateWindowExWrapW** tenta converter o parâmetro *lpWindowName* em ANSI e [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) cria uma janela com uma legenda vazia. O wrapper não notifica você quando ocorreram esses problemas.

O Microsoft Layer for Unicode (MSLU) verifica erros durante a conversão de Unicode para ANSI e retorna os valores de erro apropriados. Por exemplo, a função de invólucro [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) no MSLU retornará 0 se o item não tiver sido acrescentado com êxito.

### <a name="b"></a>b

Essas funções usam um link com atraso carregado para a função apropriada. Isso significa que a DLL que contém a função na coluna "encaminhar para" não é carregada pelo Shlwapi.dll até que uma função nessa DLL seja chamada. O vinculador Microsoft Visual C++ dá suporte a essa funcionalidade mais geralmente por meio da opção/DELAYLOAD.

### <a name="c"></a>&

Essa função manipula nomes de File. Conforme observado em [(a)](#shlwapi-wrapper-functions), as funções convertem todas as cadeias de caracteres por meio da página de código do CP \_ ACP. Eles não verificam se as funções de e/s de arquivo foram definidas para o modo ANSI. Se as funções de e/s de arquivo estiverem no modo OEM, as cadeias de caracteres serão convertidas de e para o conjunto de caractere errado. Um aplicativo pode definir as funções de e/s de arquivo para o modo OEM explicitamente chamando a função [**SetFileApisToOEM**](/windows/win32/api/fileapi/nf-fileapi-setfileapistooem) .

* * Aviso de segurança: * * o uso dessas funções de wrapper para nomes de arquivos pode comprometer a segurança do seu aplicativo. Como nenhuma verificação padrão é executada e os melhores caracteres de ajuste são empregados, os caracteres de nome de arquivo podem ser convertidos de maneiras inesperadas. Isso pode resultar em ataques de falsificação do sistema de arquivos. Além disso, a perda de dados silenciosa pode ocorrer durante a conversão de Unicode para ANSI.

O MSLU não tem essas limitações.

### <a name="d"></a>3D

Se a cadeia de caracteres que está sendo desenhada exigir um conjunto de caracteres que não esteja disponível na fonte selecionada no contexto do dispositivo, essas funções de wrapper usarão o recurso de [vinculação de fontes](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767872(v=vs.85)) da biblioteca [MLang](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767865(v=vs.85)) para renderizar cada caractere em uma fonte apropriada. Ao contrário da maioria das outras funções de wrapper, elas são funcionais no Microsoft Windows NT 4,0, além das plataformas ANSI nativas.

### <a name="e"></a>Oriental

As implementações Unicode completas dessas funções estão disponíveis em plataformas ANSI nativas. Essas funções não chamam a função ANSI relacionada.

### <a name="f"></a>fixo

Se o idioma da interface do usuário padrão usa um conjunto de caracteres diferente do idioma da interface de usuário padrão do sistema, o sistema tenta reescrever modelos de caixa de diálogo e controles de subclasse e converter itens de menu para o desenho proprietário, para que as cadeias de caracteres no idioma da interface do usuário padrão continuem a ser exibidas corretamente. Os únicos controles suportados pelas regras de reescrita de modelo de caixa de diálogo são controles estáticos, botões, caixas de listagem e caixas de combinação. Esses controles são subclasse de forma que a função **SendMessageWrapW** possa obter a cadeia de caracteres Unicode original sem ser traduzida por meio do conjunto de caracteres ANSI. Ao contrário da maioria das outras funções de wrapper, elas são funcionais no Microsoft Windows NT 4,0, bem como em plataformas ANSI nativas. Consulte os comentários na documentação da função [**MLLoadLibrary**](./callbacks.md) para obter mais informações sobre como o idioma da interface do usuário padrão do sistema e o idioma da interface de usuário padrão são determinados.

### <a name="g"></a>m

Se a conversão de cadeia de caracteres for necessária, todas as cadeias serão convertidas por meio da \_ página de código CP ACP.

Ao converter de ANSI em Unicode para saída, se a cadeia de caracteres retornada não couber no buffer que foi fornecido, as funções de wrapper truncarão a cadeia de caracteres. Essas funções que retornam o número de caracteres copiados para o buffer ou o número de caracteres necessários para evitar o truncamento não retornam o número de caracteres Unicode copiados para o buffer fornecido pelo ou exigidos pelo chamador da função de wrapper. Eles retornam o número de caracteres ANSI copiados para o buffer ou exigidos pela função ANSI subjacente. O MSLU não tem essas limitações.

### <a name="h"></a>t

Em sistemas anteriores ao Windows XP, essas funções implementam um pool de threads e uma fila de temporizador simplificados. No Windows XP e posterior, essas funções usam o pool de threads do sistema e a fila de timer do sistema. Para as funções de fila de timer, o parâmetro *hQueue* deve ser definido como **NULL** para indicar que a operação será executada na fila de temporizador padrão.

### <a name="i"></a>Encontrei

Em plataformas Unicode, essas funções convertem a mensagem de Unicode para ANSI se a janela de destino for ANSI. Essas funções não executam a conversão de mensagens em plataformas ANSI nativas. Portanto, chamar aplicativos que chamam essa função deve garantir que a mensagem esteja no formato Unicode em plataformas Unicode e no formato ANSI em plataformas ANSI. Por exemplo, na chamada de função a seguir, o *wParam* deve ser um ponto de código Unicode se o programa estiver sendo executado em uma plataforma Unicode e deverá ser um caractere ANSI se o programa estiver sendo executado em uma plataforma ANSI.

``` syntax
CallWindowProcWrapW(prevWndProc, hwnd, WM_CHAR, wParam, lParam);
```

O MSLU rastreia o conjunto de caracteres do procedimento de janela de destino e converte a mensagem conforme necessário.

### <a name="j"></a>j

Em plataformas ANSI, essas funções retornam o comprimento da cadeia de caracteres ANSI subjacente, não o comprimento da cadeia de caracteres Unicode traduzida. O MSLU não tem essas limitações.

### <a name="compareexchange"></a>CompareExchange

A sintaxe de **SHInterlockedCompareExchange** é um pouco diferente da do [**InterlockedCompareExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchangepointer), mas funciona de forma idêntica.

``` syntax
void* SHInterlockedCompareExchange(void **ppDest, void *pExch, void *pComp);
```

### <a name="comparestring"></a>CompareString

Lembre-se de que em plataformas ANSI nativas, ambas as cadeias de caracteres são convertidas em ANSI e comparadas como cadeias Se as cadeias de caracteres Unicode contiverem personagens que não podem ser representados em ANSI, os resultados poderão ser inesperados. Por exemplo, se a página de código ANSI padrão não der suporte a caracteres CJK, as cadeias L " \\ x66F0" e l " \\ x6708" compararão como iguais em plataformas ANSI nativas porque ambas mapeiam para a cadeia de caracteres ANSI "?".

### <a name="datetime"></a>Horário

No Shlwapi.dll versão 5,0, que é fornecida com o Windows 2000, a página de código do identificador de localidade que você passa como o primeiro parâmetro de **GetDateFormatWrapW** e **GetTimeFormatWrapW** deve corresponder à página de código ANSI atual. Caso contrário, a cadeia de caracteres retornada pode ser convertida incorretamente. Essa limitação não se aplica a Shlwapi.dll versões 5,5 ou superiores. Isso significa que o Windows XP e os sistemas posteriores não estão sujeitos a essa limitação. O MSLU não tem essa limitação.

### <a name="dialogboxparam"></a>(DialogBoxParam)

O parâmetro *lpTemplateName* da função **DialogBoxParamWrapW** não pode ser uma cadeia de caracteres. Ele deve ser um ordinal criado pela macro [**MAKEINTRESOURCE**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) . O procedimento de caixa de diálogo especificado pelo parâmetro *lpDialogFunc* recebe mensagens ANSI em plataformas ANSI nativas e mensagens Unicode em plataformas Unicode nativas. O procedimento da caixa de diálogo deve estar preparado para lidar com ambos os casos. O MSLU não tem essas limitações.

### <a name="exttextout"></a>ExtTextOut

As plataformas ANSI nativas implementam a função [**ExtTextOutW**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) , bem como as plataformas Unicode nativas. A finalidade de **ExtTextOutWrapW** é executar a vinculação de fontes, conforme descrito em um comentário separado.

### <a name="dragqueryfile"></a>(DragQueryFile)

A função **DragQueryFileWrapW** não permite que você consulte o comprimento de um arquivo na alça de descarte passando **NULL** como o parâmetro *lpszFile* . O MSLU não tem essas limitações.

### <a name="formatmessage"></a>FormatMessage

Em plataformas ANSI nativas, os formatos na cadeia de caracteres não são convertidos de Unicode para ANSI. Por exemplo, o exemplo de código a seguir está em erro.


```
WCHAR szBuffer[MAX_PATH];
DWORD_PTR Arguments[2] = { L"String1", L"String2" };

FormatMessageWrapW(FORMAT_MESSAGE_FROM_STRING, 
               L"%1!s! %2", 
               0, 0, 
               szBuffer, 
               MAX_PATH, 
               (va_list*)Arguments);
```



Este exemplo de código usa "! s!" . Em plataformas ANSI nativas, essa cadeia de caracteres é passada para a versão ANSI da função [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) . Consequentemente, uma cadeia de caracteres ANSI é esperada em vez de uma cadeia de caracteres Unicode. Da mesma forma, o formato "%2" implica um argumento de cadeia de caracteres. Quando passado para a função de **FormatMessage** ANSI, ele é interpretado como uma cadeia de caracteres ANSI em vez de uma cadeia de caracteres Unicode. A cadeia de caracteres de formato correta é L "%1! ws! %2! WS! ". Isso imprime cadeias de caracteres corretamente em plataformas ANSI e Unicode.

A função não dá suporte a "%0" Cadeia de caracteres de formato especial.

O MSLU não tem essas limitações.

### <a name="getclassinfo"></a>(GetClassInfo)

Em plataformas ANSI nativas, os membros **lpszMenuName** e **LpszClassName** da estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) não são convertidos em Unicode e são sempre definidos como **NULL**. Além disso, o procedimento de janela retornado no membro **lpfnWndProc** da estrutura **WNDCLASS** não é convertido em Unicode e se refere a um procedimento de janela ANSI. O MSLU não tem essas limitações.

### <a name="menu"></a>AdicionarMenu

No Shlwapi.dll versão 5,0, que acompanha o Windows 2000, as cadeias de caracteres do item de menu que contiverem caractere de tabulação ( \\ t) podem não ser exibidas corretamente. Essa limitação não se aplica a Shlwapi.dll versões 5,5 ou superiores. Isso significa que o Windows XP e os sistemas posteriores não estão sujeitos a essa limitação. O MSLU não tem essa limitação.

### <a name="menuiteminfo"></a>MenuItemInfo

Essa função dá suporte apenas à versão do Microsoft Windows NT 4,0 da estrutura [**MENUITEMINFOW**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) . Essa estrutura não tem um membro **hbmpItem** . Além disso, a função não oferece suporte ao \_ sinalizador de bitmap MIIM. O MSLU não tem essas limitações.

### <a name="openfilename"></a>Da OPENFILENAME

O membro **cbSize** da estrutura [**OPENFILENAMEW**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) deve ser definido como sizeof (da OPENFILENAME \_ NT4W).

O membro **lpstrCustomFilter** da estrutura [**OPENFILENAMEW**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) deve ser definido como **nulo**.

Os valores dos membros **nMaxFile** e **NMaxFileTitle** da estrutura [**OPENFILENAMEW**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) não devem exceder o \_ caminho máximo.

Se o membro **lpfnHook** da estrutura [**OPENFILENAMEW**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) não for **nulo**, ele deverá se referir a um procedimento de gancho ANSI em plataformas ANSI nativas e um procedimento de gancho Unicode em plataformas Unicode nativas.

O MSLU não tem essas limitações.

### <a name="peekmessage-and-postmessage"></a>(PeekMessage e a mensagem)

Em plataformas ANSI nativas, nenhuma conversão é executada na mensagem transmitida ou recuperada. A mensagem transmitida/recuperada é ANSI em plataformas ANSI nativas e Unicode em plataformas Unicode nativas. O aplicativo de chamada deve estar preparado para lidar com ambos os casos. Por exemplo, se a mensagem recuperada for WM \_ Char, o *wParam* é um código de caractere ANSI em plataformas ANSI nativas, mas é um ponto de código Unicode em plataformas Unicode nativas. O MSLU não tem essas limitações.

### <a name="queueuserworkitem"></a>QueueUserWorkItem

A função **SHQueueUserWorkItem** é ligeiramente diferente da função [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) correspondente. A sintaxe para **SHQueueUserWorkItem** é mostrada aqui.

``` syntax
BOOL SHQueueUserWorkItem(LPTHREAD_START_ROUTINE pfnCallback,
                     LPVOID pContext,
                     LONG lPriority,
                     DWORD_PTR dwTag,
                     DWORD_PTR * pdwId,
                     LPCSTR pszModule,
                     DWORD dwFlags);
```

Os parâmetros devem ser definidos da seguinte maneira:

-   Os parâmetros *pfnCallback* e *pContext* têm os mesmos significados que os parâmetros de *função* e de *contexto* , respectivamente, de [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem).
-   O parâmetro *dwTag* não é usado e deve ser definido como 0.
-   O parâmetro *pdwld* não é usado e deve ser definido como **NULL**.
-   O parâmetro *pszModule* aponta para uma cadeia de caracteres ANSI opcional terminada em NULL que especifica o nome de uma biblioteca a ser carregada antes de o item de trabalho ser iniciado e descarregado após a conclusão do item de trabalho. Este parâmetro pode ser **NULL**.
-   O parâmetro *dwFlags* dá suporte a apenas um subconjunto dos valores com suporte pelo [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem). Os sinalizadores a seguir são reconhecidos.

    

    | Name              | Valor      | Significado                          |
    |-------------------|------------|----------------------------------|
    | \_EXECUTEIO TPS    | 0x00000001 | O mesmo que WT \_ EXECUTEINIOTHREAD.   |
    | \_LONGEXECTIME TPS | 0x00000008 | O mesmo que WT \_ EXECUTELONGFUNCTION. |

    

     

    > [!Note]  
    > O sinalizador LONGEXECTIME de TPS não \_ tem o mesmo valor numérico que o sinalizador WT \_ EXECUTELONGFUNCTION. Ao usar **SHQueueUserWorkItem**, o parâmetro dwFlags deve ser uma combinação de valores de TPS \_ \* , não valores de WT \_ \* .

     

**SHQueueUserWorkItem** retornará um valor diferente de zero se o item de trabalho tiver sido enfileirado com êxito e 0 caso contrário. Se a função falhar, você poderá usar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter informações adicionais.

### <a name="registerclass"></a>RegisterClass

Em plataformas ANSI nativas, nenhuma conversão é executada no membro **lpfnWndProc** da estrutura [**WNDCLASSW**](/windows/win32/api/winuser/ns-winuser-wndclassa) . A janela receberá mensagens de janela ANSI em plataformas ANSI nativas e mensagens de janela Unicode em plataformas Unicode nativas. O procedimento de janela deve estar preparado para lidar com ambos os casos. O MSLU não tem essas limitações.

### <a name="regqueryvalueexw"></a>(RegQueryValueExW)

**RegQueryValueExWrapW** também foi chamado com o nome **RegQueryValueExW**. Assim como acontece com qualquer função sem nome exportada estritamente por ordinal, você pode escolher o nome do qual a função é conhecida em seu código.

### <a name="sendmessage"></a>SendMessage

Em plataformas Unicode nativas, a função **SendMessageWrapW** encaminha para a função [**SendMessageW**](/windows/win32/api/winuser/nf-winuser-sendmessage) . Em plataformas ANSI nativas, o **SendMessageWrapW** fornece suporte limitado para a tradução de mensagens Unicode para ANSI. A lista de mensagens com suporte é fornecida na tabela a seguir. A função não converterá nenhuma outra mensagem.

O MSLU não tem essas limitações.



|                      |                                                                                                           |
|----------------------|-----------------------------------------------------------------------------------------------------------|
| AddString CB \_        | (b) (f) (c)                                                                                               |
| localização da CB \_       | (b) (f) (c)                                                                                               |
| \_FINDSTRINGEXACT CB  | (a) (f) (c)                                                                                               |
| \_GETLBTEXT CB        | (b) (f) (c) (o) o buffer passado no parâmetro *lParam* deve ter espaço para pelo menos 256 caracteres.   |
| \_GETLBTEXTLEN CB     | um                                                                                                       |
| inserção de CB \_     | (b) (f) (c)                                                                                               |
| seleção do CB \_     | (b) (f) (c)                                                                                               |
| em \_ CHARFROMPOS      |                                                                                                           |
| em \_ GETline          | (e) o valor de retorno é o número de caracteres ANSI copiados.                                             |
| em \_ GETSEL           |                                                                                                           |
| em \_ REPLACESEL       | (b) (f)                                                                                                   |
| em \_ SETpasswordchar  | um                                                                                                       |
| em \_ SETSEL           |                                                                                                           |
| em \_ SETWORDBREAKPROC | Esta mensagem não tem nenhum efeito. O procedimento de quebra de palavra não está definido.                                          |
| seqüência de caracteres de LB \_        | (b) (f) (d)                                                                                               |
| Localizar LBstring \_       | (b) (f) (d)                                                                                               |
| \_FINDSTRINGEXACT lb  | (b) (f) (lbs)                                                                                             |
| LB \_ GETtext          | (b) (f) (lbs) (o) o buffer passado no parâmetro *lParam* deve ter espaço para pelo menos 256 caracteres. |
| \_GETTEXTLEN lb       | um                                                                                                       |
| KG \_ InsertString     | (b) (f) (d)                                                                                               |
| seleção de LBstring \_     | (b) (f) (d)                                                                                               |
| WM \_ GETtext          | (b) (f)                                                                                                   |
| GETTEXTLENGTH do WM \_    | um                                                                                                       |
| SetText do WM \_          | (b) (f)                                                                                                   |
| SETTINGCHANGE do WM \_    | (a) a mensagem é enviada com um tempo limite de três segundos.                                                  |



 


-   (a) a cadeia de caracteres ANSI que está sendo medida ou recuperada deve atender à seguinte condição: o comprimento da versão Unicode correspondente da cadeia de caracteres não pode exceder o comprimento da versão ANSI da cadeia de caracteres. Se essa condição não for atendida, o comprimento retornado será curto. Se não houver memória suficiente para determinar o comprimento da cadeia de caracteres Unicode, a função retornará zero, não o LB \_ Err ou CB \_ Err, como pode ser esperado.
-   (b) se a conversão de cadeia de caracteres for necessária, todas as cadeias serão convertidas por meio da página de código do CP \_ ACP.

    Essa função emprega caracteres de melhor ajuste e não executa a verificação padrão ao converter de Unicode em ANSI. Além disso, se a cadeia de caracteres não puder ser convertida de Unicode para ANSI, a função passará uma cadeia de caracteres nula para a função ANSI subjacente. Isso pode ocorrer, por exemplo, quando não há memória suficiente. A passagem de uma cadeia de caracteres nula pode fazer com que algumas funções falhem com um erro de parâmetro inválido, mas outras funções aceitam a cadeia de caracteres nula e a tratam como o parâmetro pretendido. Por exemplo, se ocorrer um erro quando o wrapper do WM \_ SetText tentar converter o título da janela para ANSI, a janela terá uma legenda vazia. A função não o notifica quando ocorrerem esses problemas. O MSLU não tem essas limitações.

-   (c) o identificador de janela especificado deve ser o identificador para um controle [ComboBox](../controls/combo-boxes.md) ou [ComboBoxEx](../controls/comboboxex-controls.md) . Se o identificador for para um controle ComboBox que tem o desenho proprietário e não foi criado com o estilo de [caixa de listagem](../controls/list-box-styles.md) , a tradução dessa mensagem falhará e poderá até falhar.
-   (d) o identificador de janela especificado deve ser o identificador para um controle ListBox. Se a ListBox for de desenho proprietário e não tiver sido criada com o estilo de [estilos da caixa de listagem](../controls/list-box-styles.md) , a tradução dessa mensagem falhará e poderá até falhar.
-   (e) se a conversão de cadeia de caracteres for necessária, todas as cadeias serão convertidas por meio da página de código do CP \_ ACP.

    Ao converter de ANSI em Unicode para saída, as funções de wrapper truncarão a cadeia de caracteres retornada se ela não couber no buffer fornecido. O valor de retorno para funções que retornam o número de caracteres copiados para o buffer ou o número de caracteres necessários para evitar truncamento refere-se ao número de caracteres ANSI copiados para o buffer ou exigidos pela função ANSI subjacente, não o número de caracteres Unicode copiados para o buffer fornecido pelo ou exigidos pelo aplicativo de chamada que chamou a função de wrapper. O MSLU não tem essa limitação. Para obter mais detalhes, consulte [Microsoft Layer for Unicode em sistemas Windows 95/98/me](/previous-versions/ms812865(v=msdn.10)).

### <a name="settimerqueuetimer"></a>(SetTimerQueueTimer)

A função **SHSetTimerQueueTimer** é ligeiramente diferente da função [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) correspondente. A sintaxe dela é a seguinte:

``` syntax
HANDLE SHSetTimerQueueTimer(HANDLE hQueue,
                        WAITORTIMERCALLBACK pfnCallback,
                        LPVOID pContext,
                        DWORD dwDueTime,
                        DWORD dwPeriod,
                        LPCSTR lpszLibrary,
                        DWORD dwFlags);
```

Os parâmetros devem ser definidos da seguinte maneira:

-   O parâmetro *hQueue* deve ser definido como **NULL**, especificando a fila de temporizador padrão.
-   Os parâmetros *pfnCallback*, *pContext*, *dwDueTime* e *dwPeriod* têm os mesmos significados que os parâmetros de *retorno de chamada*, *parâmetro*, *DueTime* e *período* , respectivamente, de [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer).
-   O parâmetro *lpszLibrary* não é usado e deve ser definido como **NULL**.
-   O parâmetro *flags* dá suporte a apenas um subconjunto dos valores com suporte pelo [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer).

    

    | Name              | Valor      | Significado                         |
    |-------------------|------------|---------------------------------|
    | \_EXECUTEIO TPS    | 0x00000001 | O mesmo que WT \_ EXECUTEINIOTHREAD   |
    | \_LONGEXECTIME TPS | 0x00000008 | O mesmo que WT \_ EXECUTELONGFUNCTION |

    

     

    > [!Note]  
    > O sinalizador LONGEXECTIME de TPS não \_ tem o mesmo valor numérico que o sinalizador WT \_ EXECUTELONGFUNCTION. Ao usar **SHSetTimerQueueTimer**, o parâmetro *dwFlags* deve ser uma combinação de valores de TPS \_ \* , não valores de WT \_ \* .

     

**SHSetTimerQueueTimer** retorna o identificador do temporizador criado em caso de êxito e **NULL** caso contrário.

### <a name="shellexecuteex"></a>ShellExecuteEx

O membro **lpFile** da estrutura [**SHELLEXECUTEINFO**](/windows/win32/api/Shellapi/ns-shellapi-shellexecuteinfoa) passado nesse parâmetro somente da função pode não exceder os \_ caracteres do comprimento máximo da URL da Internet \_ \_ . Se o \_ sinalizador ver máscara \_ CLASSNAME for omitido, o membro **lpClass** deverá ser inicializado como **NULL**.

### <a name="valueex"></a>(ValueEx)

Somente os seguintes tipos de dados de registro têm suporte: REG \_ sz, Reg \_ expande \_ sz, REG \_ Binary e Reg \_ DWORD. Ao contrário dessas funções de wrapper, o MSLU também dá suporte ao REG \_ multi \_ Expand \_ sz.

### <a name="windowlong"></a>(WindowLong)

Em plataformas ANSI nativas, a função não executa nenhuma tradução em nenhum dos longos de janela. Por exemplo, se você passar GWLP \_ WndProc, a função retornará o procedimento de janela ANSI, não uma conversão. O MSLU não tem essas limitações.

 

 
