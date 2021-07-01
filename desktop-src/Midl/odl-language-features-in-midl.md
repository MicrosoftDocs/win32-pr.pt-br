---
title: Recursos de linguagem ODL em MIDL
description: Atributos, palavras-chave, instruções e diretivas do ODL (Object Description Language) que fazem parte do MIDL.
ms.assetid: beca14a6-01c4-4605-b1c5-214d48a7f46a
keywords:
- MIDL e ODL MIDL, recursos de linguagem
- ODL MIDL , em MIDL
- ODL MIDL, atributos
- ODL MIDL , palavras-chave
- ODL MIDL, instruções
- ODL MIDL, diretivas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db346a664ed7b8f7beeacfe73cc928a924befe10
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119781"
---
# <a name="odl-language-features-in-midl"></a><span data-ttu-id="fd1e5-109">Recursos de linguagem ODL em MIDL</span><span class="sxs-lookup"><span data-stu-id="fd1e5-109">ODL Language Features in MIDL</span></span>

> [!Note]  
> <span data-ttu-id="fd1e5-110">A Mktyplib.exe de dados está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="fd1e5-110">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="fd1e5-111">Em vez disso, use o compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="fd1e5-111">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="fd1e5-112">Os tópicos a seguir listam os atributos, palavras-chave, instruções e diretivas do ODL (Object Description Language) que agora fazem parte do linguagem IDL da Microsoft (MIDL):</span><span class="sxs-lookup"><span data-stu-id="fd1e5-112">The following topics list the Object Description Language (ODL) attributes, keywords, statements, and directives that are now part of the Microsoft Interface Definition Language (MIDL):</span></span>

