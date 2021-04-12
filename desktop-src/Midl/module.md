---
title: atributo de módulo
description: A instrução Module define um grupo de funções, normalmente um conjunto de pontos de entrada de DLL.
ms.assetid: 4dec207f-98bc-4784-a3c9-506ffe7523fe
keywords:
- atributo de módulo MIDL
topic_type:
- apiref
api_name:
- module
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1eb310c3e126caf9b25b8c015b840aea11791d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293974"
---
# <a name="module-attribute"></a><span data-ttu-id="ddae2-104">atributo de módulo</span><span class="sxs-lookup"><span data-stu-id="ddae2-104">module attribute</span></span>

<span data-ttu-id="ddae2-105">A instrução **Module** define um grupo de funções, normalmente um conjunto de pontos de entrada de dll.</span><span class="sxs-lookup"><span data-stu-id="ddae2-105">The **module** statement defines a group of functions, typically a set of DLL entry points.</span></span>

``` syntax
[
    attributes
]
module modulename 
{
    elementlist
};
```

## <a name="parameters"></a><span data-ttu-id="ddae2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ddae2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddae2-107">*attributes*</span><span class="sxs-lookup"><span data-stu-id="ddae2-107">*attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="ddae2-108">Os \[ atributos [**UUID**](uuid.md) \] , \[ [**version**](version.md) \] , \[ [**helptype**](helpstring.md) \] , \[ [**HelpContext**](helpcontext.md) \] , \[ [**Hidden**](hidden.md) \] e \[ [**DllName**](dllname-str-.md) \] são aceitos antes de uma instrução de **módulo** .</span><span class="sxs-lookup"><span data-stu-id="ddae2-108">The \[[**uuid**](uuid.md)\], \[[**version**](version.md)\], \[[**helpstring**](helpstring.md)\], \[[**helpcontext**](helpcontext.md)\], \[[**hidden**](hidden.md)\], and \[[**dllname**](dllname-str-.md)\] attributes are accepted before a **module** statement.</span></span> <span data-ttu-id="ddae2-109">Consulte [descrições de atributo](/previous-versions/windows/desktop/automat/attribute-descriptions), no livro de automação OLE, para obter mais informações sobre os atributos aceitos antes de uma definição de módulo.</span><span class="sxs-lookup"><span data-stu-id="ddae2-109">See [Attribute Descriptions](/previous-versions/windows/desktop/automat/attribute-descriptions), in the OLE Automation book, for more information on the attributes accepted before a module definition.</span></span> <span data-ttu-id="ddae2-110">O \[ atributo **DllName** \] é necessário.</span><span class="sxs-lookup"><span data-stu-id="ddae2-110">The \[**dllname**\] attribute is required.</span></span> <span data-ttu-id="ddae2-111">Se o \[ atributo **UUID** \] for omitido, o módulo não será especificado exclusivamente no sistema.</span><span class="sxs-lookup"><span data-stu-id="ddae2-111">If the \[**uuid**\] attribute is omitted, the module is not uniquely specified in the system.</span></span>

</dd> <dt>

<span data-ttu-id="ddae2-112">*ModuleName*</span><span class="sxs-lookup"><span data-stu-id="ddae2-112">*modulename*</span></span> 
</dt> <dd>

<span data-ttu-id="ddae2-113">O nome do módulo.</span><span class="sxs-lookup"><span data-stu-id="ddae2-113">The name of the module.</span></span>

</dd> <dt>

<span data-ttu-id="ddae2-114">*elementolist*</span><span class="sxs-lookup"><span data-stu-id="ddae2-114">*elementlist*</span></span> 
</dt> <dd>

<span data-ttu-id="ddae2-115">Lista de definições de constantes e protótipos de função para cada função na DLL.</span><span class="sxs-lookup"><span data-stu-id="ddae2-115">List of constant definitions and function prototypes for each function in the DLL.</span></span> <span data-ttu-id="ddae2-116">Qualquer número de definições de função pode aparecer na lista de funções.</span><span class="sxs-lookup"><span data-stu-id="ddae2-116">Any number of function definitions can appear in the function list.</span></span> <span data-ttu-id="ddae2-117">Uma função na lista de funções tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="ddae2-117">A function in the function list has the following form:</span></span>

