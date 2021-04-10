---
title: atributo entry
description: O atributo \ entry \ especifica uma função exportada ou constante em um módulo identificando o ponto de entrada na DLL.
ms.assetid: 1d2d6429-d828-44ec-8b0a-cefb64c6e706
keywords:
- MIDL do atributo de entrada
topic_type:
- apiref
api_name:
- entry
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e596284a83c48bcfc84ef4f7985aed7c33ba7da
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293929"
---
# <a name="entry-attribute"></a><span data-ttu-id="445c9-104">atributo entry</span><span class="sxs-lookup"><span data-stu-id="445c9-104">entry attribute</span></span>

<span data-ttu-id="445c9-105">O atributo de **\[ entrada \]** especifica uma função exportada ou constante em um módulo identificando o ponto de entrada na dll.</span><span class="sxs-lookup"><span data-stu-id="445c9-105">The **\[entry\]** attribute specifies an exported function or constant in a module by identifying the entry point in the DLL.</span></span>

``` syntax
[
    uuid(uuid-number), 
    entry(entry-id)
  [, optional-attribute-list]
]
module modulename 
{
    elementlist
};
```

## <a name="parameters"></a><span data-ttu-id="445c9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="445c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="445c9-107">*UUID-número*</span><span class="sxs-lookup"><span data-stu-id="445c9-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="445c9-108">Especifica um número de identificação universalmente exclusivo para o [**módulo**](module.md).</span><span class="sxs-lookup"><span data-stu-id="445c9-108">Specifies a universally unique identification number for the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="445c9-109">*ID de entrada*</span><span class="sxs-lookup"><span data-stu-id="445c9-109">*entry-id*</span></span> 
</dt> <dd>

<span data-ttu-id="445c9-110">Especifica o nome da função do ponto de entrada do módulo ou o número de identificação do inteiro.</span><span class="sxs-lookup"><span data-stu-id="445c9-110">Specifies the module entry point function name or integer identification number.</span></span>

</dd> <dt>

<span data-ttu-id="445c9-111">*lista de atributos opcionais*</span><span class="sxs-lookup"><span data-stu-id="445c9-111">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="445c9-112">Especifica zero ou mais atributos para o compilador MIDL aplicar ao [**módulo**](module.md).</span><span class="sxs-lookup"><span data-stu-id="445c9-112">Specifies zero or more attributes for the MIDL compiler to apply to the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="445c9-113">*ModuleName*</span><span class="sxs-lookup"><span data-stu-id="445c9-113">*modulename*</span></span> 
</dt> <dd>

<span data-ttu-id="445c9-114">Especifica o nome que outros componentes de software usam para denotar o [**módulo**](module.md).</span><span class="sxs-lookup"><span data-stu-id="445c9-114">Specifies the name other software components use to denote the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="445c9-115">*elementolist*</span><span class="sxs-lookup"><span data-stu-id="445c9-115">*elementlist*</span></span> 
</dt> <dd>

<span data-ttu-id="445c9-116">Especifica uma ou mais instruções de definição de elemento de módulo.</span><span class="sxs-lookup"><span data-stu-id="445c9-116">Specifies one or more module element definition statements.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="445c9-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="445c9-117">Remarks</span></span>

<span data-ttu-id="445c9-118">Se a variável *EntryID* do atributo de **\[ entrada \]** for uma cadeia de caracteres, esse será um ponto de entrada nomeado.</span><span class="sxs-lookup"><span data-stu-id="445c9-118">If the *entryid* variable of the **\[entry\]** attribute is a string, this is a named entry point.</span></span> <span data-ttu-id="445c9-119">Se *EntryID* for um número, o ponto de entrada será definido por um ordinal.</span><span class="sxs-lookup"><span data-stu-id="445c9-119">If *entryid* is a number, the entry point is defined by an ordinal.</span></span> <span data-ttu-id="445c9-120">Esse atributo fornece uma maneira de obter o endereço de uma função em um módulo.</span><span class="sxs-lookup"><span data-stu-id="445c9-120">This attribute provides a way to obtain the address of a function in a module.</span></span>

## <a name="examples"></a><span data-ttu-id="445c9-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="445c9-121">Examples</span></span>

``` syntax
[
    dllname("MyAppsFirst.dll")
] 
module MyModule
{
    [entry(20), bindable, requestedit, 
     propputref, defaultbind ] HRESULT Func1(
         [in]IUnknown * Param1, 
         [out] MyType * Param2);
    [entry("TwentyOne"), hidden, vararg] SAFEARRAY (int) Func2(
        [in, out] SAFEARRAY (variant) *varP) ;
    [entry(22)] Float Func3(
        [in] lpstr pName, [in] double dLevel,
        [out] short * sByte) ;
    } ;
```

## <a name="see-also"></a><span data-ttu-id="445c9-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="445c9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="445c9-123">**nomedadll**</span><span class="sxs-lookup"><span data-stu-id="445c9-123">**dllname**</span></span>](dllname-str-.md)
</dt> <dt>

[<span data-ttu-id="445c9-124">**modulo**</span><span class="sxs-lookup"><span data-stu-id="445c9-124">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="445c9-125">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="445c9-125">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="445c9-126">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="445c9-126">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="445c9-127">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="445c9-127">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 