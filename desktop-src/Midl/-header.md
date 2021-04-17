---
title: comutador/header
description: A opção/header especifica o nome do arquivo de cabeçalho.
ms.assetid: d36cb6c9-df57-4ef4-aff3-9968ac8ac001
keywords:
- MIDL do comutador/header
topic_type:
- apiref
api_name:
- /header
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816310f0b584f3c30d351e0d036e1f18c2f23962
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364948"
---
# <a name="header-switch"></a><span data-ttu-id="105bb-104">comutador/header</span><span class="sxs-lookup"><span data-stu-id="105bb-104">/header switch</span></span>

<span data-ttu-id="105bb-105">A opção **/header** especifica o nome do arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="105bb-105">The **/header** switch specifies the name of the header file.</span></span>

``` syntax
midl /header filename
```

## <a name="switch-options"></a><span data-ttu-id="105bb-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="105bb-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="105bb-107">*nome do arquivo*</span><span class="sxs-lookup"><span data-stu-id="105bb-107">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="105bb-108">Especifica um nome de arquivo de cabeçalho que substitui o nome do arquivo de cabeçalho padrão.</span><span class="sxs-lookup"><span data-stu-id="105bb-108">Specifies a header file name that overrides the default header file name.</span></span> <span data-ttu-id="105bb-109">Os nomes de arquivo podem ser explicitamente entre aspas usando aspas duplas (") para impedir que o Shell interprete caracteres especiais.</span><span class="sxs-lookup"><span data-stu-id="105bb-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="105bb-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="105bb-110">Remarks</span></span>

<span data-ttu-id="105bb-111">O nome de arquivo especificado substitui o nome de arquivo padrão.</span><span class="sxs-lookup"><span data-stu-id="105bb-111">The specified file name replaces the default file name.</span></span> <span data-ttu-id="105bb-112">O nome de arquivo padrão é obtido substituindo a extensão de nome de arquivo IDL (normalmente. idl) pela extensão de nome de arquivo. h.</span><span class="sxs-lookup"><span data-stu-id="105bb-112">The default file name is obtained by replacing the IDL file name extension (usually .idl) with the file name extension .h.</span></span> <span data-ttu-id="105bb-113">Para interfaces OLE, a opção **/header** substitui o nome padrão do arquivo de cabeçalho da interface.</span><span class="sxs-lookup"><span data-stu-id="105bb-113">For OLE interfaces, the **/header** switch overrides the default name of the interface header file.</span></span>

<span data-ttu-id="105bb-114">Quando você estiver importando arquivos, o nome de arquivo especificado se aplicará a apenas um arquivo de cabeçalho — o arquivo de cabeçalho que corresponde ao arquivo IDL especificado na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="105bb-114">When you are importing files, the specified file name applies to only one header file — the header file that corresponds to the IDL file specified on the command line.</span></span>

<span data-ttu-id="105bb-115">Se o *nome* do arquivo não incluir um caminho explícito, o arquivo será gravado no diretório atual ou no diretório especificado pela opção [**/out**](-out.md) .</span><span class="sxs-lookup"><span data-stu-id="105bb-115">If *filename* does not include an explicit path, the file is written to the current directory or the directory specified by the [**/out**](-out.md) switch.</span></span> <span data-ttu-id="105bb-116">Um caminho explícito em *filename* substitui a especificação de opção **/out** .</span><span class="sxs-lookup"><span data-stu-id="105bb-116">An explicit path in *filename* overrides the **/out** switch specification.</span></span>

## <a name="examples"></a><span data-ttu-id="105bb-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="105bb-117">Examples</span></span>

<span data-ttu-id="105bb-118">**MIDL/Header "bar. h" filename. idl**</span><span class="sxs-lookup"><span data-stu-id="105bb-118">**midl /header "bar.h" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="105bb-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="105bb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="105bb-120">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="105bb-120">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="105bb-121">**/h**</span><span class="sxs-lookup"><span data-stu-id="105bb-121">**/h**</span></span>](-h.md)
</dt> <dt>

[<span data-ttu-id="105bb-122">**/cstub**</span><span class="sxs-lookup"><span data-stu-id="105bb-122">**/cstub**</span></span>](-cstub.md)
</dt> <dt>

[<span data-ttu-id="105bb-123">**/out**</span><span class="sxs-lookup"><span data-stu-id="105bb-123">**/out**</span></span>](-out.md)
</dt> <dt>

[<span data-ttu-id="105bb-124">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="105bb-124">**/sstub**</span></span>](-sstub.md)
</dt> <dt>

[<span data-ttu-id="105bb-125">**/proxy nomedearquivo**</span><span class="sxs-lookup"><span data-stu-id="105bb-125">**/proxy**</span></span>](-proxy.md)
</dt> </dl>

 

 




