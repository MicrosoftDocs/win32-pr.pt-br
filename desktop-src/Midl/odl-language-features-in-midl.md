---
title: Recursos de linguagem ODL no MIDL
description: Atributos de linguagem de descrição de objeto (ODL), palavras-chave, instruções e diretivas que fazem parte do MIDL.
ms.assetid: beca14a6-01c4-4605-b1c5-214d48a7f46a
keywords:
- MIDL e ODL, recursos de linguagem
- ODL MIDL, no MIDL
- ODL MIDL, atributos
- ODL MIDL, palavras-chave
- ODL MIDL, instruções
- ODL MIDL, diretivas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49e525322eb185e38303b387dc4aa0007322e713
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822925"
---
# <a name="odl-language-features-in-midl"></a><span data-ttu-id="07933-109">Recursos de linguagem ODL no MIDL</span><span class="sxs-lookup"><span data-stu-id="07933-109">ODL Language Features in MIDL</span></span>

> [!Note]  
> <span data-ttu-id="07933-110">A ferramenta de Mktyplib.exe está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="07933-110">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="07933-111">Em vez disso, use o compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="07933-111">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="07933-112">Os tópicos a seguir listam os atributos de linguagem de descrição de objeto (ODL), palavras-chave, instruções e diretivas que agora fazem parte do linguagem IDL da Microsoft (MIDL):</span><span class="sxs-lookup"><span data-stu-id="07933-112">The following topics list the Object Description Language (ODL) attributes, keywords, statements, and directives that are now part of the Microsoft Interface Definition Language (MIDL):</span></span>

