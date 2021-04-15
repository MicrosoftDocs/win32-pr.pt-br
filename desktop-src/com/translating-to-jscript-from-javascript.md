---
title: Convertendo para JScript do JavaScript
description: Convertendo para JScript do JavaScript
ms.assetid: 86067a69-a6a1-474f-b8d8-85caf384a311
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45535807a5ef2baf59c2e068007a5a8df8bf4863
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104498995"
---
# <a name="translating-to-jscript-from-javascript"></a><span data-ttu-id="5d922-103">Convertendo para JScript do JavaScript</span><span class="sxs-lookup"><span data-stu-id="5d922-103">Translating to JScript from JavaScript</span></span>

<span data-ttu-id="5d922-104">O JScript é amplamente compatível com o JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5d922-104">JScript is largely compatible with JavaScript.</span></span> <span data-ttu-id="5d922-105">No entanto, a versão 5,0 do JScript inclui alguns objetos que não têm suporte no momento pelo JavaScript, como ActiveXobject, enumerador, erro, global e VBArray.</span><span class="sxs-lookup"><span data-stu-id="5d922-105">However, JScript version 5.0 includes some objects not currently supported by JavaScript, such as ActiveXObject, Enumerator, Error, Global, and VBArray.</span></span>

<span data-ttu-id="5d922-106">O JScript 5,0 dá suporte à manipulação de exceção por meio de **try**... instruções **Catch** .</span><span class="sxs-lookup"><span data-stu-id="5d922-106">JScript 5.0 supports exception handling through **try**...**catch** statements.</span></span> <span data-ttu-id="5d922-107">Atualmente, o JavaScript não fornece um mecanismo de entrega de erros.</span><span class="sxs-lookup"><span data-stu-id="5d922-107">JavaScript does not currently provide an error-handing mechanism.</span></span>

<span data-ttu-id="5d922-108">Ao trabalhar com JScript ou JavaScript, há algumas diferenças sutis entre as implementações do modelo de objeto com suporte em vários navegadores da Web.</span><span class="sxs-lookup"><span data-stu-id="5d922-108">When working with either JScript or JavaScript, there are some subtle differences between the object model implementations supported by various Web browsers.</span></span> <span data-ttu-id="5d922-109">Para gravar o script que é executado no Internet Explorer e no Netscape Navigator, limite os recursos usados pelos seus scripts aos especificados no padrão de World Wide Web Consortium (W3C) para HTML versão 3,2.</span><span class="sxs-lookup"><span data-stu-id="5d922-109">To write script that runs on both Internet Explorer and Netscape Navigator, limit the features used by your scripts to those specified in the World Wide Web Consortium (W3C) standard for HTML version 3.2.</span></span> <span data-ttu-id="5d922-110">Para obter mais informações sobre esse padrão, consulte [especificação de referência de HTML 3,2](https://www.w3.org/TR/REC-html32.html).</span><span class="sxs-lookup"><span data-stu-id="5d922-110">For more information about this standard, see [HTML 3.2 Reference Specification](https://www.w3.org/TR/REC-html32.html).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d922-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5d922-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d922-112">Traduzindo para o JScript</span><span class="sxs-lookup"><span data-stu-id="5d922-112">Translating to JScript</span></span>](translating-to-jscript.md)
</dt> </dl>

 

 




