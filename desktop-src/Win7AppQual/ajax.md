---
description: AJAX
ms.assetid: F9907D49-F9FE-406A-BF5F-17C61706ADC1
title: AJAX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 575ab08530936ab083baa4bb3fcfa2956ffe3b2d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088754"
---
# <a name="ajax"></a><span data-ttu-id="16891-103">AJAX</span><span class="sxs-lookup"><span data-stu-id="16891-103">AJAX</span></span>

<span data-ttu-id="16891-104">Os recursos do AJAX no Windows Internet Explorer 8 como [**XDomainRequest (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) e [xdm (mensagens entre documentos)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) têm propriedades nativas que podem entrar em conflito com as propriedades personalizadas existentes.</span><span class="sxs-lookup"><span data-stu-id="16891-104">AJAX features in Windows Internet Explorer 8 like [**XDomainRequest (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) and [Cross-Document Messaging (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) have native properties that might conflict with existing custom properties.</span></span>

<span data-ttu-id="16891-105">O Windows Internet Explorer expõe novas propriedades para determinados recursos do AJAX, como [xdm (mensagens entre documentos)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf), mesmo no modo de exibição de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="16891-105">Windows Internet Explorer exposes new properties for certain AJAX features, such as [Cross-Document Messaging (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf), even in Compatibility View.</span></span> <span data-ttu-id="16891-106">Se você adicionar propriedades personalizadas ao objeto Event, elas poderão entrar em conflito com essas novas propriedades, como **Source**.</span><span class="sxs-lookup"><span data-stu-id="16891-106">If you add custom properties to the event object, they might conflict with these new properties, such as **source**.</span></span>

<span data-ttu-id="16891-107">O exemplo de código a seguir funciona em versões mais antigas do Internet Explorer, mas não nas versões mais recentes, pois os novos recursos usam a propriedade **Source** .</span><span class="sxs-lookup"><span data-stu-id="16891-107">The following code example works in older versions of Internet Explorer but not in newer versions because new features use the **source** property.</span></span>


```JScript
event.source = myObject;
```



<span data-ttu-id="16891-108">O exemplo de código a seguir mostra como você pode alterar esse objeto para permanecer compatível.</span><span class="sxs-lookup"><span data-stu-id="16891-108">The following code example shows how you can change this object to remain compatible.</span></span>


```JScript
event.mySource = myObject;// Read-only in IE8, use mySource instead
```



## <a name="related-topics"></a><span data-ttu-id="16891-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="16891-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16891-110">Corrigindo problemas de compatibilidade em aplicativos Web usando o modo de exibição de compatibilidade</span><span class="sxs-lookup"><span data-stu-id="16891-110">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



