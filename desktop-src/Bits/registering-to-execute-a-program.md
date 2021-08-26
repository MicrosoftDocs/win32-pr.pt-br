---
title: Registrando para executar um programa
description: Você pode se registrar para que o BITS execute um programa com base em eventos de trabalho transferidos e de erro, mas não eventos modificados por trabalho. O BITS executa o programa no contexto do usuário.
ms.assetid: f1996d08-0e35-403b-9cdb-dae9e1c42e05
keywords:
- bits de notificação de eventos, linha de comando
- registrando para BITS de notificação de linha de comando
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: db86f67ad899d190b24d74bfb04c501ca7881351cfb2f37ef53300666622c317
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922026"
---
# <a name="registering-to-execute-a-program"></a>Registrando para executar um programa

Você pode se registrar para que o BITS execute um programa com base em eventos de trabalho transferidos e de erro, mas não eventos modificados por trabalho. O BITS executa o programa no contexto do usuário.

**Para registrar-se para executar um programa**

1.  Chame o **método IBackgroundCopyJob::QueryInterface** para recuperar um ponteiro de interface [**IBackgroundCopyJob2.**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) \_ \_ Especifique uuidof(IBackgroundCopyJob2) como o identificador de interface.
2.  Chame o [**método IBackgroundCopyJob2::SetNotifyCmdLine**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) para especificar o programa a ser executado e quaisquer argumentos exigidos pelo programa, como o identificador de trabalho.

3.  Chame o [**método IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) para especificar quando a linha de comando é executada.

    Você só pode especificar os sinalizadores de evento BG \_ NOTIFY JOB TRANSFERRED e \_ \_ BG NOTIFY JOB \_ \_ \_ ERROR. O sinalizador BG \_ NOTIFY JOB MODIFICATION é \_ \_ ignorado.

Observe que o BITS não executará o programa se você também estiver registrado para receber [retornos](registering-a-com-callback.md) de chamada COM e o ponteiro da interface de retorno de chamada for válido ou se o método de notificação que o BITS chamar retornará um código de êxito. No entanto, se o método de notificação retornar um código de falha, como E \_ FAIL, o BITS executará a linha de comando.

BITS chama a [**função CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) para iniciar o programa. Se você especificar uma cadeia de caracteres de parâmetro, o primeiro parâmetro deverá ser o nome do programa.

O exemplo a seguir mostra como registrar para executar um programa quando ocorre o evento transferido pelo trabalho. O exemplo pressupo que o ponteiro da interface [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) é válido.


```C++
#define MAX_PARAMETER_LEN 4000

HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob2* pJob2 = NULL;
WCHAR szJobId[48];
const WCHAR *pProgram = L"c:\\PATHHERE\\PROGRAMNAMEHERE.exe";
WCHAR szParameters[MAX_PARAMETER_LEN+1];
GUID JobId;
int rc;

hr = pJob->GetId(&JobId);
if (SUCCEEDED(hr))
{
  rc = StringFromGUID2(JobId, szJobId, ARRAYSIZE(szJobId));
  if (rc)
  {
    StringCchPrintf(szParameters, MAX_PARAMETER_LEN+1, L"%s %s", pProgram, szJobId);
    pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
    hr = pJob2->SetNotifyCmdLine(pProgram, szParameters);
    if (SUCCEEDED(hr))
    {
      hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED);
    }
    pJob2->Release();
    if (FAILED(hr))
    {
      //Handle error - unable to register for command line notification.
    }
  }
}
```



Quando o estado do trabalho se torna BG JOB STATE TRANSFERRED, o BITS executa o \_ programa especificado em \_ \_ pProgram. O exemplo a seguir é uma implementação simples de um programa que aceita um identificador de trabalho como um argumento. O programa supõe que o número correto de argumentos seja passado para ele.


```C++
#define WIN32_LEAN_AND_MEAN // Exclude rarely-used stuff from Windows headers
#include <windows.h>
#include <bits.h>
#include <strsafe.h>

int wmain(int argc, wchar_t *argv[])
{
 HRESULT hr;
 IBackgroundCopyManager *pManager = NULL;
 IBackgroundCopyJob *pJob = NULL;
 GUID JobId;
 LPWSTR pDisplayName = NULL;
 LPCWSTR pSuccessString = L" completed successfully.";
 LPWSTR pMessage;

 hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
 hr = CoCreateInstance(__uuidof(BackgroundCopyManager),
  NULL, CLSCTX_LOCAL_SERVER,
  __uuidof(IBackgroundCopyManager), (void**)&pManager);

 if (pManager)
 {
  hr = CLSIDFromString(argv[1], &JobId);
  if (SUCCEEDED(hr))
  {
   hr = pManager->GetJob(JobId, &pJob);
   if (SUCCEEDED(hr))
   {
    hr = pJob->GetDisplayName(&pDisplayName);
    if (SUCCEEDED(hr))
    {
     int messageLen = wcslen(pDisplayName) + wcslen(pSuccessString) + 1;
     pMessage = (WCHAR*)malloc(messageLen * sizeof(WCHAR));
     if (pMessage)
     {
      StringCchPrintf(pMessage, messageLen,
       L"%s%s", pDisplayName, pSuccessString);
      MessageBox(HWND_DESKTOP, pMessage, L"MyProgram - Transferred", MB_OK);
      free(pMessage);
     }
     else
     {
      hr = E_OUTOFMEMORY;
     }
     CoTaskMemFree(pDisplayName);
    }
    pJob->Release();
   }
  }
  pManager->Release();
 }

 CoUninitialize();
 return(hr);
}
```



 

 