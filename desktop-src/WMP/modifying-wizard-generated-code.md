---
title: Modificando código gerado pelo assistente
description: Modificando código gerado pelo assistente
ms.assetid: 391a7773-c3e2-499a-bb63-e5934537d963
keywords:
- Windows Media Player Mobile, plug-ins
- Windows Media Player Mobile, plug-ins de interface do usuário
- Plug-ins móveis do Windows Media Player
- plug-ins, interface do usuário
- plug-ins, Windows Media Player Mobile
- plug-ins de interface do usuário, Windows Media Player Mobile
- Plug-ins de interface do usuário, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a83bda7cb265d0c2e039ada6d9d827c6da3faf63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105813547"
---
# <a name="modifying-wizard-generated-code"></a>Modificando código gerado pelo assistente

Há vários locais no código de plug-in gerado pelo assistente que você deve modificar antes que seu plug-in funcione com o Windows Media Player 10 Mobile. O código que você deve modificar está em negrito nos exemplos a seguir.

## <a name="changes-to-wmpplugh"></a>Alterações em wmpplug. h

Não há suporte para métodos ANSI em dispositivos que executam Windows CE, portanto, você deve modificar o seguinte método ANSI gerado pelo assistente em wmpplug. h:


```C++
return( ::PostMessage( HWND_BROADCAST, ::RegisterWindowMessageA( "WMPlayer_PluginAddRemove" ), 0, 0 ) );
```



Modifique-o conforme mostrado a seguir para que ele se torne um método Unicode:


```C++
return( ::PostMessage( HWND_BROADCAST, ::RegisterWindowMessageW( L"WMPlayer_PluginAddRemove" ), 0, 0 ) );
```



## <a name="changes-to-networkpluginh"></a>Alterações em NetworkPlugin. h

Localize o seguinte código em NetworkPlugin. h:


```C++
BEGIN_COM_MAP(CNetworkPlugin)
    COM_INTERFACE(IWMPPluginUI)
END_COM_MAP()
```



Modifique o código para que fique assim:


```C++
BEGIN_COM_MAP(CNetworkPlugin)
    
COM_INTERFACE_ENTRY_IID(__uuidof(IWMPPluginUI), IWMPPluginUI)
END_COM_MAP()
```



## <a name="changes-to-networkplugindllcpp"></a>Alterações em NetworkPlugindll. cpp

Localize a função **DllMain** em NetworkPlugindll. cpp:


```C++
extern "C" BOOL WINAPI DllMain(HINSTANCE hInstance, DWORD dwReason, LPVOID /*lpReserved*/)
{
    if (dwReason == DLL_PROCESS_ATTACH)
    {
        _Module.Init(ObjectMap, hInstance);
        DisableThreadLibraryCalls(hInstance);
    }
    else if (dwReason == DLL_PROCESS_DETACH)
        _Module.Term();
    return TRUE;    // ok
}
```



Modifique o código para que fique assim:


```C++
extern "C" BOOL WINAPI DllMain(HANDLE hInstance, DWORD dwReason, LPVOID /*lpReserved*/)
{
    if (dwReason == DLL_PROCESS_ATTACH)
    {
        _Module.Init(ObjectMap, (HINSTANCE)hInstance);
#ifndef UNDER_CE
        DisableThreadLibraryCalls((HINSTANCE)hInstance);
#endif
    }
    else if (dwReason == DLL_PROCESS_DETACH)
        _Module.Term();
    return TRUE;    // ok
}
```



## <a name="changes-to-networkplugincpp"></a>Alterações em NetworkPlugin. cpp

Localize o seguinte código em NetworkPlugin. cpp:


```C++
hr = m_spCore->QueryInterface(&spConnectionContainer);
```



Modifique o código para que fique assim:


```C++
hr = m_spCore->QueryInterface(__uuidof(IConnectionPointContainer), (void**)&spConnectionContainer);
```



## <a name="change-the-threading-model"></a>Alterar o modelo de Threading

Diferentemente do ATL para Windows, a ATL para Windows CE não oferece suporte ao modelo de threading de apartamento porque o modelo de apartamento requer mais recursos de memória do que os modelos de Threading único e threads gratuitos. Portanto, você deve encontrar todas as instâncias de threading de apartamento em StdAfx. h e NetworkPlugin. rgs e alterá-las para indicar Threading livre.

Além disso, você só pode chamar o controle móvel do Windows Media Player 10 a partir do thread no qual ele foi criado.

## <a name="build-and-test-the-project"></a>Compilar e testar o projeto

Depois de fazer essas alterações descritas aqui, você pode criar seu projeto para verificar se ele é compilado antes de adicionar qualquer código personalizado.

1.  Defina a configuração do projeto ativo como Win32 (Stone ARMV4) debug ou Win32 (Stone ARMV4) Release.
2.  Defina a plataforma ativa como Pocket PC 2003.
3.  Clique no item de menu **Compilar** e, em seguida, selecione **criar NetworkPlugin.dll**. Ele deve compilar, baixar e se registrar em seu dispositivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando um plug-in de interface do usuário para o Windows Media Player 10 Mobile**](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md)
</dt> </dl>

 

 




