---
title: Importando arquivos e bibliotecas de tipos
description: As palavras-chave MIDL incluem, Import e importlib permitem que você reutilize o código referenciando arquivos de cabeçalho, IDL e linguagem de definição de objeto (ODL) existentes e bibliotecas de tipos compiladas.
ms.assetid: b4571c1d-4bd7-4ab1-9ef6-14356a6c4bb4
keywords:
- Linguagem IDL da Microsoft MIDL, tarefas, Importando arquivos e bibliotecas de tipos
- importando MIDL
- bibliotecas de tipos MIDL, importando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84b740f29726c1ce4d401fc69b2ea07e811eac0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104298447"
---
# <a name="importing-files-and-type-libraries"></a><span data-ttu-id="10df2-106">Importando arquivos e bibliotecas de tipos</span><span class="sxs-lookup"><span data-stu-id="10df2-106">Importing Files and Type Libraries</span></span>

<span data-ttu-id="10df2-107">As palavras-chave MIDL [**incluem**](include.md), [**Import**](import.md)e [**importlib**](importlib.md) permitem que você reutilize o código referenciando arquivos de cabeçalho, IDL e linguagem de definição de objeto (ODL) existentes e bibliotecas de tipos compiladas.</span><span class="sxs-lookup"><span data-stu-id="10df2-107">The MIDL keywords [**include**](include.md), [**import**](import.md), and [**importlib**](importlib.md) let you reuse code by referencing existing header, IDL, and object definition language (ODL) files, and compiled type libraries.</span></span>

<span data-ttu-id="10df2-108">A diretiva ACF [**include**](include.md) permite que você especifique em um arquivo ACF um ou mais arquivos de cabeçalho de linguagem C a serem incluídos no código stub gerado por MIDL.</span><span class="sxs-lookup"><span data-stu-id="10df2-108">The ACF [**include**](include.md) directive lets you specify in an ACF file one or more C-language header files to be included in the MIDL-generated stub code.</span></span> <span data-ttu-id="10df2-109">O arquivo gerado terá uma linha com uma diretiva **\# include** C-pré-processador com o arquivo de cabeçalho indicado.</span><span class="sxs-lookup"><span data-stu-id="10df2-109">The generated file will have a line with a **\#include** C-preprocessor directive with the indicated header file.</span></span> <span data-ttu-id="10df2-110">Use essa diretiva **include** para trazer arquivos de cabeçalho específicos para um determinado ambiente operacional e que não contêm informações necessárias para a interface entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="10df2-110">Use this **include** directive to bring in header files that are specific to a particular operating environment and that do not contain information necessary for the interface between client and server.</span></span> <span data-ttu-id="10df2-111">Não use **include** para arquivos de cabeçalho que contenham tipos de dados que você deseja disponibilizar para o arquivo IDL; em vez disso, use a diretiva de [**importação**](import.md) .</span><span class="sxs-lookup"><span data-stu-id="10df2-111">Do not use **include** for header files containing data types that you want available to the IDL file; instead, use the [**import**](import.md) directive.</span></span>

## <a name="example-1"></a><span data-ttu-id="10df2-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="10df2-112">Example 1</span></span>

``` syntax
[
  auto_handle
] 
interface X86PC
{ 
  include "gendefs.h", "protos.h", "myfile.h"; 
  //interface typdefs and function declarations here
}
```

<span data-ttu-id="10df2-113">A diretiva de [**importação**](import.md) de IDL é o método padrão para trazer definições de tipo e de interface de outros arquivos IDL (ou ODL) e arquivos de cabeçalho em seu arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="10df2-113">The IDL [**import**](import.md) directive is the standard method for bringing type and interface definitions from other IDL (or ODL) files and header files into your IDL file.</span></span> <span data-ttu-id="10df2-114">Todas as instruções IDL no arquivo importado, como TYPEDEFs, declarações [**const**](const.md) e definições de interface, ficam disponíveis para o arquivo IDL de importação.</span><span class="sxs-lookup"><span data-stu-id="10df2-114">All IDL statements in the imported file, such as typedefs, [**const**](const.md) declarations, and interface definitions become available to the importing IDL file.</span></span>

