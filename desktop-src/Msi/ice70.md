---
description: ICE70 verifica se os valores inteiros das entradas do registro estão especificados corretamente.
ms.assetid: f8493622-867b-42e1-9fda-a7c3229bbb4e
title: ICE70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616592a772dec6f95d81b92f03f0bffea6ce7bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758956"
---
# <a name="ice70"></a><span data-ttu-id="a480f-103">ICE70</span><span class="sxs-lookup"><span data-stu-id="a480f-103">ICE70</span></span>

<span data-ttu-id="a480f-104">ICE70 verifica se os valores inteiros das entradas do registro estão especificados corretamente.</span><span class="sxs-lookup"><span data-stu-id="a480f-104">ICE70 verifies that integer values for registry entries are specified correctly.</span></span> <span data-ttu-id="a480f-105">Os valores do formato \# \# Str, \# % unexpanded Str não são validados.</span><span class="sxs-lookup"><span data-stu-id="a480f-105">Values of the form \#\#str, \#%unexpanded str are not validated.</span></span> <span data-ttu-id="a480f-106">Os valores do formato \# xhex, \# xhex, \# Integer e \# \[ Property \] são validados.</span><span class="sxs-lookup"><span data-stu-id="a480f-106">Values of the form \#xhex, \#Xhex, \#integer, and \#\[property\] are validated.</span></span> <span data-ttu-id="a480f-107">A tabela a seguir fornece uma breve visão geral.</span><span class="sxs-lookup"><span data-stu-id="a480f-107">The following table provides a brief overview.</span></span>



| <span data-ttu-id="a480f-108">Valor</span><span class="sxs-lookup"><span data-stu-id="a480f-108">Value</span></span>                 | <span data-ttu-id="a480f-109">Validação</span><span class="sxs-lookup"><span data-stu-id="a480f-109">Validation</span></span>                                                                    |
|-----------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="a480f-110">\#\#Str</span><span class="sxs-lookup"><span data-stu-id="a480f-110">\#\#str</span></span>               | <span data-ttu-id="a480f-111">válido</span><span class="sxs-lookup"><span data-stu-id="a480f-111">valid</span></span>                                                                         |
| <span data-ttu-id="a480f-112">\#% de str não expandido</span><span class="sxs-lookup"><span data-stu-id="a480f-112">\#%unexpanded str</span></span>     | <span data-ttu-id="a480f-113">válido</span><span class="sxs-lookup"><span data-stu-id="a480f-113">valid</span></span>                                                                         |
| <span data-ttu-id="a480f-114">\#xHex, \# xHex</span><span class="sxs-lookup"><span data-stu-id="a480f-114">\#xHex,\#XHex</span></span>         | <span data-ttu-id="a480f-115">Valide os caracteres hexadecimais válidos (0-9, a-f, A-F).</span><span class="sxs-lookup"><span data-stu-id="a480f-115">Validate for valid hex characters (0-9,a-f,A-F).</span></span> <span data-ttu-id="a480f-116">As propriedades são permitidas aqui.</span><span class="sxs-lookup"><span data-stu-id="a480f-116">Properties are allowed here.</span></span> |
| <span data-ttu-id="a480f-117">\#+ int, \# -int, \# int</span><span class="sxs-lookup"><span data-stu-id="a480f-117">\#+int, \#-int, \#int</span></span> | <span data-ttu-id="a480f-118">Validar para caracteres numéricos válidos (0-9).</span><span class="sxs-lookup"><span data-stu-id="a480f-118">Validate for valid numeric characters (0-9).</span></span> <span data-ttu-id="a480f-119">As propriedades são permitidas aqui.</span><span class="sxs-lookup"><span data-stu-id="a480f-119">Properties are allowed here.</span></span>     |



 

<span data-ttu-id="a480f-120">A sintaxe para um valor inteiro a ser inserido no registro é \# Integer, em que Integer é numérico.</span><span class="sxs-lookup"><span data-stu-id="a480f-120">The syntax for an integer value to be entered into the registry is \#integer where integer is numerical.</span></span>

## <a name="result"></a><span data-ttu-id="a480f-121">Resultado</span><span class="sxs-lookup"><span data-stu-id="a480f-121">Result</span></span>

<span data-ttu-id="a480f-122">ICE70 relatará um erro se os valores inteiros das entradas do registro não forem especificados corretamente.</span><span class="sxs-lookup"><span data-stu-id="a480f-122">ICE70 reports an error if integer values for registry entries are not specified correctly.</span></span>

## <a name="example"></a><span data-ttu-id="a480f-123">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a480f-123">Example</span></span>

<span data-ttu-id="a480f-124">ICE70 relata os erros a seguir para o exemplo fornecido.</span><span class="sxs-lookup"><span data-stu-id="a480f-124">ICE70 reports the following errors for the given example.</span></span>

