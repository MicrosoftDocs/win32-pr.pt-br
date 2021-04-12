---
title: Convertendo para JavaScript do JScript
description: Convertendo para JavaScript do JScript
ms.assetid: 11d31c8c-868d-4220-9298-6d24a209dc47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b18972f407cf008626245798b3f7740d98058e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104365667"
---
# <a name="translating-to-javascript-from-jscript"></a><span data-ttu-id="f5ea0-103">Convertendo para JavaScript do JScript</span><span class="sxs-lookup"><span data-stu-id="f5ea0-103">Translating to JavaScript from JScript</span></span>

<span data-ttu-id="f5ea0-104">O JScript é amplamente compatível com o JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f5ea0-104">JScript is largely compatible with JavaScript.</span></span> <span data-ttu-id="f5ea0-105">No entanto, o JScript inclui alguns objetos que não têm suporte no momento pelo JavaScript, como o ActiveXobject, o enumerador, o erro, o global e o VBArray.</span><span class="sxs-lookup"><span data-stu-id="f5ea0-105">However, JScript includes some objects not currently supported by JavaScript, such as ActiveXObject, Enumerator, Error, Global, and VBArray.</span></span>

<span data-ttu-id="f5ea0-106">A versão 5,0 do JScript dá suporte ao tratamento de exceções por meio de **try**... instruções **Catch** .</span><span class="sxs-lookup"><span data-stu-id="f5ea0-106">JScript version 5.0 supports exception handling through **try**...**catch** statements.</span></span> <span data-ttu-id="f5ea0-107">Atualmente, o JavaScript não fornece um mecanismo de entrega de erros.</span><span class="sxs-lookup"><span data-stu-id="f5ea0-107">JavaScript does not currently provide an error-handing mechanism.</span></span>

<span data-ttu-id="f5ea0-108">Ao trabalhar com JScript ou JavaScript, há algumas diferenças sutis entre as implementações do modelo de objeto com suporte em vários navegadores da Web.</span><span class="sxs-lookup"><span data-stu-id="f5ea0-108">When working with either JScript or JavaScript, there are some subtle differences between the object model implementations supported by various Web browsers.</span></span> <span data-ttu-id="f5ea0-109">Para gravar o script que é executado no Internet Explorer e no Netscape Navigator, limite os recursos usados pelos seus scripts aos especificados no padrão de World Wide Web Consortium (W3C) [para HTML versão 3,2](https://www.w3.org/tr/rec-html32.html).</span><span class="sxs-lookup"><span data-stu-id="f5ea0-109">To write script that runs on both Internet Explorer and Netscape Navigator, limit the features used by your scripts to those specified in the World Wide Web Consortium (W3C) [standard for HTML version 3.2](https://www.w3.org/tr/rec-html32.html).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5ea0-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f5ea0-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5ea0-111">Convertendo para JavaScript</span><span class="sxs-lookup"><span data-stu-id="f5ea0-111">Translating to JavaScript</span></span>](translating-to-javascript.md)
</dt> </dl>

 

 




