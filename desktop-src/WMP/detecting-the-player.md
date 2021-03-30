---
title: Detectando o Player
description: Detectando o Player
ms.assetid: dc034226-578a-45de-9463-e1798fef874e
keywords:
- Lojas online do Windows Media Player, detectando jogadores
- lojas online, detectando jogadores
- Digite 1 lojas online, detectando jogadores
- Digite 2 lojas online, detectando jogadores
- Repositórios online do Windows Media Player, detecção de Player
- lojas online, detecção de Player
- tipos 1 lojas online, detecção de Player
- tipo 2 lojas online, detecção de Player
- detecção de Player
- detectando jogadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb919e790b07ccf5d8df587abd63d2344534b16b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916349"
---
# <a name="detecting-the-player"></a><span data-ttu-id="1049a-113">Detectando o Player</span><span class="sxs-lookup"><span data-stu-id="1049a-113">Detecting the Player</span></span>

<span data-ttu-id="1049a-114">Ao criar uma página da Web para sua loja online, você pode decidir que deseja que os usuários consigam exibir a página em um navegador ou no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="1049a-114">When creating a webpage for your online store, you may decide that you want users to be able to view the page in a Web browser or in Windows Media Player.</span></span> <span data-ttu-id="1049a-115">Você pode usar um script ASP para determinar se sua página da Web está hospedada no Player.</span><span class="sxs-lookup"><span data-stu-id="1049a-115">You can use an ASP script to determine whether your webpage is hosted in the Player.</span></span>

<span data-ttu-id="1049a-116">O código de exemplo a seguir recupera o parâmetro de versão da cadeia de caracteres de consulta de URL para determinar se a página está hospedada no Windows Media Player:</span><span class="sxs-lookup"><span data-stu-id="1049a-116">The following example code retrieves the version parameter from the URL query string to determine whether the page is hosted in Windows Media Player:</span></span>


```C++
<%
    Dim sVersion

    sVersion = Trim(Request.QueryString("version")) 
 
    If sVersion = "" Then   
        Response.Write "Not hosted in Windows Media Player"
    Else 
        Response.Write "Hosted in Windows Media Player<BR>"
        Response.Write "Version is " & sVersion
    End If
%>
```



<span data-ttu-id="1049a-117">Observe que o código anterior pressupõe que o parâmetro de versão existe na cadeia de caracteres de consulta quando hospedado no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="1049a-117">Note that the preceding code assumes that the version parameter exists in the query string when hosted in Windows Media Player.</span></span> <span data-ttu-id="1049a-118">Isso é verdadeiro para páginas abertas pelo usuário, mas podem não ser verdadeiras para páginas abertas usando **external. NavigateTaskPaneURL**.</span><span class="sxs-lookup"><span data-stu-id="1049a-118">This is true for pages opened by the user, but may not be true for pages opened by using **External.NavigateTaskPaneURL**.</span></span> <span data-ttu-id="1049a-119">Para que a cadeia de consulta de versão exista durante a navegação programaticamente, você deve adicionar o parâmetro version à chamada de método ou acrescentar dinamicamente a versão à URL base do elemento **Navigate** do seu documento serviceInfo.</span><span class="sxs-lookup"><span data-stu-id="1049a-119">For the version query string to exist when navigating programmatically, you must add the version parameter to the method call or dynamically append the version to the base URL of the **Navigate** element of your ServiceInfo document.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1049a-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1049a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1049a-121">**Criando o documento do serviceInfo dinamicamente**</span><span class="sxs-lookup"><span data-stu-id="1049a-121">**Creating the ServiceInfo Document Dynamically**</span></span>](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[<span data-ttu-id="1049a-122">**External. NavigateTaskPaneURL**</span><span class="sxs-lookup"><span data-stu-id="1049a-122">**External.NavigateTaskPaneURL**</span></span>](external-navigatetaskpaneurl.md)
</dt> <dt>

[<span data-ttu-id="1049a-123">**Informações comuns às lojas online tipo 1 e tipo 2**</span><span class="sxs-lookup"><span data-stu-id="1049a-123">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