``` syntax
The value #12xz34 is an invalid numeric value for registry entry Reg1. If you meant to use a string, then the string value entry must be preceded by ## not #.
```

<span data-ttu-id="a480f-125">Para corrigir este erro: se você quiser que o valor seja numérico, altere o valor para usar todos os caracteres numéricos.</span><span class="sxs-lookup"><span data-stu-id="a480f-125">To fix this error: If you want the value to be numeric, change the value to use all numeric characters.</span></span> <span data-ttu-id="a480f-126">Se você quiser que o valor seja uma cadeia de caracteres, ele deverá ser precedido por dois ' \# ' ( \# \# ) em vez de apenas um.</span><span class="sxs-lookup"><span data-stu-id="a480f-126">If you want the value to be a string, it must be preceded by two '\#' (\#\#) instead of just one.</span></span>

``` syntax
The value #xz34 is an invalid hexadecimal value for registry entry Reg2.
```

<span data-ttu-id="a480f-127">Para corrigir esse erro: os caracteres hexadecimais válidos são 0-9, A-F e a-f.</span><span class="sxs-lookup"><span data-stu-id="a480f-127">To fix this error: Valid hexadecimal characters are 0-9, A-F, and a-f.</span></span> <span data-ttu-id="a480f-128">Somente esses caracteres podem seguir o \# x (ou \# x).</span><span class="sxs-lookup"><span data-stu-id="a480f-128">Only these characters can follow the \#x (or \#X).</span></span>

<span data-ttu-id="a480f-129">[Tabela do registro](registry-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="a480f-129">[Registry table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="a480f-130">Registro</span><span class="sxs-lookup"><span data-stu-id="a480f-130">Registry</span></span> | <span data-ttu-id="a480f-131">Valor</span><span class="sxs-lookup"><span data-stu-id="a480f-131">Value</span></span>    |
|----------|----------|
| <span data-ttu-id="a480f-132">Reg1</span><span class="sxs-lookup"><span data-stu-id="a480f-132">Reg1</span></span>     | <span data-ttu-id="a480f-133">\#12xz34</span><span class="sxs-lookup"><span data-stu-id="a480f-133">\#12xz34</span></span> |
| <span data-ttu-id="a480f-134">Reg2</span><span class="sxs-lookup"><span data-stu-id="a480f-134">Reg2</span></span>     | <span data-ttu-id="a480f-135">\#xz34</span><span class="sxs-lookup"><span data-stu-id="a480f-135">\#xz34</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="a480f-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="a480f-136">Remarks</span></span>

-   <span data-ttu-id="a480f-137">\#\[MyProperty \] é válido.</span><span class="sxs-lookup"><span data-stu-id="a480f-137">\#\[myproperty\] is valid.</span></span>
-   <span data-ttu-id="a480f-138">\#\[MyProperty não é válido (colchete de fechamento ausente).</span><span class="sxs-lookup"><span data-stu-id="a480f-138">\#\[myproperty is not valid (missing ending bracket).</span></span>
-   <span data-ttu-id="a480f-139">\#\[myprop1 \] \[ myprop2 é válido.</span><span class="sxs-lookup"><span data-stu-id="a480f-139">\#\[myprop1\] \[myprop2 is valid.</span></span> <span data-ttu-id="a480f-140">(Mesmo que o último esteja faltando o colchete final, myprop1 poderia avaliar como \# str para que você tivesse \# \# myprop2 Str \[ , que é válido</span><span class="sxs-lookup"><span data-stu-id="a480f-140">(Even though the last one is missing the ending bracket, myprop1 could evaluate to \#str so you would have \#\#str \[myprop2, which is valid</span></span>
-   <span data-ttu-id="a480f-141">\#\]MyProperty \[ não é válido</span><span class="sxs-lookup"><span data-stu-id="a480f-141">\#\]myproperty\[ is not valid</span></span>
-   <span data-ttu-id="a480f-142">Qualquer propriedade inserida em uma cadeia de caracteres de valor não pode estar no \[ \] formulário $compkey, \[ \# FileKey \] ou \[ ! FileKey \] porque elas não são numéricas.</span><span class="sxs-lookup"><span data-stu-id="a480f-142">Any embedded property in a value string cannot be in \[$compkey\], \[\#filekey\], or \[!filekey\] form because these are not numeric.</span></span> <span data-ttu-id="a480f-143">No entanto, há uma exceção, \# \[ MyProperty \] \[ $compkey \] (ou \[ \# FileKey \] ou \[ ! FileKey \] ) é válida porque, como no anterior, \[ MyProperty \] pode avaliar como \# Str.</span><span class="sxs-lookup"><span data-stu-id="a480f-143">However, there is one exception, \#\[myproperty\] \[$compkey\] (or \[\#filekey\] or \[!filekey\]) is valid because, as with the preceding, \[myproperty\] can evaluate to \#str.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a480f-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a480f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a480f-145">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="a480f-145">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



