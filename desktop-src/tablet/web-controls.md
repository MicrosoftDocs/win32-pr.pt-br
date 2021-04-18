---
description: Uma maneira de criar aplicativos Web habilitados para tinta é colocar Windows Forms controles dentro do awebpagewithin Microsoft Internet Explorer.
ms.assetid: a4fcd692-cd4a-4d2a-bfad-198010e27c6f
title: Controles da Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b28fa2a3293b6b780412ddbc755634c745b44e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810833"
---
# <a name="web-controls"></a>Controles da Web

Uma maneira de criar aplicativos Web habilitados para tinta é colocar Windows Forms controles dentro do awebpagewithin Microsoft Internet Explorer. Um bom tutorial sobre essa técnica pode ser encontrado em [usando controles de Windows Forms no Internet Explorer](https://windowsclient.net/articles/iesourcing.aspx). As etapas básicas do tutorial são:

1.  Crie um controle que herde de [**System. Windows. Forms. UserControl**](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1).
2.  Crie uma página HTML com uma marca de objeto que se refere a esse UserControl.
3.  Crie um diretório virtual e defina permissões.
4.  Carregue a URL da página HTML no navegador.

Essa técnica pode ser aplicada a controles habilitados para tinta, assim como qualquer outro [**controle**](/dotnet/api/system.windows.forms.control?view=netcore-3.1)de Windows Forms. Na verdade, a técnica pode ser usada com qualquer classe na estrutura de Microsoft .NET. Os exemplos fornecidos pelo Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) incluem uma versão de controle da Web do exemplo de declarações automáticas na seção de exemplos de tinta da Web. Este exemplo usa o [exemplo de formulário de declarações automáticas](auto-claims-form-sample.md) original e o transforma em um controle que é colocado em uma página da Web. Para obter mais informações sobre como habilitar a Web neste exemplo, consulte o [exemplo de controle da Web de tinta](ink-web-control-sample.md).

> [!Note]  
> Quando você implanta um aplicativo criado usando o .NET na Web, o aplicativo pode ser afetado pelo modelo de segurança para .NET. Para obter mais informações sobre como a segurança funciona com aplicativos Web habilitados para tinta, consulte [segurança e confiança](security-and-trust.md).

 

 

 
