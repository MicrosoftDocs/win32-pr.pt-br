---
title: Visualizadores de biblioteca de tipos e ferramentas de conversão
description: Visualizadores de biblioteca de tipos e ferramentas de conversão
ms.assetid: 35c29e2c-3ee3-4e73-b925-6aa0ccb50a00
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64bf4ac71b3c2c2ff9cc63b196485b9e0aaa4e13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635077"
---
# <a name="type-library-viewers-and-conversion-tools"></a><span data-ttu-id="d23eb-103">Visualizadores de biblioteca de tipos e ferramentas de conversão</span><span class="sxs-lookup"><span data-stu-id="d23eb-103">Type Library Viewers and Conversion Tools</span></span>

<span data-ttu-id="d23eb-104">As bibliotecas de tipos contêm a especificação para um ou mais elementos COM, incluindo classes, interfaces, enumerações e muito mais.</span><span class="sxs-lookup"><span data-stu-id="d23eb-104">Type libraries contain the specification for one or more COM elements, including classes, interfaces, enumerations, and more.</span></span> <span data-ttu-id="d23eb-105">Esses arquivos são armazenados em um formato binário padrão.</span><span class="sxs-lookup"><span data-stu-id="d23eb-105">These files are stored in a standard binary format.</span></span> <span data-ttu-id="d23eb-106">Uma biblioteca de tipos pode ser um arquivo autônomo com a extensão de nome de arquivo. tlb ou pode ser armazenada como um recurso em um arquivo executável, que pode ter uma extensão de nome de arquivo. ocx,. dll ou. exe.</span><span class="sxs-lookup"><span data-stu-id="d23eb-106">A type library can be a stand-alone file with the .tlb file name extension, or it can be stored as a resource in an executable file, which can have an .ocx, .dll, or .exe file name extension.</span></span> <span data-ttu-id="d23eb-107">Os visualizadores de biblioteca de tipos e as ferramentas de conversão descritos a seguir lêem este formato para obter informações sobre os elementos COM na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="d23eb-107">The type library viewers and conversion tools described following read this format to gain information about the COM elements in the library.</span></span>

<span data-ttu-id="d23eb-108">Antes de poder programar um objeto em uma linguagem de programação específica, você deve ser capaz de exibir sua biblioteca de tipos nesse idioma.</span><span class="sxs-lookup"><span data-stu-id="d23eb-108">Before you can program an object in a particular programming language, you must be able to view its type library in that language.</span></span> <span data-ttu-id="d23eb-109">Isso fornece a sintaxe apropriada para as classes, interfaces, métodos, propriedades e eventos do objeto COM.</span><span class="sxs-lookup"><span data-stu-id="d23eb-109">Doing this provides you with the proper syntax for the classes, interfaces, methods, properties, and events of the COM object.</span></span>

<span data-ttu-id="d23eb-110">Os produtos de desenvolvimento da Microsoft fornecem as seguintes ferramentas que você pode usar para gerar, extrair e exibir informações da biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="d23eb-110">Microsoft development products provide the following tools that you can use to generate, extract, and view type library information.</span></span>

## <a name="c"></a><span data-ttu-id="d23eb-111">C++</span><span class="sxs-lookup"><span data-stu-id="d23eb-111">C++</span></span>

-   [<span data-ttu-id="d23eb-112">Visualizador de objetos OLE-COM</span><span class="sxs-lookup"><span data-stu-id="d23eb-112">OLE-COM Object Viewer</span></span>](ole-com-object-viewer.md)
-   [<span data-ttu-id="d23eb-113">Compilador de MIDL</span><span class="sxs-lookup"><span data-stu-id="d23eb-113">MIDL compiler</span></span>](midl-compiler.md)
-   [<span data-ttu-id="d23eb-114">MkTypLib</span><span class="sxs-lookup"><span data-stu-id="d23eb-114">MkTypLib</span></span>](mktyplib-command-line-tool.md)

## <a name="visual-basic"></a><span data-ttu-id="d23eb-115">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="d23eb-115">Visual Basic</span></span>

-   [<span data-ttu-id="d23eb-116">Pesquisador de objetos do Visual Basic</span><span class="sxs-lookup"><span data-stu-id="d23eb-116">Visual Basic Object Browser</span></span>](visual-basic-object-browser.md)

## <a name="java"></a><span data-ttu-id="d23eb-117">Java</span><span class="sxs-lookup"><span data-stu-id="d23eb-117">Java</span></span>

-   [<span data-ttu-id="d23eb-118">JActiveX</span><span class="sxs-lookup"><span data-stu-id="d23eb-118">JActiveX</span></span>](jactivex-command-line-tool.md)
-   [<span data-ttu-id="d23eb-119">Assistente de biblioteca de tipos Java</span><span class="sxs-lookup"><span data-stu-id="d23eb-119">Java Type Library Wizard</span></span>](java-type-library-wizard.md)
-   [<span data-ttu-id="d23eb-120">JavaTLB</span><span class="sxs-lookup"><span data-stu-id="d23eb-120">JavaTLB</span></span>](javatlb-command-line-tool.md)

<span data-ttu-id="d23eb-121">Para obter uma visão geral de como essas ferramentas interagem com bibliotecas de tipos, consulte [como ferramentas para desenvolvedores usar bibliotecas de tipos](how-developer-tools-use-type-libraries.md).</span><span class="sxs-lookup"><span data-stu-id="d23eb-121">For an overview of how these tools interact with type libraries, see [How Developer Tools Use Type Libraries](how-developer-tools-use-type-libraries.md).</span></span>

 

 




