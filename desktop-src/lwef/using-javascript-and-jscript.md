---
title: Usando JavaScript e JScript
description: Usando JavaScript e JScript
ms.assetid: c6927663-9432-4fa9-8de6-abb7237909b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fbac6d69de69daecbf21c50aafdafce81ed9d95
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084518"
---
# <a name="using-javascript-and-jscript"></a><span data-ttu-id="a01eb-103">Usando JavaScript e JScript</span><span class="sxs-lookup"><span data-stu-id="a01eb-103">Using JavaScript and JScript</span></span>

<span data-ttu-id="a01eb-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a01eb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="a01eb-105">Se você usar o JavaScript ou o Microsoft JScript para acessar a interface de programação do Microsoft Agent, siga as convenções para este idioma para especificar métodos ou propriedades:</span><span class="sxs-lookup"><span data-stu-id="a01eb-105">If you use JavaScript or Microsoft JScript to access Microsoft Agent's programming interface, follow the conventions for this language for specifying methods or properties:</span></span>

``` syntax
agent.object.Method (parameter)
agent.object.Property = value
```

<span data-ttu-id="a01eb-106">No momento, o JavaScript não tem uma sintaxe de evento para objetos não HTML.</span><span class="sxs-lookup"><span data-stu-id="a01eb-106">JavaScript does not currently have event syntax for non-HTML objects.</span></span> <span data-ttu-id="a01eb-107">No entanto, com o Internet Explorer, você pode usar a `<SCRIPT>` marca **para...** Sintaxe do evento:</span><span class="sxs-lookup"><span data-stu-id="a01eb-107">However, with Internet Explorer you can use the `<SCRIPT>` tag's **For...Event** syntax:</span></span>

``` syntax
<SCRIPT LANGUAGE="JScript" FOR="object" EVENT="event()">
statements
</SCRIPT>
```

<span data-ttu-id="a01eb-108">Como nem todos os navegadores dão suporte a essa sintaxe de evento, talvez você queira usar o JavaScript somente para páginas que dão suporte ao Microsoft Internet Explorer ou para códigos que não exigem manipulação de eventos.</span><span class="sxs-lookup"><span data-stu-id="a01eb-108">Because not all browsers currently support this event syntax, you may want to use JavaScript only for pages that support Microsoft Internet Explorer or for code that does not require event handling.</span></span>

<span data-ttu-id="a01eb-109">Para acessar as coleções de objetos do agente, use a função de [**enumerador**](https://www.bing.com/search?q=**Enumerator**) do JScript.</span><span class="sxs-lookup"><span data-stu-id="a01eb-109">To access Agent's object collections, use the JScript [**Enumerator**](https://www.bing.com/search?q=**Enumerator**) function.</span></span> <span data-ttu-id="a01eb-110">No entanto, as versões do JScript incluídas antes do Internet Explorer 4,0 não dão suporte a essa função e não oferecem suporte a coleções.</span><span class="sxs-lookup"><span data-stu-id="a01eb-110">However, versions of JScript included prior to Internet Explorer 4.0 do not support this function and do not support collections.</span></span> <span data-ttu-id="a01eb-111">Para acessar métodos e propriedades do objeto [**Character**](/windows/desktop/lwef/the-characters-object) , use o método [**Character**](character-method.md) .</span><span class="sxs-lookup"><span data-stu-id="a01eb-111">To access methods and properties of the [**Character**](/windows/desktop/lwef/the-characters-object) object, use the [**Character**](character-method.md) method.</span></span> <span data-ttu-id="a01eb-112">Da mesma forma, para acessar as propriedades de um objeto de [**comando**](/windows/desktop/lwef/the-command-object) , use o método de [**comando**](command-method.md) .</span><span class="sxs-lookup"><span data-stu-id="a01eb-112">Similarly, to access the properties of a [**Command**](/windows/desktop/lwef/the-command-object) object, use the [**Command**](command-method.md) method.</span></span>

 

 