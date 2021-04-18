---
title: Opção /out
description: A opção/out especifica o diretório padrão em que o compilador MIDL grava os arquivos de saída.
ms.assetid: 37cfe989-137a-4336-8c66-e6b9c23473df
keywords:
- opção/out de MIDL
topic_type:
- apiref
api_name:
- /out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d688f17957170c6f3a8887030ea2c67140c0ff8c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105760693"
---
# <a name="out-switch"></a><span data-ttu-id="91635-104">Opção /out</span><span class="sxs-lookup"><span data-stu-id="91635-104">/out switch</span></span>

<span data-ttu-id="91635-105">A opção **/out** especifica o diretório padrão em que o compilador MIDL grava os arquivos de saída.</span><span class="sxs-lookup"><span data-stu-id="91635-105">The **/out** switch specifies the default directory where the MIDL compiler writes output files.</span></span>

``` syntax
midl /out path-specification
```

## <a name="switch-options"></a><span data-ttu-id="91635-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="91635-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="91635-107">*especificação de caminho*</span><span class="sxs-lookup"><span data-stu-id="91635-107">*path-specification*</span></span> 
</dt> <dd>

<span data-ttu-id="91635-108">Especifica o caminho para o diretório no qual os arquivos stub, cabeçalho e comutador são gerados.</span><span class="sxs-lookup"><span data-stu-id="91635-108">Specifies the path to the directory in which the stub, header, and switch files are generated.</span></span> <span data-ttu-id="91635-109">Uma especificação de unidade, um caminho de diretório absoluto ou ambos podem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="91635-109">A drive specification, an absolute directory path, or both can be specified.</span></span> <span data-ttu-id="91635-110">Os caminhos podem ser explicitamente entre aspas usando aspas duplas (") para impedir que o Shell interprete os caracteres especiais.</span><span class="sxs-lookup"><span data-stu-id="91635-110">Paths can be explicitly quoted using double quotes (") to prevent the shell from interpreting the special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91635-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="91635-111">Remarks</span></span>

<span data-ttu-id="91635-112">O diretório de saída pode ser especificado com uma letra de unidade, um nome de caminho absoluto ou ambos.</span><span class="sxs-lookup"><span data-stu-id="91635-112">The output directory can be specified with a drive letter, an absolute path name, or both.</span></span> <span data-ttu-id="91635-113">A opção **/out** pode ser usada com qualquer uma das opções que habilitam a especificação de arquivo de saída individual.</span><span class="sxs-lookup"><span data-stu-id="91635-113">The **/out** option can be used with any of the switches that enable individual output file specification.</span></span>

<span data-ttu-id="91635-114">Quando a opção **/out** não é especificada, os arquivos são gravados no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="91635-114">When the **/out** switch is not specified, files are written to the current directory.</span></span>

<span data-ttu-id="91635-115">O diretório padrão especificado pela opção **/out** pode ser substituído por um nome de caminho explícito especificado como parte da opção [**/cstub**](-cstub.md), [**/header**](-header.md), [**/proxy nomedearquivo**](-proxy.md)ou [**/sstub**](-sstub.md) .</span><span class="sxs-lookup"><span data-stu-id="91635-115">The default directory specified by the **/out** switch can be overridden by an explicit path name specified as part of the [**/cstub**](-cstub.md), [**/header**](-header.md), [**/proxy**](-proxy.md), or [**/sstub**](-sstub.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="91635-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="91635-116">Examples</span></span>

<span data-ttu-id="91635-117">**MIDL/out c: \\ mydir \\ mysubdir \\ subdir2 mais profundo nome do arquivo. idl**</span><span class="sxs-lookup"><span data-stu-id="91635-117">**midl /out c:\\mydir\\mysubdir\\subdir2 deeper filename.idl**</span></span>

<span data-ttu-id="91635-118">**MIDL/out c: filename. idl**</span><span class="sxs-lookup"><span data-stu-id="91635-118">**midl /out c: filename.idl**</span></span>

<span data-ttu-id="91635-119">**MIDL/out \\ mydir \\ mysubdir \\ outro nome de arquivo. idl**</span><span class="sxs-lookup"><span data-stu-id="91635-119">**midl /out \\mydir\\mysubdir\\another filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="91635-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="91635-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91635-121">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="91635-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="91635-122">**/cstub**</span><span class="sxs-lookup"><span data-stu-id="91635-122">**/cstub**</span></span>](-cstub.md)
</dt> <dt>

[<span data-ttu-id="91635-123">**/header**</span><span class="sxs-lookup"><span data-stu-id="91635-123">**/header**</span></span>](-header.md)
</dt> <dt>

[<span data-ttu-id="91635-124">**/proxy nomedearquivo**</span><span class="sxs-lookup"><span data-stu-id="91635-124">**/proxy**</span></span>](-proxy.md)
</dt> <dt>

[<span data-ttu-id="91635-125">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="91635-125">**/sstub**</span></span>](-sstub.md)
</dt> </dl>

 

 




