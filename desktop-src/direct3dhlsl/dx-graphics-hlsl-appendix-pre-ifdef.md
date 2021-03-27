---
title: " Diretivas ifdef e ifndef"
description: Diretivas de pré-processador que determinam se uma macro ou constante de pré-processador específico está definida.
ms.assetid: c1cc2e1d-2599-45ec-9629-56c4b42e0d0e
keywords:
- ifdef e diretivas ifndef HLSL
topic_type:
- apiref
api_name:
- ifdef and ifndef Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 338308b58f1cdc68ec78984e65ffbf056a36b10b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006546"
---
# <a name="ifdef-and-ifndef-directives"></a><span data-ttu-id="09f7a-104">\#Diretivas ifdef e \# ifndef</span><span class="sxs-lookup"><span data-stu-id="09f7a-104">\#ifdef and \#ifndef Directives</span></span>

<span data-ttu-id="09f7a-105">Diretivas de pré-processador que determinam se uma macro ou constante de pré-processador específico está definida.</span><span class="sxs-lookup"><span data-stu-id="09f7a-105">Preprocessor directives that determine whether a specific preprocessor constant or macro is defined.</span></span>



| <span data-ttu-id="09f7a-106">\#*identificador* de ifdef...</span><span class="sxs-lookup"><span data-stu-id="09f7a-106">\#ifdef *identifier* ...</span></span>  |
|---------------------------|
| <span data-ttu-id="09f7a-107">\#endif</span><span class="sxs-lookup"><span data-stu-id="09f7a-107">\#endif</span></span>                   |
| <span data-ttu-id="09f7a-108">\#*identificador* de ifndef...</span><span class="sxs-lookup"><span data-stu-id="09f7a-108">\#ifndef *identifier* ...</span></span> |
| <span data-ttu-id="09f7a-109">\#endif</span><span class="sxs-lookup"><span data-stu-id="09f7a-109">\#endif</span></span>                   |



 

## <a name="parameters"></a><span data-ttu-id="09f7a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09f7a-110">Parameters</span></span>



| <span data-ttu-id="09f7a-111">Item</span><span class="sxs-lookup"><span data-stu-id="09f7a-111">Item</span></span>                                                                              | <span data-ttu-id="09f7a-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="09f7a-112">Description</span></span>                                               |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="09f7a-113"><span id="identifier"></span><span id="IDENTIFIER"></span>*ID*</span><span class="sxs-lookup"><span data-stu-id="09f7a-113"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/> | <span data-ttu-id="09f7a-114">Identificador da constante ou macro a ser verificada.</span><span class="sxs-lookup"><span data-stu-id="09f7a-114">Identifier of the constant or macro to check.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="09f7a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="09f7a-115">Remarks</span></span>

<span data-ttu-id="09f7a-116">Você pode usar as \# diretivas ifdef e \# ifndef em qualquer lugar que o [ \# se](dx-graphics-hlsl-appendix-pre-if.md) possa ser usado.</span><span class="sxs-lookup"><span data-stu-id="09f7a-116">You can use the \#ifdef and \#ifndef directives anywhere that the [\#if](dx-graphics-hlsl-appendix-pre-if.md) can be used.</span></span> <span data-ttu-id="09f7a-117">A \# diretiva ifdef é equivalente a).</span><span class="sxs-lookup"><span data-stu-id="09f7a-117">The \#ifdef statement is equivalent to ) directive.</span></span> <span data-ttu-id="09f7a-118">Essas diretivas verificam apenas a presença ou a ausência de identificadores definidos usando a diretiva [ \# definir](dx-graphics-hlsl-appendix-pre-define.md) , não para identificadores declarados no código-fonte C ou C++.</span><span class="sxs-lookup"><span data-stu-id="09f7a-118">These directives check only for the presence or absence of identifiers defined using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive, not for identifiers declared in the C or C++ source code.</span></span>

<span data-ttu-id="09f7a-119">Essas políticas são fornecidas somente para compatibilidade com versões anteriores da linguagem.</span><span class="sxs-lookup"><span data-stu-id="09f7a-119">These directives are provided only for compatibility with previous versions of the language.</span></span> <span data-ttu-id="09f7a-120">O uso do operador [definido](dx-graphics-hlsl-appendix-pre-if.md) com a \# diretiva If é preferencial.</span><span class="sxs-lookup"><span data-stu-id="09f7a-120">The use of the [defined](dx-graphics-hlsl-appendix-pre-if.md) operator with the \#if directive is preferred.</span></span>

<span data-ttu-id="09f7a-121">A \# diretiva ifndef verifica o oposto da condição verificada por \# ifdef.</span><span class="sxs-lookup"><span data-stu-id="09f7a-121">The \#ifndef directive checks for the opposite of the condition checked by \#ifdef.</span></span> <span data-ttu-id="09f7a-122">Se o identificador não for definido, a condição será true (diferente de zero); caso contrário, a condição será false (zero).</span><span class="sxs-lookup"><span data-stu-id="09f7a-122">If the identifier is not defined, the condition is true (nonzero); otherwise, the condition is false (zero).</span></span>

## <a name="examples"></a><span data-ttu-id="09f7a-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="09f7a-123">Examples</span></span>

<span data-ttu-id="09f7a-124">O identificador pode ser passado da linha de comando usando a opção /D.</span><span class="sxs-lookup"><span data-stu-id="09f7a-124">The identifier can be passed from the command line using the /D option.</span></span> <span data-ttu-id="09f7a-125">Até 30 macros podem ser especificadas com /D.</span><span class="sxs-lookup"><span data-stu-id="09f7a-125">Up to 30 macros can be specified with /D.</span></span> <span data-ttu-id="09f7a-126">Isso é útil para verificar se uma definição existe, uma vez que uma definição pode ser passada da linha de comando.</span><span class="sxs-lookup"><span data-stu-id="09f7a-126">This is useful for checking whether a definition exists, because a definition can be passed from the command line.</span></span> <span data-ttu-id="09f7a-127">O exemplo a seguir usa esse comportamento para determinar se um aplicativo deve ser executado no modo de teste.</span><span class="sxs-lookup"><span data-stu-id="09f7a-127">The following example uses this behavior to determine whether to run an application in test mode.</span></span>


```
// PROG.CPP
#ifndef test
  #define final
#endif
int main()
{
}
```



<span data-ttu-id="09f7a-128">Quando compilado usando o comando a seguir, PROG. cpp será compilado no modo de teste; caso contrário, ele será compilado no modo final.</span><span class="sxs-lookup"><span data-stu-id="09f7a-128">When compiled using the following command, prog.cpp will compile in test mode; otherwise, it will compile in final mode.</span></span>


```
CL.EXE /Dtest prog.cpp
```



## <a name="see-also"></a><span data-ttu-id="09f7a-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="09f7a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09f7a-130">Diretivas de pré-processador (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="09f7a-130">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="09f7a-131">\#se,)</span><span class="sxs-lookup"><span data-stu-id="09f7a-131">\#if, )</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





