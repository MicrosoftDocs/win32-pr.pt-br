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
# <a name="quickstart-sending-a-toast-notification-from-the-desktop"></a>Início rápido: enviando uma notificação do sistema da área de trabalho

Este guia de início rápido mostra como gerar uma notificação do sistema de um aplicativo de desktop.

## <a name="prerequisites"></a>Pré-requisitos

-   Bibliotecas
    -   C++: Runtime. Object. lib
    -   C \# : Windows. Winmd
-   Um atalho para seu aplicativo, com um [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md), deve ser instalado na tela inicial. No entanto, observe que ele não precisa ser fixado na tela inicial. Para obter mais informações, consulte [como habilitar notificações do sistema de área de trabalho por meio de um AppUserModelID](enable-desktop-toast-with-appusermodelid.md).
-   Uma versão do Microsoft Visual Studio que oferece suporte a pelo menos o Windows 8

## <a name="instructions"></a>Instruções

### <a name="1-create-your-toast-content"></a>1. criar seu conteúdo de notificação do sistema

> [!Note]  
> Quando você especifica um modelo de notificação de sistema que inclui uma imagem, esteja ciente de que os aplicativos de desktop podem usar apenas imagens locais; Não há suporte para imagens da Web. Além disso, o caminho para o arquivo de imagem local deve ser fornecido como um caminho absoluto (não relativo).

 


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



### <a name="2-create-and-attach-the-event-handlers"></a>2. criar e anexar os manipuladores de eventos

Registre manipuladores para eventos do sistema: ativados, ignorados e com falha. Um aplicativo de área de trabalho deve, pelo menos, assinar o evento ativado para que ele possa manipular a ativação esperada do aplicativo a partir do sistema de notificação quando o usuário o seleciona.


```csharp
toast.Activated += ToastActivated;
toast.Dismissed += ToastDismissed;
toast.Failed += ToastFailed;
```



### <a name="3-send-the-toast"></a>3. enviar o sistema de notificação

> [!IMPORTANT]
> Você deve incluir o [AppUserModelID](../properties/props-system-appusermodel-id.md) do atalho do seu aplicativo na tela inicial toda vez que chamar [**CreateToastNotifier**](/uwp/api/Windows.UI.Notifications.ToastNotificationManager?view=winrt-19041). Se você não conseguir fazer isso, seu sistema de notificação não será exibido.

 


```csharp
ToastNotificationManager.CreateToastNotifier(appID).Show(toast);
```



### <a name="4-handle-the-callbacks"></a>4. manipular os retornos de chamada

Traga a janela do aplicativo para o primeiro plano se receber um retorno de chamada "ativado" da notificação do sistema. Quando um usuário seleciona um sistema de notificação, a expectativa é que o aplicativo será iniciado em uma exibição relacionada ao conteúdo desse sistema.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Enviando notificações do sistema de exemplo de aplicativos da área de trabalho](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts)
</dt> <dt>

[Como habilitar notificações do sistema de área de trabalho por meio de um AppUserModelID](enable-desktop-toast-with-appusermodelid.md)
</dt> <dt>

[Esquema XML do sistema](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

[Visão geral da notificação do sistema](/previous-versions/windows/apps/hh779727(v=win.10))
</dt> <dt>

[Início rápido: enviando uma notificação do sistema](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Início rápido: enviando uma notificação por push do sistema](/previous-versions/windows/hh761487(v=win.10))
</dt> <dt>

[Diretrizes e lista de verificação para notificações do sistema](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

[Como escolher e usar um modelo de notificação do sistema](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Como lidar com a ativação de uma notificação do sistema](/previous-versions/windows/apps/hh761468(v=win.10))
</dt> <dt>

[Como aceitar notificações do sistema](/previous-versions/windows/apps/hh781238(v=win.10))
</dt> <dt>

[Escolhendo um modelo de notificação do sistema](/previous-versions/windows/apps/hh761494(v=win.10))
</dt> <dt>

[Opções de áudio do sistema](/previous-versions/windows/apps/hh761492(v=win.10))
</dt> </dl>

 

 