<span data-ttu-id="10df2-115">Assim como a diretiva de pré-processador de linguagem C **\# , a diretiva de** [**importação**](import.md) informa o compilador para incluir tipos de dados que foram definidos nos arquivos IDL importados.</span><span class="sxs-lookup"><span data-stu-id="10df2-115">Like the C-language preprocessor directive **\#include**, the [**import**](import.md) directive tells the compiler to include data types that were defined in the imported IDL files.</span></span> <span data-ttu-id="10df2-116">Ao contrário da diretiva **\# include** , a diretiva de **importação** ignora os protótipos de procedimento, pois nenhum stub é gerado para qualquer coisa no arquivo importado.</span><span class="sxs-lookup"><span data-stu-id="10df2-116">Unlike the **\#include** directive, the **import** directive ignores procedure prototypes, since no stubs are generated for anything in the imported file.</span></span> <span data-ttu-id="10df2-117">Como o pré-processador é invocado separadamente para o arquivo importado, as diretivas de pré-processador (como \* \*) não são transportadas para o arquivo IDL de importação.</span><span class="sxs-lookup"><span data-stu-id="10df2-117">Because the preprocessor is invoked separately for the imported file, preprocessor directives (such as \*\*) do not carry over to the importing IDL file.</span></span>

<span data-ttu-id="10df2-118">Para obter informações adicionais sobre como usar a [**importação**](import.md) para incluir arquivos de cabeçalho do sistema em um arquivo IDL, consulte [Importando arquivos de cabeçalho do sistema](importing-system-header-files.md).</span><span class="sxs-lookup"><span data-stu-id="10df2-118">For additional information on using [**import**](import.md) to include system header files in an IDL file, see [Importing System Header Files](importing-system-header-files.md).</span></span>

## <a name="example-2"></a><span data-ttu-id="10df2-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="10df2-119">Example 2</span></span>

``` syntax
[
  uuid(. . .), object
] 
interface IKnown : IUnknown
{
  import "base.idl", "unknwn.idl", "helper.idl";
  //remainder of interface definition
}
```

<span data-ttu-id="10df2-120">A diretiva ODL [**importlib**](importlib.md) permite que você referencie uma biblioteca de tipos compilada em seu arquivo IDL ou ODL.</span><span class="sxs-lookup"><span data-stu-id="10df2-120">The ODL [**importlib**](importlib.md) directive lets you reference a compiled type library in your IDL or ODL file.</span></span> <span data-ttu-id="10df2-121">A diretiva **importlib** deve estar dentro de uma instrução de [**biblioteca**](library.md) e deve preceder outras descrições de tipo na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="10df2-121">The **importlib** directive must be inside a [**library**](library.md) statement, and must precede other type descriptions in the library.</span></span> <span data-ttu-id="10df2-122">A biblioteca importada, bem como a biblioteca gerada, deve estar disponível para o aplicativo em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="10df2-122">The imported library, as well as the generated library, must be available to the application at runtime.</span></span>

## <a name="example-3"></a><span data-ttu-id="10df2-123">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="10df2-123">Example 3</span></span>

``` syntax
library NewBrowser
{
  importlib("stdole32.tlb");
  importlib("legacy.tlb");
  //remainder of library definition
};
```

<span data-ttu-id="10df2-124">Você também pode usar a diretiva C-pré-processador **\# include** para incluir cabeçalhos e outros arquivos em seu arquivo IDL ou ODL.</span><span class="sxs-lookup"><span data-stu-id="10df2-124">You can also use the C-preprocessor **\#include** directive to include headers and other files in your IDL or ODL file.</span></span> <span data-ttu-id="10df2-125">No entanto, lembre-se de que essa diretiva incluirá literalmente todo o conteúdo do arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="10df2-125">Be aware, however, that this directive will literally include the entire contents of the specified file.</span></span> <span data-ttu-id="10df2-126">Se um arquivo de cabeçalho contiver protótipos que você não precisa ou deseja nos arquivos stub gerados por MIDL, ou se ele contiver definições de tipo não-Remotable, você deverá usar a diretiva de [**importação**](import.md) MIDL em vez da diretiva **\# include** .</span><span class="sxs-lookup"><span data-stu-id="10df2-126">If a header file contains prototypes that you do not need or want in the MIDL-generated stub files, or if it contains nonremotable type definitions, you should use the MIDL [**import**](import.md) directive instead of the **\#include** directive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10df2-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="10df2-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10df2-128">**importe**</span><span class="sxs-lookup"><span data-stu-id="10df2-128">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="10df2-129">**importlib**</span><span class="sxs-lookup"><span data-stu-id="10df2-129">**importlib**</span></span>](importlib.md)
</dt> <dt>

[<span data-ttu-id="10df2-130">**incluir**</span><span class="sxs-lookup"><span data-stu-id="10df2-130">**include**</span></span>](include.md)
</dt> <dt>

[<span data-ttu-id="10df2-131">Importar arquivos de cabeçalho do sistema</span><span class="sxs-lookup"><span data-stu-id="10df2-131">Importing System Header Files</span></span>](importing-system-header-files.md)
</dt> </dl>

 

 