-   [<span data-ttu-id="07933-113">Atributos ODL</span><span class="sxs-lookup"><span data-stu-id="07933-113">ODL Attributes</span></span>](#odl-attributes)
-   [<span data-ttu-id="07933-114">Palavras-chave, instruções e diretivas do ODL</span><span class="sxs-lookup"><span data-stu-id="07933-114">ODL Keywords, Statements, and Directives</span></span>](#odl-keywords-statements-and-directives)

## <a name="odl-attributes"></a><span data-ttu-id="07933-115">Atributos ODL</span><span class="sxs-lookup"><span data-stu-id="07933-115">ODL Attributes</span></span>



|                                            |                                        |
|--------------------------------------------|----------------------------------------|
| <span data-ttu-id="07933-116">\[[**appobject**](appobject.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-116">\[[**appobject**](appobject.md)\]</span></span>         | <span data-ttu-id="07933-117">\[[**vinculáveis**](bindable.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-117">\[[**bindable**](bindable.md)\]</span></span>       |
| <span data-ttu-id="07933-118">\[[**controlo**](control.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-118">\[[**control**](control.md)\]</span></span>             | <span data-ttu-id="07933-119">\[[**os**](default.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-119">\[[**default**](default.md)\]</span></span>         |
| <span data-ttu-id="07933-120">\[[**ValorPadrão**](defaultvalue.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-120">\[[**defaultvalue**](defaultvalue.md)\]</span></span>   | <span data-ttu-id="07933-121">\[[**displaybind**](displaybind.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-121">\[[**displaybind**](displaybind.md)\]</span></span> |
| <span data-ttu-id="07933-122">\[[**nomedadll**](dllname-str-.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-122">\[[**dllname**](dllname-str-.md)\]</span></span>        | <span data-ttu-id="07933-123">\[[**simplifica**](dual.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-123">\[[**dual**](dual.md)\]</span></span>               |
| <span data-ttu-id="07933-124">\[[**inicial**](entry.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-124">\[[**entry**](entry.md)\]</span></span>                 | <span data-ttu-id="07933-125">\[[**identificação**](helpcontext.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-125">\[[**helpcontext**](helpcontext.md)\]</span></span> |
| <span data-ttu-id="07933-126">\[[**HelpString**](helpstring.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-126">\[[**helpstring**](helpstring.md)\]</span></span>       | <span data-ttu-id="07933-127">\[[**HelpFile**](helpfile.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-127">\[[**helpfile**](helpfile.md)\]</span></span>       |
| <span data-ttu-id="07933-128">\[[**oculto**](hidden.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-128">\[[**hidden**](hidden.md)\]</span></span>               | <span data-ttu-id="07933-129">\[[**sessão**](id.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-129">\[[**id**](id.md)\]</span></span>                   |
| <span data-ttu-id="07933-130">\[[**immediatebind**](immediatebind.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-130">\[[**immediatebind**](immediatebind.md)\]</span></span> | <span data-ttu-id="07933-131">\[[**no**](in.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-131">\[[**in**](in.md)\]</span></span>                   |
| <span data-ttu-id="07933-132">\[[**LCID**](lcid.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-132">\[[**lcid**](lcid.md)\]</span></span>                   | <span data-ttu-id="07933-133">\[[**licenças**](licensed.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-133">\[[**licensed**](licensed.md)\]</span></span>       |
| <span data-ttu-id="07933-134">\[[**performancecategory**](nonextensible.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-134">\[[**nonextensible**](nonextensible.md)\]</span></span> | <span data-ttu-id="07933-135">\[[**odl**](odl.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-135">\[[**odl**](odl.md)\]</span></span>                 |
| <span data-ttu-id="07933-136">\[[**oleautomation**](oleautomation.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-136">\[[**oleautomation**](oleautomation.md)\]</span></span> | <span data-ttu-id="07933-137">\[[**adicional**](optional.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-137">\[[**optional**](optional.md)\]</span></span>       |
| <span data-ttu-id="07933-138">\[[**fora**](out-idl.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-138">\[[**out**](out-idl.md)\]</span></span>                 | <span data-ttu-id="07933-139">\[[**propget**](propget.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-139">\[[**propget**](propget.md)\]</span></span>         |
| <span data-ttu-id="07933-140">\[[**propput**](propput.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-140">\[[**propput**](propput.md)\]</span></span>             | <span data-ttu-id="07933-141">\[[**propputref**](propputref.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-141">\[[**propputref**](propputref.md)\]</span></span>   |
| <span data-ttu-id="07933-142">\[[**publicada**](public.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-142">\[[**public**](public.md)\]</span></span>               | <span data-ttu-id="07933-143">\[[ **somente leitura**](readonly.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-143">\[ [**readonly**](readonly.md)\]</span></span>      |
| <span data-ttu-id="07933-144">\[[**requestedit**](requestedit.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-144">\[[**requestedit**](requestedit.md)\]</span></span>     | <span data-ttu-id="07933-145">\[[**Restricted**](restricted.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-145">\[[**restricted**](restricted.md)\]</span></span>   |
| <span data-ttu-id="07933-146">\[[**retval**](retval.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-146">\[[**retval**](retval.md)\]</span></span>               | <span data-ttu-id="07933-147">\[[**original**](source.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-147">\[[**source**](source.md)\]</span></span>           |
| <span data-ttu-id="07933-148">\[[**personalizado**](uuid.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-148">\[[**uuid**](uuid.md)\]</span></span>                   | <span data-ttu-id="07933-149">[**vararg**](vararg.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-149">[**vararg**](vararg.md)\]</span></span>             |
| <span data-ttu-id="07933-150">\[[**Versão**](version.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-150">\[[**version**](version.md)\]</span></span>             | <span data-ttu-id="07933-151">Â</span><span class="sxs-lookup"><span data-stu-id="07933-151">Â</span></span>                                      |



 

## <a name="odl-keywords-statements-and-directives"></a><span data-ttu-id="07933-152">Palavras-chave, instruções e diretivas do ODL</span><span class="sxs-lookup"><span data-stu-id="07933-152">ODL Keywords, Statements, and Directives</span></span>



|                                        |
|----------------------------------------|
| [<span data-ttu-id="07933-153">**coclass**</span><span class="sxs-lookup"><span data-stu-id="07933-153">**coclass**</span></span>](coclass.md)             |
| [<span data-ttu-id="07933-154">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="07933-154">**dispinterface**</span></span>](dispinterface.md) |
| [<span data-ttu-id="07933-155">**enumera**</span><span class="sxs-lookup"><span data-stu-id="07933-155">**enum**</span></span>](enum.md)                   |
| <span data-ttu-id="07933-156">\[[**importlib**](importlib.md)\]</span><span class="sxs-lookup"><span data-stu-id="07933-156">\[[**importlib**](importlib.md)\]</span></span>     |
| [<span data-ttu-id="07933-157">**interface**</span><span class="sxs-lookup"><span data-stu-id="07933-157">**interface**</span></span>](interface.md)         |
| [<span data-ttu-id="07933-158">**biblioteca**</span><span class="sxs-lookup"><span data-stu-id="07933-158">**library**</span></span>](library.md)             |
| [<span data-ttu-id="07933-159">**modulo**</span><span class="sxs-lookup"><span data-stu-id="07933-159">**module**</span></span>](module.md)               |
| [<span data-ttu-id="07933-160">**struct**</span><span class="sxs-lookup"><span data-stu-id="07933-160">**struct**</span></span>](struct.md)               |
| [<span data-ttu-id="07933-161">**typedef**</span><span class="sxs-lookup"><span data-stu-id="07933-161">**typedef**</span></span>](typedef.md)             |
| [<span data-ttu-id="07933-162">**unida**</span><span class="sxs-lookup"><span data-stu-id="07933-162">**union**</span></span>](union.md)                 |



 

<span data-ttu-id="07933-163">Para obter informações sobre como realizar marshaling de tipos de automação OLE, como **BSTR**, **Variant** e **SafeArray**, consulte [marshaling OLE Data Types](marshaling-ole-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="07933-163">For information on how to marshal OLE Automation types, such as **BSTR**, **VARIANT**, and **SAFEARRAY**, see [Marshaling OLE Data Types](marshaling-ole-data-types.md).</span></span>

 

 




