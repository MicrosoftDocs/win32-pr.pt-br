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
# <a name="web-controls"></a><span data-ttu-id="d0043-103">Controles da Web</span><span class="sxs-lookup"><span data-stu-id="d0043-103">Web Controls</span></span>

<span data-ttu-id="d0043-104">Uma maneira de criar aplicativos Web habilitados para tinta é colocar Windows Forms controles dentro do awebpagewithin Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="d0043-104">One way to create ink-enabled Web applications is to put Windows Forms controls inside awebpagewithin Microsoft Internet Explorer.</span></span> <span data-ttu-id="d0043-105">Um bom tutorial sobre essa técnica pode ser encontrado em [usando controles de Windows Forms no Internet Explorer](https://windowsclient.net/articles/iesourcing.aspx).</span><span class="sxs-lookup"><span data-stu-id="d0043-105">A good tutorial on this technique can be found at [Using Windows Forms Controls in Internet Explorer](https://windowsclient.net/articles/iesourcing.aspx).</span></span> <span data-ttu-id="d0043-106">As etapas básicas do tutorial são:</span><span class="sxs-lookup"><span data-stu-id="d0043-106">The basic steps in the tutorial are:</span></span>

1.  <span data-ttu-id="d0043-107">Crie um controle que herde de [**System. Windows. Forms. UserControl**](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1).</span><span class="sxs-lookup"><span data-stu-id="d0043-107">Create a control that inherits from [**System.Windows.Forms.UserControl**](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1).</span></span>
2.  <span data-ttu-id="d0043-108">Crie uma página HTML com uma marca de objeto que se refere a esse UserControl.</span><span class="sxs-lookup"><span data-stu-id="d0043-108">Create an HTML page with an object tag that refers to that UserControl.</span></span>
3.  <span data-ttu-id="d0043-109">Crie um diretório virtual e defina permissões.</span><span class="sxs-lookup"><span data-stu-id="d0043-109">Create a virtual directory and set permissions.</span></span>
4.  <span data-ttu-id="d0043-110">Carregue a URL da página HTML no navegador.</span><span class="sxs-lookup"><span data-stu-id="d0043-110">Load the URL of the HTML page into the browser.</span></span>

<span data-ttu-id="d0043-111">Essa técnica pode ser aplicada a controles habilitados para tinta, assim como qualquer outro [**controle**](/dotnet/api/system.windows.forms.control?view=netcore-3.1)de Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="d0043-111">This technique can be applied to ink-enabled controls, just like any other Windows Forms [**Control**](/dotnet/api/system.windows.forms.control?view=netcore-3.1).</span></span> <span data-ttu-id="d0043-112">Na verdade, a técnica pode ser usada com qualquer classe na estrutura de Microsoft .NET.</span><span class="sxs-lookup"><span data-stu-id="d0043-112">In fact, the technique can be used with any class in the Microsoft .NET Framework.</span></span> <span data-ttu-id="d0043-113">Os exemplos fornecidos pelo Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) incluem uma versão de controle da Web do exemplo de declarações automáticas na seção de exemplos de tinta da Web.</span><span class="sxs-lookup"><span data-stu-id="d0043-113">The samples provided by the Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) include a Web control version of the Auto Claims sample in the Ink Web Samples section.</span></span> <span data-ttu-id="d0043-114">Este exemplo usa o [exemplo de formulário de declarações automáticas](auto-claims-form-sample.md) original e o transforma em um controle que é colocado em uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="d0043-114">This example takes the original [Auto Claims Form Sample](auto-claims-form-sample.md) and turns it into a control that is put on a Web page.</span></span> <span data-ttu-id="d0043-115">Para obter mais informações sobre como habilitar a Web neste exemplo, consulte o [exemplo de controle da Web de tinta](ink-web-control-sample.md).</span><span class="sxs-lookup"><span data-stu-id="d0043-115">For more information about Web-enabling this sample, see the [Ink Web Control Sample](ink-web-control-sample.md).</span></span>

> [!Note]  
> <span data-ttu-id="d0043-116">Quando você implanta um aplicativo criado usando o .NET na Web, o aplicativo pode ser afetado pelo modelo de segurança para .NET.</span><span class="sxs-lookup"><span data-stu-id="d0043-116">When you deploy an application created by using .NET over the Web, the application may be affected by security model for .NET.</span></span> <span data-ttu-id="d0043-117">Para obter mais informações sobre como a segurança funciona com aplicativos Web habilitados para tinta, consulte [segurança e confiança](security-and-trust.md).</span><span class="sxs-lookup"><span data-stu-id="d0043-117">For more information about how security works with ink-enabled Web applications, see [Security and Trust](security-and-trust.md).</span></span>

 

 

 
