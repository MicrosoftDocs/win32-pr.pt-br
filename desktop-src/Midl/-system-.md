---
title: /comutador do sistema
description: O comutador/sistema direciona o compilador MIDL para gerar uma biblioteca de tipos para o sistema especificado. O padrão é o sistema operacional atual.
ms.assetid: 0fb69ffc-5ab4-49f3-b34d-859da776ce9e
keywords:
- /comutador do sistema MIDL
topic_type:
- apiref
api_name:
- / system
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e09f2cf97f8edb86ad831cff35420fad9a07d76
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293231"
---
# <a name="system-switch"></a><span data-ttu-id="291a7-105">/<system> comutador</span><span class="sxs-lookup"><span data-stu-id="291a7-105">/<system> switch</span></span>

<span data-ttu-id="291a7-106">A **/<system>** opção direciona o compilador MIDL para gerar uma biblioteca de tipos para o sistema especificado.</span><span class="sxs-lookup"><span data-stu-id="291a7-106">The **/<system>** switch directs the MIDL compiler to generate a type library for the specified system.</span></span> <span data-ttu-id="291a7-107">O padrão é o sistema operacional atual.</span><span class="sxs-lookup"><span data-stu-id="291a7-107">The default is the current operating system.</span></span>

``` syntax
midl /{win32 | ia64 | amd64}
```

## <a name="switch-options"></a><span data-ttu-id="291a7-108">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="291a7-108">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span data-ttu-id="291a7-109"><span id="win32"></span><span id="WIN32"></span>Win32 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="291a7-109"><span id="win32"></span><span id="WIN32"></span>\*\*\*\*win32\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="291a7-110">Windows 2000, Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="291a7-110">Windows 2000, Windows XP, Windows Vista, Windows 7</span></span>

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span data-ttu-id="291a7-111"><span id="ia64"></span><span id="IA64"></span>IA64 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="291a7-111"><span id="ia64"></span><span id="IA64"></span>\*\*\*\*ia64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="291a7-112">Um ambiente Windows de 64 bits baseado em Intel, como o Windows 2000, o Windows Server 2003, o Windows XP Professional x64 Edition, o Windows Vista ou o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="291a7-112">An Intel-based 64-bit Windows environment such as Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista, or Windows 7.</span></span>

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span data-ttu-id="291a7-113"><span id="amd64"></span><span id="AMD64"></span>AMD64 \* \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="291a7-113"><span id="amd64"></span><span id="AMD64"></span>\*\*\*\*amd64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="291a7-114">Um ambiente do Windows de 64 bits com base em dispositivos American micro, como o Windows 2000, o Windows Server 2003, o Windows XP Professional x64 Edition, o Windows Vista ou o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="291a7-114">An American Micro Devices-based 64-bit Windows environment such as Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista, or Windows 7.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="291a7-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="291a7-115">Remarks</span></span>

<span data-ttu-id="291a7-116">O **/<system>** switch é funcionalmente o mesmo que a opção MIDL [**/env**](-env.md) e é reconhecido pelo compilador MIDL exclusivamente para compatibilidade com versões anteriores com MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="291a7-116">The **/<system>** switch is functionally the same as the MIDL [**/env**](-env.md) option and is recognized by the MIDL compiler solely for backward compatibility with MkTypLib.</span></span> <span data-ttu-id="291a7-117">Se você estiver gerando um novo makefile, use a opção **/env** .</span><span class="sxs-lookup"><span data-stu-id="291a7-117">If you are generating a new makefile, use the **/env** switch.</span></span>

## <a name="examples"></a><span data-ttu-id="291a7-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="291a7-118">Examples</span></span>

<span data-ttu-id="291a7-119">**MIDL/Win32 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="291a7-119">**midl /win32 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="291a7-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="291a7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="291a7-121">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="291a7-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="291a7-122">**/env**</span><span class="sxs-lookup"><span data-stu-id="291a7-122">**/env**</span></span>](-env.md)
</dt> </dl>

 

 




