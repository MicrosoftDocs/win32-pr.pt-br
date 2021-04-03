---
title: atributo helpfile
description: O atributo \ HelpFile \ define o nome do arquivo de ajuda para uma biblioteca de tipos. Todos os tipos em uma biblioteca compartilham o mesmo arquivo de ajuda.
ms.assetid: caa248b1-a1a7-4c36-886a-079a66a01907
keywords:
- MIDL do atributo HelpFile
topic_type:
- apiref
api_name:
- helpfile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0b4283b0285631a710af774d364a01b82c9d44b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640565"
---
# <a name="helpfile-attribute"></a><span data-ttu-id="680fb-105">atributo helpfile</span><span class="sxs-lookup"><span data-stu-id="680fb-105">helpfile attribute</span></span>

<span data-ttu-id="680fb-106">O atributo **\[ HelpFile \]** define o nome do arquivo de ajuda para uma biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="680fb-106">The **\[helpfile\]** attribute sets the name of the Help file for a type library.</span></span> <span data-ttu-id="680fb-107">Todos os tipos em uma biblioteca compartilham o mesmo arquivo de ajuda.</span><span class="sxs-lookup"><span data-stu-id="680fb-107">All types in a library share the same Help file.</span></span>

``` syntax
[
    uuid(uuid-number), 
    helpfile("filename") 
    [, optional-attribute-list]
] 
library 
{
    library statements
};
```

## <a name="parameters"></a><span data-ttu-id="680fb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="680fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="680fb-109">*UUID-número*</span><span class="sxs-lookup"><span data-stu-id="680fb-109">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="680fb-110">Especifica um número de identificação universalmente exclusivo para a [**biblioteca**](library.md).</span><span class="sxs-lookup"><span data-stu-id="680fb-110">Specifies a universally unique identification number for the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="680fb-111">*nome do arquivo*</span><span class="sxs-lookup"><span data-stu-id="680fb-111">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="680fb-112">Especifica o nome do arquivo que contém o texto de ajuda.</span><span class="sxs-lookup"><span data-stu-id="680fb-112">Specifies the name of the file containing the help text.</span></span>

</dd> <dt>

<span data-ttu-id="680fb-113">*lista de atributos opcionais*</span><span class="sxs-lookup"><span data-stu-id="680fb-113">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="680fb-114">Especifica zero ou mais atributos que o compilador MIDL aplicará à [**biblioteca**](library.md).</span><span class="sxs-lookup"><span data-stu-id="680fb-114">Specifies zero or more attributes that the MIDL compiler will apply to the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="680fb-115">*instruções de biblioteca*</span><span class="sxs-lookup"><span data-stu-id="680fb-115">*library statements*</span></span> 
</dt> <dd>

<span data-ttu-id="680fb-116">Especifica uma ou mais instruções MIDL que definem a interface da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="680fb-116">Specifies one or more MIDL statements that define the library interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="680fb-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="680fb-117">Remarks</span></span>

<span data-ttu-id="680fb-118">Use as funções **GetDocumentation** nas interfaces **ITypeLib** e **ITypeInfo** para recuperar o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="680fb-118">Use the **GetDocumentation** functions in the **ITypeLib** and **ITypeInfo** interfaces to retrieve the file name.</span></span>

## <a name="examples"></a><span data-ttu-id="680fb-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="680fb-119">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpfile("filename.hlp"),
    lcid(0x0409), 
    version(2.0)
]
library Hello
{
    /* Library definition statements here. */
};
```

## <a name="see-also"></a><span data-ttu-id="680fb-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="680fb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="680fb-121">**biblioteca**</span><span class="sxs-lookup"><span data-stu-id="680fb-121">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="680fb-122">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="680fb-122">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="680fb-123">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="680fb-123">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="680fb-124">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="680fb-124">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 