<span data-ttu-id="ddae2-118">\[*atributos* \] do *ReturnType* \[ *chamando convenção funcname* \] (*params*);</span><span class="sxs-lookup"><span data-stu-id="ddae2-118">\[*attributes*\] *returntype* \[*calling convention funcname*\](*params*);</span></span>

<span data-ttu-id="ddae2-119">\[*atributos* \] do [**const**](const.md) constante *constname*  =  *constval*;</span><span class="sxs-lookup"><span data-stu-id="ddae2-119">\[*attributes*\] [**const**](const.md) constanttype *constname* = *constval*;</span></span>

<span data-ttu-id="ddae2-120">Somente os \[ atributos [**HelpString**](helpstring.md) \] e \[ [**HelpContext**](helpcontext.md) \] são aceitos para uma [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="ddae2-120">Only the \[[**helpstring**](helpstring.md)\] and \[[**helpcontext**](helpcontext.md)\] attributes are accepted for a [**const**](const.md).</span></span>

<span data-ttu-id="ddae2-121">Os seguintes atributos são aceitos em uma função em um módulo: \[ [**HelpString**](helpstring.md) \] , \[ [**HelpContext**](helpcontext.md) \] , \[ [**String**](string.md) \] , \[ [**entry**](entry.md) \] , \[ [**propget**](propget.md) \] , \[ [**propput**](propput.md) \] , \[ [**propputref**](propputref.md) \] e \[ [**vararg**](vararg.md) \] .</span><span class="sxs-lookup"><span data-stu-id="ddae2-121">The following attributes are accepted on a function in a module: \[[**helpstring**](helpstring.md)\], \[[**helpcontext**](helpcontext.md)\], \[[**string**](string.md)\], \[[**entry**](entry.md)\], \[[**propget**](propget.md)\], \[[**propput**](propput.md)\], \[[**propputref**](propputref.md)\], and \[[**vararg**](vararg.md)\].</span></span> <span data-ttu-id="ddae2-122">Se \[ **vararg** \] for especificado, o último parâmetro deverá ser uma matriz segura de tipo **Variant** .</span><span class="sxs-lookup"><span data-stu-id="ddae2-122">If \[**vararg**\] is specified, the last parameter must be a safe array of **VARIANT** type.</span></span>

<span data-ttu-id="ddae2-123">A Convenção de chamada opcional pode ser um dos \_ \_ Pascal/ \_ Pascal/Pascal, \_ \_ cdecl/ \_ cdecl/cdecl ou \_ \_ stdcall/ \_ stdcall/stdcall.</span><span class="sxs-lookup"><span data-stu-id="ddae2-123">The optional calling convention can be one of \_\_pascal/\_pascal/pascal, \_\_cdecl/\_cdecl/cdecl, or \_\_stdcall/\_stdcall/stdcall.</span></span> <span data-ttu-id="ddae2-124">O *tipo de Convenção de chamada paramName* pode incluir até dois sublinhados à esquerda.</span><span class="sxs-lookup"><span data-stu-id="ddae2-124">The *calling convention type paramname* can include up to two leading underscores.</span></span>

<span data-ttu-id="ddae2-125">A lista de parâmetros é uma lista delimitada por vírgulas de:</span><span class="sxs-lookup"><span data-stu-id="ddae2-125">The parameter list is a comma-delimited list of:</span></span>

<span data-ttu-id="ddae2-126">\[*atributos*\]</span><span class="sxs-lookup"><span data-stu-id="ddae2-126">\[*attributes*\]</span></span>

<span data-ttu-id="ddae2-127">O tipo pode ser qualquer tipo ou tipo interno declarado anteriormente, um ponteiro para qualquer tipo ou um ponteiro para um tipo interno.</span><span class="sxs-lookup"><span data-stu-id="ddae2-127">The type can be any previously declared type or built-in type, a pointer to any type, or a pointer to a built-in type.</span></span> <span data-ttu-id="ddae2-128">Os atributos em parâmetros são:</span><span class="sxs-lookup"><span data-stu-id="ddae2-128">Attributes on parameters are:</span></span>

<span data-ttu-id="ddae2-129">\[[**in**](in.md) \] , \[ [**out**](out-idl.md) \] , \[ [**opcional**](optional.md) \] .</span><span class="sxs-lookup"><span data-stu-id="ddae2-129">\[[**in**](in.md)\], \[[**out**](out-idl.md)\], \[[**optional**](optional.md)\].</span></span>

<span data-ttu-id="ddae2-130">Se \[ [**opcional**](optional.md) \] for usado, os tipos desses parâmetros deverão ser **Variant** ou **Variant** \* .</span><span class="sxs-lookup"><span data-stu-id="ddae2-130">If \[[**optional**](optional.md)\] is used, the types of those parameters must be **VARIANT** or **VARIANT**\*.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ddae2-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="ddae2-131">Remarks</span></span>

<span data-ttu-id="ddae2-132">A saída do arquivo de cabeçalho (. h) para módulos é uma série de protótipos de função.</span><span class="sxs-lookup"><span data-stu-id="ddae2-132">The header file (.h) output for modules is a series of function prototypes.</span></span> <span data-ttu-id="ddae2-133">A palavra-chave do **módulo** e os colchetes ao redor são removidos da saída do arquivo de cabeçalho (. h), mas um comentário ( **//módulo** *ModuleName*) é inserido antes dos protótipos.</span><span class="sxs-lookup"><span data-stu-id="ddae2-133">The **module** keyword and surrounding brackets are stripped from the header (.h) file output, but a comment (// **module** *modulename*) is inserted before the prototypes.</span></span> <span data-ttu-id="ddae2-134">A palavra-chave **extern** é inserida antes das declarações.</span><span class="sxs-lookup"><span data-stu-id="ddae2-134">The keyword **extern** is inserted before the declarations.</span></span>

## <a name="examples"></a><span data-ttu-id="ddae2-135">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ddae2-135">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("This is not GDI.EXE"), 
    helpcontext(190), 
    dllname("MATH.DLL")
] 
module somemodule
{ 
    [helpstring("Color for the frame")] 
            unsigned long const COLOR_FRAME = 0xH80000006; 
    [helpstring("Not a rectangle but a square"), 
     entry(1)] 
            pascal double square([in] double x); 
};
```

## <a name="see-also"></a><span data-ttu-id="ddae2-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="ddae2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddae2-137">**const**</span><span class="sxs-lookup"><span data-stu-id="ddae2-137">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="ddae2-138">Conteúdo de uma biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ddae2-138">Contents of a Type Library</span></span>](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[<span data-ttu-id="ddae2-139">**nomedadll**</span><span class="sxs-lookup"><span data-stu-id="ddae2-139">**dllname**</span></span>](dllname-str-.md)
</dt> <dt>

[<span data-ttu-id="ddae2-140">**inicial**</span><span class="sxs-lookup"><span data-stu-id="ddae2-140">**entry**</span></span>](entry.md)
</dt> <dt>

[<span data-ttu-id="ddae2-141">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="ddae2-141">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="ddae2-142">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="ddae2-142">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="ddae2-143">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="ddae2-143">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="ddae2-144">**oculto**</span><span class="sxs-lookup"><span data-stu-id="ddae2-144">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="ddae2-145">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="ddae2-145">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="ddae2-146">**propget**</span><span class="sxs-lookup"><span data-stu-id="ddae2-146">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="ddae2-147">**propput**</span><span class="sxs-lookup"><span data-stu-id="ddae2-147">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="ddae2-148">**propputref**</span><span class="sxs-lookup"><span data-stu-id="ddae2-148">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="ddae2-149">**string**</span><span class="sxs-lookup"><span data-stu-id="ddae2-149">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="ddae2-150">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="ddae2-150">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="ddae2-151">**personalizado**</span><span class="sxs-lookup"><span data-stu-id="ddae2-151">**uuid**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="ddae2-152">**vararg**</span><span class="sxs-lookup"><span data-stu-id="ddae2-152">**vararg**</span></span>](vararg.md)
</dt> <dt>

[<span data-ttu-id="ddae2-153">**Versão**</span><span class="sxs-lookup"><span data-stu-id="ddae2-153">**version**</span></span>](version.md)
</dt> </dl>

 

 