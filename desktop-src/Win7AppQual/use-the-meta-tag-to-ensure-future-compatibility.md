---
description: Use a marca meta para garantir a compatibilidade futura
ms.assetid: 254A1C0D-B24B-4014-8D15-662FC7F2AB81
title: Use a marca meta para garantir a compatibilidade futura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a69180470c60dffc772f20fe6c515ba3803cbf2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084164"
---
# <a name="use-the-meta-tag-to-ensure-future-compatibility"></a><span data-ttu-id="6d5c5-103">Use a marca meta para garantir a compatibilidade futura</span><span class="sxs-lookup"><span data-stu-id="6d5c5-103">Use the Meta Tag to Ensure Future Compatibility</span></span>

<span data-ttu-id="6d5c5-104">O Windows Internet Explorer 8 permite que você controle modos de compatibilidade de documentos, para que você possa instruir o navegador a renderizar páginas da Web da mesma forma que as versões mais antigas do navegador.</span><span class="sxs-lookup"><span data-stu-id="6d5c5-104">Windows Internet Explorer 8 enables you to control document compatibility modes, so you can instruct the browser to render webpages in the same way as older browser versions.</span></span> <span data-ttu-id="6d5c5-105">Você também pode escolher quando atualizar a página da Web, enquanto ela continua a ser usada e funciona corretamente.</span><span class="sxs-lookup"><span data-stu-id="6d5c5-105">You can also choose when to update the webpage, while it continues to be usable and function correctly.</span></span>

## <a name="setting-the-meta-element"></a><span data-ttu-id="6d5c5-106">Configurando o elemento meta</span><span class="sxs-lookup"><span data-stu-id="6d5c5-106">Setting the Meta Element</span></span>

<span data-ttu-id="6d5c5-107">O **meta** Element inclui um atributo **Content** que permite que você especifique o modo no qual o conteúdo é renderizado para a página da Web, como mostra a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6d5c5-107">The **meta** element includes a **content** attribute that enables you to specify the mode that content is rendered in for the webpage, as the following table shows.</span></span>



| <span data-ttu-id="6d5c5-108">Valor</span><span class="sxs-lookup"><span data-stu-id="6d5c5-108">Value</span></span> | <span data-ttu-id="6d5c5-109">Modo de renderização</span><span class="sxs-lookup"><span data-stu-id="6d5c5-109">Rendering mode</span></span>                                                 |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="6d5c5-110">IE = 9</span><span class="sxs-lookup"><span data-stu-id="6d5c5-110">IE=9</span></span>  | <span data-ttu-id="6d5c5-111">Usar o modo de renderização de padrões do Windows Internet Explorer 9</span><span class="sxs-lookup"><span data-stu-id="6d5c5-111">Use the Windows Internet Explorer 9 standards rendering mode</span></span>   |
| <span data-ttu-id="6d5c5-112">IE = 8</span><span class="sxs-lookup"><span data-stu-id="6d5c5-112">IE=8</span></span>  | <span data-ttu-id="6d5c5-113">Usar o modo de renderização de padrões do Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="6d5c5-113">Use the Internet Explorer 8 standards rendering mode</span></span>           |
| <span data-ttu-id="6d5c5-114">IE = 7</span><span class="sxs-lookup"><span data-stu-id="6d5c5-114">IE=7</span></span>  | <span data-ttu-id="6d5c5-115">Usar o modo de renderização de padrões do Windows Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="6d5c5-115">Use the Windows Internet Explorer 7 standards rendering mode</span></span>   |
| <span data-ttu-id="6d5c5-116">IE=5</span><span class="sxs-lookup"><span data-stu-id="6d5c5-116">IE=5</span></span>  | <span data-ttu-id="6d5c5-117">Usar o modo de renderização de padrões do Microsoft Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="6d5c5-117">Use the Microsoft Internet Explorer 5 standards rendering mode</span></span> |



 

<span data-ttu-id="6d5c5-118">Para obter mais informações sobre compatibilidade e o cabeçalho de X-UA-Compatible, consulte [definindo a compatibilidade de documentos](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)) na biblioteca MSDN.</span><span class="sxs-lookup"><span data-stu-id="6d5c5-118">For more information about compatibility and the X-UA-Compatible header, see [Defining Document Compatibility](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)) in the MSDN Library.</span></span>

<span data-ttu-id="6d5c5-119">O exemplo de código a seguir demonstra como forçar uma página da Web a ser renderizada no modo do Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="6d5c5-119">The following code example demonstrates how to force a webpage to be rendered in Internet Explorer 8 mode.</span></span>


```HTML
<html>
   <head>
   <!-- Mimic Internet Explorer 8 -->
      <title>My Web Page</title>
      <meta http-equiv="X-UA-Compatible" content="IE=EmulateIE8" />
   </head>
   <body>
      <p>Content goes here.</p>
   </body>
</html>
```



## <a name="using-an-http-header"></a><span data-ttu-id="6d5c5-120">Usando um cabeçalho HTTP</span><span class="sxs-lookup"><span data-stu-id="6d5c5-120">Using an HTTP Header</span></span>

<span data-ttu-id="6d5c5-121">Muitos sites contêm milhares (ou dezenas de milhares) de páginas da Web individuais, portanto, a definição do elemento **meta** em cada documento não é prática.</span><span class="sxs-lookup"><span data-stu-id="6d5c5-121">Many websites contain thousands (or tens of thousands) of individual webpages so setting the **meta** element on each document is impractical.</span></span> <span data-ttu-id="6d5c5-122">Se desejar definir o elemento **meta** para todas as páginas ou uma coleção de páginas selecionadas por pasta, você poderá ajustar a configuração do servidor e adicionar os metadados compatíveis com X-UA no [cabeçalho http](/previous-versions/cc817572(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="6d5c5-122">If you want to set the **meta** element for all pages or a collection of pages that are selected by folder, you can adjust your server configuration instead and add the X-UA-Compatible metadata in the [HTTP header](/previous-versions/cc817572(v=msdn.10)).</span></span>

<span data-ttu-id="6d5c5-123">Para sites que exigem valores diferentes de elementos **meta** para páginas no mesmo servidor, há várias ferramentas que geram e inserem automaticamente o elemento **meta** apropriado para você.</span><span class="sxs-lookup"><span data-stu-id="6d5c5-123">For sites that require different **meta** element values for pages on the same server, there are several tools that automatically generate and insert the appropriate **meta** element for you.</span></span> <span data-ttu-id="6d5c5-124">Por exemplo, o utilitário [A ArtinSoft Web Tools](https://www.mobilize.net/what-is-aggiorno-ie8-compatibility-tagging.aspx) da aggiorno insere e remove o recurso de marca de compatibilidade do Internet Explorer 8 e pode ajudar seu site a atender a padrões de compatibilidade específicos.</span><span class="sxs-lookup"><span data-stu-id="6d5c5-124">For example, the [ArtinSoft Web Tools](https://www.mobilize.net/what-is-aggiorno-ie8-compatibility-tagging.aspx) utility from Aggiorno inserts and removes the Internet Explorer 8 compatibility tag feature and can help your site meet specific compatibility standards.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d5c5-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6d5c5-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d5c5-126">Corrigindo problemas de compatibilidade em aplicativos Web usando o modo de exibição de compatibilidade</span><span class="sxs-lookup"><span data-stu-id="6d5c5-126">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-with-compatibility-view.md)
</dt> </dl>

 

 
