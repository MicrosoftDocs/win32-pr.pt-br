---
description: Este programa verifica a presença e a configuração dos componentes principais do PC MicrosoftTablet e do touch Technology.
ms.assetid: 0b379dc9-a86f-40c0-9403-d9c9091ca8c3
title: Exemplo de informações sobre a plataforma do Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1731fc30e0405b2702bb45d0a9d0556b861ad09994ac683d739da33afe018088
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819976"
---
# <a name="tablet-pc-platform-info-sample"></a>Exemplo de informações sobre a plataforma do Tablet PC

Este programa verifica a presença e a configuração dos componentes principais do PC MicrosoftTablet e do touch Technology. Ele determina se os componentes do Tablet PC estão habilitados no sistema operacional, listando nomes e informações de versão para controles principais e o reconhecedor de fala e manuscrito padrão.

o aplicativo usa a API de Windows do GetSystemMetrics, passando o tablet de tablet \_ , para determinar se o aplicativo está em execução em um pc de mesa. O SM \_ Tablet é definido em winuser. h.

De interesse específico é a maneira como o aplicativo usa a coleção reconhecedores para fornecer informações sobre o reconhecedor padrão. Antes de tentar usar a coleção de reconhecedores e o objeto reconhecedor, o aplicativo testa a criação bem-sucedida.

## <a name="components"></a>Componentes

usando o módulo de mesclagem redistribuível, determinadas partes da API da plataforma do tablet PC podem ser instaladas em versões não-Tablet do Vista e do Windows XP Professional. a chamada GetSystemMetrics indica apenas que o Windows XP Tablet PC Edition está instalado. Um aplicativo sempre deve determinar se um determinado componente está disponível. A maneira apropriada de determinar se um componente da API está instalado é tentar criar uma instância de um objeto ou controle e verificar se ela existe antes de tentar usá-la, conforme mostrado no exemplo a seguir.


```C++
IInkRecognizers* pIInkRecognizers = NULL;
HRESULT hr = CoCreateInstance(CLSID_InkRecognizers,
                              NULL, 
                              CLSCTX_INPROC_SERVER, 
                              IID_IInkRecognizers, 
                              (void **)&pIInkRecognizers);
if (SUCCEEDED(hr)) 
{
  // use the component
} else
{
  // component unavailable
}
```



O aplicativo descobre sobre os componentes de fala instalados examinando a chave do registro apropriada:


```C++
const WCHAR* gc_wszSpeechKey = L"Software\\Microsoft\\Speech\\Recognizers";
//...
if (RegOpenKeyExW(HKEY_LOCAL_MACHINE, gc_wszSpeechKey, 0, KEY_READ, 
                  &hkeySpeech) == ERROR_SUCCESS) 
```



A chave é lida usando RegQueryValueExW.

Por fim, o exemplo descobre quais controles estão instalados.


```C++
LPCOLESTR gc_wszProgId[NUM_CONTROLS] = {L"InkEd.InkEdit", L"msinkaut.InkOverlay"};
// ...
for (int i = 0, j = 0; i < NUM_CONTROLS; i++)
{
    // Get the component info
    CLSID clsid;
    if (SUCCEEDED(CLSIDFromProgID(gc_wszProgId[i], &clsid)) && GetComponentInfo(clsid, info) == TRUE)
    {
        SetDlgItemTextW(hwnd, gc_uiCtrlId[j][0], info.wchName);
        SetDlgItemTextW(hwnd, gc_uiCtrlId[j][1], info.wchVersion);
        j++;
    }
}
```



 

 



