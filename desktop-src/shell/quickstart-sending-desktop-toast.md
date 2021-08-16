---
description: Este início rápido mostra como criar uma notificação do sistema de um aplicativo da área de trabalho.
title: Envio de uma notificação do sistema usando a área de trabalho
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1D20ED75-E24A-4e60-91AB-CFCBE902A68E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbSyntax
ms.openlocfilehash: 79f8f65b18fd6774f318541b15d1649b7c25526f46bf3ab57f02edc4788687c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858650"
---
# <a name="quickstart-sending-a-toast-notification-from-the-desktop"></a>Início Rápido: Enviar uma notificação do sistema da área de trabalho

Este início rápido mostra como criar uma notificação do sistema de um aplicativo da área de trabalho.

## <a name="prerequisites"></a>Pré-requisitos

-   Bibliotecas
    -   C++: Runtime.object.lib
    -   C: \# Windows. Winmd
-   Um atalho para seu aplicativo, com um [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md), deve ser instalado no tela inicial. Observe, no entanto, que ele não precisa ser fixado ao tela inicial. Para obter mais informações, [consulte Como habilitar notificações do sistema de área de trabalho por meio de um AppUserModelID](enable-desktop-toast-with-appusermodelid.md).
-   Uma versão do Microsoft Visual Studio que dá suporte a pelo menos Windows 8

## <a name="instructions"></a>Instruções

### <a name="1-create-your-toast-content"></a>1. Criar o conteúdo do sistema

> [!Note]  
> Ao especificar um modelo de sistema que inclui uma imagem, esteja ciente de que os aplicativos da área de trabalho podem usar apenas imagens locais; Não há suporte para imagens da Web. Além disso, o caminho para o arquivo de imagem local deve ser fornecido como um caminho absoluto (não relativo).

 


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



### <a name="2-create-and-attach-the-event-handlers"></a>2. Criar e anexar os manipuladores de eventos

Registre manipuladores para os eventos do toast: Ativado, Ignorado e Com Falha. Um aplicativo da área de trabalho deve pelo menos assinar o evento Ativado para que ele possa lidar com a ativação esperada do aplicativo do sistema quando o usuário o selecionar.


```csharp
toast.Activated += ToastActivated;
toast.Dismissed += ToastDismissed;
toast.Failed += ToastFailed;
```



### <a name="3-send-the-toast"></a>3. Enviar o toast

> [!IMPORTANT]
> Você deve incluir [o AppUserModelID](../properties/props-system-appusermodel-id.md) do atalho do aplicativo no tela inicial sempre que chamar [**CreateToastNotifier**](/uwp/api/Windows.UI.Notifications.ToastNotificationManager?view=winrt-19041). Se você não conseguir fazer isso, o toast não será exibido.

 


```csharp
ToastNotificationManager.CreateToastNotifier(appID).Show(toast);
```



### <a name="4-handle-the-callbacks"></a>4. Manipular os retornos de chamada

Traga a janela do aplicativo para o primeiro plano se ele receber um retorno de chamada "ativado" da notificação do toast. Quando um usuário seleciona um toast, a expectativa é que o aplicativo seja lançado para uma exibição relacionada ao conteúdo desse toast..

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplo de envio de notificações do sistema de aplicativos da área de trabalho](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts)
</dt> <dt>

[Como habilitar notificações do sistema de área de trabalho por meio de um AppUserModelID](enable-desktop-toast-with-appusermodelid.md)
</dt> <dt>

[Esquema XML do toast](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

[Visão geral da notificação do toast](/previous-versions/windows/apps/hh779727(v=win.10))
</dt> <dt>

[Início Rápido: Enviar uma notificação do toast](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Início Rápido: Enviar uma notificação por push do toast](/previous-versions/windows/hh761487(v=win.10))
</dt> <dt>

[Diretrizes e lista de verificação para notificações do toast](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

[Como escolher e usar um modelo de sistema](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Como lidar com a ativação de uma notificação do sistema](/previous-versions/windows/apps/hh761468(v=win.10))
</dt> <dt>

[Como optar por notificações do toast](/previous-versions/windows/apps/hh781238(v=win.10))
</dt> <dt>

[Escolhendo um modelo de sistema](/previous-versions/windows/apps/hh761494(v=win.10))
</dt> <dt>

[Opções de áudio do sistema](/previous-versions/windows/apps/hh761492(v=win.10))
</dt> </dl>

 

 
