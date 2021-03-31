---
title: Fornecendo para o RDP Client Security
description: Algumas propriedades do objeto de controle ActiveX Área de Trabalho Remota são restritas a zonas de segurança de URL específicas do Internet Explorer.
ms.assetid: fd20ec03-a5e4-4c3e-9bf5-5fa841e869c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15bbb143abd3ec09a7f1aeff67a7b6dfa224b56b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635797"
---
# <a name="providing-for-rdp-client-security"></a>Fornecendo para o RDP Client Security

Para permitir que os clientes se protejam de servidores potencialmente não confiáveis, algumas propriedades do objeto de controle ActiveX Área de Trabalho Remota são restritas a zonas de segurança de URL específicas do Internet Explorer. Isso significa que, quando um usuário navega na Web acessa a página e a página está em uma zona de segurança de URL mais alta do que o computador com o qual está navegando pela Web, essas propriedades são desabilitadas. Essas propriedades restritas são acessadas usando a interface [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) e a interface [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) , e estão disponíveis nas seguintes zonas de segurança de URL do Internet Explorer:

-   Meu computador
-   Intranet local
-   Sites confiáveis

Eles são desabilitados nessas zonas:

-   Internet
-   Sites restritos

Se você chamar essas propriedades restritas dentro de seu aplicativo Web Serviços de Área de Trabalho Remota, deverá chamar [**IMsTscAx:: get \_ SecuredSettings**](imstscax-securedsettings.md) e [**IMsTscAx:: get \_ SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) para acessar as propriedades de configurações protegidas.

As propriedades restritas que a interface **IMsTscSecuredSettings** acessa são as seguintes:

-   [**StartProgram**](imstscsecuredsettings-startprogram.md). Esta propriedade especifica o programa que será iniciado durante a conexão.
-   [**WorkDir**](imstscsecuredsettings-workdir.md). Esta propriedade especifica o diretório de trabalho do programa especificado em [**StartProgram**](imstscsecuredsettings-startprogram.md).
-   [**Tela inteira**](imstscsecuredsettings-fullscreen.md). Esta propriedade especifica se o estado do controle na conexão estará em modo de tela inteira ou de janela. Se o valor dessa propriedade for **true**, a conexão será aberta no modo de tela inteira. Embora o uso da propriedade **fullscreen** seja restrito às zonas de segurança de URL do Internet Explorer listadas anteriormente, um usuário sempre pode mudar para o modo de tela inteira após a conexão pressionando a combinação de [teclas de atalho](terminal-services-shortcut-keys.md) no modo de tela inteira (Ctrl + Alt + Break).

As propriedades que a interface **IMsRdpClientSecuredSettings** acessa são as seguintes:

-   [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md). Essa propriedade especifica se é para redirecionar sons ou tocar sons no servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).
-   [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md). Esta propriedade especifica como e quando aplicar combinações de tecla do Windows; por exemplo, ALT + TAB.

O script a seguir inicia o Microsoft Notepad.exe na conexão. Execute este script antes de chamar o método [**IMsTscAx:: Connect**](imstscax-connect.md) .

``` syntax
if MsRdpClient.SecuredSettingsEnabled then
    MsRdpClient.SecuredSettings.StartProgram = "notepad.exe"
else
    msgbox "Cannot access secured setting (startprogram) in the current browser zone"
end if
```

 

 




