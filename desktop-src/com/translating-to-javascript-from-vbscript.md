---
title: Convertendo para JavaScript a partir do VBScript
description: Convertendo para JavaScript a partir do VBScript
ms.assetid: 39a712c5-f8d7-4441-a602-93cda43c24d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff950c58c87e926c8593e5c009db4efbce0a371
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291852"
---
# <a name="translating-to-javascript-from-vbscript"></a><span data-ttu-id="d6790-103">Convertendo para JavaScript a partir do VBScript</span><span class="sxs-lookup"><span data-stu-id="d6790-103">Translating to JavaScript from VBScript</span></span>

<span data-ttu-id="d6790-104">No JavaScript, há vários tipos de dados, como números, cadeias de caracteres, Boolianos, objetos e o atributo nulo.</span><span class="sxs-lookup"><span data-stu-id="d6790-104">In JavaScript, there are several data types such as numbers, strings, Booleans, objects, and the null attribute.</span></span> <span data-ttu-id="d6790-105">O VBScript usa apenas um tipo de dados, **Variant**, que pode ser subtipoado para representar cadeias de caracteres, números, Boolianos e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="d6790-105">VBScript only uses one data type, **Variant**, which can be subtyped to represent strings, numbers, Booleans, and so on.</span></span>

<span data-ttu-id="d6790-106">No JavaScript, as matrizes podem ser expandidas dinamicamente definindo um novo valor para a propriedade Length da matriz.</span><span class="sxs-lookup"><span data-stu-id="d6790-106">In JavaScript, arrays can be expanded dynamically by setting a new value for the array's length property.</span></span> <span data-ttu-id="d6790-107">No VBScript, as matrizes não podem ser ampliadas; Eles devem ser redimensionados usando a instrução **ReDim** .</span><span class="sxs-lookup"><span data-stu-id="d6790-107">In VBScript, arrays cannot be enlarged; they must be redimensioned using the **redim** statement.</span></span>

<span data-ttu-id="d6790-108">As funções de suporte do VBScript e do JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d6790-108">Both VBScript and JavaScript support functions.</span></span> <span data-ttu-id="d6790-109">O VBScript, no entanto, também oferece suporte a sub-rotinas.</span><span class="sxs-lookup"><span data-stu-id="d6790-109">VBScript, however, also supports subroutines.</span></span> <span data-ttu-id="d6790-110">As sub-rotinas são semelhantes às funções, mas não retornam um valor.</span><span class="sxs-lookup"><span data-stu-id="d6790-110">Subroutines are similar to functions but do not return a value.</span></span>

<span data-ttu-id="d6790-111">JavaScript diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d6790-111">JavaScript is case-sensitive.</span></span> <span data-ttu-id="d6790-112">O VBScript não é.</span><span class="sxs-lookup"><span data-stu-id="d6790-112">VBScript is not.</span></span>

<span data-ttu-id="d6790-113">O JavaScript é compatível com uma ampla variedade de navegadores da Web, incluindo o Internet Explorer e o Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="d6790-113">JavaScript is supported by a wide variety of Web browsers, including both Internet Explorer and Netscape Navigator.</span></span> <span data-ttu-id="d6790-114">O VBScript só tem suporte do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="d6790-114">VBScript is only supported by Internet Explorer.</span></span>

<span data-ttu-id="d6790-115">O VBScript fornece suporte ao tratamento de erros por meio de seu objeto Err.</span><span class="sxs-lookup"><span data-stu-id="d6790-115">VBScript provides error handling support through its Err object.</span></span> <span data-ttu-id="d6790-116">Atualmente, o JavaScript não fornece um meio de interceptação e manipulação de erros.</span><span class="sxs-lookup"><span data-stu-id="d6790-116">JavaScript does not currently provide a means of trapping and handling errors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6790-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d6790-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6790-118">Convertendo para JavaScript</span><span class="sxs-lookup"><span data-stu-id="d6790-118">Translating to JavaScript</span></span>](translating-to-javascript.md)
</dt> </dl>

 

 




