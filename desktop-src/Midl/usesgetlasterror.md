---
title: atributo usesgetlasterror
description: O atributo \ usesgetlasterror \ sinaliza ao chamador que ele pode chamar GetLastError para recuperar o código de erro.
ms.assetid: 8e9ab8b5-f446-4aab-bb40-b6f78799e18e
keywords:
- usesgetlasterror do atributo MIDL
topic_type:
- apiref
api_name:
- usesgetlasterror
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0f403430f70fde71696ec2a35a34161f08bada9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640559"
---
# <a name="usesgetlasterror-attribute"></a><span data-ttu-id="bc2e0-104">atributo usesgetlasterror</span><span class="sxs-lookup"><span data-stu-id="bc2e0-104">usesgetlasterror attribute</span></span>

<span data-ttu-id="bc2e0-105">O atributo **\[ usesgetlasterror \]** sinaliza ao chamador que ele pode chamar [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para recuperar o código de erro.</span><span class="sxs-lookup"><span data-stu-id="bc2e0-105">The **\[usesgetlasterror\]** attribute signals the caller that it can call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to retrieve the error code.</span></span>

``` syntax
[
    module-attributes
]
module module-name
{
    [entry(entry-id), usesgetlasterror [, other-attributes]] return-type function-name(param-list);
};
```

## <a name="parameters"></a><span data-ttu-id="bc2e0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc2e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc2e0-107">*atributos de módulo*</span><span class="sxs-lookup"><span data-stu-id="bc2e0-107">*module-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="bc2e0-108">Zero ou mais atributos MIDL que serão aplicados ao [**módulo**](module.md).</span><span class="sxs-lookup"><span data-stu-id="bc2e0-108">Zero or more MIDL attributes that will be applied to the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc2e0-109">*nome do módulo*</span><span class="sxs-lookup"><span data-stu-id="bc2e0-109">*module-name*</span></span> 
</dt> <dd>

<span data-ttu-id="bc2e0-110">O nome do identificador do [**módulo**](module.md).</span><span class="sxs-lookup"><span data-stu-id="bc2e0-110">The identifier name of the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc2e0-111">*ID de entrada*</span><span class="sxs-lookup"><span data-stu-id="bc2e0-111">*entry-id*</span></span> 
</dt> <dd>

<span data-ttu-id="bc2e0-112">Especifica o ponto de entrada do módulo – nome da função ou número de identificação de inteiro.</span><span class="sxs-lookup"><span data-stu-id="bc2e0-112">Specifies the module entry point–function name or integer-identification number.</span></span>

</dd> <dt>

<span data-ttu-id="bc2e0-113">*outros atributos*</span><span class="sxs-lookup"><span data-stu-id="bc2e0-113">*other-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="bc2e0-114">Zero ou mais atributos MIDL que serão aplicados ao procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="bc2e0-114">Zero or more MIDL attributes that will be applied to the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="bc2e0-115">*tipo de retorno*</span><span class="sxs-lookup"><span data-stu-id="bc2e0-115">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="bc2e0-116">O tipo dos dados que o procedimento remoto retornará após a conclusão.</span><span class="sxs-lookup"><span data-stu-id="bc2e0-116">The type of the data that the remote procedure will return upon completion.</span></span>

</dd> <dt>

<span data-ttu-id="bc2e0-117">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="bc2e0-117">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="bc2e0-118">O nome do procedimento remoto conforme definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="bc2e0-118">The name of the remote procedure as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="bc2e0-119">*parâmetro-lista*</span><span class="sxs-lookup"><span data-stu-id="bc2e0-119">*param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="bc2e0-120">Zero ou mais parâmetros para o procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="bc2e0-120">Zero or more parameters to the remote procedure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc2e0-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc2e0-121">Remarks</span></span>

<span data-ttu-id="bc2e0-122">O atributo **\[ \] usesgetlasterror** pode ser definido em um ponto de entrada de módulo, se esse ponto de entrada usar a função [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) do Windows para retornar códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="bc2e0-122">The **\[usesgetlasterror\]** attribute can be set on a module entry point, if that entry point uses the Windows function [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to return error codes.</span></span> <span data-ttu-id="bc2e0-123">O atributo informa ao chamador que, se houver um erro ao chamar essa função, o chamador poderá chamar [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para recuperar o código de erro.</span><span class="sxs-lookup"><span data-stu-id="bc2e0-123">The attribute tells the caller that, if there is an error when calling that function, the caller can then call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to retrieve the error code.</span></span>

## <a name="examples"></a><span data-ttu-id="bc2e0-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bc2e0-124">Examples</span></span>

``` syntax
[
    dllname("MyOwn.dll")
] 
module MyModule
{
    [entry("One"), usesgetlasterror, bindable, requestedit,
     propputref, defaultbind] HRESULT Func1(
         [in]IUnknown * iParam1, 
         [out] long * Param2) ;
    [entry("TwentyOne"), usesgetlasterror, 
     hidden, vararg] SAFEARRAY (int) Func2(
         [in, out] SAFEARRAY (variant) *varP) ;

    // Other module definition statements.
};
```

## <a name="see-also"></a><span data-ttu-id="bc2e0-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc2e0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc2e0-126">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="bc2e0-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="bc2e0-127">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="bc2e0-127">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="bc2e0-128">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="bc2e0-128">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 