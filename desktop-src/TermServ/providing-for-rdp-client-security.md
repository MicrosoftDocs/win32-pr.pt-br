---
title: Fornecendo para o RDP Client Security
description: algumas propriedades do objeto de controle de ActiveX de Área de Trabalho Remota são restritas a zonas de segurança de URL específicas do Internet Explorer.
ms.assetid: fd20ec03-a5e4-4c3e-9bf5-5fa841e869c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdcfbc2b26363ff7f13ed15b3486249aab804cd1bde418f60d71db918f25567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117940610"
---
# <a name="providing-for-rdp-client-security"></a>Fornecendo para o RDP Client Security

para permitir que os clientes se protejam de servidores potencialmente não confiáveis, algumas propriedades do objeto de controle de ActiveX de Área de Trabalho Remota são restritas a zonas de segurança de URL específicas do Internet Explorer. Isso significa que, quando um usuário navega na Web acessa a página e a página está em uma zona de segurança de URL mais alta do que o computador com o qual está navegando pela Web, essas propriedades são desabilitadas. Essas propriedades restritas são acessadas usando a interface [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) e a interface [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) , e estão disponíveis nas seguintes zonas de segurança de URL do Internet Explorer:

-   Meu computador
-   Intranet local
-   Sites confiáveis

Eles são desabilitados nessas zonas:

-   Internet
-   Sites restritos

se você chamar essas propriedades restritas dentro de seu aplicativo web Serviços de Área de Trabalho Remota, deverá chamar [**IMsTscAx:: get \_ SecuredSettings**](imstscax-securedsettings.md) e [**IMsTscAx:: get \_ SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) para acessar as propriedades protegidas de Configurações.

As propriedades restritas que a interface **IMsTscSecuredSettings** acessa são as seguintes:

-   [**StartProgram**](imstscsecuredsettings-startprogram.md). Esta propriedade especifica o programa que será iniciado durante a conexão.
-   [**WorkDir**](imstscsecuredsettings-workdir.md). Esta propriedade especifica o diretório de trabalho do programa especificado em [**StartProgram**](imstscsecuredsettings-startprogram.md).
-   [**Tela inteira**](imstscsecuredsettings-fullscreen.md). Esta propriedade especifica se o estado do controle na conexão estará em modo de tela inteira ou de janela. Se o valor dessa propriedade for **true**, a conexão será aberta no modo de tela inteira. Embora o uso da propriedade **fullscreen** seja restrito às zonas de segurança de URL do Internet Explorer listadas anteriormente, um usuário sempre pode mudar para o modo de tela inteira após a conexão pressionando a combinação de [teclas de atalho](terminal-services-shortcut-keys.md) no modo de tela inteira (Ctrl + Alt + Break).

As propriedades que a interface **IMsRdpClientSecuredSettings** acessa são as seguintes:

-   [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md). Essa propriedade especifica se é para redirecionar sons ou tocar sons no servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).
-   [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md). esta propriedade especifica como e quando aplicar Windows combinações de teclas; por exemplo, ALT + TAB.

O script a seguir inicia o Microsoft Notepad.exe na conexão. execute este script antes de chamar o método [**IMsTscAx:: Conexão**](imstscax-connect.md) .

``` syntax
if MsRdpClient.SecuredSettingsEnabled then
    MsRdpClient.SecuredSettings.StartProgram = "notepad.exe"
else
    msgbox "Cannot access secured setting (startprogram) in the current browser zone"
end if
```

 

 




