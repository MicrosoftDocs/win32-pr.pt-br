---
description: Este exemplo mostra como criar um controle habilitado para tinta para uso em um navegador da Web. O exemplo usa o exemplo de formulário de declarações automáticas original e o transforma em um controle que é colocado em uma página da Web.
ms.assetid: 7a9e304c-57ef-41a3-83be-2b2d31435da8
title: Exemplo de controle da Web de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101537c4cc7b42181cf8d9ff177a5854c5b84054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761684"
---
# <a name="ink-web-control-sample"></a><span data-ttu-id="c128e-104">Exemplo de controle da Web de tinta</span><span class="sxs-lookup"><span data-stu-id="c128e-104">Ink Web Control Sample</span></span>

<span data-ttu-id="c128e-105">Este exemplo mostra como criar um controle habilitado para tinta para uso em um navegador da Web.</span><span class="sxs-lookup"><span data-stu-id="c128e-105">This sample shows how to create an ink-enabled control for use in a Web browser.</span></span> <span data-ttu-id="c128e-106">O exemplo usa o [exemplo de formulário de declarações automáticas](auto-claims-form-sample.md) original e o transforma em um controle que é colocado em uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="c128e-106">The sample takes the original [Auto Claims Form Sample](auto-claims-form-sample.md) and turns it into a control that is put on a Web page.</span></span>

<span data-ttu-id="c128e-107">Para obter mais informações sobre como usar a tinta na Web, consulte [tinta na Web](ink-on-the-web.md).</span><span class="sxs-lookup"><span data-stu-id="c128e-107">For more information about using ink on the Web, see [Ink on the Web](ink-on-the-web.md).</span></span>

## <a name="modifications-to-the-original-sample-project"></a><span data-ttu-id="c128e-108">Modificações no projeto de exemplo original</span><span class="sxs-lookup"><span data-stu-id="c128e-108">Modifications to the Original Sample Project</span></span>

<span data-ttu-id="c128e-109">Este exemplo consiste em uma solução que inclui dois projetos e um arquivo HTML.</span><span class="sxs-lookup"><span data-stu-id="c128e-109">This sample consists of a solution that includes two projects and an HTML file.</span></span> <span data-ttu-id="c128e-110">O primeiro projeto, autodeclarations, é um projeto de biblioteca de controle do Microsoft Visual C \# (um controle de usuário).</span><span class="sxs-lookup"><span data-stu-id="c128e-110">The first project, AutoClaims, is a Microsoft Visual C\# Control Library project (a User Control).</span></span> <span data-ttu-id="c128e-111">O código-fonte para esse controle é quase idêntico ao da amostra de autodeclarações com duas diferenças:</span><span class="sxs-lookup"><span data-stu-id="c128e-111">The source code for this control is almost identical to that of the AutoClaims sample with two differences:</span></span>

