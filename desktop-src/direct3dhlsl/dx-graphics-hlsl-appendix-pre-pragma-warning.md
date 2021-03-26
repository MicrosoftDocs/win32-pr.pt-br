---
title: Diretiva de pragma de aviso
description: A diretiva pragma que modifica o comportamento das mensagens de aviso do compilador.
ms.assetid: 69488014-36e3-4c87-8b65-6123b5e87bcb
keywords:
- aviso de diretiva pragma HLSL
topic_type:
- apiref
api_name:
- warning pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7599886b47830b33c69f11c0c341c7775c644dd3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103916754"
---
# <a name="warning-pragma-directive"></a><span data-ttu-id="2be1f-104">Diretiva de pragma de aviso</span><span class="sxs-lookup"><span data-stu-id="2be1f-104">warning pragma Directive</span></span>

<span data-ttu-id="2be1f-105">A diretiva pragma que modifica o comportamento das mensagens de aviso do compilador.</span><span class="sxs-lookup"><span data-stu-id="2be1f-105">Pragma directive that modifies the behavior of compiler warning messages.</span></span>



| <span data-ttu-id="2be1f-106">\#pragma warning ( *aviso-especificador* : *aviso-número-lista* \[ ; *aviso-especificador* : *aviso-número-lista*... \] )</span><span class="sxs-lookup"><span data-stu-id="2be1f-106">\#pragma warning( *warning-specifier* : *warning-number-list* \[; *warning-specifier* : *warning-number-list*...\] )</span></span> |
|----------------------------------------------------------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="2be1f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2be1f-107">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2be1f-108">Item</span><span class="sxs-lookup"><span data-stu-id="2be1f-108">Item</span></span></th>
<th><span data-ttu-id="2be1f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="2be1f-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2be1f-110"><span id="warning-specifier"></span><span id="WARNING-SPECIFIER"></span><em>especificador de aviso</em></span><span class="sxs-lookup"><span data-stu-id="2be1f-110"><span id="warning-specifier"></span><span id="WARNING-SPECIFIER"></span><em>warning-specifier</em></span></span><br/></td>
<td><span data-ttu-id="2be1f-111">Comportamento a ser definido para os avisos especificados.</span><span class="sxs-lookup"><span data-stu-id="2be1f-111">Behavior to set for the specified warnings.</span></span> <span data-ttu-id="2be1f-112">Esse parâmetro pode usar um dos valores listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2be1f-112">This parameter can take one of the values listed in the following table.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2be1f-113">Valor</span><span class="sxs-lookup"><span data-stu-id="2be1f-113">Value</span></span></th>
<th><span data-ttu-id="2be1f-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="2be1f-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2be1f-115">uma vez</span><span class="sxs-lookup"><span data-stu-id="2be1f-115">once</span></span></td>
<td><span data-ttu-id="2be1f-116">Exiba a mensagem dos avisos com os números especificados apenas uma vez.</span><span class="sxs-lookup"><span data-stu-id="2be1f-116">Display the message of the warnings with the specified numbers only once.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2be1f-117">padrão</span><span class="sxs-lookup"><span data-stu-id="2be1f-117">default</span></span></td>
<td><span data-ttu-id="2be1f-118">Redefina o comportamento dos avisos com os números especificados para o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="2be1f-118">Reset the behavior of the warnings with the specified numbers to their default value.</span></span> <span data-ttu-id="2be1f-119">Isso também tem o efeito de ativar um aviso por padrão.</span><span class="sxs-lookup"><span data-stu-id="2be1f-119">This also has the effect of turning a warning on that is off by default.</span></span> <span data-ttu-id="2be1f-120">O aviso será gerado em seu nível padrão.</span><span class="sxs-lookup"><span data-stu-id="2be1f-120">The warning will be generated at its default level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2be1f-121">1, 2, 3, 4</span><span class="sxs-lookup"><span data-stu-id="2be1f-121">1, 2, 3, 4</span></span></td>
<td><span data-ttu-id="2be1f-122">Aplique o nível especificado aos avisos com os números especificados.</span><span class="sxs-lookup"><span data-stu-id="2be1f-122">Apply the specified level to the warnings with the specified numbers.</span></span> <span data-ttu-id="2be1f-123">Isso também tem o efeito de ativar um aviso por padrão.</span><span class="sxs-lookup"><span data-stu-id="2be1f-123">This also has the effect of turning a warning on that is off by default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2be1f-124">disable</span><span class="sxs-lookup"><span data-stu-id="2be1f-124">disable</span></span></td>
<td><span data-ttu-id="2be1f-125">Não emita os avisos com os números especificados.</span><span class="sxs-lookup"><span data-stu-id="2be1f-125">Do not issue the warnings with the specified numbers.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2be1f-126">erro</span><span class="sxs-lookup"><span data-stu-id="2be1f-126">error</span></span></td>
<td><span data-ttu-id="2be1f-127">Relatar os avisos com os números especificados como erros.</span><span class="sxs-lookup"><span data-stu-id="2be1f-127">Report the warnings with the specified numbers as errors.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2be1f-128"><span id="warning-number-list"></span><span id="WARNING-NUMBER-LIST"></span><em>aviso-lista de números</em></span><span class="sxs-lookup"><span data-stu-id="2be1f-128"><span id="warning-number-list"></span><span id="WARNING-NUMBER-LIST"></span><em>warning-number-list</em></span></span></p></td>
<td><p><span data-ttu-id="2be1f-129">Lista delimitada por espaço em branco dos números dos avisos para modificar o comportamento de.</span><span class="sxs-lookup"><span data-stu-id="2be1f-129">White space-delimited list of the numbers of the warnings to modify the behavior of.</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="2be1f-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="2be1f-130">Remarks</span></span>

