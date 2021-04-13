---
title: Usando objetos COM em páginas Active Server
description: Você pode criar scripts de objetos COM em aplicativos de Active Server Pages (ASP).
ms.assetid: 3a074360-8b6c-4cb6-813b-73863fe11c46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5d73244ce5bd6c56deeda9bf4e3e4986b3d4039
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291848"
---
# <a name="using-com-objects-in-active-server-pages"></a><span data-ttu-id="95f56-103">Usando objetos COM em páginas Active Server</span><span class="sxs-lookup"><span data-stu-id="95f56-103">Using COM Objects in Active Server Pages</span></span>

<span data-ttu-id="95f56-104">Você pode criar scripts de objetos COM em aplicativos de Active Server Pages (ASP).</span><span class="sxs-lookup"><span data-stu-id="95f56-104">You can script COM objects in Active Server Pages (ASP) applications.</span></span> <span data-ttu-id="95f56-105">Para fazer isso, você deve primeiro criar uma instância do objeto usando a marca OBJECT ou chamando o método CreateObject do objeto do servidor ASP.</span><span class="sxs-lookup"><span data-stu-id="95f56-105">To do so, you must first create an instance of the object either by using the OBJECT tag or by calling the CreateObject method of the ASP Server object.</span></span> <span data-ttu-id="95f56-106">Depois que um objeto COM tiver sido criado, você poderá usá-lo em scripts subsequentes na página ASP.</span><span class="sxs-lookup"><span data-stu-id="95f56-106">Once a COM object has been created, you can use it in subsequent scripts on the ASP page.</span></span>

<span data-ttu-id="95f56-107">Usando o ASP, você pode trabalhar com muitos tipos diferentes de mecanismos de script, cada um com suporte para uma linguagem de script diferente.</span><span class="sxs-lookup"><span data-stu-id="95f56-107">Using ASP, you can work with many different types of scripting engines, each of which supports a different scripting language.</span></span> <span data-ttu-id="95f56-108">O ASP vem com os mecanismos de script VBScript e JScript.</span><span class="sxs-lookup"><span data-stu-id="95f56-108">ASP comes with VBScript and JScript scripting engines.</span></span> <span data-ttu-id="95f56-109">Você também pode conectar mecanismos de script desenvolvidos por outras empresas para dar suporte a idiomas como PerlScript, PScript, Python e outros.</span><span class="sxs-lookup"><span data-stu-id="95f56-109">You can also plug in scripting engines developed by other companies to support languages such as PerlScript, PScript, Python, and others.</span></span>

<span data-ttu-id="95f56-110">Se você não definir a linguagem de script para uma página ASP, o VBScript será o padrão.</span><span class="sxs-lookup"><span data-stu-id="95f56-110">If you do not set the scripting language for an ASP page, VBScript is the default.</span></span> <span data-ttu-id="95f56-111">Para especificar uma linguagem de script diferente do VBScript, inclua uma linha como a seguinte na parte superior de cada página ASP:</span><span class="sxs-lookup"><span data-stu-id="95f56-111">To specify a scripting language other than VBScript, include a line such as the following at the top of each ASP page:</span></span>

``` syntax
<%@ LANGUAGE=JScript %>
 
```

<span data-ttu-id="95f56-112">Para usar um objeto COM em uma página ASP, você deve primeiro criar uma instância desse objeto.</span><span class="sxs-lookup"><span data-stu-id="95f56-112">To use a COM object in an ASP page, you must first create an instance of that object.</span></span> <span data-ttu-id="95f56-113">Você faz isso usando a marca OBJECT e especificando o valor "SERVER" para o atributo RUNAT, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="95f56-113">You do this by using the OBJECT tag and specifying the value "SERVER" for the RUNAT attribute, as shown in the following example.</span></span> <span data-ttu-id="95f56-114">Por padrão, a marca OBJECT cria uma instância do objeto no cliente.</span><span class="sxs-lookup"><span data-stu-id="95f56-114">By default, the OBJECT tag creates an instance of the object on the client.</span></span> <span data-ttu-id="95f56-115">Definir o atributo RUNAT como servidor faz com que o objeto seja criado no servidor.</span><span class="sxs-lookup"><span data-stu-id="95f56-115">Setting the RUNAT attribute to SERVER causes the object to be created on the server.</span></span> <span data-ttu-id="95f56-116">O objeto deve ser executado no servidor para ser usado pelo ASP.</span><span class="sxs-lookup"><span data-stu-id="95f56-116">The object must run on the server in order to be used by ASP.</span></span>

