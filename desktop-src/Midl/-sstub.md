---
title: comutador/sstub
description: A opção/sstub especifica o nome do arquivo stub do servidor para uma interface RPC.
ms.assetid: 8e695e81-7c1b-40c0-aeaa-5390512fa099
keywords:
- MIDL do comutador/sstub
topic_type:
- apiref
api_name:
- /sstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 131be3dd1890967f7107bea64c3dc2634833653d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105766250"
---
# <a name="sstub-switch"></a><span data-ttu-id="73991-104">comutador/sstub</span><span class="sxs-lookup"><span data-stu-id="73991-104">/sstub switch</span></span>

<span data-ttu-id="73991-105">A opção **/sstub** especifica o nome do arquivo stub do servidor para uma interface RPC.</span><span class="sxs-lookup"><span data-stu-id="73991-105">The **/sstub** switch specifies the name of the server stub file for an RPC interface.</span></span>

``` syntax
midl /sstub stub_file_name
```

## <a name="switch-options"></a><span data-ttu-id="73991-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="73991-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="73991-107">*\_nome do arquivo stub \_*</span><span class="sxs-lookup"><span data-stu-id="73991-107">*stub\_file\_name*</span></span> 
</dt> <dd>

<span data-ttu-id="73991-108">Especifica um nome de arquivo que substitui o nome de arquivo stub do servidor padrão.</span><span class="sxs-lookup"><span data-stu-id="73991-108">Specifies a file name that overrides the default server stub file name.</span></span> <span data-ttu-id="73991-109">Os nomes de arquivo podem ser explicitamente entre aspas usando aspas duplas (") para impedir que o Shell interprete os caracteres especiais.</span><span class="sxs-lookup"><span data-stu-id="73991-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting the special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73991-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="73991-110">Remarks</span></span>

<span data-ttu-id="73991-111">O nome de arquivo especificado substitui o nome de arquivo padrão.</span><span class="sxs-lookup"><span data-stu-id="73991-111">The specified file name replaces the default file name.</span></span> <span data-ttu-id="73991-112">Por padrão, o nome do arquivo é obtido adicionando \_ S. C ao nome do arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="73991-112">By default, the file name is obtained by adding \_S.C to the name of the IDL file.</span></span> <span data-ttu-id="73991-113">Essa opção não afeta as interfaces OLE.</span><span class="sxs-lookup"><span data-stu-id="73991-113">This switch does not affect OLE interfaces.</span></span>

<span data-ttu-id="73991-114">Quando você estiver importando arquivos, o nome de arquivo especificado se aplicará a apenas um arquivo stub — o arquivo stub que corresponde ao arquivo IDL especificado na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="73991-114">When you are importing files, the specified file name applies to only one stub file — the stub file that corresponds to the IDL file specified on the command line.</span></span>

<span data-ttu-id="73991-115">Se *o \_ \_ nome do arquivo stub* não incluir um caminho explícito, o arquivo será gravado no diretório atual ou no diretório especificado pela opção [**/out**](-out.md) .</span><span class="sxs-lookup"><span data-stu-id="73991-115">If *stub\_file\_name* does not include an explicit path, the file is written to the current directory or the directory specified by the [**/out**](-out.md) switch.</span></span> <span data-ttu-id="73991-116">Um caminho explícito no *\_ \_ nome do arquivo de stub* substitui a especificação de opção **/out** .</span><span class="sxs-lookup"><span data-stu-id="73991-116">An explicit path in *stub\_file\_name* overrides the **/out** switch specification.</span></span>

<span data-ttu-id="73991-117">A opção **/Server** None tem precedência sobre a opção **/sstub**</span><span class="sxs-lookup"><span data-stu-id="73991-117">The **/server** none switch takes precedence over the **/sstub** switch.</span></span>

## <a name="examples"></a><span data-ttu-id="73991-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="73991-118">Examples</span></span>

<span data-ttu-id="73991-119">**MIDL/sstub My \_ sstub. c filename. idl**</span><span class="sxs-lookup"><span data-stu-id="73991-119">**midl /sstub my\_sstub.c filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="73991-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="73991-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73991-121">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="73991-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="73991-122">**/cstub**</span><span class="sxs-lookup"><span data-stu-id="73991-122">**/cstub**</span></span>](-cstub.md)
</dt> <dt>

[<span data-ttu-id="73991-123">**/header**</span><span class="sxs-lookup"><span data-stu-id="73991-123">**/header**</span></span>](-header.md)
</dt> <dt>

[<span data-ttu-id="73991-124">**/out**</span><span class="sxs-lookup"><span data-stu-id="73991-124">**/out**</span></span>](-out.md)
</dt> </dl>

 

 




