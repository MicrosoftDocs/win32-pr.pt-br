---
title: opção/no_def_idir
description: Quando os diretórios são especificados com a opção/I, a \_ \_ opção de Idir de alteração de mudança instrui o compilador MIDL a pesquisar somente os diretórios especificados com a opção/i.
ms.assetid: 9a396de4-332d-4832-8e8b-291690cd3a10
keywords:
- /no_def_idir MIDL do comutador
topic_type:
- apiref
api_name:
- /no_def_idir
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62ed845c73c36fbbfe4ea7dea952ee4541b043a7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823352"
---
# <a name="no_def_idir-switch"></a><span data-ttu-id="bb2ae-104">\_opção de \_ Idir def de alteração</span><span class="sxs-lookup"><span data-stu-id="bb2ae-104">/no\_def\_idir switch</span></span>

<span data-ttu-id="bb2ae-105">Quando os diretórios são especificados com a opção [**/i**](-i.md) , a opção de **\_ \_ Idir de////** opções de alteração instrui o compilador MIDL a pesquisar somente os diretórios especificados com a opção **/i** , ignorando o diretório atual, bem como os diretórios especificados pela variável de ambiente INCLUDE.</span><span class="sxs-lookup"><span data-stu-id="bb2ae-105">When directories are specified with the [**/I**](-i.md) switch, the **/no\_def\_idir** switch instructs the MIDL compiler to search only the directories specified with the **/I** switch, ignoring the current directory as well as the directories specified by the INCLUDE environment variable.</span></span>

``` syntax
midl /no_def_idir
```

## <a name="switch-options"></a><span data-ttu-id="bb2ae-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="bb2ae-106">Switch Options</span></span>

<span data-ttu-id="bb2ae-107">Essa opção não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="bb2ae-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb2ae-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb2ae-108">Remarks</span></span>

<span data-ttu-id="bb2ae-109">Quando nenhum diretório é especificado com a opção [**/i**](-i.md) , a opção de **\_ \_ Idir de//** chave de alteração instrui o compilador MIDL a pesquisar somente o diretório atual.</span><span class="sxs-lookup"><span data-stu-id="bb2ae-109">When no directories are specified with the [**/I**](-i.md) switch, the **/no\_def\_idir** switch instructs the MIDL compiler to search only the current directory.</span></span>

## <a name="examples"></a><span data-ttu-id="bb2ae-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bb2ae-110">Examples</span></span>

``` syntax
; search only the current directory 
midl /no_def_idir filename.idl  

; search only the specified directories 
midl /no_def_idir /I c:\c700\include filename.idl 
```

## <a name="see-also"></a><span data-ttu-id="bb2ae-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb2ae-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb2ae-112">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="bb2ae-112">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="bb2ae-113">**/acf**</span><span class="sxs-lookup"><span data-stu-id="bb2ae-113">**/acf**</span></span>](-acf.md)
</dt> <dt>

[<span data-ttu-id="bb2ae-114">**/I**</span><span class="sxs-lookup"><span data-stu-id="bb2ae-114">**/I**</span></span>](-i.md)
</dt> </dl>

 

 




