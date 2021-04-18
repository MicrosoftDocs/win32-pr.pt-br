---
description: Cada efeito em conformidade com o DXSAS deve definir, no mínimo, um único parâmetro de efeito global com a semântica global.
ms.assetid: 2112db8d-6a11-451d-a9d2-ac1b3cb2da95
title: Parâmetro global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647ef789e37cd7c8d6cd2fe554f1f8becbfd5e92
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105786317"
---
# <a name="global-parameter"></a><span data-ttu-id="03107-103">Parâmetro global</span><span class="sxs-lookup"><span data-stu-id="03107-103">Global Parameter</span></span>

<span data-ttu-id="03107-104">Cada efeito em conformidade com o DXSAS deve definir, no mínimo, um único parâmetro de efeito global com a semântica global.</span><span class="sxs-lookup"><span data-stu-id="03107-104">Each DXSAS compliant effect must define, as a minimum, a single global effect parameter with the global semantic.</span></span> <span data-ttu-id="03107-105">O parâmetro global também pode usar uma ou mais anotações opcionais.</span><span class="sxs-lookup"><span data-stu-id="03107-105">The global parameter can also use one or more optional annotations.</span></span> <span data-ttu-id="03107-106">A sintaxe dela é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="03107-106">The syntax is as follows:</span></span>


```
int VariableName : SasGlobal
<
    SasVersion 
    [OptionalAnnotations]
>;
```



<span data-ttu-id="03107-107">onde:</span><span class="sxs-lookup"><span data-stu-id="03107-107">where:</span></span>

