---
title: atributo helpstringdll
description: O atributo \ helpstringdll \ define o nome da DLL a ser usada para executar uma pesquisa de cadeia de caracteres de documento.
ms.assetid: 1b9b962c-c355-4428-b5ea-dc7fd48b50a9
keywords:
- helpstringdll do atributo MIDL
topic_type:
- apiref
api_name:
- helpstringdll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dace4fb9ddc3908ce637cd2d8521a1ab4671d620
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917203"
---
# <a name="helpstringdll-attribute"></a><span data-ttu-id="8db84-104">atributo helpstringdll</span><span class="sxs-lookup"><span data-stu-id="8db84-104">helpstringdll attribute</span></span>

<span data-ttu-id="8db84-105">O atributo **\[ helpstringdll \]** define o nome da dll a ser usada para executar uma pesquisa de cadeia de caracteres de documento.</span><span class="sxs-lookup"><span data-stu-id="8db84-105">The **\[helpstringdll\]** attribute sets the name of the DLL to use to perform a document string lookup.</span></span>

``` syntax
[
    helpstringdll(help-text-string)
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
};
```

## <a name="parameters"></a><span data-ttu-id="8db84-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8db84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8db84-107">*ajuda-texto-cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="8db84-107">*help-text-string*</span></span> 
</dt> <dd>

<span data-ttu-id="8db84-108">Uma cadeia de caracteres terminada em zero especificando o nome de arquivo totalmente qualificado de uma DLL.</span><span class="sxs-lookup"><span data-stu-id="8db84-108">A zero-terminated string of characters specifying the fully qualified file name of a DLL.</span></span>

</dd> <dt>

<span data-ttu-id="8db84-109">*lista de atributos opcionais*</span><span class="sxs-lookup"><span data-stu-id="8db84-109">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="8db84-110">Outros atributos que se aplicam à instrução da biblioteca como um todo.</span><span class="sxs-lookup"><span data-stu-id="8db84-110">Other attributes that apply to the library statement as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="8db84-111">*nome da biblioteca*</span><span class="sxs-lookup"><span data-stu-id="8db84-111">*library-name*</span></span> 
</dt> <dd>

<span data-ttu-id="8db84-112">O identificador que os componentes de software usarão para denotar essa [**biblioteca**](library.md).</span><span class="sxs-lookup"><span data-stu-id="8db84-112">The identifier that software components will use to denote this [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="8db84-113">*bibliotecas-definição-instruções*</span><span class="sxs-lookup"><span data-stu-id="8db84-113">*library-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="8db84-114">Uma ou mais instruções MIDL que definem a interface da [**biblioteca**](library.md).</span><span class="sxs-lookup"><span data-stu-id="8db84-114">One or more MIDL statement which define the interface of the [**library**](library.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8db84-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8db84-115">Remarks</span></span>

<span data-ttu-id="8db84-116">Use o atributo **\[ helpstringdll \]** em uma instrução de biblioteca para especificar, como uma cadeia de caracteres, o nome de arquivo totalmente qualificado de uma biblioteca de vínculo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="8db84-116">Use the **\[helpstringdll\]** attribute on a library statement to specify, as a character string, the fully qualified file name of a dynamic link library.</span></span> <span data-ttu-id="8db84-117">Isso permite que um usuário exiba uma descrição da DLL com o Visualizador de objetos.</span><span class="sxs-lookup"><span data-stu-id="8db84-117">This allows a user to view a description of the DLL with the object viewer.</span></span>

<span data-ttu-id="8db84-118">Use as funções **GetDocumentation2** nas interfaces **ITypeLib2** e **ITypeInfo2** para recuperar a cadeia de caracteres de ajuda.</span><span class="sxs-lookup"><span data-stu-id="8db84-118">Use the **GetDocumentation2** functions in the **ITypeLib2** and **ITypeInfo2** interfaces to retrieve the help string.</span></span>

## <a name="see-also"></a><span data-ttu-id="8db84-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="8db84-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8db84-120">**biblioteca**</span><span class="sxs-lookup"><span data-stu-id="8db84-120">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="8db84-121">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="8db84-121">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="8db84-122">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="8db84-122">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="8db84-123">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="8db84-123">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 