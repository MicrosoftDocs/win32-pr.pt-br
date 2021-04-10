---
description: .
ms.assetid: 2F6FDE88-C852-46BC-B6B1-630C266AF0AA
title: JSON (JavaScript Object Notation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b995edc8e83405791a1d96598b827fc77f0204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170014"
---
# <a name="javascript-object-notation-json"></a><span data-ttu-id="7bc17-103">JSON (JavaScript Object Notation)</span><span class="sxs-lookup"><span data-stu-id="7bc17-103">JavaScript Object Notation (JSON)</span></span>

<span data-ttu-id="7bc17-104">[JavaScript Object Notation (JSON)](https://www.json.org/) é um formato de intercâmbio de dados simples e leve baseado em um subconjunto da notação literal do objeto da linguagem JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7bc17-104">[JavaScript Object Notation (JSON)](https://www.json.org/) is a simple and lightweight data-interchange format that is based on a subset of the object literal notation of the JavaScript language.</span></span> <span data-ttu-id="7bc17-105">O mecanismo de JavaScript no Windows Internet Explorer 8 implementa a [proposta de json 3,1 do ECMAScript](https://www.ecma-international.org/) para funções nativas de manipulação de JSON (que usa a [API de json2.js do Douglas Crockford](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)).</span><span class="sxs-lookup"><span data-stu-id="7bc17-105">The JavaScript engine in Windows Internet Explorer 8 implements the [ECMAScript 3.1 JSON proposal](https://www.ecma-international.org/) for native JSON-handling functions (which uses [Douglas Crockford's json2.js API](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)).</span></span>

<span data-ttu-id="7bc17-106">O Internet Explorer 8 inclui um objeto JSON nativo que está em conformidade com o suporte a JSON descrito no [rascunho de trabalho da proposta es 3.1](https://www.ecma-international.org/).</span><span class="sxs-lookup"><span data-stu-id="7bc17-106">Internet Explorer 8 includes a native JSON object that complies with the JSON support that is described in the [ES3.1 Proposal Working Draft](https://www.ecma-international.org/).</span></span> <span data-ttu-id="7bc17-107">Algumas páginas da Web detectam o objeto JSON nativo e, em seguida, o utilizam de forma não padrão.</span><span class="sxs-lookup"><span data-stu-id="7bc17-107">Some webpages detect the native JSON object, and then use it in a non-standard way.</span></span> <span data-ttu-id="7bc17-108">Esse uso normalmente causa um erro de script e interrompe a manipulação de solicitações AJAX.</span><span class="sxs-lookup"><span data-stu-id="7bc17-108">This usage typically causes a script error and breaks the handling of AJAX requests.</span></span> <span data-ttu-id="7bc17-109">O exemplo de código a seguir mostra a maneira errada de usar o objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="7bc17-109">The following code example shows the wrong way to use the JSON object.</span></span>


```JScript
    if(!window.JSON) JSON = myJSON; 
    JSON.encode(obj); // Not part of the standard
```



<span data-ttu-id="7bc17-110">Em vez disso, o exemplo de código a seguir mostra uma boa maneira de usar o objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="7bc17-110">Instead, the following code example shows a good way to use the JSON object.</span></span>


```JScript
    JSON = myJSON; 
    JSON.encode(obj);
```



<span data-ttu-id="7bc17-111">O Windows Internet Explorer inclui suporte nativo para JSON introduzindo um objeto JSON global que tem dois métodos internos: **stringify** e **Parse**.</span><span class="sxs-lookup"><span data-stu-id="7bc17-111">Windows Internet Explorer includes native supports for JSON by introducing a global JSON object that has two built-in methods: **stringify** and **parse**.</span></span> <span data-ttu-id="7bc17-112">O objeto JSON global é definido no mecanismo de JavaScript e é criado durante a fase de inicialização do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="7bc17-112">The global JSON object is defined in the JavaScript engine and is created during the engine initialization phase.</span></span> <span data-ttu-id="7bc17-113">Para manter a compatibilidade com versões anteriores, esse recurso está disponível somente quando um site usa a versão mais recente dos recursos do JavaScript usando o modo de layout "padrões do Internet Explorer 8" (documento).</span><span class="sxs-lookup"><span data-stu-id="7bc17-113">To maintain backward compatibility, this feature is available only when a website uses the latest version of JavaScript features by using the "Internet Explorer 8 Standards" layout (document) mode.</span></span> <span data-ttu-id="7bc17-114">Esse recurso também pode afetar o comportamento de páginas da Web que dependem de uma variável global JSON ou usam [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js).</span><span class="sxs-lookup"><span data-stu-id="7bc17-114">This feature also might affect the behavior of webpages that depend on a global variable JSON or use [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js).</span></span>

<span data-ttu-id="7bc17-115">Você pode substituir o objeto JSON global.</span><span class="sxs-lookup"><span data-stu-id="7bc17-115">You can override the global JSON object.</span></span> <span data-ttu-id="7bc17-116">Mas quando uma página da Web usa o modo de layout (documento) "padrões do Internet Explorer 8", ela não é mais um objeto indefinido.</span><span class="sxs-lookup"><span data-stu-id="7bc17-116">But when a webpage uses the “Internet Explorer 8 Standards” layout (document) mode, it is not an undefined object anymore.</span></span> <span data-ttu-id="7bc17-117">Como o JSON é instanciado como um nome global pelo mecanismo de JavaScript, o verifica como "if (! this.JSON)" é avaliado como false e deve ser alterado no código do usuário.</span><span class="sxs-lookup"><span data-stu-id="7bc17-117">Because JSON is instantiated as a global name by the JavaScript engine, checks like "if(!this.JSON)" evaluate to False and must be changed in the user code.</span></span>

<span data-ttu-id="7bc17-118">As páginas da Web que usam [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js) provavelmente não serão afetadas.</span><span class="sxs-lookup"><span data-stu-id="7bc17-118">Webpages that use [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js) are likely not affected.</span></span> <span data-ttu-id="7bc17-119">Com poucas exceções, essas páginas devem funcionar mais rapidamente.</span><span class="sxs-lookup"><span data-stu-id="7bc17-119">With few exceptions, these pages should work faster.</span></span> <span data-ttu-id="7bc17-120">As exceções são devido às diferenças entre a implementação do JSON nativo do Internet Explorer e o json2.js.</span><span class="sxs-lookup"><span data-stu-id="7bc17-120">The exceptions are because of the differences between the Internet Explorer native JSON implementation and json2.js.</span></span> <span data-ttu-id="7bc17-121">Por exemplo, durante a serialização, a implementação JSON nativa detecta ciclos e não entra em recursão infinita como json.js.</span><span class="sxs-lookup"><span data-stu-id="7bc17-121">For example, during serialization, the native JSON implementation detects cycles and does not go in infinite recursion like json.js.</span></span> <span data-ttu-id="7bc17-122">Para obter mais informações sobre essas exceções, consulte os [Blogs do JavaScript](/archive/blogs/jscript/).</span><span class="sxs-lookup"><span data-stu-id="7bc17-122">For more information about these exceptions, see the [JavaScript Blogs](/archive/blogs/jscript/).</span></span>

<span data-ttu-id="7bc17-123">Para obter mais informações, consulte [documentação](https://msdn.microsoft.com/library/cc836458(VS.85).aspx) e [controle de versão JSON e suporte de versão do mecanismo JavaScript](https://www.microsoft.com/windows/internet-explorer/readiness/developers-new.aspx).</span><span class="sxs-lookup"><span data-stu-id="7bc17-123">For more information, see [JSON Documentation](https://msdn.microsoft.com/library/cc836458(VS.85).aspx) and [Versioning and JavaScript Engine’s Version Support](https://www.microsoft.com/windows/internet-explorer/readiness/developers-new.aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7bc17-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7bc17-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bc17-125">Corrigindo problemas de compatibilidade em aplicativos Web usando o modo de exibição de compatibilidade</span><span class="sxs-lookup"><span data-stu-id="7bc17-125">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
