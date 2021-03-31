---
title: Registrando para executar um programa
description: Você pode se registrar para que o BITS execute um programa com base nos eventos de trabalho e transferidos, mas não nos eventos de modificação de trabalho. O BITS executa o programa no contexto do usuário.
ms.assetid: f1996d08-0e35-403b-9cdb-dae9e1c42e05
keywords:
- BITS de notificação de eventos, linha de comando
- Registrando para BITS de notificação de linha de comando
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 7831a959a73112b21bdf3e0fbc2b7d3dd4f6a447
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641311"
---
# <a name="registering-to-execute-a-program"></a>Registrando para executar um programa

Você pode se registrar para que o BITS execute um programa com base nos eventos de trabalho e transferidos, mas não nos eventos de modificação de trabalho. O BITS executa o programa no contexto do usuário.

**Para se registrar para executar um programa**

1.  Chame o método **método ibackgroundcopyjob:: QueryInterface** para recuperar um ponteiro de interface [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) . Especifique \_ \_ uuidof (IBackgroundCopyJob2) como o identificador de interface.
2.  Chame o método [**IBackgroundCopyJob2:: SetNotifyCmdLine**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) para especificar o programa a ser executado e os argumentos exigidos pelo programa, como o identificador de trabalho.

3.  Chame o método [**método ibackgroundcopyjob:: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) para especificar quando a linha de comando é executada.

    Você só pode especificar os \_ sinalizadores de evento de erro BG notificar \_ trabalho \_ transferido e BG \_ Notify \_ Job \_ . O \_ sinalizador de modificação do trabalho BG Notify \_ \_ é ignorado.

Observe que o BITS não executará o programa se você também estiver [registrado para receber retornos de chamada com](registering-a-com-callback.md) e o ponteiro da interface de retorno de chamada for válido ou se o método de notificação que o bits chamar retornar um código de êxito. No entanto, se o método de notificação retornar um código de falha, como E \_ falhar, o bits executará a linha de comando.

O BITS chama a função [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) para iniciar o programa. Se você especificar uma cadeia de caracteres de parâmetro, o primeiro parâmetro deverá ser o nome do programa.

O exemplo a seguir mostra como registrar para executar um programa quando o evento de transferência de trabalho ocorre. O exemplo supõe que o ponteiro de interface [**método ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) é válido.


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



Quando o estado do trabalho se torna BG \_ \_ , o estado do trabalho é \_ transferido, o bits executa o programa especificado em pProgram. O exemplo a seguir é uma implementação simples de um programa que usa um identificador de trabalho como um argumento. O programa assume que o número correto de argumentos é passado para ele.


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



 

 