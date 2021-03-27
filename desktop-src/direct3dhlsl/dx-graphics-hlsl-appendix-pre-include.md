---
title: " Diretiva include"
description: Diretiva de pré-processador que insere o conteúdo do arquivo especificado no programa de origem no ponto em que a diretiva é exibida.
ms.assetid: 24796d89-5690-469b-950e-df56783aa05a
keywords:
- incluir diretiva HLSL
topic_type:
- apiref
api_name:
- include Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a844459234200ca99233eb3f64a2a1c30449cdcc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988672"
---
# <a name="include-directive"></a><span data-ttu-id="eda38-104">\#Diretiva include</span><span class="sxs-lookup"><span data-stu-id="eda38-104">\#include Directive</span></span>

<span data-ttu-id="eda38-105">Diretiva de pré-processador que insere o conteúdo do arquivo especificado no programa de origem no ponto em que a diretiva é exibida.</span><span class="sxs-lookup"><span data-stu-id="eda38-105">Preprocessor directive that inserts the contents of the specified file into the source program at the point where the directive appears.</span></span>


| <span data-ttu-id="eda38-106">\#incluir "*filename*"</span><span class="sxs-lookup"><span data-stu-id="eda38-106">\#include "*filename*"</span></span>       |
|------------------------------|
| <span data-ttu-id="eda38-107">\#incluir *nome de arquivo* <></span><span class="sxs-lookup"><span data-stu-id="eda38-107">\#include <*filename*></span></span> |

## <a name="parameters"></a><span data-ttu-id="eda38-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eda38-108">Parameters</span></span>

| <span data-ttu-id="eda38-109">Item</span><span class="sxs-lookup"><span data-stu-id="eda38-109">Item</span></span> | <span data-ttu-id="eda38-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="eda38-110">Description</span></span> |
|------|-------------|
| <span data-ttu-id="eda38-111">*filename*</span><span class="sxs-lookup"><span data-stu-id="eda38-111">*filename*</span></span> | <span data-ttu-id="eda38-112">Nome do arquivo a ser incluído, opcionalmente precedido por uma especificação de diretório.</span><span class="sxs-lookup"><span data-stu-id="eda38-112">Filename of the file to include, optionally preceded by a directory specification.</span></span> <span data-ttu-id="eda38-113">O filename deve especificar um arquivo existente.</span><span class="sxs-lookup"><span data-stu-id="eda38-113">The filename must specify an existing file.</span></span> |

## <a name="remarks"></a><span data-ttu-id="eda38-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="eda38-114">Remarks</span></span>

<span data-ttu-id="eda38-115">A \# diretiva include causa a substituição da diretiva pelo conteúdo inteiro do arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="eda38-115">The \#include directive causes replacement of the directive by the entire contents of the specified file.</span></span> <span data-ttu-id="eda38-116">O pré-processador para de Pesquisar assim que encontrar um arquivo com o nome especificado; Se você especificar uma especificação de caminho completa e não ambígua para o arquivo, o pré-processador pesquisará apenas o caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="eda38-116">The preprocessor stops searching as soon as it finds a file with the specified name; if you specify a complete, unambiguous path specification for the file, the preprocessor searches only the specified path.</span></span>

> [!NOTE]
> <span data-ttu-id="eda38-117">A [ferramenta de compilador de efeito](/windows/desktop/direct3dtools/fxc) tem um manipulador de inclusão interno usando a opção/i.</span><span class="sxs-lookup"><span data-stu-id="eda38-117">The [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) has a built-in include handler using the /I switch.</span></span> <span data-ttu-id="eda38-118">No entanto, ao executar o compilador da API, você pode fornecer um manipulador de inclusão personalizado implementando a interface ID3DXInclude.</span><span class="sxs-lookup"><span data-stu-id="eda38-118">However, when executing the compiler from the API, you can provide a customized include handler by implementing the ID3DXInclude interface.</span></span>

