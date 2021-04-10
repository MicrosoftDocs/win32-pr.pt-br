---
title: Usando o controle do Windows Media Player em um aplicativo de console
description: Usando o controle do Windows Media Player em um aplicativo de console
ms.assetid: e5162aad-69d5-4253-83d1-46735336e6da
keywords:
- Windows Media Player, incorporando controle ActiveX
- Modelo de objeto do Windows Media Player, inserindo controle ActiveX
- modelo de objeto, inserindo controle ActiveX
- Windows Media Player Mobile, inserindo controle ActiveX
- Controle ActiveX do Windows Media Player, incorporando
- Controle ActiveX móvel do Windows Media Player, incorporando
- Controle ActiveX, incorporando
- Windows Media Player, aplicativos de console
- Modelo de objeto do Windows Media Player, aplicativos de console
- modelo de objeto, aplicativos de console
- Windows Media Player Mobile, aplicativos de console
- Controle ActiveX do Windows Media Player, aplicativos de console
- Controle ActiveX móvel do Windows Media Player, aplicativos de console
- Controle ActiveX, aplicativos de console
- inserção de aplicativo de console
- incorporação, aplicativos de console
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53cc7701fc10848ca246d9cf100d0716e1955b5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292365"
---
# <a name="using-the-windows-media-player-control-in-a-console-application"></a>Usando o controle do Windows Media Player em um aplicativo de console

Você pode criar uma instância do objeto COM do Windows Media Player diretamente usando **CoCreateInstance**. Quando você faz isso, o objeto **Player** não exibe nenhuma interface do usuário. No entanto, o objeto ainda é útil para tarefas que não exigem a interface do usuário, como trabalhar com a biblioteca, reproduzir arquivos de áudio digital ou acessar propriedades do Player.

O código de exemplo a seguir mostra um programa de console simples que exibe a versão do Windows Media Player em uma caixa de mensagem. O código de exemplo usa a ATL para aproveitar os ponteiros inteligentes e a classe de cadeia de caracteres **CComBSTR** .


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

[**Usando o controle do Windows Media Player em um programa C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




