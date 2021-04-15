---
description: Este exemplo mostra como implantar um aplicativo gerenciado do Tablet PC pela Web usando a implantação no-touch.
ms.assetid: d226bd67-e20d-431b-b0c3-9361b00a9340
title: Exemplo de Web de implantação No-Touch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0742deef8ea9b418fba6de4724975ee27693f8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104506324"
---
# <a name="no-touch-deployment-web-sample"></a><span data-ttu-id="bac96-103">Exemplo de Web de implantação No-Touch</span><span class="sxs-lookup"><span data-stu-id="bac96-103">No-Touch Deployment Web Sample</span></span>

<span data-ttu-id="bac96-104">Este exemplo mostra como implantar um aplicativo gerenciado do Tablet PC pela Web usando a implantação no-touch.</span><span class="sxs-lookup"><span data-stu-id="bac96-104">This sample shows how to deploy a managed Tablet PC application over the Web by using no-touch deployment.</span></span> <span data-ttu-id="bac96-105">Você deve estar familiarizado com os conceitos discutidos em [implantação sem interatividade no .NET Framework](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp).</span><span class="sxs-lookup"><span data-stu-id="bac96-105">You should be familiar with the concepts discussed in [No-Touch Deployment in the .NET Framework](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp).</span></span> <span data-ttu-id="bac96-106">Seu computador deve ter o Microsoft Serviços de Informações da Internet (IIS) instalado para executar este exemplo.</span><span class="sxs-lookup"><span data-stu-id="bac96-106">Your computer must have Microsoft Internet Information Services (IIS) installed to run this sample.</span></span>

## <a name="overview"></a><span data-ttu-id="bac96-107">Visão geral</span><span class="sxs-lookup"><span data-stu-id="bac96-107">Overview</span></span>

<span data-ttu-id="bac96-108">Com a implantação do-touch, aplicativos do Tablet PCWindows Forms-aplicativos da área de trabalho criados usando as classes no namespace System. Windows. Forms do Microsoft .NET Framework e o Microsoft Windows XP Tablet PC Edition Development Kit 1,7-podem ser baixados, instalados e executados diretamente nos computadores dos usuários sem qualquer alteração do registro ou componentes do sistema compartilhado.</span><span class="sxs-lookup"><span data-stu-id="bac96-108">With no-touch deployment, Tablet PCWindows Forms applications-desktop applications built by using the classes in the System.Windows.Forms namespace of the Microsoft .NET Framework and the Microsoft Windows XP Tablet PC Edition Development Kit 1.7-can be downloaded, installed, and run directly on users' computers without any alteration of the registry or shared system components.</span></span>

<span data-ttu-id="bac96-109">Este exemplo usa o projeto original para [exemplo de formulário de declarações automática](auto-claims-form-sample.md), autodeclaras e fornece um projeto de instalador, autodeclaras \_ NoTouchWeb.</span><span class="sxs-lookup"><span data-stu-id="bac96-109">This sample takes the original project for [Auto Claims Form Sample](auto-claims-form-sample.md), AutoClaims, and provides an installer project, AutoClaims\_NoTouchWeb.</span></span> <span data-ttu-id="bac96-110">Depois de compilado e executado, o projeto do instalador cria uma nova raiz virtual, também chamada de autodeclaração \_ NoTouchWeb.</span><span class="sxs-lookup"><span data-stu-id="bac96-110">Once compiled and run, the installer project creates a new virtual root, also called AutoClaims\_NoTouchWeb.</span></span> <span data-ttu-id="bac96-111">O instalador copia um arquivo, default.htm, que inclui um link para o assembly AutoClaims.exe.</span><span class="sxs-lookup"><span data-stu-id="bac96-111">The installer copies a file, default.htm, that includes a link to the AutoClaims.exe assembly.</span></span> <span data-ttu-id="bac96-112">Para iniciar o aplicativo cliente avançado, navegue até a raiz virtual com o Microsoft Internet Explorer e, em seguida, clique no link na página default.htm.</span><span class="sxs-lookup"><span data-stu-id="bac96-112">To launch the rich client application, navigate to the virtual root with Microsoft Internet Explorer, and then click the link in the default.htm page.</span></span>

> [!Note]  
> <span data-ttu-id="bac96-113">Você deve navegar até a raiz virtual por meio do IIS (por exemplo, https://localhost/AutoClaims\_NoTouchWeb/default.htm) e não diretamente por meio do sistema de arquivos para que o aplicativo funcione no domínio do aplicativo Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="bac96-113">You must navigate to the virtual root by way of IIS (for example, https://localhost/AutoClaims\_NoTouchWeb/default.htm) and not directly through the file system in order for the application to work in the Internet Explorer application domain.</span></span>

 


```C++
<html>
    <head>
        <title>AutoClaims (No Touch Web)</title>
      </head>
      <body>
          <a href="AutoClaims.exe">Launch AutoClaims Sample</a>
      </body>
</html>
```



## <a name="no-touch-deployment-requirements"></a><span data-ttu-id="bac96-114">Requisitos de implantação do No-Touch</span><span class="sxs-lookup"><span data-stu-id="bac96-114">No-Touch Deployment Requirements</span></span>

<span data-ttu-id="bac96-115">Todos os assemblies dependentes devem estar localizados no caminho de pesquisa do assembly ou na raiz do diretório virtual do site.</span><span class="sxs-lookup"><span data-stu-id="bac96-115">All dependent assemblies must be located either in the assembly search path or the root of the virtual directory of the Web site.</span></span> <span data-ttu-id="bac96-116">O projeto de implantação NoTouchWeb de autodeclarações \_ instala o assembly e a página de referência, default.htm, na mesma raiz virtual (autodeclarações \_ NoTouchWeb).</span><span class="sxs-lookup"><span data-stu-id="bac96-116">The AutoClaims\_NoTouchWeb deployment project installs the assembly and the referring page, default.htm, into the same virtual root (AutoClaims\_NoTouchWeb).</span></span>

> [!Note]  
> <span data-ttu-id="bac96-117">Os exemplos da Web compilados não são instalados pela opção de instalação padrão para o SDK.</span><span class="sxs-lookup"><span data-stu-id="bac96-117">The compiled web samples are not installed by the default installation option for the SDK.</span></span> <span data-ttu-id="bac96-118">Você deve concluir uma instalação personalizada e selecionar a subopção "amostras da Web pré-compiladas" para instalá-las.</span><span class="sxs-lookup"><span data-stu-id="bac96-118">You must complete a custom installation and select the "Pre-compiled Web Samples" sub-option to install them.</span></span>

 

<span data-ttu-id="bac96-119">Para obter mais informações sobre como usar a tinta na Web, consulte [tinta na Web](ink-on-the-web.md).</span><span class="sxs-lookup"><span data-stu-id="bac96-119">For more information about using ink on the Web, see [Ink on the Web](ink-on-the-web.md).</span></span>

 

 