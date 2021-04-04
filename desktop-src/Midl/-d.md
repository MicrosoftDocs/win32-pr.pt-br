---
title: Opção/d
description: A opção/D define um nome e um valor opcional a ser passado para o pré-processador de C como se fosse uma diretiva \ define. Várias diretivas/D podem ser usadas em uma linha de comando.
ms.assetid: 65642bf6-8e25-400b-8b1c-43513ab6b313
keywords:
- /D opção MIDL
topic_type:
- apiref
api_name:
- /D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d51cdcbecb5386acb1a97d933be8b25f68720ee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104084208"
---
# <a name="d-switch"></a><span data-ttu-id="e235a-105">Opção/d</span><span class="sxs-lookup"><span data-stu-id="e235a-105">/D switch</span></span>

<span data-ttu-id="e235a-106">A opção **/d** define um nome e um valor opcional a ser passado para o pré-processador de C como se fosse por uma diretiva de **\# definição** .</span><span class="sxs-lookup"><span data-stu-id="e235a-106">The **/D** switch defines a name and an optional value to be passed to the C preprocessor as if by a **\#define** directive.</span></span> <span data-ttu-id="e235a-107">Várias diretivas **/d** podem ser usadas em uma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="e235a-107">Multiple **/D** directives can be used in a command line.</span></span>

``` syntax
midl /Dname[=definition]
```

## <a name="switch-options"></a><span data-ttu-id="e235a-108">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="e235a-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="e235a-109">*name*</span><span class="sxs-lookup"><span data-stu-id="e235a-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="e235a-110">Especifica um nome definido que é passado para o pré-processador C quando a opção [**/cpp \_ cmd**](-cpp-cmd.md) está presente e a opção de [**/cpp \_ opt**](-cpp-opt.md) não está presente.</span><span class="sxs-lookup"><span data-stu-id="e235a-110">Specifies a defined name that is passed to the C preprocessor when the [**/cpp\_cmd**](-cpp-cmd.md) switch is present and the [**/cpp\_opt**](-cpp-opt.md) switch is not present.</span></span>

</dd> <dt>

<span data-ttu-id="e235a-111">*defini*</span><span class="sxs-lookup"><span data-stu-id="e235a-111">*definition*</span></span> 
</dt> <dd>

<span data-ttu-id="e235a-112">Especifica um valor associado ao nome definido.</span><span class="sxs-lookup"><span data-stu-id="e235a-112">Specifies a value associated with the defined name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e235a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e235a-113">Remarks</span></span>

<span data-ttu-id="e235a-114">O espaço em branco entre a opção **/d** e o nome definido é opcional.</span><span class="sxs-lookup"><span data-stu-id="e235a-114">White space between the **/D** switch and the defined name is optional.</span></span>

<span data-ttu-id="e235a-115">Quando a [**opção \_ /cpp cmd**](-cpp-cmd.md) está presente e a opção de [**/cpp \_ opt**](-cpp-opt.md) não é, o compilador MIDL concatena a cadeia de caracteres especificada pela opção **\_ cmd/cpp** com as opções [**/i**](-i.md), **/d** e [**/U**](-u.md) e usa essa cadeia de caracteres concatenada para invocar o pré-processador C para cada arquivo de origem IDL e ACF.</span><span class="sxs-lookup"><span data-stu-id="e235a-115">When the [**/cpp\_cmd**](-cpp-cmd.md) switch is present and the [**/cpp\_opt**](-cpp-opt.md) switch is not, the MIDL compiler concatenates the string specified by the **/cpp\_cmd** switch with the [**/I**](-i.md), **/D**, and [**/U**](-u.md) options and uses this concatenated string to invoke the C preprocessor for each IDL and ACF source file.</span></span>

<span data-ttu-id="e235a-116">A opção de compilador MIDL **/d** é ignorada quando o parâmetro de compilador MIDL switch [/ \_](-no-cpp-nocpp.md) [**/cpp \_ opt**](-cpp-opt.md) é especificado.</span><span class="sxs-lookup"><span data-stu-id="e235a-116">The MIDL compiler switch **/D** is ignored when the MIDL compiler switch [/no\_cpp](-no-cpp-nocpp.md) or [**/cpp\_opt**](-cpp-opt.md) is specified.</span></span>

## <a name="examples"></a><span data-ttu-id="e235a-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e235a-117">Examples</span></span>

<span data-ttu-id="e235a-118">**MIDL-DUNICODE filename. idl**</span><span class="sxs-lookup"><span data-stu-id="e235a-118">**midl -DUNICODE filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="e235a-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="e235a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e235a-120">**/cpp \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="e235a-120">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="e235a-121">**/cpp \_ aceitar**</span><span class="sxs-lookup"><span data-stu-id="e235a-121">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="e235a-122">**/I**</span><span class="sxs-lookup"><span data-stu-id="e235a-122">**/I**</span></span>](-i.md)
</dt> <dt>

[<span data-ttu-id="e235a-123">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="e235a-123">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="e235a-124">**///// \_ cpp**</span><span class="sxs-lookup"><span data-stu-id="e235a-124">**/no\_cpp**</span></span>](-no-cpp-nocpp.md)
</dt> <dt>

[<span data-ttu-id="e235a-125">**/U**</span><span class="sxs-lookup"><span data-stu-id="e235a-125">**/U**</span></span>](-u.md)
</dt> </dl>

 

 




