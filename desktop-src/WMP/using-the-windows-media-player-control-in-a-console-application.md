---
title: usando o controle de Windows Media Player em um aplicativo de Console
description: usando o controle de Windows Media Player em um aplicativo de Console
ms.assetid: e5162aad-69d5-4253-83d1-46735336e6da
keywords:
- Windows Media Player, inserindo controle de ActiveX
- modelo de objeto Windows Media Player, inserindo ActiveX controle
- modelo de objeto, inserindo ActiveX controle
- Windows Media Player controle de ActiveX móvel, incorporando
- Windows Media Player controle de ActiveX, inserindo
- Windows Media Player controle de ActiveX móvel, incorporando
- controle de ActiveX, inserindo
- Windows Media Player, aplicativos de console
- modelo de objeto Windows Media Player, aplicativos de console
- modelo de objeto, aplicativos de console
- Windows Media Player Aplicativos móveis, de console
- Windows Media Player ActiveX controle, aplicativos de console
- Windows Media Player controle de ActiveX móvel, aplicativos de console
- controle de ActiveX, aplicativos de console
- inserção de aplicativo de console
- incorporação, aplicativos de console
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eef4bab6457314546f8953980678c672dad82984a4badc548a5c9d868da2839
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830465"
---
# <a name="using-the-windows-media-player-control-in-a-console-application"></a>usando o controle de Windows Media Player em um aplicativo de Console

você pode criar uma instância do objeto COM Windows Media Player diretamente usando **CoCreateInstance**. Quando você faz isso, o objeto **Player** não exibe nenhuma interface do usuário. No entanto, o objeto ainda é útil para tarefas que não exigem a interface do usuário, como trabalhar com a biblioteca, reproduzir arquivos de áudio digital ou acessar propriedades do Player.

o código de exemplo a seguir mostra um programa de console simples que exibe a versão Windows Media Player em uma caixa de mensagem. O código de exemplo usa a ATL para aproveitar os ponteiros inteligentes e a classe de cadeia de caracteres **CComBSTR** .


```C++
#include "atlbase.h"
#include "atlwin.h"
#include "wmp.h"

int _tmain(int argc, _TCHAR* argv[])
{
    CoInitialize(NULL);

    HRESULT hr = S_OK;
    CComBSTR bstrVersionInfo; // Contains the version string.
    CComPtr<IWMPPlayer> spPlayer;  // Smart pointer to IWMPPlayer interface.

    hr = spPlayer.CoCreateInstance( __uuidof(WindowsMediaPlayer), 0, CLSCTX_INPROC_SERVER );

    if(SUCCEEDED(hr))
    {
        hr = spPlayer->get_versionInfo(&bstrVersionInfo);
    }

    if(SUCCEEDED(hr))
    {
        // Show the version in a message box.
        COLE2T pStr(bstrVersionInfo);
        MessageBox( NULL, (LPCSTR)pStr, _T("Windows Media Player Version"), MB_OK );
    }

    // Clean up.
    spPlayer.Release();
    CoUninitialize();

    return 0;
}

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**usando o controle Windows Media Player em um programa C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




