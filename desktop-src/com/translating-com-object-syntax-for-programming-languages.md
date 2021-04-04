---
title: Convertendo sintaxe de objeto COM para linguagens de programação
description: Convertendo sintaxe de objeto COM para linguagens de programação
ms.assetid: 021e0085-c720-401e-9637-76580e67b307
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9d1ec65e5b4ff8f3b61106a4b7a8c9ee3134b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822559"
---
# <a name="translating-com-object-syntax-for-programming-languages"></a><span data-ttu-id="6305b-103">Convertendo sintaxe de objeto COM para linguagens de programação</span><span class="sxs-lookup"><span data-stu-id="6305b-103">Translating COM Object Syntax for Programming Languages</span></span>

<span data-ttu-id="6305b-104">Para chamar um objeto COM de um aplicativo escrito em uma linguagem de programação diferente daquela usada para gravar o objeto COM, você deve primeiro converter a sintaxe do objeto em sua linguagem de programação.</span><span class="sxs-lookup"><span data-stu-id="6305b-104">To call a COM object from an application written in a programming language other than the one used to write the COM object, you must first translate the object's syntax to your programming language.</span></span> <span data-ttu-id="6305b-105">Isso pode ser feito usando as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="6305b-105">This can be done using the following steps:</span></span>

1.  <span data-ttu-id="6305b-106">Exiba a biblioteca de tipos do objeto COM na sintaxe da linguagem de programação.</span><span class="sxs-lookup"><span data-stu-id="6305b-106">View the COM object's type library in your programming language's syntax.</span></span> <span data-ttu-id="6305b-107">Isso fornece descrições das classes, interfaces, métodos, propriedades e eventos do objeto na sintaxe de linguagem usada.</span><span class="sxs-lookup"><span data-stu-id="6305b-107">Doing this provides you with descriptions of the object's classes, interfaces, methods, properties and events in the language syntax you use.</span></span>

    <span data-ttu-id="6305b-108">Os produtos de desenvolvedor da Microsoft fornecem várias ferramentas para ajudá-lo a exibir e converter bibliotecas de tipos.</span><span class="sxs-lookup"><span data-stu-id="6305b-108">Microsoft developer products provide several tools to assist you in viewing and converting type libraries.</span></span> <span data-ttu-id="6305b-109">Para obter mais informações, consulte [visualizadores de biblioteca de tipos e ferramentas de conversão](type-library-viewers-and-conversion-tools.md) e [como ferramentas para desenvolvedores usar bibliotecas de tipos](how-developer-tools-use-type-libraries.md).</span><span class="sxs-lookup"><span data-stu-id="6305b-109">For more information, see [Type Library Viewers and Conversion Tools](type-library-viewers-and-conversion-tools.md) and [How Developer Tools Use Type Libraries](how-developer-tools-use-type-libraries.md).</span></span>

    <span data-ttu-id="6305b-110">Depois de exibir a biblioteca de tipos do objeto em sua linguagem de programação preferida, você pode comparar sua sintaxe com essa na documentação do objeto.</span><span class="sxs-lookup"><span data-stu-id="6305b-110">Once you can view the object's type library in your preferred programming language, you can compare its syntax to that in the documentation for the object.</span></span> <span data-ttu-id="6305b-111">Se o objeto estiver documentado em uma linguagem de programação diferente daquela que você está usando, os tipos de dados e a sintaxe poderão ser diferentes, mas as descrições dos parâmetros, os valores de retorno e a funcionalidade do objeto deverão ser iguais.</span><span class="sxs-lookup"><span data-stu-id="6305b-111">If the object is documented in a programming language other than the one you are using, the data types and syntax may differ, but descriptions of parameters, return values, and the object's functionality should be the same.</span></span>

2.  <span data-ttu-id="6305b-112">Leve em consideração quaisquer considerações especiais para a tradução para a linguagem de programação.</span><span class="sxs-lookup"><span data-stu-id="6305b-112">Take into account any special considerations for translating to your programming language.</span></span>

    <span data-ttu-id="6305b-113">Como cada linguagem de programação define conceitos que podem não ter um equivalente em outras linguagens, parte da funcionalidade de um objeto pode funcionar de modo diferente em outra linguagem ou não estar disponível.</span><span class="sxs-lookup"><span data-stu-id="6305b-113">Because each programming language defines concepts that may not have an equivalent in other languages, some of an object's functionality may work differently in another language, or not be available at all.</span></span> <span data-ttu-id="6305b-114">Por exemplo, a linguagem de programação Visual Basic não reconhece tipos de dados C++ não assinados, como **unsignedÂ Long**.</span><span class="sxs-lookup"><span data-stu-id="6305b-114">For example, the Visual Basic programming language does not recognize C++ unsigned data types, such as **unsignedÂ long**.</span></span> <span data-ttu-id="6305b-115">Um aplicativo escrito em Visual Basic não pode usar métodos COM que aceitem ou retornem variáveis de tipo de dados não assinado.</span><span class="sxs-lookup"><span data-stu-id="6305b-115">An application written in Visual Basic cannot use COM methods that accept or return unsigned data type variables.</span></span>

3.  <span data-ttu-id="6305b-116">Adicione o código compilado do objeto COM ao seu projeto.</span><span class="sxs-lookup"><span data-stu-id="6305b-116">Add the COM object's compiled code to your project.</span></span> <span data-ttu-id="6305b-117">O código compilado normalmente está contido em um arquivo. dll ou. ocx.</span><span class="sxs-lookup"><span data-stu-id="6305b-117">The compiled code is typically contained in a .dll or .ocx file.</span></span> <span data-ttu-id="6305b-118">Essa etapa é necessária para que o compilador reconheça as classes do objeto COM.</span><span class="sxs-lookup"><span data-stu-id="6305b-118">This step is necessary for the compiler to recognize the COM object's classes.</span></span> <span data-ttu-id="6305b-119">Depois de adicionar o objeto COM, seu aplicativo poderá usar suas classes e interfaces.</span><span class="sxs-lookup"><span data-stu-id="6305b-119">After you add the COM object, your application can use its classes and interfaces.</span></span>

<span data-ttu-id="6305b-120">Os tópicos a seguir descrevem como converter e usar objetos COM em uma variedade de linguagens de programação:</span><span class="sxs-lookup"><span data-stu-id="6305b-120">The following topics describe how to translate and use COM objects in a variety of programming languages:</span></span>

-   [<span data-ttu-id="6305b-121">Convertendo para C++</span><span class="sxs-lookup"><span data-stu-id="6305b-121">Translating to C++</span></span>](translating-to-c--.md)
-   [<span data-ttu-id="6305b-122">Convertendo para Visual Basic</span><span class="sxs-lookup"><span data-stu-id="6305b-122">Translating to Visual Basic</span></span>](translating-to-visual-basic.md)
-   [<span data-ttu-id="6305b-123">Convertendo para Java</span><span class="sxs-lookup"><span data-stu-id="6305b-123">Translating to Java</span></span>](translating-to-java.md)

<span data-ttu-id="6305b-124">Estes tópicos descrevem as ferramentas de conversão e os processos fornecidos pelos produtos de desenvolvedor da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6305b-124">These topics describe conversion tools and processes provided by Microsoft developer products.</span></span> <span data-ttu-id="6305b-125">Para obter instruções sobre como programar objetos COM usando ferramentas de desenvolvimento criadas por outras empresas, consulte a documentação das ferramentas de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="6305b-125">For instructions on how to program COM objects using development tools created by other companies, see those development tools' documentation.</span></span>

 

 




