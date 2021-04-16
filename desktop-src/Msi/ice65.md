---
description: ICE65 verifica se a tabela de ambiente não tem valores de acréscimo ou de prefixo inválidos.
ms.assetid: 95d4e618-9a19-40db-910a-daab105559ae
title: ICE65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3d2b7bcd844c970ccc7fddf376b27c2ec54f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752256"
---
# <a name="ice65"></a><span data-ttu-id="8b819-103">ICE65</span><span class="sxs-lookup"><span data-stu-id="8b819-103">ICE65</span></span>

<span data-ttu-id="8b819-104">ICE65 verifica se a [tabela de ambiente](environment-table.md) não tem valores de acréscimo ou de prefixo inválidos.</span><span class="sxs-lookup"><span data-stu-id="8b819-104">ICE65 checks that the [Environment table](environment-table.md) does not have invalid prefix or append values.</span></span>

<span data-ttu-id="8b819-105">Falha ao corrigir um aviso ou erro relatado por ICE65 geralmente leva a problemas na instalação, na desinstalação ou no reparo da variável de ambiente.</span><span class="sxs-lookup"><span data-stu-id="8b819-105">Failure to fix a warning or error reported by ICE65 generally leads to problems in install, uninstall, or repair of the environment variable.</span></span> <span data-ttu-id="8b819-106">Por exemplo, somente alguns valores de uma variável específica poderão ser removidos se um ou mais dos valores dessa variável tiverem um separador à direita.</span><span class="sxs-lookup"><span data-stu-id="8b819-106">For example, only some values of a particular variable may be removed if one or more of the values for that variable have a trailing separator.</span></span>

## <a name="result"></a><span data-ttu-id="8b819-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="8b819-107">Result</span></span>

<span data-ttu-id="8b819-108">ICE65 lançará um aviso ou um erro se a tabela de ambiente tiver valores de prefixo ou acréscimo inválidos.</span><span class="sxs-lookup"><span data-stu-id="8b819-108">ICE65 posts a warning or an error if the environment table has invalid prefix or append values.</span></span>

## <a name="example"></a><span data-ttu-id="8b819-109">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8b819-109">Example</span></span>

<span data-ttu-id="8b819-110">ICE65 relata o seguinte erro e aviso para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="8b819-110">ICE65 reports the following error and warning for the example shown.</span></span>

``` syntax
The environment variable 'Var3' has a separator beginning or ending its value.
```

<span data-ttu-id="8b819-111">O nulo à direita no final do valor ( \[ ~ \] ) marca esse valor como sendo anexado a qualquer valor existente.</span><span class="sxs-lookup"><span data-stu-id="8b819-111">The trailing null at the end of the value (\[~\]) marks this value to be prepended to any existing value.</span></span> <span data-ttu-id="8b819-112">O caractere imediatamente antes de NULL (ponto-e-vírgula) torna-se o separador desse valor.</span><span class="sxs-lookup"><span data-stu-id="8b819-112">The character immediately before the null (a semicolon) becomes the separator for this value.</span></span> <span data-ttu-id="8b819-113">Esse valor também tem um ponto e vírgula no início da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8b819-113">This value has a semicolon at the beginning of the string as well.</span></span>

<span data-ttu-id="8b819-114">Para corrigir esse erro, basta excluir o ponto-e-vírgula à esquerda.</span><span class="sxs-lookup"><span data-stu-id="8b819-114">To fix this error, simply delete the leading semicolon.</span></span>

``` syntax
WARNING: The environment variable 'Var2' has an alphanumeric separator
```

<span data-ttu-id="8b819-115">O nulo à esquerda no valor ( \[ ~ \] ) marca esse valor a ser anexado a qualquer valor existente.</span><span class="sxs-lookup"><span data-stu-id="8b819-115">The leading null in the value (\[~\]) marks this value to be appended to any existing value.</span></span> <span data-ttu-id="8b819-116">O caractere imediatamente após NULL torna-se o separador desse valor.</span><span class="sxs-lookup"><span data-stu-id="8b819-116">The character immediately after the null becomes the separator for this value.</span></span> <span data-ttu-id="8b819-117">Nesse caso, esse caractere é a letra "e", que também ocorre no meio da cadeia de caracteres a ser acrescentada.</span><span class="sxs-lookup"><span data-stu-id="8b819-117">In this case, that character is the letter "e", which also occurs in the middle of the string to be appended.</span></span> <span data-ttu-id="8b819-118">Essa condição (com um separador igual a um caractere dentro da cadeia de caracteres a ser acrescentada) pode causar resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="8b819-118">This condition (having a separator that is the same as a character within the string to be appended) can cause unpredictable results.</span></span>