``` syntax
<OBJECT 
RUNAT=SERVER 
ID=MyAds 
CLASSID="Clsid:1621F7C0-60AC-11CF-9427-444553540000">
</OBJECT> 
 
```

<span data-ttu-id="95f56-117">Você também pode criar uma instância de um objeto COM em uma página ASP chamando o método CreateObject do objeto do servidor ASP.</span><span class="sxs-lookup"><span data-stu-id="95f56-117">You can also create an instance of a COM object on an ASP page by calling the CreateObject method of the ASP Server object.</span></span> <span data-ttu-id="95f56-118">O uso de Server. CreateObject é mais lento do que criar o objeto usando uma marca de objeto, mas é um pouco mais legível porque especifica o identificador programático em vez do identificador de classe do objeto COM.</span><span class="sxs-lookup"><span data-stu-id="95f56-118">Using Server.CreateObject is slower than creating the object using an OBJECT tag, but it is slightly more readable because it specifies the programmatic identifier instead of the class identifier of the COM object.</span></span> <span data-ttu-id="95f56-119">O objeto Server é exposto pelo ASP e não precisa ser criado.</span><span class="sxs-lookup"><span data-stu-id="95f56-119">The Server object is exposed by ASP and does not need to be created.</span></span> <span data-ttu-id="95f56-120">Como chamar Server. CreateObject é ilustrado nos exemplos a seguir.</span><span class="sxs-lookup"><span data-stu-id="95f56-120">How to call Server.CreateObject is illustrated in the following examples.</span></span> <span data-ttu-id="95f56-121">O primeiro exemplo é o VBScript:</span><span class="sxs-lookup"><span data-stu-id="95f56-121">The first example is VBScript:</span></span>

``` syntax
<% 
  Set MyAds = Server.CreateObject("MSWC.AdRotator") 
%>
 
```

<span data-ttu-id="95f56-122">O exemplo a seguir é JScript:</span><span class="sxs-lookup"><span data-stu-id="95f56-122">The next example is JScript:</span></span>

``` syntax
<% 
  var MyAds = Server.CreateObject("MSWC.AdRotator") 
%>
 
```

<span data-ttu-id="95f56-123">Chamar CreateObject é mais lento do que usar a marca OBJECT para criar um objeto COM.</span><span class="sxs-lookup"><span data-stu-id="95f56-123">Calling CreateObject is slower than using the OBJECT tag to create a COM object.</span></span> <span data-ttu-id="95f56-124">Em aplicativos em que o desempenho é crítico, você deve usar a marca OBJECT.</span><span class="sxs-lookup"><span data-stu-id="95f56-124">In applications where performance is critical, you should use the OBJECT tag.</span></span>

<span data-ttu-id="95f56-125">Depois de criar uma instância do objeto COM, você pode usá-la em scripts.</span><span class="sxs-lookup"><span data-stu-id="95f56-125">After you have created an instance of the COM object, you can use it in scripts.</span></span> <span data-ttu-id="95f56-126">Fazer isso é ilustrado no exemplo de VBScript a seguir, que define o valor da propriedade border do objeto COM.</span><span class="sxs-lookup"><span data-stu-id="95f56-126">Doing this is illustrated in the VBScript example following, which sets the value of the COM object's Border property.</span></span>

``` syntax
<% MyAds.Border = 0 %>
 
```

## <a name="related-topics"></a><span data-ttu-id="95f56-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="95f56-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95f56-128">Criando scripts com objetos COM</span><span class="sxs-lookup"><span data-stu-id="95f56-128">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)
</dt> </dl>

 

 




