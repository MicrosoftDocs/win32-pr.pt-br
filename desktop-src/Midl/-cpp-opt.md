---
title: opção/cpp_opt
description: A \_ opção/cpp opt especifica opções a serem passadas para o pré-processador do C/C++.
ms.assetid: f0059caa-aff3-4e96-95f8-a0014d6a6556
keywords:
- /cpp_opt MIDL do comutador
topic_type:
- apiref
api_name:
- /cpp_opt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00e352a89ddadfc0a92e33e964afb5f0d9e9df6e
ms.sourcegitcommit: 97d62bfd3213d9c4ce46c3cd2b1177caf720681a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104368989"
---
# <a name="cpp_opt-switch"></a><span data-ttu-id="199a5-104">\_comutador opcional/cpp</span><span class="sxs-lookup"><span data-stu-id="199a5-104">/cpp\_opt switch</span></span>

<span data-ttu-id="199a5-105">A opção **/cpp \_ opt** especifica opções a serem passadas para o pré-processador do C/C++.</span><span class="sxs-lookup"><span data-stu-id="199a5-105">The **/cpp\_opt** switch specifies options to pass to the C/C++ preprocessor.</span></span>

``` syntax
midl /cpp_opt "C_preprocessor_option" file.idl
```

## <a name="switch-options"></a><span data-ttu-id="199a5-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="199a5-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="199a5-107">*\_Opção de pré-processador C \_*</span><span class="sxs-lookup"><span data-stu-id="199a5-107">*C\_preprocessor\_option*</span></span> 
</dt> <dd>

<span data-ttu-id="199a5-108">Especifica a opção de linha de comando associada ao pré-processador invocado.</span><span class="sxs-lookup"><span data-stu-id="199a5-108">Specifies command-line option associated with the invoked preprocessor.</span></span> 

<span data-ttu-id="199a5-109">**Observação**: para os pré-processadores Microsoft c/C++, você deve fornecer o `/E` comutador como parte da cadeia de caracteres da *\_ \_ opção de pré-processador C* .</span><span class="sxs-lookup"><span data-stu-id="199a5-109">**Note**: For the Microsoft C/C++ preprocessors you must supply the `/E` switch as part of the *C\_preprocessor\_option* string.</span></span> 

<span data-ttu-id="199a5-110">As aspas são necessárias quando mais de uma opção é usada e para espaços.</span><span class="sxs-lookup"><span data-stu-id="199a5-110">Quotes are required when more than one option is used, and for spaces.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="199a5-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="199a5-111">Remarks</span></span>

<span data-ttu-id="199a5-112">Não use essa opção, a menos que haja um motivo específico para isso.</span><span class="sxs-lookup"><span data-stu-id="199a5-112">Do not use this switch unless there is a specific reason for doing so.</span></span> <span data-ttu-id="199a5-113">Consulte [requisitos de pré-processador do C para MIDL](c-preprocessor-requirements-for-midl.md) para obter informações importantes sobre o pré-processamento.</span><span class="sxs-lookup"><span data-stu-id="199a5-113">Consult [C-Preprocessor Requirements for MIDL](c-preprocessor-requirements-for-midl.md) for important information regarding preprocessing.</span></span>

<span data-ttu-id="199a5-114">A opção **/cpp \_ opt** pode ser usada com ou sem a opção [**\_ cmd do/CPP**](-cpp-cmd.md) .</span><span class="sxs-lookup"><span data-stu-id="199a5-114">The **/cpp\_opt** switch can be used with or without the [**/cpp\_cmd**](-cpp-cmd.md) switch.</span></span> <span data-ttu-id="199a5-115">Consulte **/cpp \_ cmd** para obter detalhes de como a linha de comando do pré-processador é construída em ambos os casos.</span><span class="sxs-lookup"><span data-stu-id="199a5-115">Consult **/cpp\_cmd** for details of how the preprocessor command line is constructed in either case.</span></span>

<span data-ttu-id="199a5-116">A opção **/cpp \_ opt** , se especificada, deve sempre incluir `/E` para funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="199a5-116">The **/cpp\_opt** switch, if specified, must always include `/E` in order to function correctly.</span></span>

## <a name="examples"></a><span data-ttu-id="199a5-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="199a5-117">Examples</span></span>

<span data-ttu-id="199a5-118">**MIDL/cpp \_ cmd d: \\ NT \\ Tools \\ IA64 \\cl.exe/DFLAG = true/IC: \\ Inc filename. idl**</span><span class="sxs-lookup"><span data-stu-id="199a5-118">**midl /cpp\_cmd d:\\nt\\tools\\ia64\\cl.exe /DFLAG=TRUE /Ic:\\inc filename.idl**</span></span>

<span data-ttu-id="199a5-119">**MIDL/cpp \_ cmd "mycpp"/DFLAG = true/IC: \\ Inc filename. idl**</span><span class="sxs-lookup"><span data-stu-id="199a5-119">**midl /cpp\_cmd "mycpp" /DFLAG=TRUE /Ic:\\inc filename.idl**</span></span>

<span data-ttu-id="199a5-120">**MIDL/cpp \_ opt "/E/DFLAG = true/IC: \\ Inc" filename. idl**</span><span class="sxs-lookup"><span data-stu-id="199a5-120">**midl /cpp\_opt "/E /DFLAG=TRUE /Ic:\\inc" filename.idl**</span></span>

<span data-ttu-id="199a5-121">**MIDL/cpp \_ cmd "CL"/cpp \_ opt "/e/DFLAG = true/IC: \\ Inc" filename. idl**</span><span class="sxs-lookup"><span data-stu-id="199a5-121">**midl /cpp\_cmd "cl" /cpp\_opt "/E /DFLAG=TRUE /Ic:\\inc" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="199a5-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="199a5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="199a5-123">**/savePP**</span><span class="sxs-lookup"><span data-stu-id="199a5-123">**/savePP**</span></span>](-savepp.md)
</dt> <dt>

[<span data-ttu-id="199a5-124">**/cpp \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="199a5-124">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="199a5-125">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="199a5-125">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="199a5-126">**///// \_ cpp**</span><span class="sxs-lookup"><span data-stu-id="199a5-126">**/no\_cpp**</span></span>](-no-cpp-nocpp.md)
</dt> <dt>

[<span data-ttu-id="199a5-127">Requisitos de pré-processador do C para MIDL</span><span class="sxs-lookup"><span data-stu-id="199a5-127">C-Preprocessor Requirements for MIDL</span></span>](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 




