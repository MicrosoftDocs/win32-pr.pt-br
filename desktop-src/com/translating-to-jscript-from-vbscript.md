---
title: Convertendo para JScript do VBScript
description: Convertendo para JScript do VBScript
ms.assetid: cdf04a01-8bc3-4f37-872b-3a0aae962f26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a18c2ccb11ffa4f5f000d8cfc73f7db6f857cf6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635079"
---
# <a name="translating-to-jscript-from-vbscript"></a><span data-ttu-id="b2f7c-103">Convertendo para JScript do VBScript</span><span class="sxs-lookup"><span data-stu-id="b2f7c-103">Translating to JScript from VBScript</span></span>

<span data-ttu-id="b2f7c-104">No VBScript, a **para**... **Cada** loop enumera os membros de uma coleção; no JScript, a **para**... o loop **in** enumera os membros de um objeto ou matriz JScript.</span><span class="sxs-lookup"><span data-stu-id="b2f7c-104">In VBScript, the **For**...**Each** loop enumerates the members of a collection; in JScript, the **for**...**in** loop enumerates the members of a JScript object or array.</span></span> <span data-ttu-id="b2f7c-105">Para enumerar uma coleção em JScript, use um objeto de enumerador.</span><span class="sxs-lookup"><span data-stu-id="b2f7c-105">To enumerate a collection in JScript, use an Enumerator object.</span></span>

<span data-ttu-id="b2f7c-106">No JScript, há vários tipos de dados, como números, cadeias de caracteres, Boolianos, objetos e o atributo nulo.</span><span class="sxs-lookup"><span data-stu-id="b2f7c-106">In JScript, there are several data types such as numbers, strings, Booleans, objects, and the null attribute.</span></span> <span data-ttu-id="b2f7c-107">O VBScript usa apenas um tipo de dados, **Variant**, que pode ser subtipoado para representar cadeias de caracteres, números, Boolianos e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="b2f7c-107">VBScript only uses one data type, **Variant**, which can be subtyped to represent strings, numbers, Booleans, and so on.</span></span>

<span data-ttu-id="b2f7c-108">No JScript, as matrizes podem ser expandidas dinamicamente definindo um novo valor para a propriedade Length da matriz.</span><span class="sxs-lookup"><span data-stu-id="b2f7c-108">In JScript, arrays can be expanded dynamically by setting a new value for the array's length property.</span></span> <span data-ttu-id="b2f7c-109">No VBScript, as matrizes não podem ser ampliadas; Eles devem ser redimensionados usando a instrução **ReDim** .</span><span class="sxs-lookup"><span data-stu-id="b2f7c-109">In VBScript, arrays cannot be enlarged; they must be redimensioned using the **redim** statement.</span></span>

<span data-ttu-id="b2f7c-110">As funções de suporte a VBScript e JScript.</span><span class="sxs-lookup"><span data-stu-id="b2f7c-110">Both VBScript and JScript support functions.</span></span> <span data-ttu-id="b2f7c-111">O VBScript, no entanto, também oferece suporte a sub-rotinas.</span><span class="sxs-lookup"><span data-stu-id="b2f7c-111">VBScript, however, also supports subroutines.</span></span> <span data-ttu-id="b2f7c-112">As sub-rotinas são semelhantes às funções, mas não retornam um valor.</span><span class="sxs-lookup"><span data-stu-id="b2f7c-112">Subroutines are similar to functions but do not return a value.</span></span>

<span data-ttu-id="b2f7c-113">O JScript diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b2f7c-113">JScript is case-sensitive.</span></span> <span data-ttu-id="b2f7c-114">O VBScript não é.</span><span class="sxs-lookup"><span data-stu-id="b2f7c-114">VBScript is not.</span></span>

<span data-ttu-id="b2f7c-115">O JScript é compatível com o Internet Explorer e com o Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="b2f7c-115">JScript is supported by both Internet Explorer and Netscape Navigator.</span></span> <span data-ttu-id="b2f7c-116">O Netscape Navigator não oferece suporte a VBScript.</span><span class="sxs-lookup"><span data-stu-id="b2f7c-116">Netscape Navigator does not support VBScript.</span></span>

<span data-ttu-id="b2f7c-117">O JScript fornece o objeto Error, que pode ser usado para interceptar e manipular erros.</span><span class="sxs-lookup"><span data-stu-id="b2f7c-117">JScript provides the Error object, which can be used to trap and handle errors.</span></span> <span data-ttu-id="b2f7c-118">O objeto de erro é análogo ao objeto VBScript Err.</span><span class="sxs-lookup"><span data-stu-id="b2f7c-118">The Error object is analogous to the VBScript Err object.</span></span>

<span data-ttu-id="b2f7c-119">As matrizes JScript não são matrizes do tipo de variável **Variant SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="b2f7c-119">JScript arrays are not arrays of the variable type **VARIANT SAFEARRAY**.</span></span> <span data-ttu-id="b2f7c-120">Se o script receber uma variável **Variant SafeArray** de um objeto com ou script VBScript, ele deverá usar um objeto VBArray para acessar a variável **Variant SafeArray** .</span><span class="sxs-lookup"><span data-stu-id="b2f7c-120">If your script receives a **VARIANT SAFEARRAY** variable from a COM object or VBScript script, it must use a VBArray object to access the **VARIANT SAFEARRAY** variable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2f7c-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b2f7c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2f7c-122">Traduzindo para o JScript</span><span class="sxs-lookup"><span data-stu-id="b2f7c-122">Translating to JScript</span></span>](translating-to-jscript.md)
</dt> </dl>

 

 