<span data-ttu-id="2be1f-131">Você pode especificar qualquer número de alterações de comportamento de aviso distintas no mesmo pragma de aviso, separando as alterações com ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="2be1f-131">You can specify any number of distinct warning behavior changes within the same warning pragma by separating the changes with semicolons.</span></span>

<span data-ttu-id="2be1f-132">O compilador adicionará 4000 a qualquer número de aviso que esteja entre 0 e 999.</span><span class="sxs-lookup"><span data-stu-id="2be1f-132">The compiler will add 4000 to any warning number that is between 0 and 999.</span></span> <span data-ttu-id="2be1f-133">Para números de aviso maiores que 4699 (aqueles associados à geração de código), o pragma de aviso só tem efeito quando colocado fora das definições de função.</span><span class="sxs-lookup"><span data-stu-id="2be1f-133">For warning numbers greater than 4699, (those associated with code generation) the warning pragma has effect only when placed outside function definitions.</span></span> <span data-ttu-id="2be1f-134">O pragma será ignorado se ele especificar um número maior que 4699 e for usado dentro de uma função.</span><span class="sxs-lookup"><span data-stu-id="2be1f-134">The pragma is ignored if it specifies a number greater than 4699 and is used inside a function.</span></span>

<span data-ttu-id="2be1f-135">O pragma de aviso HLSL não dá suporte à funcionalidade **Push** e **pop** do pragma de aviso incluído no compilador C++.</span><span class="sxs-lookup"><span data-stu-id="2be1f-135">The HLSL warning pragma does not support the **push** and **pop** functionality of the warning pragma included in the C++ compiler.</span></span>

## <a name="examples"></a><span data-ttu-id="2be1f-136">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2be1f-136">Examples</span></span>

<span data-ttu-id="2be1f-137">O exemplo a seguir desabilita os avisos 4507 e 4034, exibe o aviso 4385 uma vez e relata o aviso de 4164 como um erro.</span><span class="sxs-lookup"><span data-stu-id="2be1f-137">The following example disables warnings 4507 and 4034, displays warning 4385 once once, and reports warning 4164 as an error.</span></span>


```
#pragma warning( disable : 4507 34; once : 4385; error : 164 )
```



<span data-ttu-id="2be1f-138">O exemplo anterior é funcionalmente equivalente ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="2be1f-138">The preceding example is functionally equivalent to the following:</span></span>


```
#pragma warning( disable : 4507 34 )
#pragma warning( once : 4385 )
#pragma warning( error : 164 )
```



## <a name="see-also"></a><span data-ttu-id="2be1f-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="2be1f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2be1f-140">Diretivas de pré-processador (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2be1f-140">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="2be1f-141">\#Diretiva pragma (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2be1f-141">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





