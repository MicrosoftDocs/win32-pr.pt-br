---
title: Convertendo para VBScript
description: Convertendo para VBScript
ms.assetid: 12eac4bd-06d9-45db-81c2-0591200cbacc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b9f64e25a22ffe83c148c1fd1b7a7603b8f3f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159612"
---
# <a name="translating-to-vbscript"></a><span data-ttu-id="fa0ec-103">Convertendo para VBScript</span><span class="sxs-lookup"><span data-stu-id="fa0ec-103">Translating to VBScript</span></span>

<span data-ttu-id="fa0ec-104">O VBScript é um subconjunto da linguagem Microsoft Visual Basic for Applications.</span><span class="sxs-lookup"><span data-stu-id="fa0ec-104">VBScript is a subset of the Microsoft Visual Basic for Applications language.</span></span> <span data-ttu-id="fa0ec-105">Como o VBScript deve ser seguro para uso em aplicativos do lado do cliente, como páginas da Web, ele não fornece entrada e saída de arquivo ou acesso direto ao sistema operacional subjacente.</span><span class="sxs-lookup"><span data-stu-id="fa0ec-105">Because VBScript is intended to be safe for use in client-side applications such as webpages, it does not provide file input and output or direct access to the underlying operating system.</span></span> <span data-ttu-id="fa0ec-106">Isso impede que um script baseado na Web exclua ou altere arquivos em seu computador.</span><span class="sxs-lookup"><span data-stu-id="fa0ec-106">This prevents a Web-based script from deleting or altering files on your computer.</span></span> <span data-ttu-id="fa0ec-107">Para obter uma lista completa de recursos de Visual Basic que não têm suporte no VBScript, consulte a documentação do Visual Basic for Applications.</span><span class="sxs-lookup"><span data-stu-id="fa0ec-107">For a complete list of Visual Basic features that are not supported in VBScript, see the Visual Basic for Applications documentation.</span></span>

<span data-ttu-id="fa0ec-108">Além dos recursos de linguagem fornecidos pelo VBScript, o host de script também pode expor um modelo de objeto VBScript que seu script pode acessar.</span><span class="sxs-lookup"><span data-stu-id="fa0ec-108">In addition to the language features provided by VBScript, the scripting host may also expose a VBScript object model that your script can access.</span></span> <span data-ttu-id="fa0ec-109">Por exemplo, o Internet Explorer expõe um modelo de objeto que permite que os scripts interajam e controlem o navegador de forma programática.</span><span class="sxs-lookup"><span data-stu-id="fa0ec-109">For example, Internet Explorer exposes an object model that enables scripts to interact with and programmatically control the browser.</span></span> <span data-ttu-id="fa0ec-110">Para obter mais informações sobre como trabalhar com esses modelos de objeto, consulte a documentação em seu host de script.</span><span class="sxs-lookup"><span data-stu-id="fa0ec-110">For more information about working with such object models, see the documentation on your scripting host.</span></span>

<span data-ttu-id="fa0ec-111">Os tópicos a seguir descrevem os problemas que você deve considerar ao traduzir um script para o VBScript do JavaScript ou JScript:</span><span class="sxs-lookup"><span data-stu-id="fa0ec-111">The following topics describe issues you should consider when translating a script to VBScript from JavaScript or JScript:</span></span>

-   [<span data-ttu-id="fa0ec-112">Convertendo para VBScript do JScript</span><span class="sxs-lookup"><span data-stu-id="fa0ec-112">Translating to VBScript from JScript</span></span>](translating-to-vbscript-from-jscript.md)
-   [<span data-ttu-id="fa0ec-113">Convertendo para VBScript do JavaScript</span><span class="sxs-lookup"><span data-stu-id="fa0ec-113">Translating to VBScript from JavaScript</span></span>](translating-to-vbscript-from-javascript.md)

## <a name="related-topics"></a><span data-ttu-id="fa0ec-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fa0ec-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa0ec-115">Convertendo para JavaScript</span><span class="sxs-lookup"><span data-stu-id="fa0ec-115">Translating to JavaScript</span></span>](translating-to-javascript.md)
</dt> <dt>

[<span data-ttu-id="fa0ec-116">Traduzindo para o JScript</span><span class="sxs-lookup"><span data-stu-id="fa0ec-116">Translating to JScript</span></span>](translating-to-jscript.md)
</dt> </dl>

 

 




