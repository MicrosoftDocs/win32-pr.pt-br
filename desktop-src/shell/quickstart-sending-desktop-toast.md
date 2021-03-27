---
description: Este guia de início rápido mostra como gerar uma notificação do sistema de um aplicativo de desktop.
title: Envio de uma notificação do sistema usando a área de trabalho
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1D20ED75-E24A-4e60-91AB-CFCBE902A68E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbSyntax
ms.openlocfilehash: 36f9da25c20d99da74be30046fc5f9f4789dfd73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828904"
---
# <a name="quickstart-sending-a-toast-notification-from-the-desktop"></a><span data-ttu-id="fe160-103">Início rápido: enviando uma notificação do sistema da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="fe160-103">Quickstart: Sending a toast notification from the desktop</span></span>

<span data-ttu-id="fe160-104">Este guia de início rápido mostra como gerar uma notificação do sistema de um aplicativo de desktop.</span><span class="sxs-lookup"><span data-stu-id="fe160-104">This quickstart shows how to raise a toast notification from a desktop app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fe160-105">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="fe160-105">Prerequisites</span></span>

-   <span data-ttu-id="fe160-106">Bibliotecas</span><span class="sxs-lookup"><span data-stu-id="fe160-106">Libraries</span></span>
    -   <span data-ttu-id="fe160-107">C++: Runtime. Object. lib</span><span class="sxs-lookup"><span data-stu-id="fe160-107">C++: Runtime.object.lib</span></span>
    -   <span data-ttu-id="fe160-108">C \# : Windows. Winmd</span><span class="sxs-lookup"><span data-stu-id="fe160-108">C\#: Windows.Winmd</span></span>
-   <span data-ttu-id="fe160-109">Um atalho para seu aplicativo, com um [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md), deve ser instalado na tela inicial.</span><span class="sxs-lookup"><span data-stu-id="fe160-109">A shortcut to your app, with a [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md), must be installed to the Start screen.</span></span> <span data-ttu-id="fe160-110">No entanto, observe que ele não precisa ser fixado na tela inicial.</span><span class="sxs-lookup"><span data-stu-id="fe160-110">Note, however, that it does not need to be pinned to the Start screen.</span></span> <span data-ttu-id="fe160-111">Para obter mais informações, consulte [como habilitar notificações do sistema de área de trabalho por meio de um AppUserModelID](enable-desktop-toast-with-appusermodelid.md).</span><span class="sxs-lookup"><span data-stu-id="fe160-111">For more information, see [How to enable desktop toast notifications through an AppUserModelID](enable-desktop-toast-with-appusermodelid.md).</span></span>
-   <span data-ttu-id="fe160-112">Uma versão do Microsoft Visual Studio que oferece suporte a pelo menos o Windows 8</span><span class="sxs-lookup"><span data-stu-id="fe160-112">A version of Microsoft Visual Studio that supports at least Windows 8</span></span>

## <a name="instructions"></a><span data-ttu-id="fe160-113">Instruções</span><span class="sxs-lookup"><span data-stu-id="fe160-113">Instructions</span></span>

### <a name="1-create-your-toast-content"></a><span data-ttu-id="fe160-114">1. criar seu conteúdo de notificação do sistema</span><span class="sxs-lookup"><span data-stu-id="fe160-114">1. Create your toast content</span></span>

> [!Note]  
> <span data-ttu-id="fe160-115">Quando você especifica um modelo de notificação de sistema que inclui uma imagem, esteja ciente de que os aplicativos de desktop podem usar apenas imagens locais; Não há suporte para imagens da Web.</span><span class="sxs-lookup"><span data-stu-id="fe160-115">When you specify a toast template that includes an image, be aware that desktop apps can use only local images; web images are not supported.</span></span> <span data-ttu-id="fe160-116">Além disso, o caminho para o arquivo de imagem local deve ser fornecido como um caminho absoluto (não relativo).</span><span class="sxs-lookup"><span data-stu-id="fe160-116">Also, the path to the local image file must be provided as an absolute (not relative) path.</span></span>

 


```csharp
// Get a toast XML template
XmlDocument toastXml = ToastNotificationManager.GetTemplateContent(ToastTemplateType.ToastImageAndText04);

// Fill in the text elements
XmlNodeList stringElements = toastXml.GetElementsByTagName("text");
for (int i = 0; i < stringElements.Length; i++)
{
    stringElements[i].AppendChild(toastXml.CreateTextNode("Line " + i));
}

// Specify the absolute path to an image
String imagePath = "file:///" + Path.GetFullPath("toastImageAndText.png");
XmlNodeList imageElements = toastXml.GetElementsByTagName("image");

ToastNotification toast = new ToastNotification(toastXml);
```



### <a name="2-create-and-attach-the-event-handlers"></a><span data-ttu-id="fe160-117">2. criar e anexar os manipuladores de eventos</span><span class="sxs-lookup"><span data-stu-id="fe160-117">2. Create and attach the event handlers</span></span>