<span data-ttu-id="eda38-119">A diferença entre as duas formas de sintaxe é a ordem na qual o pré-processador procura por arquivos de cabeçalho quando o caminho é especificado incompletamente, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="eda38-119">The difference between the two syntax forms is the order in which the preprocessor searches for header files when the path is incompletely specified, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eda38-120">Formato de sintaxe</span><span class="sxs-lookup"><span data-stu-id="eda38-120">Syntax form</span></span></th>
<th><span data-ttu-id="eda38-121">Padrão de pesquisa de pré-processador</span><span class="sxs-lookup"><span data-stu-id="eda38-121">Preprocessor search pattern</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eda38-122">#incluir <b>&quot;</b> <em>nome de arquivo</em><b>&quot;</b></span><span class="sxs-lookup"><span data-stu-id="eda38-122">#include <b>&quot;</b><em>filename</em><b>&quot;</b></span></span></td>
<td><span data-ttu-id="eda38-123">Procura o arquivo de inclusão:</span><span class="sxs-lookup"><span data-stu-id="eda38-123">Searches for the include file:</span></span>
<ol>
<li><span data-ttu-id="eda38-124">no mesmo diretório que o arquivo que contém a diretiva #include.</span><span class="sxs-lookup"><span data-stu-id="eda38-124">in the same directory as the file that contains the #include directive.</span></span></li>
<li><span data-ttu-id="eda38-125">nos diretórios de todos os arquivos que contêm uma diretiva #include para o arquivo que contém a diretiva #include.</span><span class="sxs-lookup"><span data-stu-id="eda38-125">in the directories of any files that contain a #include directive for the file that contains the #include directive.</span></span></li>
<li><span data-ttu-id="eda38-126">em caminhos especificados pela opção de compilador/I, na ordem em que são listados.</span><span class="sxs-lookup"><span data-stu-id="eda38-126">in paths specified by the /I compiler option, in the order in which they are listed.</span></span></li>
<li><p><span data-ttu-id="eda38-127">em caminhos especificados pela variável de ambiente INCLUDE, na ordem em que eles são listados.</span><span class="sxs-lookup"><span data-stu-id="eda38-127">in paths specified by the INCLUDE environment variable, in the order in which they are listed.</span></span></p>
<blockquote>
[!NOTE]<br />
<span data-ttu-id="eda38-128">A variável de ambiente INCLUDE é ignorada em um ambiente de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="eda38-128">The INCLUDE environment variable is ignored in an development environment.</span></span> <span data-ttu-id="eda38-129">Consulte a documentação do ambiente de desenvolvimento para obter informações sobre como definir os caminhos de inclusão para o seu projeto.</span><span class="sxs-lookup"><span data-stu-id="eda38-129">Refer to your development environment's documentation for information about how to set the include paths for your project.</span></span>
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eda38-130">#incluir <b><</b> <em>nome de arquivo</em><b>></b></span><span class="sxs-lookup"><span data-stu-id="eda38-130">#include <b><</b><em>filename</em><b>></b></span></span></td>
<td><span data-ttu-id="eda38-131">Procura o arquivo de inclusão:</span><span class="sxs-lookup"><span data-stu-id="eda38-131">Searches for the include file:</span></span>
<ol>
<li><span data-ttu-id="eda38-132">em caminhos especificados pela opção de compilador/I, na ordem em que são listados.</span><span class="sxs-lookup"><span data-stu-id="eda38-132">in paths specified by the /I compiler option, in the order in which they are listed.</span></span></li>
<li><p><span data-ttu-id="eda38-133">em caminhos especificados pela variável de ambiente INCLUDE, na ordem em que eles são listados.</span><span class="sxs-lookup"><span data-stu-id="eda38-133">in paths specified by the INCLUDE environment variable, in the order in which they are listed.</span></span></p>
<blockquote>
[!NOTE]<br />
<span data-ttu-id="eda38-134">A variável de ambiente INCLUDE é ignorada em um ambiente de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="eda38-134">The INCLUDE environment variable is ignored in an development environment.</span></span> <span data-ttu-id="eda38-135">Consulte a documentação do ambiente de desenvolvimento para obter informações sobre como definir os caminhos de inclusão para o seu projeto.</span><span class="sxs-lookup"><span data-stu-id="eda38-135">Refer to your development environment's documentation for information about how to set the include paths for your project.</span></span>
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="examples"></a><span data-ttu-id="eda38-136">Exemplos</span><span class="sxs-lookup"><span data-stu-id="eda38-136">Examples</span></span>

<span data-ttu-id="eda38-137">O exemplo a seguir faz com que o pré-processador substitua a \# diretiva include pelo conteúdo de stdio. h.</span><span class="sxs-lookup"><span data-stu-id="eda38-137">The following example causes the preprocessor to replace the \#include directive with the contents of stdio.h.</span></span> <span data-ttu-id="eda38-138">Como o exemplo usa o formato de colchete angular, o pré-processador pesquisará o arquivo somente nos diretórios listados pela opção de compilador/I e a variável de ambiente INCLUDE.</span><span class="sxs-lookup"><span data-stu-id="eda38-138">Because the example uses the angle bracket format, the preprocessor will search for the file only in the directories listed by the /I compiler option and the INCLUDE environment variable.</span></span>

```cpp
#include <stdio.h>
```

## <a name="see-also"></a><span data-ttu-id="eda38-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="eda38-139">See also</span></span>

- [<span data-ttu-id="eda38-140">Diretivas de pré-processador (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eda38-140">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)

- <span data-ttu-id="eda38-141">[Interface ID3D10Include](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eda38-141">[ID3D10Include Interface](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span></span>

- [<span data-ttu-id="eda38-142">Efeito-ferramenta do compilador</span><span class="sxs-lookup"><span data-stu-id="eda38-142">Effect-Compiler Tool</span></span>](/windows/desktop/direct3dtools/fxc)