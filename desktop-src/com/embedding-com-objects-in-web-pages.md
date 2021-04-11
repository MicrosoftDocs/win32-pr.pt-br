---
title: Inserindo objetos COM em páginas da Web
description: Você pode usar objetos COM em páginas da Web. Para fazer isso, primeiro crie uma instância do objeto COM. Depois que uma instância de objeto é criada, você pode usá-la em scripts subsequentes nessa página da Web.
ms.assetid: 7e2c9da7-aeae-4206-8be9-1303240b2b1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4762dd01d4bc07aab5c0b146c56cdb1aec3cb28f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292033"
---
# <a name="embedding-com-objects-in-web-pages"></a><span data-ttu-id="684a8-105">Inserindo objetos COM em páginas da Web</span><span class="sxs-lookup"><span data-stu-id="684a8-105">Embedding COM Objects in Web Pages</span></span>

<span data-ttu-id="684a8-106">Você pode usar objetos COM em páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="684a8-106">You can use COM objects in webpages.</span></span> <span data-ttu-id="684a8-107">Para fazer isso, primeiro crie uma instância do objeto COM.</span><span class="sxs-lookup"><span data-stu-id="684a8-107">To do this, first create an instance of that COM object.</span></span> <span data-ttu-id="684a8-108">Depois que uma instância de objeto é criada, você pode usá-la em scripts subsequentes nessa página da Web.</span><span class="sxs-lookup"><span data-stu-id="684a8-108">After an object instance is created, you can use it in subsequent scripts on that webpage.</span></span>

<span data-ttu-id="684a8-109">Para criar uma instância de objeto COM em uma página da Web, você pode usar uma marca de objeto.</span><span class="sxs-lookup"><span data-stu-id="684a8-109">To create a COM object instance in a webpage, you can use an OBJECT tag.</span></span> <span data-ttu-id="684a8-110">Como alternativa, se a linguagem de script fornecer uma maneira nativa de criar objetos COM, você poderá criar uma instância de objeto usando script.</span><span class="sxs-lookup"><span data-stu-id="684a8-110">Alternatively, if your scripting language provides a native way to create COM objects, you can create an object instance using script.</span></span>

<span data-ttu-id="684a8-111">Observe que a inserção de objetos COM em páginas da Web só funciona com navegadores que dão suporte a ActiveX e COM, por exemplo, o Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="684a8-111">Note that embedding COM objects in webpages only works with browsers that support ActiveX and COM, for example Internet Explorer.</span></span>

<span data-ttu-id="684a8-112">O exemplo a seguir ilustra o uso da marca OBJECT para inserir um objeto COM em uma página da Web:</span><span class="sxs-lookup"><span data-stu-id="684a8-112">The following example illustrates using the OBJECT tag to embed a COM object in a webpage:</span></span>

``` syntax
<OBJECT 
  ID = vid 
  CLASSID = "clsid:31263EC0-2957-11CF-A1E5-00AA9EC79700" 
  BORDER = 0 
  VSPACE = 0 
  HSPACE = 0 
  ALIGN = TOP 
  HEIGHT = 100% 
  WIDTH = 100%
>
</OBJECT>
 
```

<span data-ttu-id="684a8-113">Você também pode criar uma instância de objeto COM no script, se a linguagem de script fornecer uma maneira de criar objetos COM.</span><span class="sxs-lookup"><span data-stu-id="684a8-113">You can also create a COM object instance in script, if your scripting language provides a way to create COM objects.</span></span> <span data-ttu-id="684a8-114">Por exemplo, o VBScript fornece o método CreateObject e o JScript fornece o objeto ActiveXobject.</span><span class="sxs-lookup"><span data-stu-id="684a8-114">For example, VBScript provides the CreateObject method and JScript provides the ActiveXObject object.</span></span> <span data-ttu-id="684a8-115">A criação de objetos no script é ilustrada nos exemplos a seguir.</span><span class="sxs-lookup"><span data-stu-id="684a8-115">Creating objects in script is illustrated in the following examples.</span></span>

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Dim objXL
  Set objXL = CreateObject("Excel.Application")
</SCRIPT>
 
<SCRIPT LANGUAGE = "JScript">
  var objXL = new ActiveXObject("Excel.Application");
</SCRIPT>
 
```

<span data-ttu-id="684a8-116">Além do método CreateObject e do objeto ActiveXobject, o VBScript e o JScript fornecem o método GetObject, que retorna uma instância de objeto.</span><span class="sxs-lookup"><span data-stu-id="684a8-116">In addition to the CreateObject method and the ActiveXObject object, both VBScript and JScript provide the method GetObject, which returns an object instance.</span></span>

<span data-ttu-id="684a8-117">Depois que um objeto COM tiver sido criado, você poderá referenciá-lo em scripts subsequentes usando o identificador especificado no atributo ID da marca do objeto.</span><span class="sxs-lookup"><span data-stu-id="684a8-117">After a COM object has been created, you can reference it in subsequent scripts by using the identifier specified in the OBJECT tag's ID attribute.</span></span> <span data-ttu-id="684a8-118">No exemplo anterior, esse identificador foi especificado como "vid".</span><span class="sxs-lookup"><span data-stu-id="684a8-118">In the preceding example, this identifier was specified as "vid."</span></span> <span data-ttu-id="684a8-119">Observe que o script que usa o objeto COM deve aparecer após a marca de objeto ou o script que cria a instância do objeto; caso contrário, o identificador de objeto será indefinido.</span><span class="sxs-lookup"><span data-stu-id="684a8-119">Note that the script that uses the COM object must appear after the OBJECT tag or script that creates the object instance; otherwise, the object identifier is undefined.</span></span> <span data-ttu-id="684a8-120">O script a seguir usa o objeto objXL para exibir as informações de versão do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="684a8-120">The following script uses the objXL object to display the version information for Microsoft Excel.</span></span>

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Msgbox objXL.Version
</SCRIPT>
 
```

<span data-ttu-id="684a8-121">Se você estiver escrevendo scripts inseridos em uma página da Web, o navegador também expõe um modelo de objeto que seus scripts podem acessar.</span><span class="sxs-lookup"><span data-stu-id="684a8-121">If you are writing scripts embedded in a webpage, the browser also exposes an object model that your scripts can access.</span></span> <span data-ttu-id="684a8-122">O modelo usado pelo Internet Explorer está em conformidade com o Modelo de Objeto do Documento (DOM) proposto pelo World Wide Web Consortium (W3C).</span><span class="sxs-lookup"><span data-stu-id="684a8-122">The model used by Internet Explorer conforms to the Document Object Model (DOM) proposed by the World Wide Web Consortium (W3C).</span></span>

## <a name="related-topics"></a><span data-ttu-id="684a8-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="684a8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="684a8-124">Criando scripts com objetos COM</span><span class="sxs-lookup"><span data-stu-id="684a8-124">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)
</dt> </dl>

 

 