-   <span data-ttu-id="03107-108">VariableName é um nome de variável de cadeia de caracteres de texto ASCII especificado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="03107-108">VariableName is a user-specified, ASCII text string variable name.</span></span>
-   <span data-ttu-id="03107-109">SasGlobal é a palavra-chave semântica que identifica esse parâmetro como o parâmetro global DXSAS.</span><span class="sxs-lookup"><span data-stu-id="03107-109">SasGlobal is the semantic keyword that identifies this parameter as the global DXSAS parameter.</span></span>
-   <span data-ttu-id="03107-110">SasVersion é a única anotação necessária.</span><span class="sxs-lookup"><span data-stu-id="03107-110">SasVersion is the only required annotation.</span></span>
-   <span data-ttu-id="03107-111">OptionalAnnotations pode incluir o seguinte:</span><span class="sxs-lookup"><span data-stu-id="03107-111">OptionalAnnotations can include the following:</span></span>
    -   [<span data-ttu-id="03107-112">SasEffectAuthor</span><span class="sxs-lookup"><span data-stu-id="03107-112">SasEffectAuthor</span></span>](#saseffectauthor)
    -   [<span data-ttu-id="03107-113">SasEffectAuthoringSoftware</span><span class="sxs-lookup"><span data-stu-id="03107-113">SasEffectAuthoringSoftware</span></span>](#saseffectauthoringsoftware)
    -   [<span data-ttu-id="03107-114">SasEffectCategory</span><span class="sxs-lookup"><span data-stu-id="03107-114">SasEffectCategory</span></span>](#saseffectcategory)
    -   [<span data-ttu-id="03107-115">SasEffectCompany</span><span class="sxs-lookup"><span data-stu-id="03107-115">SasEffectCompany</span></span>](#saseffectcompany)
    -   [<span data-ttu-id="03107-116">SasEffectDescription</span><span class="sxs-lookup"><span data-stu-id="03107-116">SasEffectDescription</span></span>](#saseffectdescription)
    -   [<span data-ttu-id="03107-117">SasEffectHelp</span><span class="sxs-lookup"><span data-stu-id="03107-117">SasEffectHelp</span></span>](#saseffecthelp)
    -   [<span data-ttu-id="03107-118">SasEffectRevision</span><span class="sxs-lookup"><span data-stu-id="03107-118">SasEffectRevision</span></span>](#saseffectrevision)

## <a name="sasversion"></a><span data-ttu-id="03107-119">SasVersion</span><span class="sxs-lookup"><span data-stu-id="03107-119">SasVersion</span></span>

<span data-ttu-id="03107-120">A única anotação necessária é SasVersion.</span><span class="sxs-lookup"><span data-stu-id="03107-120">The only required annotation is SasVersion.</span></span> <span data-ttu-id="03107-121">Ela é declarada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="03107-121">It is declared like this:</span></span>


```
int3 SasVersion = { major, minor, revision };
```



<span data-ttu-id="03107-122">onde:</span><span class="sxs-lookup"><span data-stu-id="03107-122">where:</span></span>

-   <span data-ttu-id="03107-123">principal indica a versão principal do DXSAS.</span><span class="sxs-lookup"><span data-stu-id="03107-123">major indicates the DXSAS major release.</span></span> <span data-ttu-id="03107-124">As principais versões do DXSAS podem conter alterações de varredura no conjunto de semânticas e anotações definidas.</span><span class="sxs-lookup"><span data-stu-id="03107-124">Major releases of DXSAS can contain sweeping changes to the set of semantics and annotations defined.</span></span> <span data-ttu-id="03107-125">A semântica e as anotações podem ser adicionadas e removidas e, em geral, a compatibilidade com versões anteriores não é garantida.</span><span class="sxs-lookup"><span data-stu-id="03107-125">Semantics and annotations can be added and removed and, in general, backward compatibility with previous releases is not guaranteed.</span></span>
-   <span data-ttu-id="03107-126">Minor indica a versão secundária SAS.</span><span class="sxs-lookup"><span data-stu-id="03107-126">minor indicates the SAS minor release.</span></span> <span data-ttu-id="03107-127">As versões secundárias do DXSAS podem incluir a adição de novas semânticas ou anotações.</span><span class="sxs-lookup"><span data-stu-id="03107-127">Minor releases of DXSAS can include the addition of new semantics or annotations.</span></span> <span data-ttu-id="03107-128">Além disso, a semântica e as anotações podem ser marcadas como preteridas no padrão DXSAS.</span><span class="sxs-lookup"><span data-stu-id="03107-128">Additionally, semantics and annotations may be marked as deprecated in the DXSAS standard.</span></span> <span data-ttu-id="03107-129">A semântica preterida e as anotações ainda devem ser suportadas por aplicativos host, mas podem emitir um diagnóstico de aviso quando essa semântica ou anotação é usada.</span><span class="sxs-lookup"><span data-stu-id="03107-129">Deprecated semantics and annotations must still be supported by host applications but can emit a warning diagnostic when such a semantic or annotation is used.</span></span> <span data-ttu-id="03107-130">Versões secundárias são compatíveis com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="03107-130">Minor releases are backward compatible with previous releases.</span></span>
-   <span data-ttu-id="03107-131">revisão indica a revisão DXSAS.</span><span class="sxs-lookup"><span data-stu-id="03107-131">revision indicates the DXSAS revision.</span></span> <span data-ttu-id="03107-132">As revisões de DXSAS existem apenas como um meio de corrigir bugs, remover ambigüidade e refinar o padrão.</span><span class="sxs-lookup"><span data-stu-id="03107-132">Revisions of DXSAS exist only as a means to fix bugs, remove ambiguity, and refine the standard.</span></span> <span data-ttu-id="03107-133">As revisões para o padrão são compatíveis com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="03107-133">Revisions to the standard are backward compatible with previous releases.</span></span>

<span data-ttu-id="03107-134">A versão atual é a 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="03107-134">The current version is 1.0.0.</span></span> <span data-ttu-id="03107-135">Não há valor padrão para esta anotação.</span><span class="sxs-lookup"><span data-stu-id="03107-135">There is no default value for this annotation.</span></span>

## <a name="saseffectauthor"></a><span data-ttu-id="03107-136">SasEffectAuthor</span><span class="sxs-lookup"><span data-stu-id="03107-136">SasEffectAuthor</span></span>

<span data-ttu-id="03107-137">Isso declara a pessoa que criou o efeito.</span><span class="sxs-lookup"><span data-stu-id="03107-137">This declares the person who created the effect.</span></span> <span data-ttu-id="03107-138">Ela é declarada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="03107-138">It is declared like this:</span></span>


```
string SasEffectAuthor = "value";
```



<span data-ttu-id="03107-139">em que value é uma cadeia de caracteres que identifica o autor do efeito.</span><span class="sxs-lookup"><span data-stu-id="03107-139">where value is a string that identifies the effect author.</span></span> <span data-ttu-id="03107-140">O padrão é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="03107-140">The default is an empty string.</span></span>

## <a name="saseffectauthoringsoftware"></a><span data-ttu-id="03107-141">SasEffectAuthoringSoftware</span><span class="sxs-lookup"><span data-stu-id="03107-141">SasEffectAuthoringSoftware</span></span>

<span data-ttu-id="03107-142">Isso declara o software no qual o efeito foi criado.</span><span class="sxs-lookup"><span data-stu-id="03107-142">This declares the software that the effect was authored on.</span></span> <span data-ttu-id="03107-143">Ela é declarada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="03107-143">It is declared like this:</span></span>


```
string SasEffectAuthoringSoftware = "value";
```



<span data-ttu-id="03107-144">em que value é uma cadeia de caracteres que identifica o efeito de criação de software.</span><span class="sxs-lookup"><span data-stu-id="03107-144">where value is a string that identifies the effect authoring software.</span></span> <span data-ttu-id="03107-145">O padrão é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="03107-145">The default is an empty string.</span></span>

## <a name="saseffectcategory"></a><span data-ttu-id="03107-146">SasEffectCategory</span><span class="sxs-lookup"><span data-stu-id="03107-146">SasEffectCategory</span></span>

<span data-ttu-id="03107-147">Isso declara a categoria de efeito.</span><span class="sxs-lookup"><span data-stu-id="03107-147">This declares the effect category.</span></span> <span data-ttu-id="03107-148">Ela é declarada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="03107-148">It is declared like this:</span></span>


```
string SasEffectCategory = "value";
```



<span data-ttu-id="03107-149">em que value é uma cadeia de caracteres que identifica a categoria de efeito.</span><span class="sxs-lookup"><span data-stu-id="03107-149">where value is a string that identifies the effect category.</span></span> <span data-ttu-id="03107-150">O padrão é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="03107-150">The default is an empty string.</span></span> <span data-ttu-id="03107-151">A categoria é expressa por meio de um valor do tipo caminho usando a barra como um delimitador.</span><span class="sxs-lookup"><span data-stu-id="03107-151">The category is expressed via a path-like value using the forward slash as a delimiter.</span></span> <span data-ttu-id="03107-152">Os efeitos só podem pertencer a uma categoria, já que não há sintaxe para expressar a inclusão em vários caminhos em um único valor SasEffectCategory.</span><span class="sxs-lookup"><span data-stu-id="03107-152">Effects can only belong to one category as there is no syntax for expressing inclusion in multiple paths within a single SasEffectCategory value.</span></span> <span data-ttu-id="03107-153">O valor dessa anotação não é tratado como diferenciação de maiúsculas e minúsculas pelo aplicativo host.</span><span class="sxs-lookup"><span data-stu-id="03107-153">The value of this annotation is not treated as case-sensitive by the host application.</span></span>

## <a name="saseffectcompany"></a><span data-ttu-id="03107-154">SasEffectCompany</span><span class="sxs-lookup"><span data-stu-id="03107-154">SasEffectCompany</span></span>

<span data-ttu-id="03107-155">Isso declara a empresa que criou o efeito.</span><span class="sxs-lookup"><span data-stu-id="03107-155">This declares the company that created the effect.</span></span> <span data-ttu-id="03107-156">Ela é declarada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="03107-156">It is declared like this:</span></span>


```
string SasEffectCompany = "value";
```



<span data-ttu-id="03107-157">em que value é uma cadeia de caracteres que identifica o nome da empresa que possui o efeito.</span><span class="sxs-lookup"><span data-stu-id="03107-157">where value is a string that identifies the name of the company that owns the effect.</span></span> <span data-ttu-id="03107-158">O padrão é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="03107-158">The default is an empty string.</span></span>

## <a name="saseffectdescription"></a><span data-ttu-id="03107-159">SasEffectDescription</span><span class="sxs-lookup"><span data-stu-id="03107-159">SasEffectDescription</span></span>

<span data-ttu-id="03107-160">Isso descreve o efeito.</span><span class="sxs-lookup"><span data-stu-id="03107-160">This describes the effect.</span></span> <span data-ttu-id="03107-161">Ela é declarada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="03107-161">It is declared like this:</span></span>


```
string SasEffectDescription = "value";
```



<span data-ttu-id="03107-162">em que value é uma cadeia de caracteres que descreve o efeito.</span><span class="sxs-lookup"><span data-stu-id="03107-162">where value is a string that describes the effect.</span></span> <span data-ttu-id="03107-163">O padrão é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="03107-163">The default is an empty string.</span></span>

## <a name="saseffecthelp"></a><span data-ttu-id="03107-164">SasEffectHelp</span><span class="sxs-lookup"><span data-stu-id="03107-164">SasEffectHelp</span></span>

<span data-ttu-id="03107-165">Essa é uma cadeia de caracteres de ajuda que pode ser exibida para o usuário sempre que a ajuda no efeito associado for solicitada.</span><span class="sxs-lookup"><span data-stu-id="03107-165">This is a help string that can be displayed to the user whenever help on the associated effect is requested.</span></span> <span data-ttu-id="03107-166">Ela é declarada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="03107-166">It is declared like this:</span></span>


```
string SasEffectHelp = "value";
```



<span data-ttu-id="03107-167">em que value é uma cadeia de caracteres que pode ser exibida se o usuário solicitar ajuda.</span><span class="sxs-lookup"><span data-stu-id="03107-167">where value is a string that can be displayed if the user requests help.</span></span> <span data-ttu-id="03107-168">O padrão é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="03107-168">The default is an empty string.</span></span>

## <a name="saseffectrevision"></a><span data-ttu-id="03107-169">SasEffectRevision</span><span class="sxs-lookup"><span data-stu-id="03107-169">SasEffectRevision</span></span>

<span data-ttu-id="03107-170">Essa anotação permite que as ferramentas e os usuários registrem o número de revisão do arquivo de efeito associado.</span><span class="sxs-lookup"><span data-stu-id="03107-170">This annotation allows tools and users to record the revision number of the associated effect file.</span></span> <span data-ttu-id="03107-171">Por exemplo, os usuários podiam inserir palavras-chave apropriadas no valor dessa anotação para invocar a substituição de palavra-chave em seu software de controle de revisão favorito.</span><span class="sxs-lookup"><span data-stu-id="03107-171">For example, users could insert appropriate keywords in the value of this annotation to invoke keyword substitution in their favorite revision control software.</span></span> <span data-ttu-id="03107-172">Ela é declarada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="03107-172">It is declared like this:</span></span>


```
string SasEffectRevision = "value";
```



<span data-ttu-id="03107-173">em que value é uma cadeia de caracteres que identifica a revisão do efeito.</span><span class="sxs-lookup"><span data-stu-id="03107-173">where value is a string that identifies the effect revision.</span></span> <span data-ttu-id="03107-174">O padrão é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="03107-174">The default is an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="03107-175">Exemplos</span><span class="sxs-lookup"><span data-stu-id="03107-175">Examples</span></span>

<span data-ttu-id="03107-176">Aqui está um exemplo que usa apenas a anotação única necessária:</span><span class="sxs-lookup"><span data-stu-id="03107-176">Here is an example that uses only the single, required annotation:</span></span>


```
int gp : SasGlobal
<
  int3 SasVersion = {1,0,0};
>;
```



<span data-ttu-id="03107-177">Aqui está um exemplo que usa a anotação necessária e várias anotações opcionais:</span><span class="sxs-lookup"><span data-stu-id="03107-177">Here is an example that uses the required annotation and several optional annotations:</span></span>


```
int gp : SasGlobal
<
  int3 SasVersion = {1,0,0};
  string SasEffectAuthor = "Mike's Shader";
  string SasEffectAuthoringSoftware = "fxe 2.5.4";
  string SasEffectCategory = "/surface/procedural/wood";
  string SasEffectCompany = "Microsoft Corporation";
  string SasEffectDescription = "Renders an irridescent surface.";
  string SasEffectHelp = "For more information, see https://somelocation/skin.htm";    
  string SasEffectRevision = "$Revision$";  
>;
```



## <a name="related-topics"></a><span data-ttu-id="03107-178">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="03107-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03107-179">Referência de semântica e anotações padrão do DirectX</span><span class="sxs-lookup"><span data-stu-id="03107-179">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



