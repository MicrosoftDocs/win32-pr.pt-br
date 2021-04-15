---
title: atributo importlib
description: A diretiva \ importlib \ torna os tipos que já foram compilados em outra biblioteca de tipos disponíveis para a biblioteca de tipos que está sendo criada.
ms.assetid: d5f15a77-c6b1-4918-be86-07d2995ca2d4
keywords:
- importlib do atributo MIDL
topic_type:
- apiref
api_name:
- importlib
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b9c233103330e9f8ae7318a613cbc5103315a74
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104453977"
---
# <a name="importlib-attribute"></a><span data-ttu-id="82f90-104">atributo importlib</span><span class="sxs-lookup"><span data-stu-id="82f90-104">importlib attribute</span></span>

<span data-ttu-id="82f90-105">A diretiva **\[ importlib \]** torna os tipos que já foram compilados em outra biblioteca de tipos disponíveis para a biblioteca de tipos que está sendo criada.</span><span class="sxs-lookup"><span data-stu-id="82f90-105">The **\[importlib\]** directive makes types that have already been compiled into another type library available to the type library being created.</span></span>

``` syntax
[
    library-attributes
]
library (library-name)
{
    importlib(file-to-import); 
    ... 
}
```

## <a name="parameters"></a><span data-ttu-id="82f90-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82f90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82f90-107">*biblioteca-atributos*</span><span class="sxs-lookup"><span data-stu-id="82f90-107">*library-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="82f90-108">Zero ou mais atributos que serão aplicados à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="82f90-108">Zero or more attributes that will be applied to the library.</span></span>

</dd> <dt>

<span data-ttu-id="82f90-109">*nome da biblioteca*</span><span class="sxs-lookup"><span data-stu-id="82f90-109">*library-name*</span></span> 
</dt> <dd>

<span data-ttu-id="82f90-110">O identificador que os componentes de software usarão para denotar essa [**biblioteca**](library.md).</span><span class="sxs-lookup"><span data-stu-id="82f90-110">The identifier that software components will use to denote this [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="82f90-111">*arquivo a ser importado*</span><span class="sxs-lookup"><span data-stu-id="82f90-111">*file-to-import*</span></span> 
</dt> <dd>

<span data-ttu-id="82f90-112">O nome e o local do arquivo importado em tempo de compilação de MIDL.</span><span class="sxs-lookup"><span data-stu-id="82f90-112">The name and location of the imported file at MIDL compile-time.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82f90-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="82f90-113">Remarks</span></span>

<span data-ttu-id="82f90-114">Todas as diretivas **\[ importlib \]** devem preceder as outras descrições de tipo na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="82f90-114">All **\[importlib\]** directives must precede the other type descriptions in the library.</span></span> <span data-ttu-id="82f90-115">Observe que a biblioteca importada, bem como a biblioteca gerada, deve ser distribuída com o aplicativo para que esteja disponível em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="82f90-115">Note that the imported library, as well as the generated library, must be distributed with the application so that it is available at run time.</span></span>

<span data-ttu-id="82f90-116">Na maioria dos casos, você deve usar a diretiva de **\[** [**importação**](import.md) MIDL **\]** para fazer referência a definições de outro. Arquivo IDL em seu. Arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="82f90-116">In most cases you should use the MIDL **\[**[**import**](import.md)**\]** directive to reference definitions from another .IDL file in your .IDL file.</span></span> <span data-ttu-id="82f90-117">Esse método fornece a biblioteca de tipos com todas as informações do arquivo original, enquanto **\[ importlib \]** só traz o conteúdo da biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="82f90-117">This method provides your type library with all the information from the original file, whereas **\[importlib\]** only brings in the contents of the type library.</span></span>

> [!Note]  
> <span data-ttu-id="82f90-118">A diretiva **\[ importlib \]** torna qualquer tipo definido na biblioteca importada acessível de dentro da biblioteca que está sendo compilada.</span><span class="sxs-lookup"><span data-stu-id="82f90-118">The **\[importlib\]** directive makes any type defined in the imported library accessible from within the library being compiled.</span></span> <span data-ttu-id="82f90-119">Para evitar ambigüidade quando houver referências duplicadas, recomendamos qualificar cada referência desse tipo com o nome de biblioteca apropriado, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="82f90-119">To avoid ambiguity when there are duplicate references, we recommend that you qualify each such reference with the appropriate library name, as follows:</span></span>

 

``` syntax
library_name.type
```

<span data-ttu-id="82f90-120">Na ausência de tal qualificação, o MIDL resolve a ambiguidade de referência duplicada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="82f90-120">In the absence of such qualification, MIDL resolves duplicate reference ambiguity as follows:</span></span>

-   <span data-ttu-id="82f90-121">Em vigor com a versão 3,1, MIDL usa a primeira referência encontrada.</span><span class="sxs-lookup"><span data-stu-id="82f90-121">Effective with version 3.1, MIDL uses the first reference it finds.</span></span>
-   <span data-ttu-id="82f90-122">A versão 3,0 do MIDL, a primeira versão do MIDL que poderia gerar bibliotecas de tipos, usa a última referência encontrada.</span><span class="sxs-lookup"><span data-stu-id="82f90-122">Version 3.0 of MIDL, the first version of MIDL that could generate type libraries, uses the last reference it found.</span></span>

## <a name="examples"></a><span data-ttu-id="82f90-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="82f90-123">Examples</span></span>

``` syntax
library BrowseHelper 
{ 
    importlib("stdole32.tlb"); 
    importlib("mydisp.tlb"); 
    //Remainder of library definition 
};
```

## <a name="see-also"></a><span data-ttu-id="82f90-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="82f90-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82f90-125">**biblioteca**</span><span class="sxs-lookup"><span data-stu-id="82f90-125">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="82f90-126">**importe**</span><span class="sxs-lookup"><span data-stu-id="82f90-126">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="82f90-127">Importar arquivos de cabeçalho do sistema</span><span class="sxs-lookup"><span data-stu-id="82f90-127">Importing System Header Files</span></span>](importing-system-header-files.md)
</dt> <dt>

[<span data-ttu-id="82f90-128">Importando arquivos e bibliotecas de tipos</span><span class="sxs-lookup"><span data-stu-id="82f90-128">Importing Files and Type Libraries</span></span>](importing-files-and-type-libraries.md)
</dt> <dt>

[<span data-ttu-id="82f90-129">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="82f90-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="82f90-130">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="82f90-130">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="82f90-131">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="82f90-131">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 