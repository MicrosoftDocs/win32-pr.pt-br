---
title: atributo DllName (Str)
description: O atributo \ DllName \ define o nome da DLL que contém os pontos de entrada para um módulo.
ms.assetid: dbf062ce-9dcc-4cc6-b7cd-cdc5945e399b
keywords:
- o atributo DllName (Str) MIDL
topic_type:
- apiref
api_name:
- dllname(str)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 990d277db855c2988021d19a0a756c49454546f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007533"
---
# <a name="dllnamestr-attribute"></a><span data-ttu-id="44bea-104">atributo DllName (Str)</span><span class="sxs-lookup"><span data-stu-id="44bea-104">dllname(str) attribute</span></span>

<span data-ttu-id="44bea-105">O atributo **\[ DllName \]** define o nome da dll que contém os pontos de entrada para um módulo.</span><span class="sxs-lookup"><span data-stu-id="44bea-105">The **\[dllname\]** attribute defines the name of the DLL that contains the entry points for a module.</span></span>

``` syntax
[
    uuid(uuid-number), 
    dllname("filename")
    [, optional-attribute-list]
]
module modulename
{
    elementlist
};
```

## <a name="parameters"></a><span data-ttu-id="44bea-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44bea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44bea-107">*UUID-número*</span><span class="sxs-lookup"><span data-stu-id="44bea-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="44bea-108">Especifica um número de identificação universalmente exclusivo para o [**módulo**](module.md).</span><span class="sxs-lookup"><span data-stu-id="44bea-108">Specifies a universally unique identification number for the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="44bea-109">*nome do arquivo*</span><span class="sxs-lookup"><span data-stu-id="44bea-109">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="44bea-110">Especifica uma cadeia de caracteres terminada em nulo que contém o caminho completo para o arquivo dll.</span><span class="sxs-lookup"><span data-stu-id="44bea-110">Specifies a NULL-terminated string which contains the full path to the Dll file.</span></span>

</dd> <dt>

<span data-ttu-id="44bea-111">*lista de atributos opcionais*</span><span class="sxs-lookup"><span data-stu-id="44bea-111">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="44bea-112">Especifica uma lista de zero ou mais atributos de interface MIDL.</span><span class="sxs-lookup"><span data-stu-id="44bea-112">Specifies a list of zero or more MIDL interface attributes.</span></span>

</dd> <dt>

<span data-ttu-id="44bea-113">*ModuleName*</span><span class="sxs-lookup"><span data-stu-id="44bea-113">*modulename*</span></span> 
</dt> <dd>

<span data-ttu-id="44bea-114">Especifica o nome que outros componentes de software podem usar para se referir ao módulo.</span><span class="sxs-lookup"><span data-stu-id="44bea-114">Specifies the name which other software components can use to refer to the module.</span></span>

</dd> <dt>

<span data-ttu-id="44bea-115">*elementolist*</span><span class="sxs-lookup"><span data-stu-id="44bea-115">*elementlist*</span></span> 
</dt> <dd>

<span data-ttu-id="44bea-116">Especifica uma ou mais instruções de definição de elemento de módulo.</span><span class="sxs-lookup"><span data-stu-id="44bea-116">Specifies one or more module element definition statements.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44bea-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="44bea-117">Remarks</span></span>

<span data-ttu-id="44bea-118">O atributo **\[ DllName \]** é necessário em um módulo.</span><span class="sxs-lookup"><span data-stu-id="44bea-118">The **\[dllname\]** attribute is required on a module.</span></span>

## <a name="examples"></a><span data-ttu-id="44bea-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="44bea-119">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("A meaningful comment"),   
    dllname("HANDY.DLL")
] 
module HandyStuff
{
    /* Module content definitions */
};
```

## <a name="see-also"></a><span data-ttu-id="44bea-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="44bea-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44bea-121">**modulo**</span><span class="sxs-lookup"><span data-stu-id="44bea-121">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="44bea-122">**inicial**</span><span class="sxs-lookup"><span data-stu-id="44bea-122">**entry**</span></span>](entry.md)
</dt> <dt>

[<span data-ttu-id="44bea-123">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="44bea-123">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="44bea-124">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="44bea-124">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="44bea-125">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="44bea-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 