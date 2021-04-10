---
title: comutador/cstub
description: A opção/cstub especifica o nome do arquivo stub do cliente para uma interface RPC.
ms.assetid: f2c9e083-3511-4e72-b1d1-14a3a662ffaf
keywords:
- MIDL do comutador/cstub
topic_type:
- apiref
api_name:
- /cstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 878f6eee47deaac3887c3f9936c18b0185cc807a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293332"
---
# <a name="cstub-switch"></a><span data-ttu-id="468c0-104">comutador/cstub</span><span class="sxs-lookup"><span data-stu-id="468c0-104">/cstub switch</span></span>

<span data-ttu-id="468c0-105">A opção **/cstub** especifica o nome do arquivo stub do cliente para uma interface RPC.</span><span class="sxs-lookup"><span data-stu-id="468c0-105">The **/cstub** switch specifies the name of the client stub file for an RPC interface.</span></span>

``` syntax
midl /cstub stub_file_name
```

## <a name="switch-options"></a><span data-ttu-id="468c0-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="468c0-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="468c0-107">*\_nome do arquivo stub \_*</span><span class="sxs-lookup"><span data-stu-id="468c0-107">*stub\_file\_name*</span></span> 
</dt> <dd>

<span data-ttu-id="468c0-108">Especifica um nome de arquivo que substitui o nome de arquivo stub do cliente padrão.</span><span class="sxs-lookup"><span data-stu-id="468c0-108">Specifies a file name that overrides the default client stub file name.</span></span> <span data-ttu-id="468c0-109">Os nomes de arquivo podem ser explicitamente entre aspas usando aspas duplas (") para impedir que o Shell interprete os caracteres especiais.</span><span class="sxs-lookup"><span data-stu-id="468c0-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting the special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="468c0-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="468c0-110">Remarks</span></span>

<span data-ttu-id="468c0-111">O nome de arquivo especificado substitui o nome de arquivo padrão.</span><span class="sxs-lookup"><span data-stu-id="468c0-111">The specified file name replaces the default file name.</span></span> <span data-ttu-id="468c0-112">Por padrão, o nome do arquivo é obtido adicionando a extensão \_ c. c ao nome do arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="468c0-112">By default, the file name is obtained by adding the extension \_c.c to the name of the IDL file.</span></span> <span data-ttu-id="468c0-113">Essa opção não afeta as interfaces OLE.</span><span class="sxs-lookup"><span data-stu-id="468c0-113">This switch does not affect OLE interfaces.</span></span>

<span data-ttu-id="468c0-114">Quando você estiver importando arquivos, o nome de arquivo especificado se aplicará a apenas um arquivo stub — o arquivo stub que corresponde ao arquivo IDL especificado na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="468c0-114">When you are importing files, the specified file name applies to only one stub file — the stub file that corresponds to the IDL file specified on the command line.</span></span>

<span data-ttu-id="468c0-115">Se *o \_ \_ nome do arquivo stub* não incluir um caminho explícito, o arquivo será gravado no diretório atual ou no diretório especificado pela opção [**/out**](-out.md) .</span><span class="sxs-lookup"><span data-stu-id="468c0-115">If *stub\_file\_name* does not include an explicit path, the file is written to the current directory or the directory specified by the [**/out**](-out.md) switch.</span></span> <span data-ttu-id="468c0-116">Um caminho explícito no *\_ \_ nome do arquivo de stub* substitui a especificação de opção **/out** .</span><span class="sxs-lookup"><span data-stu-id="468c0-116">An explicit path in *stub\_file\_name* overrides the **/out** switch specification.</span></span>

<span data-ttu-id="468c0-117">A opção **/Client** None tem precedência sobre a opção **/cstub**</span><span class="sxs-lookup"><span data-stu-id="468c0-117">The **/client** none switch takes precedence over the **/cstub** switch.</span></span>

## <a name="examples"></a><span data-ttu-id="468c0-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="468c0-118">Examples</span></span>

<span data-ttu-id="468c0-119">**MIDL/cstub My \_ cstub. c filename. idl**</span><span class="sxs-lookup"><span data-stu-id="468c0-119">**midl /cstub my\_cstub.c filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="468c0-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="468c0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="468c0-121">**/header**</span><span class="sxs-lookup"><span data-stu-id="468c0-121">**/header**</span></span>](-header.md)
</dt> <dt>

[<span data-ttu-id="468c0-122">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="468c0-122">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="468c0-123">**/out**</span><span class="sxs-lookup"><span data-stu-id="468c0-123">**/out**</span></span>](-out.md)
</dt> <dt>

[<span data-ttu-id="468c0-124">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="468c0-124">**/sstub**</span></span>](-sstub.md)
</dt> </dl>

 

 




