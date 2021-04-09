---
title: Convertendo para VBScript do JScript
description: Convertendo para VBScript do JScript
ms.assetid: db1115e1-2abd-4b06-ad8d-c1f917cd3087
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704f5ac608e94f883edc3b319fd04625e9a08d18
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005208"
---
# <a name="translating-to-vbscript-from-jscript"></a><span data-ttu-id="a6b22-103">Convertendo para VBScript do JScript</span><span class="sxs-lookup"><span data-stu-id="a6b22-103">Translating to VBScript from JScript</span></span>

<span data-ttu-id="a6b22-104">No VBScript, a **para**... **Cada** loop enumera os membros de uma coleção; no JScript, a **para**... o loop **in** enumera os membros de um objeto ou matriz JScript.</span><span class="sxs-lookup"><span data-stu-id="a6b22-104">In VBScript, the **For**...**Each** loop enumerates the members of a collection; in JScript, the **for**...**in** loop enumerates the members of a JScript object or array.</span></span> <span data-ttu-id="a6b22-105">Para enumerar uma coleção em JScript, use um objeto de enumerador.</span><span class="sxs-lookup"><span data-stu-id="a6b22-105">To enumerate a collection in JScript, use an Enumerator object.</span></span>

<span data-ttu-id="a6b22-106">O JScript fornece o objeto Error, que pode ser usado para interceptar e manipular erros.</span><span class="sxs-lookup"><span data-stu-id="a6b22-106">JScript provides the Error object, which can be used to trap and handle errors.</span></span> <span data-ttu-id="a6b22-107">O objeto de erro é análogo ao objeto VBScript Err.</span><span class="sxs-lookup"><span data-stu-id="a6b22-107">The Error object is analogous to the VBScript Err object.</span></span>

<span data-ttu-id="a6b22-108">No JScript, há vários tipos de dados, como números, cadeias de caracteres, Boolianos, objetos e o atributo nulo.</span><span class="sxs-lookup"><span data-stu-id="a6b22-108">In JScript, there are several data types such as numbers, strings, Booleans, objects, and the null attribute.</span></span> <span data-ttu-id="a6b22-109">O VBScript usa apenas um tipo de dados, **Variant**, que pode ser subtipoado para representar cadeias de caracteres, números, Boolianos e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="a6b22-109">VBScript only uses one data type, **Variant**, which can be subtyped to represent strings, numbers, Booleans, and so on.</span></span>

<span data-ttu-id="a6b22-110">No JScript, as matrizes podem ser expandidas dinamicamente definindo um novo valor para a propriedade Length da matriz.</span><span class="sxs-lookup"><span data-stu-id="a6b22-110">In JScript, arrays can be expanded dynamically by setting a new value for the array's length property.</span></span> <span data-ttu-id="a6b22-111">No VBScript, as matrizes não podem ser ampliadas; Eles devem ser redimensionados usando a instrução **ReDim** .</span><span class="sxs-lookup"><span data-stu-id="a6b22-111">In VBScript, arrays cannot be enlarged; they must be redimensioned using the **redim** statement.</span></span>

<span data-ttu-id="a6b22-112">As funções de suporte a VBScript e JScript.</span><span class="sxs-lookup"><span data-stu-id="a6b22-112">Both VBScript and JScript support functions.</span></span> <span data-ttu-id="a6b22-113">O VBScript, no entanto, também oferece suporte a sub-rotinas.</span><span class="sxs-lookup"><span data-stu-id="a6b22-113">VBScript, however, also supports subroutines.</span></span> <span data-ttu-id="a6b22-114">As sub-rotinas são semelhantes às funções, mas não retornam um valor.</span><span class="sxs-lookup"><span data-stu-id="a6b22-114">Subroutines are similar to functions but do not return a value.</span></span>

<span data-ttu-id="a6b22-115">O JScript diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a6b22-115">JScript is case-sensitive.</span></span> <span data-ttu-id="a6b22-116">O VBScript não é.</span><span class="sxs-lookup"><span data-stu-id="a6b22-116">VBScript is not.</span></span>

<span data-ttu-id="a6b22-117">O JScript é compatível com uma ampla variedade de navegadores da Web, incluindo o Internet Explorer e o Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="a6b22-117">JScript is supported by a wide variety of Web browsers, including both Internet Explorer and Netscape Navigator.</span></span> <span data-ttu-id="a6b22-118">O Netscape Navigator não oferece suporte a VBScript.</span><span class="sxs-lookup"><span data-stu-id="a6b22-118">Netscape Navigator does not support VBScript.</span></span>

<span data-ttu-id="a6b22-119">As matrizes JScript não são matrizes do tipo de variável **Variant SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="a6b22-119">JScript arrays are not arrays of the variable type **VARIANT SAFEARRAY**.</span></span> <span data-ttu-id="a6b22-120">Um script JScript deve usar um objeto VBArray para acessar a variável **Variant SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="a6b22-120">A JScript script must use a VBArray object to access the **VARIANT SAFEARRAY** variable.</span></span> <span data-ttu-id="a6b22-121">Os scripts VBScript podem acessar as variáveis **Variant SafeArray** diretamente.</span><span class="sxs-lookup"><span data-stu-id="a6b22-121">VBScript scripts can access **VARIANT SAFEARRAY** variables directly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6b22-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a6b22-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6b22-123">Convertendo para VBScript</span><span class="sxs-lookup"><span data-stu-id="a6b22-123">Translating to VBScript</span></span>](translating-to-vbscript.md)
</dt> </dl>

 

 




