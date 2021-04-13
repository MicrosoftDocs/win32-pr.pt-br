---
description: Um vetor de versão processa comentários condicionais em uma página da Web HTML. Ou seja, os vetores de versão permitem criar marcação com base na versão do navegador.
ms.assetid: 526080CD-CE76-48B8-AEBC-6A135FD95BB0
title: Vetores da Versão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41fb0b24a205b280be163caeb63287fc5036b21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297758"
---
# <a name="version-vectors"></a><span data-ttu-id="e9c03-104">Vetores da Versão</span><span class="sxs-lookup"><span data-stu-id="e9c03-104">Version Vectors</span></span>

<span data-ttu-id="e9c03-105">Um *vetor de versão* processa comentários condicionais em uma página da Web HTML.</span><span class="sxs-lookup"><span data-stu-id="e9c03-105">A *version vector* processes conditional comments in an HTML webpage.</span></span> <span data-ttu-id="e9c03-106">Ou seja, os vetores de versão permitem criar marcação com base na versão do navegador.</span><span class="sxs-lookup"><span data-stu-id="e9c03-106">That is, version vectors enable you to create markup based on the browser version.</span></span>

<span data-ttu-id="e9c03-107">Considere o exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="e9c03-107">Consider the following code example.</span></span>


```HTML
<!-[if gte IE 5.5]
   <p>you are using IE5 or higher</p>
<![endif]->
<!-[if IE6]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/ie6.css”/>
<![endif]->
<!-[if IE7]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/ie7.css”/>
<![endif]->
<!-[if gte IE8]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/standards.css”/>
<![endif]->
```



<span data-ttu-id="e9c03-108">Nesse caso, se a versão do navegador do Windows Internet Explorer for pelo menos 5,5, o parágrafo correspondente será exibido na página da Web.</span><span class="sxs-lookup"><span data-stu-id="e9c03-108">In this case, if the Windows Internet Explorer browser version is at least 5.5, the corresponding paragraph is displayed in the webpage.</span></span> <span data-ttu-id="e9c03-109">Embora a primeira condição neste exemplo ilustre a função de comentários condicionais, esses comentários não são normalmente usados para exibir marcação como a primeira condição.</span><span class="sxs-lookup"><span data-stu-id="e9c03-109">Although the first condition in this example illustrates the function of conditional comments, these comments are not typically used to display markup like the first condition.</span></span> <span data-ttu-id="e9c03-110">Em vez disso, os comentários condicionais restantes no exemplo anterior são mais comuns.</span><span class="sxs-lookup"><span data-stu-id="e9c03-110">Instead, the remaining conditional comments in the previous example are more common.</span></span> <span data-ttu-id="e9c03-111">Nesses comentários restantes, os comentários condicionais usam uma folha de estilos diferente para cada versão diferente do navegador.</span><span class="sxs-lookup"><span data-stu-id="e9c03-111">In these remaining comments, the conditional comments use a different style sheet for each different version of the browser.</span></span>

<span data-ttu-id="e9c03-112">O exemplo de código anterior também verifica a igualdade do Microsoft Internet Explorer 6 e do Windows Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="e9c03-112">The preceding code example also checks for equality for Microsoft Internet Explorer 6 and Windows Internet Explorer 7.</span></span> <span data-ttu-id="e9c03-113">Mas, para o Windows Internet Explorer 8, o exemplo usa o operador GTE (maior ou igual).</span><span class="sxs-lookup"><span data-stu-id="e9c03-113">But for Windows Internet Explorer 8, the example uses the gte operator (greater than or equal).</span></span> <span data-ttu-id="e9c03-114">Esse operador ajuda a verificar o futuro o exemplo de forma que a versão em conformidade com os padrões da folha de estilos seja usada quando uma nova versão do navegador for liberada (em vez de usar a folha de estilos incorreta ou nenhuma folha de estilos).</span><span class="sxs-lookup"><span data-stu-id="e9c03-114">This operator helps future-proof the example so that the most standards-compliant version of the style sheet is used when a new version of the browser is released (instead of using the wrong style sheet or no style sheet).</span></span> <span data-ttu-id="e9c03-115">Os aplicativos existentes geralmente não consideram uma versão do Internet Explorer anterior 7 (ou a versão mais recente do Internet Explorer para a qual o site é criado).</span><span class="sxs-lookup"><span data-stu-id="e9c03-115">Existing applications often do not consider a version of Internet Explorer past 7 (or the newest version of Internet Explorer that the site is built for).</span></span> <span data-ttu-id="e9c03-116">Para obter mais informações sobre os vetores de versão, consulte [vetores de versão](/previous-versions/cc817577(v=msdn.10)) na biblioteca MSDN.</span><span class="sxs-lookup"><span data-stu-id="e9c03-116">For more information about version vectors, see [Version Vectors](/previous-versions/cc817577(v=msdn.10)) in the MSDN Library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9c03-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e9c03-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9c03-118">Corrigindo problemas de compatibilidade em aplicativos Web usando o modo de exibição de compatibilidade</span><span class="sxs-lookup"><span data-stu-id="e9c03-118">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



