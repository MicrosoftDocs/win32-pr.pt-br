---
title: comutador/align
description: O comutador/align é funcionalmente o mesmo que a opção MIDL/ZP e é reconhecido pelo compilador MIDL exclusivamente para compatibilidade com versões anteriores com MkTypLib.
ms.assetid: 7f303c49-a6b5-4e3c-95e5-5c49e338c766
keywords:
- MIDL do comutador/align
topic_type:
- apiref
api_name:
- /align
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 019a06be10a4937127d98d508275b57dfe508399
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104498893"
---
# <a name="align-switch"></a><span data-ttu-id="1bfc5-104">comutador/align</span><span class="sxs-lookup"><span data-stu-id="1bfc5-104">/align switch</span></span>

<span data-ttu-id="1bfc5-105">O comutador **/align** é funcionalmente o mesmo que a opção MIDL [**/ZP**](-zp.md) e é reconhecido pelo compilador MIDL exclusivamente para compatibilidade com versões anteriores com MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="1bfc5-105">The **/align** switch is functionally the same as the MIDL [**/Zp**](-zp.md) option and is recognized by the MIDL compiler solely for backward compatibility with MkTypLib.</span></span>

> [!Note]  
> <span data-ttu-id="1bfc5-106">A ferramenta de Mktyplib.exe está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="1bfc5-106">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="1bfc5-107">Em vez disso, use o compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="1bfc5-107">Use the MIDL compiler instead.</span></span>

 

``` syntax
midl /align:alignment
```

## <a name="switch-options"></a><span data-ttu-id="1bfc5-108">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="1bfc5-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="1bfc5-109">*sintonia*</span><span class="sxs-lookup"><span data-stu-id="1bfc5-109">*alignment*</span></span> 
</dt> <dd>

<span data-ttu-id="1bfc5-110">Especifica o alinhamento dos tipos na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="1bfc5-110">Specifies the alignment for types in the library.</span></span> <span data-ttu-id="1bfc5-111">O valor de *alinhamento* pode ser 1, 2, 4 ou 8.</span><span class="sxs-lookup"><span data-stu-id="1bfc5-111">The *alignment* value can be 1, 2, 4, or 8.</span></span> <span data-ttu-id="1bfc5-112">O valor 1 indica o alinhamento natural; *n* indica alinhamento no byte *n*.</span><span class="sxs-lookup"><span data-stu-id="1bfc5-112">The value 1 indicates natural alignment; *n* indicates alignment on byte *n*.</span></span> <span data-ttu-id="1bfc5-113">Quando você não especificar a opção **/align** , o padrão será 8.</span><span class="sxs-lookup"><span data-stu-id="1bfc5-113">When you do not specify the **/align** switch, the default is 8.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1bfc5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1bfc5-114">Remarks</span></span>

<span data-ttu-id="1bfc5-115">Se você estiver gerando um novo makefile, use a opção [**/ZP**](-zp.md) .</span><span class="sxs-lookup"><span data-stu-id="1bfc5-115">If you are generating a new makefile, use the [**/Zp**](-zp.md) switch.</span></span>

<span data-ttu-id="1bfc5-116">O valor de alinhamento corresponde ao valor da opção [**/ZP**](-zp.md) usado pelo compilador C/C++ da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1bfc5-116">The alignment value corresponds to the [**/Zp**](-zp.md) option value used by the Microsoft C/C++ compiler.</span></span> <span data-ttu-id="1bfc5-117">Certifique-se de especificar o mesmo alinhamento ao invocar o compilador C como quando você invoca o compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="1bfc5-117">Be sure that you specify the same alignment when you invoke the C compiler as when you invoke the MIDL compiler.</span></span>

<span data-ttu-id="1bfc5-118">Para obter mais informações, consulte a documentação de programação do Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="1bfc5-118">For more information, see your Microsoft C/C++ programming documentation.</span></span> <span data-ttu-id="1bfc5-119">Para obter uma discussão sobre os perigos potenciais no uso de níveis de embalagem não padrão, consulte o tópico da ajuda do [**/ZP**](-zp.md) .</span><span class="sxs-lookup"><span data-stu-id="1bfc5-119">For a discussion of the potential dangers in using nonstandard packing levels, see the [**/Zp**](-zp.md) help topic.</span></span>

## <a name="examples"></a><span data-ttu-id="1bfc5-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1bfc5-120">Examples</span></span>

<span data-ttu-id="1bfc5-121">**MIDL/align: 4 nome de arquivo. idl**</span><span class="sxs-lookup"><span data-stu-id="1bfc5-121">**midl /align:4 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="1bfc5-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="1bfc5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bfc5-123">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="1bfc5-123">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="1bfc5-124">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="1bfc5-124">**/Zp**</span></span>](-zp.md)
</dt> </dl>

 

 




