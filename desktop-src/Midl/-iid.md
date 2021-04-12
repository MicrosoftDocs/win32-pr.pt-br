---
title: comutador/IID nomedearquivo
description: A opção/IID nomedearquivo especifica o nome do arquivo de identificador de interface para uma interface COM, substituindo o nome padrão obtido adicionando \_ i. c ao nome do arquivo IDL.
ms.assetid: 051593f5-e612-4b19-94e5-d7885dbede21
keywords:
- MIDL do comutador/IID nomedearquivo
topic_type:
- apiref
api_name:
- /iid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 631a28f1bc5a1a24253c9416104df9941cd8da33
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364946"
---
# <a name="iid-switch"></a><span data-ttu-id="c254b-104">comutador/IID nomedearquivo</span><span class="sxs-lookup"><span data-stu-id="c254b-104">/iid switch</span></span>

<span data-ttu-id="c254b-105">A opção **/IID nomedearquivo** especifica o nome do arquivo de identificador de interface para uma interface com, substituindo o nome padrão obtido adicionando \_ i. c ao nome do arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="c254b-105">The **/iid** switch specifies the name of the interface identifier file for a COM interface, overriding the default name obtained by adding \_i.c to the IDL file name.</span></span>

``` syntax
midl /iid filename
```

## <a name="switch-options"></a><span data-ttu-id="c254b-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="c254b-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="c254b-107">*nome do arquivo*</span><span class="sxs-lookup"><span data-stu-id="c254b-107">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="c254b-108">Especifica um nome de arquivo de identificador de interface que substitui o nome de arquivo do identificador de interface padrão para uma interface COM.</span><span class="sxs-lookup"><span data-stu-id="c254b-108">Specifies an interface identifier file name that overrides the default interface identifier file name for a COM interface.</span></span> <span data-ttu-id="c254b-109">Os nomes de arquivo podem ser explicitamente entre aspas usando aspas duplas (") para impedir que o Shell interprete os caracteres especiais.</span><span class="sxs-lookup"><span data-stu-id="c254b-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting the special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c254b-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="c254b-110">Remarks</span></span>

<span data-ttu-id="c254b-111">A opção **/IID nomedearquivo** não afeta as interfaces RPC.</span><span class="sxs-lookup"><span data-stu-id="c254b-111">The **/iid** switch does not affect RPC interfaces.</span></span>

<span data-ttu-id="c254b-112">Se o *nome* do arquivo não incluir um caminho explícito, o arquivo será gravado no diretório atual ou no diretório especificado pela opção [**/out**](-out.md) .</span><span class="sxs-lookup"><span data-stu-id="c254b-112">If *filename* does not include an explicit path, the file is written to the current directory or to the directory specified by the [**/out**](-out.md) switch.</span></span> <span data-ttu-id="c254b-113">Um caminho explícito em *filename* substitui a especificação de opção **/out** .</span><span class="sxs-lookup"><span data-stu-id="c254b-113">An explicit path in *filename* overrides the **/out** switch specification.</span></span>

## <a name="examples"></a><span data-ttu-id="c254b-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c254b-114">Examples</span></span>

<span data-ttu-id="c254b-115">**MIDL/IID nomedearquivo "meu \_ IID. c" filename. idl**</span><span class="sxs-lookup"><span data-stu-id="c254b-115">**midl /iid "my\_iid.c" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="c254b-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="c254b-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c254b-117">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="c254b-117">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="c254b-118">**/header**</span><span class="sxs-lookup"><span data-stu-id="c254b-118">**/header**</span></span>](-header.md)
</dt> <dt>

[<span data-ttu-id="c254b-119">**/out**</span><span class="sxs-lookup"><span data-stu-id="c254b-119">**/out**</span></span>](-out.md)
</dt> <dt>

[<span data-ttu-id="c254b-120">**/proxy nomedearquivo**</span><span class="sxs-lookup"><span data-stu-id="c254b-120">**/proxy**</span></span>](-proxy.md)
</dt> </dl>

 

 