-   [<span data-ttu-id="fd1e5-113">Atributos ODL</span><span class="sxs-lookup"><span data-stu-id="fd1e5-113">ODL Attributes</span></span>](#odl-attributes)
-   [<span data-ttu-id="fd1e5-114">Palavras-chave, instruções e diretivas ODL</span><span class="sxs-lookup"><span data-stu-id="fd1e5-114">ODL Keywords, Statements, and Directives</span></span>](#odl-keywords-statements-and-directives)

## <a name="odl-attributes"></a><span data-ttu-id="fd1e5-115">Atributos ODL</span><span class="sxs-lookup"><span data-stu-id="fd1e5-115">ODL Attributes</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="fd1e5-116">\[[**appobject**](appobject.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-116">\[[**appobject**](appobject.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="fd1e5-117">\[[**Ligável**](bindable.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-117">\[[**bindable**](bindable.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="fd1e5-118">\[[**Controle**](control.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-118">\[[**control**](control.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="fd1e5-119">\[[**Padrão**](default.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-119">\[[**default**](default.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="fd1e5-120">\[[**Defaultvalue**](defaultvalue.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-120">\[[**defaultvalue**](defaultvalue.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="fd1e5-121">\[[**displaybind**](displaybind.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-121">\[[**displaybind**](displaybind.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="fd1e5-122">\[[**Dllname**](dllname-str-.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-122">\[[**dllname**](dllname-str-.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="fd1e5-123">\[[**Dupla**](dual.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-123">\[[**dual**](dual.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="fd1e5-124">\[[**Entrada**](entry.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-124">\[[**entry**](entry.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="fd1e5-125">\[[**Helpcontext**](helpcontext.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-125">\[[**helpcontext**](helpcontext.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="fd1e5-126">\[[**Helpstring**](helpstring.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-126">\[[**helpstring**](helpstring.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="fd1e5-127">\[[**Helpfile**](helpfile.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-127">\[[**helpfile**](helpfile.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="fd1e5-128">\[[**Escondidos**](hidden.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-128">\[[**hidden**](hidden.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="fd1e5-129">\[[**Id**](id.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-129">\[[**id**](id.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="fd1e5-130">\[[**immediatebind**](immediatebind.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-130">\[[**immediatebind**](immediatebind.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="fd1e5-131">\[[**Em**](in.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-131">\[[**in**](in.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="fd1e5-132">\[[**Lcid**](lcid.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-132">\[[**lcid**](lcid.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="fd1e5-133">\[[**Licenciado**](licensed.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-133">\[[**licensed**](licensed.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="fd1e5-134">\[[**Nonextensible**](nonextensible.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-134">\[[**nonextensible**](nonextensible.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="fd1e5-135">\[[**Odl**](odl.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-135">\[[**odl**](odl.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="fd1e5-136">\[[**Oleautomation**](oleautomation.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-136">\[[**oleautomation**](oleautomation.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="fd1e5-137">\[[**Opcional**](optional.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-137">\[[**optional**](optional.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="fd1e5-138">\[[**out**](out-idl.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-138">\[[**out**](out-idl.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="fd1e5-139">\[[**Propget**](propget.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-139">\[[**propget**](propget.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="fd1e5-140">\[[**Propput**](propput.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-140">\[[**propput**](propput.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="fd1e5-141">\[[**Propputref**](propputref.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-141">\[[**propputref**](propputref.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="fd1e5-142">\[[**Público**](public.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-142">\[[**public**](public.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="fd1e5-143">\[[ **readonly**](readonly.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-143">\[ [**readonly**](readonly.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="fd1e5-144">\[[**Requestedit**](requestedit.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-144">\[[**requestedit**](requestedit.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="fd1e5-145">\[[**Restrito**](restricted.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-145">\[[**restricted**](restricted.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="fd1e5-146">\[[**Retval**](retval.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-146">\[[**retval**](retval.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="fd1e5-147">\[[**Fonte**](source.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-147">\[[**source**](source.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="fd1e5-148">\[[**Uuid**](uuid.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-148">\[[**uuid**](uuid.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="fd1e5-149">[**Vararg**](vararg.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-149">[**vararg**](vararg.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="fd1e5-150">\[[**Versão**](version.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-150">\[[**version**](version.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="fd1e5-151">Â</span><span class="sxs-lookup"><span data-stu-id="fd1e5-151">Â</span></span>
    :::column-end:::
:::row-end:::

## <a name="odl-keywords-statements-and-directives"></a><span data-ttu-id="fd1e5-152">Palavras-chave, instruções e diretivas ODL</span><span class="sxs-lookup"><span data-stu-id="fd1e5-152">ODL Keywords, Statements, and Directives</span></span>

[<span data-ttu-id="fd1e5-153">**coclass**</span><span class="sxs-lookup"><span data-stu-id="fd1e5-153">**coclass**</span></span>](coclass.md)

[<span data-ttu-id="fd1e5-154">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="fd1e5-154">**dispinterface**</span></span>](dispinterface.md)

[<span data-ttu-id="fd1e5-155">**Enum**</span><span class="sxs-lookup"><span data-stu-id="fd1e5-155">**enum**</span></span>](enum.md)

<span data-ttu-id="fd1e5-156">\[[**Importlib**](importlib.md)\]</span><span class="sxs-lookup"><span data-stu-id="fd1e5-156">\[[**importlib**](importlib.md)\]</span></span>

[<span data-ttu-id="fd1e5-157">**Interface**</span><span class="sxs-lookup"><span data-stu-id="fd1e5-157">**interface**</span></span>](interface.md)

[<span data-ttu-id="fd1e5-158">**Biblioteca**</span><span class="sxs-lookup"><span data-stu-id="fd1e5-158">**library**</span></span>](library.md)

[<span data-ttu-id="fd1e5-159">**Módulo**</span><span class="sxs-lookup"><span data-stu-id="fd1e5-159">**module**</span></span>](module.md)

[<span data-ttu-id="fd1e5-160">**Struct**</span><span class="sxs-lookup"><span data-stu-id="fd1e5-160">**struct**</span></span>](struct.md)

[<span data-ttu-id="fd1e5-161">**Typedef**</span><span class="sxs-lookup"><span data-stu-id="fd1e5-161">**typedef**</span></span>](typedef.md)

[<span data-ttu-id="fd1e5-162">**União**</span><span class="sxs-lookup"><span data-stu-id="fd1e5-162">**union**</span></span>](union.md)

<span data-ttu-id="fd1e5-163">Para obter informações sobre como efetuar marshaling de tipos de Automação OLE, como **BSTR,** **VARIANT** e **SAFEARRAY,** consulte [Marshaling de tipos](marshaling-ole-data-types.md)de dados OLE .</span><span class="sxs-lookup"><span data-stu-id="fd1e5-163">For information on how to marshal OLE Automation types, such as **BSTR**, **VARIANT**, and **SAFEARRAY**, see [Marshaling OLE Data Types](marshaling-ole-data-types.md).</span></span>

 

 




