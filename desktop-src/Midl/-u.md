---
title: Opção/u
description: A opção/U remove qualquer definição anterior de um nome, passando o nome para o pré-processador de C como se fosse uma diretiva \ undefinetion.
ms.assetid: 3c253fb3-9448-4b55-bfd5-852e6feec280
keywords:
- /U opção MIDL
topic_type:
- apiref
api_name:
- /U
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d018d47dd5cbcc8192dee490965bd06c56d0e3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104084185"
---
# <a name="u-switch"></a><span data-ttu-id="d77cf-104">Opção/u</span><span class="sxs-lookup"><span data-stu-id="d77cf-104">/U switch</span></span>

<span data-ttu-id="d77cf-105">A opção **/u** remove qualquer definição anterior de um nome, passando o nome para o pré-processador de C como se fosse uma diretiva **\# undefine** .</span><span class="sxs-lookup"><span data-stu-id="d77cf-105">The **/U** switch removes any previous definition of a name by passing the name to the C preprocessor as if by a **\#undefine** directive.</span></span>

``` syntax
midl /U name
```

## <a name="switch-options"></a><span data-ttu-id="d77cf-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="d77cf-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="d77cf-107">*name*</span><span class="sxs-lookup"><span data-stu-id="d77cf-107">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="d77cf-108">Especifica um nome definido a ser passado para o pré-processador de C como se fosse uma diretiva **\# undefine** .</span><span class="sxs-lookup"><span data-stu-id="d77cf-108">Specifies a defined name to be passed to the C preprocessor as if by a **\#undefine** directive.</span></span> <span data-ttu-id="d77cf-109">O nome é predefinido pelo pré-processador C ou definido anteriormente pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="d77cf-109">The name is predefined by the C preprocessor or previously defined by the user.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d77cf-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d77cf-110">Remarks</span></span>

<span data-ttu-id="d77cf-111">Várias diretivas **/u** podem ser usadas em uma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="d77cf-111">Multiple **/U** directives can be used in a command line.</span></span> <span data-ttu-id="d77cf-112">O espaço em branco entre a opção **/u** e o nome indefinido é opcional.</span><span class="sxs-lookup"><span data-stu-id="d77cf-112">White space between the **/U** switch and the undefined name is optional.</span></span>

<span data-ttu-id="d77cf-113">Quando a [**opção \_ /cpp cmd**](-cpp-cmd.md) está presente e a opção de [**/cpp \_ opt**](-cpp-opt.md) não é, o compilador MIDL concatena a cadeia de caracteres especificada pela \_ opção cmd/cpp com as opções [**/i**](-i.md), [**/d**](-d.md)e **/u** e usa essa cadeia de caracteres concatenada para invocar o pré-processador C para cada arquivo de origem IDL e ACF.</span><span class="sxs-lookup"><span data-stu-id="d77cf-113">When the [**/cpp\_cmd**](-cpp-cmd.md) switch is present and the [**/cpp\_opt**](-cpp-opt.md) switch is not, the MIDL compiler concatenates the string specified by the /cpp\_cmd switch with the [**/I**](-i.md), [**/D**](-d.md), and **/U** options and uses this concatenated string to invoke the C preprocessor for each IDL and ACF source file.</span></span> <span data-ttu-id="d77cf-114">A opção de compilador MIDL **/u** é ignorada quando o parâmetro de compilador MIDL switch **/ \_** **/cpp \_ opt** é especificado.</span><span class="sxs-lookup"><span data-stu-id="d77cf-114">The MIDL compiler switch **/U** is ignored when the MIDL compiler switch **/no\_cpp** or **/cpp\_opt** is specified.</span></span>

## <a name="examples"></a><span data-ttu-id="d77cf-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d77cf-115">Examples</span></span>

<span data-ttu-id="d77cf-116">**MIDL/UUNICODE filename. idl**</span><span class="sxs-lookup"><span data-stu-id="d77cf-116">**midl /UUNICODE filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="d77cf-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="d77cf-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d77cf-118">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="d77cf-118">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="d77cf-119">**/cpp \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="d77cf-119">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="d77cf-120">**/cpp \_ aceitar**</span><span class="sxs-lookup"><span data-stu-id="d77cf-120">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="d77cf-121">**/D**</span><span class="sxs-lookup"><span data-stu-id="d77cf-121">**/D**</span></span>](-d.md)
</dt> <dt>

[<span data-ttu-id="d77cf-122">**/I**</span><span class="sxs-lookup"><span data-stu-id="d77cf-122">**/I**</span></span>](-i.md)
</dt> <dt>

[<span data-ttu-id="d77cf-123">**///// \_ cpp**</span><span class="sxs-lookup"><span data-stu-id="d77cf-123">**/no\_cpp**</span></span>](-no-cpp-nocpp.md)
</dt> </dl>

 

 




