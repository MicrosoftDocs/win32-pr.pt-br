---
title: opção/c_ext
description: Essa opção é obsoleta a partir da versão 3,0 do compilador MIDL. No entanto, usar a \_ opção c ext não gerará um erro do compilador, portanto, você não precisa remover referências a/MS \_ ext ou/c \_ ext de um makefile existente.
ms.assetid: 3d4072ba-5563-4014-a4ed-2e3aa26bb00a
keywords:
- /c_ext MIDL do comutador
topic_type:
- apiref
api_name:
- /c_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8b3f179c2ce56b8e8ab6802b2d4bf5dd96c458e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105782795"
---
# <a name="c_ext-switch"></a><span data-ttu-id="30f4d-105">\_opção/c ext</span><span class="sxs-lookup"><span data-stu-id="30f4d-105">/c\_ext switch</span></span>

<span data-ttu-id="30f4d-106">Essa opção é obsoleta a partir da versão 3,0 do compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="30f4d-106">This switch is obsolete as of version 3.0 of the MIDL compiler.</span></span> <span data-ttu-id="30f4d-107">No entanto, usar a opção **c \_ ext** não gerará um erro do compilador, portanto, você não precisa remover referências a [**/MS \_ ext**](-ms-ext.md) ou **/c \_ ext** de um makefile existente.</span><span class="sxs-lookup"><span data-stu-id="30f4d-107">However, using the **c\_ext** switch will not generate a compiler error, so you do not have to remove references to [**/ms\_ext**](-ms-ext.md) or **/c\_ext** from an existing makefile.</span></span>

``` syntax
midl /c_ext
```

## <a name="switch-options"></a><span data-ttu-id="30f4d-108">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="30f4d-108">Switch Options</span></span>

<span data-ttu-id="30f4d-109">Essa opção não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="30f4d-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="30f4d-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="30f4d-110">Remarks</span></span>

<span data-ttu-id="30f4d-111">Os recursos a seguir agora estão disponíveis por padrão:</span><span class="sxs-lookup"><span data-stu-id="30f4d-111">The following features are now available by default:</span></span>

-   <span data-ttu-id="30f4d-112">Muitos arquivos de cabeçalho existentes definem tipos com qualificadores, como **far** e **stdcall**, que não fazem parte da IDL de DCE.</span><span class="sxs-lookup"><span data-stu-id="30f4d-112">Many existing header files define types with qualifiers, such as **far** and **stdcall**, that are not part of the DCE IDL.</span></span> <span data-ttu-id="30f4d-113">Esses compiladores (e o compilador MIDL no modo de compatibilidade do DCE) geram erros quando tentam processar esses qualificadores.</span><span class="sxs-lookup"><span data-stu-id="30f4d-113">Those compilers (and the MIDL compiler in DCE-compatibility mode) generate errors when they attempt to process these qualifiers.</span></span> <span data-ttu-id="30f4d-114">O compilador MIDL permite que você compile arquivos IDL que contenham esses qualificadores.</span><span class="sxs-lookup"><span data-stu-id="30f4d-114">The MIDL compiler allows you to compile IDL files that contain these qualifiers.</span></span> <span data-ttu-id="30f4d-115">Os qualificadores de tipo não afetam a maneira como os dados são transmitidos na rede.</span><span class="sxs-lookup"><span data-stu-id="30f4d-115">The type qualifiers do not affect the way the data is transmitted on the network.</span></span>
-   <span data-ttu-id="30f4d-116">Você pode omitir atributos direcionais como [**\[ in \]**](in.md) ou [**\[ out \]**](out-idl.md).</span><span class="sxs-lookup"><span data-stu-id="30f4d-116">You can omit directional attributes such as [**\[in\]**](in.md) or [**\[out\]**](out-idl.md).</span></span>

<span data-ttu-id="30f4d-117">As seguintes extensões C-Language têm suporte no modo padrão:</span><span class="sxs-lookup"><span data-stu-id="30f4d-117">The following C-language extensions are supported in default mode:</span></span>

-   <span data-ttu-id="30f4d-118">Campos de bits em estruturas e uniões</span><span class="sxs-lookup"><span data-stu-id="30f4d-118">Bit fields in structures and unions</span></span>
-   <span data-ttu-id="30f4d-119">Comentários que começam com dois caracteres de barra (//)</span><span class="sxs-lookup"><span data-stu-id="30f4d-119">Comments that start with two slash characters (//)</span></span>
-   <span data-ttu-id="30f4d-120">Declarações externas</span><span class="sxs-lookup"><span data-stu-id="30f4d-120">External declarations</span></span>
-   <span data-ttu-id="30f4d-121">Procedimentos com reticências na lista de parâmetros (...)</span><span class="sxs-lookup"><span data-stu-id="30f4d-121">Procedures with ellipses in the parameter list (…)</span></span>
-   <span data-ttu-id="30f4d-122">Em plataformas de 32 bits, [**int**](int.md) é um tipo de base de 32 bits nativo; em plataformas de 16 bits, **int** é reconhecido, mas não é um tipo remoto</span><span class="sxs-lookup"><span data-stu-id="30f4d-122">On 32-bit platforms, [**int**](int.md) is a native 32-bit base type; on 16-bit platforms, **int** is recognized but is not a remotable type</span></span>
-   <span data-ttu-id="30f4d-123">Tipo [**void \***](void.md) que não é usado em operações remotas</span><span class="sxs-lookup"><span data-stu-id="30f4d-123">Type [**void \***](void.md) that is not used in remote operations</span></span>
-   <span data-ttu-id="30f4d-124">Qualificadores de tipo — incluindo o formulário com o prefixo de conformidade com ANSI — contêm dois caracteres de sublinhado: **cdecl**, **\_ \_ cdecl**, [**const**](const.md), **\_ \_ const**, **Export**, **\_ \_ Export**, **muito** **\_ \_ longe,** **LOADDS**, **\_ \_ LOADDS**, **Near**, **\_ \_ Near**, **Pascal**, **\_ \_ Pascal**, **stdcall**, **\_ \_ stdcall**, **volátil** e **\_ \_ volátil**.</span><span class="sxs-lookup"><span data-stu-id="30f4d-124">Type qualifiers—including the form with the ANSI-conformant prefix—contain two underscore characters: **cdecl**, **\_\_cdecl**, [**const**](const.md), **\_\_const**, **export**, **\_\_export**, **far**, **\_\_far**, **loadds**, **\_\_loadds**, **near**, **\_\_near**, **pascal**, **\_\_pascal**, **stdcall**, **\_\_stdcall**, **volatile**, and **\_\_volatile**.</span></span>

<span data-ttu-id="30f4d-125">Para obter mais informações sobre qualificadores de declaração, consulte a documentação do Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="30f4d-125">For more information about declaration qualifiers, see your Microsoft C/C++ documentation.</span></span>

## <a name="see-also"></a><span data-ttu-id="30f4d-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="30f4d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30f4d-127">**configuração do/App \_**</span><span class="sxs-lookup"><span data-stu-id="30f4d-127">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="30f4d-128">**/osf**</span><span class="sxs-lookup"><span data-stu-id="30f4d-128">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="30f4d-129">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="30f4d-129">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




