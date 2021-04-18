---
title: Convertendo para VBScript do JavaScript
description: Convertendo para VBScript do JavaScript
ms.assetid: f302e032-4e94-42f1-839b-022dab538760
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eda8169a665dc93133f7ac933de12ecc612f3e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105815555"
---
# <a name="translating-to-vbscript-from-javascript"></a><span data-ttu-id="743ed-103">Convertendo para VBScript do JavaScript</span><span class="sxs-lookup"><span data-stu-id="743ed-103">Translating to VBScript from JavaScript</span></span>

<span data-ttu-id="743ed-104">No JavaScript, há vários tipos de dados, como números, cadeias de caracteres, Boolianos, objetos e o atributo nulo.</span><span class="sxs-lookup"><span data-stu-id="743ed-104">In JavaScript, there are several data types, such as numbers, strings, Booleans, objects, and the null attribute.</span></span> <span data-ttu-id="743ed-105">O VBScript usa apenas um tipo de dados, **Variant**, que pode ser subtipoado para representar cadeias de caracteres, números, Boolianos e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="743ed-105">VBScript only uses one data type, **Variant**, which can be subtyped to represent strings, numbers, Booleans, and so on.</span></span>

<span data-ttu-id="743ed-106">No JavaScript, as matrizes podem ser expandidas dinamicamente definindo um novo valor para a propriedade Length da matriz.</span><span class="sxs-lookup"><span data-stu-id="743ed-106">In JavaScript, arrays can be expanded dynamically by setting a new value for the array's length property.</span></span> <span data-ttu-id="743ed-107">No VBScript, as matrizes não podem ser ampliadas; Eles devem ser redimensionados usando a instrução **ReDim** .</span><span class="sxs-lookup"><span data-stu-id="743ed-107">In VBScript, arrays cannot be enlarged; they must be redimensioned using the **redim** statement.</span></span>

<span data-ttu-id="743ed-108">As funções de suporte do VBScript e do JavaScript.</span><span class="sxs-lookup"><span data-stu-id="743ed-108">Both VBScript and JavaScript support functions.</span></span> <span data-ttu-id="743ed-109">O VBScript, no entanto, também oferece suporte a sub-rotinas.</span><span class="sxs-lookup"><span data-stu-id="743ed-109">VBScript, however, also supports subroutines.</span></span> <span data-ttu-id="743ed-110">As sub-rotinas são semelhantes às funções, exceto que não retornam um valor.</span><span class="sxs-lookup"><span data-stu-id="743ed-110">Subroutines are similar to functions, except they do not return a value.</span></span>

<span data-ttu-id="743ed-111">JavaScript diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="743ed-111">JavaScript is case-sensitive.</span></span> <span data-ttu-id="743ed-112">O VBScript não é.</span><span class="sxs-lookup"><span data-stu-id="743ed-112">VBScript is not.</span></span>

<span data-ttu-id="743ed-113">O JavaScript é compatível com uma ampla variedade de navegadores da Web, incluindo o Internet Explorer e o Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="743ed-113">JavaScript is supported by a wide variety of Web browsers, including both Internet Explorer and Netscape Navigator.</span></span> <span data-ttu-id="743ed-114">O Netscape Navigator não oferece suporte a VBScript.</span><span class="sxs-lookup"><span data-stu-id="743ed-114">Netscape Navigator does not support VBScript.</span></span>

<span data-ttu-id="743ed-115">O VBScript dá suporte ao tratamento de erros por meio de seu objeto Err.</span><span class="sxs-lookup"><span data-stu-id="743ed-115">VBScript supports error handling through its Err object.</span></span> <span data-ttu-id="743ed-116">Atualmente, o JavaScript não fornece um meio de interceptação e manipulação de erros.</span><span class="sxs-lookup"><span data-stu-id="743ed-116">JavaScript does not currently provide a means of trapping and handling errors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="743ed-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="743ed-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="743ed-118">Convertendo para VBScript</span><span class="sxs-lookup"><span data-stu-id="743ed-118">Translating to VBScript</span></span>](translating-to-vbscript.md)
</dt> </dl>

 

 




