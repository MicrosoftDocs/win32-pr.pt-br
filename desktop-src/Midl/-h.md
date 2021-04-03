---
title: opção/h
description: A opção/h é funcionalmente equivalente à opção/header.
ms.assetid: 1b74d5f2-6624-4b71-832d-fb55a0e84c86
keywords:
- /h alternar MIDL
topic_type:
- apiref
api_name:
- /h
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ff2cd7aa5e4b8386e0c9faecfaccd860207403
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006641"
---
# <a name="h-switch"></a><span data-ttu-id="a6d68-104">opção/h</span><span class="sxs-lookup"><span data-stu-id="a6d68-104">/h switch</span></span>

<span data-ttu-id="a6d68-105">A opção **/h** é funcionalmente equivalente à opção [**/header**](-header.md) .</span><span class="sxs-lookup"><span data-stu-id="a6d68-105">The **/h** option is functionally equivalent to the [**/header**](-header.md) option.</span></span>

``` syntax
midl /h filename
```

## <a name="switch-options"></a><span data-ttu-id="a6d68-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="a6d68-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="a6d68-107">*nome do arquivo*</span><span class="sxs-lookup"><span data-stu-id="a6d68-107">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="a6d68-108">Especifica um nome de arquivo de cabeçalho que substitui o nome do arquivo de cabeçalho padrão.</span><span class="sxs-lookup"><span data-stu-id="a6d68-108">Specifies a header file name that overrides the default header file name.</span></span> <span data-ttu-id="a6d68-109">Os nomes de arquivo podem ser explicitamente entre aspas usando aspas duplas (") para impedir que o Shell interprete caracteres especiais.</span><span class="sxs-lookup"><span data-stu-id="a6d68-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6d68-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6d68-110">Remarks</span></span>

<span data-ttu-id="a6d68-111">A opção **/h** especifica *filename* como o nome de um arquivo de cabeçalho que contém todas as definições contidas no arquivo IDL sem a sintaxe IDL.</span><span class="sxs-lookup"><span data-stu-id="a6d68-111">The **/h** switch specifies *filename* as the name for a header file that contains all the definitions contained in the IDL file, without the IDL syntax.</span></span> <span data-ttu-id="a6d68-112">Esse arquivo pode ser usado como um arquivo de cabeçalho C ou C++.</span><span class="sxs-lookup"><span data-stu-id="a6d68-112">This file can be used as a C or C++ header file.</span></span>

## <a name="examples"></a><span data-ttu-id="a6d68-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a6d68-113">Examples</span></span>

<span data-ttu-id="a6d68-114">**MIDL/h tlibhead. h filename. idl**</span><span class="sxs-lookup"><span data-stu-id="a6d68-114">**midl /h tlibhead.h filename.idl**</span></span>

<span data-ttu-id="a6d68-115">**MIDL/h "MIDL. h" filename. idl**</span><span class="sxs-lookup"><span data-stu-id="a6d68-115">**midl /h "midl.h" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="a6d68-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6d68-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6d68-117">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="a6d68-117">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="a6d68-118">**/header**</span><span class="sxs-lookup"><span data-stu-id="a6d68-118">**/header**</span></span>](-header.md)
</dt> </dl>

 

 




