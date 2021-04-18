---
description: Coloca uma instrução de inclusão C ou IDL no código gerado.
ms.assetid: 7a7ffd54-09e9-412d-a637-5dc27597b46e
title: elemento literalInclude
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2701b2b21d14b629d5d9b61dcbc73e11371f54e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772975"
---
# <a name="literalinclude-element"></a><span data-ttu-id="b6aed-103">elemento literalInclude</span><span class="sxs-lookup"><span data-stu-id="b6aed-103">literalInclude element</span></span>

<span data-ttu-id="b6aed-104">Coloca uma instrução de inclusão C ou IDL no código gerado.</span><span class="sxs-lookup"><span data-stu-id="b6aed-104">Places a C or IDL include statement in the generated code.</span></span>

## <a name="usage"></a><span data-ttu-id="b6aed-105">Uso</span><span class="sxs-lookup"><span data-stu-id="b6aed-105">Usage</span></span>

``` syntax
<literalInclude
  Language = "language string"
  Local = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="b6aed-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="b6aed-106">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b6aed-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="b6aed-107">Attribute</span></span></th>
<th><span data-ttu-id="b6aed-108">Type</span><span class="sxs-lookup"><span data-stu-id="b6aed-108">Type</span></span></th>
<th><span data-ttu-id="b6aed-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b6aed-109">Required</span></span></th>
<th><span data-ttu-id="b6aed-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6aed-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b6aed-111"><strong>Idioma</strong></span><span class="sxs-lookup"><span data-stu-id="b6aed-111"><strong>Language</strong></span></span><br/></td>
<td><span data-ttu-id="b6aed-112">Cadeia de caracteres de idioma</span><span class="sxs-lookup"><span data-stu-id="b6aed-112">language string</span></span><br/></td>
<td><span data-ttu-id="b6aed-113">No</span><span class="sxs-lookup"><span data-stu-id="b6aed-113">No</span></span><br/></td>
<td><span data-ttu-id="b6aed-114">O tipo de arquivo de cabeçalho a ser incluído.</span><span class="sxs-lookup"><span data-stu-id="b6aed-114">The type of header file to be included.</span></span> <br/> <br/><span data-ttu-id="b6aed-115">
<dt><strong>&</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b6aed-115">
<dt><strong>C</strong></dt> </span></span><dd> <span data-ttu-id="b6aed-116">Incluir um arquivo de cabeçalho C.</span><span class="sxs-lookup"><span data-stu-id="b6aed-116">Include a C header file.</span></span><br/> </dd> <span data-ttu-id="b6aed-117"><dt><strong>INSERI</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b6aed-117"><dt><strong>IDL</strong></dt> </span></span><dd> <span data-ttu-id="b6aed-118">Incluir um arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="b6aed-118">Include an IDL file.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6aed-119"><strong>Local</strong></span><span class="sxs-lookup"><span data-stu-id="b6aed-119"><strong>Local</strong></span></span><br/></td>
<td><span data-ttu-id="b6aed-120">Boolean</span><span class="sxs-lookup"><span data-stu-id="b6aed-120">Boolean</span></span><br/></td>
<td><span data-ttu-id="b6aed-121">No</span><span class="sxs-lookup"><span data-stu-id="b6aed-121">No</span></span><br/></td>
<td><span data-ttu-id="b6aed-122">Esse atributo só é usado quando o <strong>idioma</strong> é definido como &quot; C &quot; .</span><span class="sxs-lookup"><span data-stu-id="b6aed-122">This attribute is only used when <strong>Language</strong> is set to &quot;C&quot;.</span></span><br/> <br/><span data-ttu-id="b6aed-123">
<dt><strong>True</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b6aed-123">
<dt><strong>True</strong></dt> </span></span><dd> <span data-ttu-id="b6aed-124">Pesquisa o diretório atual para o cabeçalho nomeado antes de Pesquisar os diretórios do sistema.</span><span class="sxs-lookup"><span data-stu-id="b6aed-124">Searches the current directory for the named header before searching the system directories.</span></span><br/> </dd> <span data-ttu-id="b6aed-125"><dt><strong>For</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b6aed-125"><dt><strong>False</strong></dt> </span></span><dd> <span data-ttu-id="b6aed-126">Pesquise somente os diretórios do sistema para o cabeçalho nomeado.</span><span class="sxs-lookup"><span data-stu-id="b6aed-126">Only search system directories for the named header.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="b6aed-127">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="b6aed-127">Child elements</span></span>

<span data-ttu-id="b6aed-128">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="b6aed-128">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="b6aed-129">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="b6aed-129">Parent elements</span></span>



| <span data-ttu-id="b6aed-130">Elemento</span><span class="sxs-lookup"><span data-stu-id="b6aed-130">Element</span></span>                         | <span data-ttu-id="b6aed-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6aed-131">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="b6aed-132">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="b6aed-132">**file**</span></span>](file.md)<br/> | <span data-ttu-id="b6aed-133">Gera um arquivo do gerador de código.</span><span class="sxs-lookup"><span data-stu-id="b6aed-133">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="b6aed-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6aed-134">Remarks</span></span>

<span data-ttu-id="b6aed-135">Os exemplos a seguir mostram o código gerado de diferentes elementos **literalInclude** .</span><span class="sxs-lookup"><span data-stu-id="b6aed-135">The following examples show the code generated from different **literalInclude** elements.</span></span>

### <a name="example-1---generating-a-c-include-statement"></a><span data-ttu-id="b6aed-136">Exemplo 1-gerando uma instrução C include</span><span class="sxs-lookup"><span data-stu-id="b6aed-136">Example 1 - Generating a C include statement</span></span>

<span data-ttu-id="b6aed-137">XML de entrada:</span><span class="sxs-lookup"><span data-stu-id="b6aed-137">Input XML:</span></span>

``` syntax
<literalInclude Language="C" Local="False">wsdapi.h</literalInclude>
```

<span data-ttu-id="b6aed-138">Código de saída:</span><span class="sxs-lookup"><span data-stu-id="b6aed-138">Output code:</span></span>

``` syntax
#include <wsdapi.h>
```

### <a name="example-2---generating-a-c-include-statement"></a><span data-ttu-id="b6aed-139">Exemplo 2-gerando uma instrução C include</span><span class="sxs-lookup"><span data-stu-id="b6aed-139">Example 2 - Generating a C include statement</span></span>

<span data-ttu-id="b6aed-140">XML de entrada:</span><span class="sxs-lookup"><span data-stu-id="b6aed-140">Input XML:</span></span>

``` syntax
<literalInclude Language="C" Local="True">wsdapi.h</literalInclude>
```

<span data-ttu-id="b6aed-141">Código de saída:</span><span class="sxs-lookup"><span data-stu-id="b6aed-141">Output code:</span></span>

``` syntax
#include "wsdapi.h"
```

### <a name="example-3---generating-an-idl-import-statement"></a><span data-ttu-id="b6aed-142">Exemplo 3-gerando uma instrução de importação de IDL</span><span class="sxs-lookup"><span data-stu-id="b6aed-142">Example 3 - Generating an IDL import statement</span></span>

<span data-ttu-id="b6aed-143">XML de entrada:</span><span class="sxs-lookup"><span data-stu-id="b6aed-143">Input XML:</span></span>

``` syntax
<literalInclude Language="IDL">wsdclient.idl</literalInclude>
```

<span data-ttu-id="b6aed-144">Código de saída:</span><span class="sxs-lookup"><span data-stu-id="b6aed-144">Output code:</span></span>

``` syntax
import wsdclient.idl;
```

## <a name="element-information"></a><span data-ttu-id="b6aed-145">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="b6aed-145">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="b6aed-146">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6aed-146">Minimum supported system</span></span><br/> | <span data-ttu-id="b6aed-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6aed-147">Windows Vista</span></span> |
| <span data-ttu-id="b6aed-148">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="b6aed-148">Can be empty</span></span>                        | <span data-ttu-id="b6aed-149">Sim</span><span class="sxs-lookup"><span data-stu-id="b6aed-149">Yes</span></span>           |



 

 




