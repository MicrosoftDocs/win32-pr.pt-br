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
# <a name="providing-for-rdp-client-security"></a><span data-ttu-id="890a0-103">Fornecendo para o RDP Client Security</span><span class="sxs-lookup"><span data-stu-id="890a0-103">Providing for RDP client security</span></span>

<span data-ttu-id="890a0-104">Para permitir que os clientes se protejam de servidores potencialmente não confiáveis, algumas propriedades do objeto de controle ActiveX Área de Trabalho Remota são restritas a zonas de segurança de URL específicas do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="890a0-104">To allow clients to protect themselves from potentially untrustworthy servers, some properties of the Remote Desktop ActiveX control object are restricted to specific Internet Explorer URL security zones.</span></span> <span data-ttu-id="890a0-105">Isso significa que, quando um usuário navega na Web acessa a página e a página está em uma zona de segurança de URL mais alta do que o computador com o qual está navegando pela Web, essas propriedades são desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="890a0-105">This means that, when a user browsing the web accesses the page and the page is in a higher URL security zone than the computer they are browsing the web with, these properties are disabled.</span></span> <span data-ttu-id="890a0-106">Essas propriedades restritas são acessadas usando a interface [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) e a interface [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) , e estão disponíveis nas seguintes zonas de segurança de URL do Internet Explorer:</span><span class="sxs-lookup"><span data-stu-id="890a0-106">These restricted properties are accessed using the [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface and the [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface, and are available in the following Internet Explorer URL security zones:</span></span>

-   <span data-ttu-id="890a0-107">Meu computador</span><span class="sxs-lookup"><span data-stu-id="890a0-107">My computer</span></span>
-   <span data-ttu-id="890a0-108">Intranet local</span><span class="sxs-lookup"><span data-stu-id="890a0-108">Local intranet</span></span>
-   <span data-ttu-id="890a0-109">Sites confiáveis</span><span class="sxs-lookup"><span data-stu-id="890a0-109">Trusted sites</span></span>

<span data-ttu-id="890a0-110">Eles são desabilitados nessas zonas:</span><span class="sxs-lookup"><span data-stu-id="890a0-110">They are disabled in these zones:</span></span>

-   <span data-ttu-id="890a0-111">Internet</span><span class="sxs-lookup"><span data-stu-id="890a0-111">Internet</span></span>
-   <span data-ttu-id="890a0-112">Sites restritos</span><span class="sxs-lookup"><span data-stu-id="890a0-112">Restricted sites</span></span>

<span data-ttu-id="890a0-113">Se você chamar essas propriedades restritas dentro de seu aplicativo Web Serviços de Área de Trabalho Remota, deverá chamar [**IMsTscAx:: get \_ SecuredSettings**](imstscax-securedsettings.md) e [**IMsTscAx:: get \_ SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) para acessar as propriedades de configurações protegidas.</span><span class="sxs-lookup"><span data-stu-id="890a0-113">If you call these restricted properties within your Remote Desktop Services web application, you should call [**IMsTscAx::get\_SecuredSettings**](imstscax-securedsettings.md) and [**IMsTscAx::get\_SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) to access the Secured Settings properties.</span></span>

<span data-ttu-id="890a0-114">As propriedades restritas que a interface **IMsTscSecuredSettings** acessa são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="890a0-114">The restricted properties that the **IMsTscSecuredSettings** interface accesses are the following:</span></span>

-   <span data-ttu-id="890a0-115">[**StartProgram**](imstscsecuredsettings-startprogram.md).</span><span class="sxs-lookup"><span data-stu-id="890a0-115">[**StartProgram**](imstscsecuredsettings-startprogram.md).</span></span> <span data-ttu-id="890a0-116">Esta propriedade especifica o programa que será iniciado durante a conexão.</span><span class="sxs-lookup"><span data-stu-id="890a0-116">This property specifies the program that will be started upon connection.</span></span>
-   <span data-ttu-id="890a0-117">[**WorkDir**](imstscsecuredsettings-workdir.md).</span><span class="sxs-lookup"><span data-stu-id="890a0-117">[**WorkDir**](imstscsecuredsettings-workdir.md).</span></span> <span data-ttu-id="890a0-118">Esta propriedade especifica o diretório de trabalho do programa especificado em [**StartProgram**](imstscsecuredsettings-startprogram.md).</span><span class="sxs-lookup"><span data-stu-id="890a0-118">This property specifies the working directory of the program specified in [**StartProgram**](imstscsecuredsettings-startprogram.md).</span></span>
-   <span data-ttu-id="890a0-119">[**Tela inteira**](imstscsecuredsettings-fullscreen.md).</span><span class="sxs-lookup"><span data-stu-id="890a0-119">[**FullScreen**](imstscsecuredsettings-fullscreen.md).</span></span> <span data-ttu-id="890a0-120">Esta propriedade especifica se o estado do controle na conexão estará em modo de tela inteira ou de janela.</span><span class="sxs-lookup"><span data-stu-id="890a0-120">This property specifies whether the state of the control upon connection will be in full-screen or window mode.</span></span> <span data-ttu-id="890a0-121">Se o valor dessa propriedade for **true**, a conexão será aberta no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="890a0-121">If the value of this property is **TRUE**, the connection will be opened in full-screen mode.</span></span> <span data-ttu-id="890a0-122">Embora o uso da propriedade **fullscreen** seja restrito às zonas de segurança de URL do Internet Explorer listadas anteriormente, um usuário sempre pode mudar para o modo de tela inteira após a conexão pressionando a combinação de [teclas de atalho](terminal-services-shortcut-keys.md) no modo de tela inteira (Ctrl + Alt + Break).</span><span class="sxs-lookup"><span data-stu-id="890a0-122">Although the use of the **FullScreen** property is restricted to the Internet Explorer URL security zones listed earlier, a user can always change to full-screen mode after connection by pressing the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span>

<span data-ttu-id="890a0-123">As propriedades que a interface **IMsRdpClientSecuredSettings** acessa são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="890a0-123">The properties that the **IMsRdpClientSecuredSettings** interface accesses are the following:</span></span>

-   <span data-ttu-id="890a0-124">[**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md).</span><span class="sxs-lookup"><span data-stu-id="890a0-124">[**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md).</span></span> <span data-ttu-id="890a0-125">Essa propriedade especifica se é para redirecionar sons ou tocar sons no servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="890a0-125">This property specifies whether to redirect sounds, or play sounds at the Remote Desktop Session Host (RD Session Host) server.</span></span>
-   <span data-ttu-id="890a0-126">[**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md).</span><span class="sxs-lookup"><span data-stu-id="890a0-126">[**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md).</span></span> <span data-ttu-id="890a0-127">Esta propriedade especifica como e quando aplicar combinações de tecla do Windows; por exemplo, ALT + TAB.</span><span class="sxs-lookup"><span data-stu-id="890a0-127">This property specifies how and when to apply Windows key combinations; for example, ALT+TAB.</span></span>

<span data-ttu-id="890a0-128">O script a seguir inicia o Microsoft Notepad.exe na conexão.</span><span class="sxs-lookup"><span data-stu-id="890a0-128">The following script launches Microsoft Notepad.exe upon connection.</span></span> <span data-ttu-id="890a0-129">Execute este script antes de chamar o método [**IMsTscAx:: Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="890a0-129">Run this script before calling the [**IMsTscAx::Connect**](imstscax-connect.md) method.</span></span>

``` syntax
if MsRdpClient.SecuredSettingsEnabled then
    MsRdpClient.SecuredSettings.StartProgram = "notepad.exe"
else
    msgbox "Cannot access secured setting (startprogram) in the current browser zone"
end if
```

 

 