-   <span data-ttu-id="c128e-112">A `AutoClaims` classe neste exemplo herda da classe [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) em vez da classe [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="c128e-112">The `AutoClaims` class in this sample inherits from the [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) class rather than the [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) class.</span></span>

    ```C++
    public class AutoClaims : System.Windows.Forms.UserControl 
    ```

    

-   <span data-ttu-id="c128e-113">A classe autodeclarations neste exemplo tem um método público adicionado, `DisposeResources` que descarta os controles filho internos usados para coletar tinta.</span><span class="sxs-lookup"><span data-stu-id="c128e-113">The AutoClaims Class in this sample has an added public method, `DisposeResources` that disposes of the internal child controls used for collecting ink.</span></span> <span data-ttu-id="c128e-114">Esse método deve ser chamado por thewebpageon que o controle é usado quando a página é concluída usando o controle.</span><span class="sxs-lookup"><span data-stu-id="c128e-114">This method must be called by thewebpageon which the control is used when that page is finished using the control.</span></span>

## <a name="referencing-the-control-in-html"></a><span data-ttu-id="c128e-115">Referenciando o controle em HTML</span><span class="sxs-lookup"><span data-stu-id="c128e-115">Referencing the Control in HTML</span></span>

<span data-ttu-id="c128e-116">A solução inclui um arquivo HTML, default.htm.</span><span class="sxs-lookup"><span data-stu-id="c128e-116">The solution includes an HTML file, default.htm.</span></span> <span data-ttu-id="c128e-117">Esse arquivo é a página para a qual o navegador navega para carregar o controle.</span><span class="sxs-lookup"><span data-stu-id="c128e-117">This file is the page that the browser navigates to in order to load the control.</span></span> <span data-ttu-id="c128e-118">O arquivo contém uma <object> marca que faz referência ao controle.</span><span class="sxs-lookup"><span data-stu-id="c128e-118">The file contains an <object> tag that references the control.</span></span> <span data-ttu-id="c128e-119">Ele também inclui um script que é chamado quando a página é descarregada, conforme indicado pela presença do atributo OnLoad = " `OnUnload()` " no</span><span class="sxs-lookup"><span data-stu-id="c128e-119">It also includes a script that is called when the page unloads, as indicated by the presence of the onload=" `OnUnload()` " attribute in the</span></span> <body> <span data-ttu-id="c128e-120">Tags.</span><span class="sxs-lookup"><span data-stu-id="c128e-120">tag.</span></span> <span data-ttu-id="c128e-121">Essa função chama o `DisposeResources` método no controle para garantir que todos os recursos sejam liberados corretamente no desligamento.</span><span class="sxs-lookup"><span data-stu-id="c128e-121">This function calls the `DisposeResources` method on the control to make sure that all resources are properly released at shutdown.</span></span>


```C++
<html>
    <script language="jscript">
        // Release any resources held by the AutoClaims control
        function OnUnload()
        {
            autoClaimsControl.DisposeResources();
        }
    </script>
    <head>
        <title>AutoClaims (Web Control)</title>
    </head>
    <body onunload="OnUnload()">
        <object 
          id="autoClaimsControl" 
          classid="AutoClaims.dll#AutoClaims.AutoClaims">
        </object>
    </body>
</html> 
```



<span data-ttu-id="c128e-122">Observe o formato do valor do atributo ClassID para a <object> marca.</span><span class="sxs-lookup"><span data-stu-id="c128e-122">Notice the format of the classid attribute value for the <object> tag.</span></span> <span data-ttu-id="c128e-123">Ele nomeia o assembly, seguido de um \# separador de sinal e, em seguida, o namespace que contém o controle e, em seguida, o nome da classe do controle.</span><span class="sxs-lookup"><span data-stu-id="c128e-123">It names the assembly, followed with a \# sign separator, and then the namespace that contains the control and then the class name of the control.</span></span>

<span data-ttu-id="c128e-124">Um controle de usuário do mundo real provavelmente incluiria métodos adicionais usados para persistir ou enviar os dados coletados no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c128e-124">A real-world user control would likely include additional methods used to persist or send the data collected in the application.</span></span>

## <a name="the-autoclaims_webcontrol-project"></a><span data-ttu-id="c128e-125">O projeto WebControl de autodeclaração \_</span><span class="sxs-lookup"><span data-stu-id="c128e-125">The AutoClaims\_WebControl Project</span></span>

<span data-ttu-id="c128e-126">O projeto de WebControl de declarações autodeclaras \_ é um projeto de implantação que cria uma configuração que adiciona uma raiz virtual, o WebControl de autodeclaração \_ , no servidor Web quando instalado.</span><span class="sxs-lookup"><span data-stu-id="c128e-126">The AutoClaims\_WebControl project is a Deployment Project that creates a setup that adds a virtual root, AutoClaims\_WebControl, on the Web server when installed.</span></span> <span data-ttu-id="c128e-127">O controle e o arquivo HTML são colocados nessa raiz virtual.</span><span class="sxs-lookup"><span data-stu-id="c128e-127">The control and the HTML file are placed in this virtual root.</span></span>

> [!Note]  
> <span data-ttu-id="c128e-128">Os exemplos da Web compilados não são instalados pela opção de instalação padrão para o SDK.</span><span class="sxs-lookup"><span data-stu-id="c128e-128">The compiled web samples are not installed by the default installation option for the SDK.</span></span> <span data-ttu-id="c128e-129">Você deve concluir uma instalação personalizada e selecionar a subopção "amostras da Web pré-compiladas" para instalá-las.</span><span class="sxs-lookup"><span data-stu-id="c128e-129">You must complete a custom installation and select the "Pre-compiled Web Samples" sub-option to install them.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c128e-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c128e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c128e-131">Exemplo de formulário de declarações automáticas</span><span class="sxs-lookup"><span data-stu-id="c128e-131">Auto Claims Form Sample</span></span>](auto-claims-form-sample.md)
</dt> <dt>

[<span data-ttu-id="c128e-132">Tinta na Web</span><span class="sxs-lookup"><span data-stu-id="c128e-132">Ink on the Web</span></span>](ink-on-the-web.md)
</dt> </dl>

 

 