<span data-ttu-id="fe160-118">Registre manipuladores para eventos do sistema: ativados, ignorados e com falha.</span><span class="sxs-lookup"><span data-stu-id="fe160-118">Register handlers for the toast events: Activated, Dismissed, and Failed.</span></span> <span data-ttu-id="fe160-119">Um aplicativo de área de trabalho deve, pelo menos, assinar o evento ativado para que ele possa manipular a ativação esperada do aplicativo a partir do sistema de notificação quando o usuário o seleciona.</span><span class="sxs-lookup"><span data-stu-id="fe160-119">A desktop app must at least subscribe to the Activated event so that it can handle the expected activation of the app from the toast when the user selects it.</span></span>


```csharp
toast.Activated += ToastActivated;
toast.Dismissed += ToastDismissed;
toast.Failed += ToastFailed;
```



### <a name="3-send-the-toast"></a><span data-ttu-id="fe160-120">3. enviar o sistema de notificação</span><span class="sxs-lookup"><span data-stu-id="fe160-120">3. Send the toast</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fe160-121">Você deve incluir o [AppUserModelID](../properties/props-system-appusermodel-id.md) do atalho do seu aplicativo na tela inicial toda vez que chamar [**CreateToastNotifier**](/uwp/api/Windows.UI.Notifications.ToastNotificationManager?view=winrt-19041).</span><span class="sxs-lookup"><span data-stu-id="fe160-121">You must include the [AppUserModelID](../properties/props-system-appusermodel-id.md) of your app's shortcut on the Start screen each time that you call [**CreateToastNotifier**](/uwp/api/Windows.UI.Notifications.ToastNotificationManager?view=winrt-19041).</span></span> <span data-ttu-id="fe160-122">Se você não conseguir fazer isso, seu sistema de notificação não será exibido.</span><span class="sxs-lookup"><span data-stu-id="fe160-122">If you fail to do this, your toast will not be displayed.</span></span>

 


```csharp
ToastNotificationManager.CreateToastNotifier(appID).Show(toast);
```



### <a name="4-handle-the-callbacks"></a><span data-ttu-id="fe160-123">4. manipular os retornos de chamada</span><span class="sxs-lookup"><span data-stu-id="fe160-123">4. Handle the callbacks</span></span>

<span data-ttu-id="fe160-124">Traga a janela do aplicativo para o primeiro plano se receber um retorno de chamada "ativado" da notificação do sistema.</span><span class="sxs-lookup"><span data-stu-id="fe160-124">Bring your app's window to the foreground if it receives an "activated" callback from the toast notification.</span></span> <span data-ttu-id="fe160-125">Quando um usuário seleciona um sistema de notificação, a expectativa é que o aplicativo será iniciado em uma exibição relacionada ao conteúdo desse sistema.</span><span class="sxs-lookup"><span data-stu-id="fe160-125">When a user selects a toast, the expectation is that the app will be launched to a view related to the content of that toast..</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe160-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fe160-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe160-127">Enviando notificações do sistema de exemplo de aplicativos da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="fe160-127">Sending toast notifications from desktop apps sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts)
</dt> <dt>

[<span data-ttu-id="fe160-128">Como habilitar notificações do sistema de área de trabalho por meio de um AppUserModelID</span><span class="sxs-lookup"><span data-stu-id="fe160-128">How to enable desktop toast notifications through an AppUserModelID</span></span>](enable-desktop-toast-with-appusermodelid.md)
</dt> <dt>

[<span data-ttu-id="fe160-129">Esquema XML do sistema</span><span class="sxs-lookup"><span data-stu-id="fe160-129">Toast XML schema</span></span>](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

<span data-ttu-id="fe160-130">[Visão geral da notificação do sistema](/previous-versions/windows/apps/hh779727(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="fe160-130">[Toast notification overview](/previous-versions/windows/apps/hh779727(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="fe160-131">[Início rápido: enviando uma notificação do sistema](/previous-versions/windows/apps/hh465448(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="fe160-131">[Quickstart: Sending a toast notification](/previous-versions/windows/apps/hh465448(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="fe160-132">[Início rápido: enviando uma notificação por push do sistema](/previous-versions/windows/hh761487(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="fe160-132">[Quickstart: Sending a toast push notification](/previous-versions/windows/hh761487(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="fe160-133">Diretrizes e lista de verificação para notificações do sistema</span><span class="sxs-lookup"><span data-stu-id="fe160-133">Guidelines and checklist for toast notifications</span></span>](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

<span data-ttu-id="fe160-134">[Como escolher e usar um modelo de notificação do sistema](/previous-versions/windows/apps/hh465448(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="fe160-134">[How to choose and use a toast template](/previous-versions/windows/apps/hh465448(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="fe160-135">[Como lidar com a ativação de uma notificação do sistema](/previous-versions/windows/apps/hh761468(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="fe160-135">[How to handle activation from a toast notification](/previous-versions/windows/apps/hh761468(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="fe160-136">[Como aceitar notificações do sistema](/previous-versions/windows/apps/hh781238(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="fe160-136">[How to opt in for toast notifications](/previous-versions/windows/apps/hh781238(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="fe160-137">[Escolhendo um modelo de notificação do sistema](/previous-versions/windows/apps/hh761494(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="fe160-137">[Choosing a toast template](/previous-versions/windows/apps/hh761494(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="fe160-138">[Opções de áudio do sistema](/previous-versions/windows/apps/hh761492(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="fe160-138">[Toast audio options](/previous-versions/windows/apps/hh761492(v=win.10))</span></span>
</dt> </dl>

 

 