<span data-ttu-id="8b819-119">A letra "e", sendo uma letra comum, provavelmente será encontrada no valor.</span><span class="sxs-lookup"><span data-stu-id="8b819-119">The letter "e", being a common letter, is likely to be found in the value.</span></span> <span data-ttu-id="8b819-120">Uma opção melhor seria ";" ou algum outro caractere não alfanumérico.</span><span class="sxs-lookup"><span data-stu-id="8b819-120">A better choice would be ";" or some other non-alphanumeric character.</span></span> <span data-ttu-id="8b819-121">(No entanto, se o valor for um caminho, ":" e " \\ " e "." são opções arriscadas.)</span><span class="sxs-lookup"><span data-stu-id="8b819-121">(However, if the value is a path, then ":" and "\\" and "." are risky choices.)</span></span>

<span data-ttu-id="8b819-122">Para corrigir esse aviso, use um caractere separador diferente.</span><span class="sxs-lookup"><span data-stu-id="8b819-122">To fix this warning, use a different separator character.</span></span>

[<span data-ttu-id="8b819-123">Tabela de ambiente</span><span class="sxs-lookup"><span data-stu-id="8b819-123">Environment Table</span></span>](environment-table.md)



| <span data-ttu-id="8b819-124">Componente</span><span class="sxs-lookup"><span data-stu-id="8b819-124">Component</span></span> | <span data-ttu-id="8b819-125">Diretório</span><span class="sxs-lookup"><span data-stu-id="8b819-125">Directory</span></span> | <span data-ttu-id="8b819-126">Atributos</span><span class="sxs-lookup"><span data-stu-id="8b819-126">Attributes</span></span>         | <span data-ttu-id="8b819-127">KeyPath</span><span class="sxs-lookup"><span data-stu-id="8b819-127">KeyPath</span></span>       |
|-----------|-----------|--------------------|---------------|
| <span data-ttu-id="8b819-128">Var1</span><span class="sxs-lookup"><span data-stu-id="8b819-128">Var1</span></span>      | <span data-ttu-id="8b819-129">TestVar</span><span class="sxs-lookup"><span data-stu-id="8b819-129">TestVar</span></span>   | <span data-ttu-id="8b819-130">\[~\]; AppendThis</span><span class="sxs-lookup"><span data-stu-id="8b819-130">\[~\];AppendThis</span></span>   | <span data-ttu-id="8b819-131">TestComponent</span><span class="sxs-lookup"><span data-stu-id="8b819-131">TestComponent</span></span> |
| <span data-ttu-id="8b819-132">Var2</span><span class="sxs-lookup"><span data-stu-id="8b819-132">Var2</span></span>      | <span data-ttu-id="8b819-133">TestVar</span><span class="sxs-lookup"><span data-stu-id="8b819-133">TestVar</span></span>   | <span data-ttu-id="8b819-134">\[~\]eAppendThis</span><span class="sxs-lookup"><span data-stu-id="8b819-134">\[~\]eAppendThis</span></span>   | <span data-ttu-id="8b819-135">TestComponent</span><span class="sxs-lookup"><span data-stu-id="8b819-135">TestComponent</span></span> |
| <span data-ttu-id="8b819-136">Var3</span><span class="sxs-lookup"><span data-stu-id="8b819-136">Var3</span></span>      | <span data-ttu-id="8b819-137">TestVar</span><span class="sxs-lookup"><span data-stu-id="8b819-137">TestVar</span></span>   | <span data-ttu-id="8b819-138">; PrependThis;\[~\]</span><span class="sxs-lookup"><span data-stu-id="8b819-138">;PrependThis;\[~\]</span></span> | <span data-ttu-id="8b819-139">TestComponent</span><span class="sxs-lookup"><span data-stu-id="8b819-139">TestComponent</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8b819-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8b819-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b819-141">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="8b819-141">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



