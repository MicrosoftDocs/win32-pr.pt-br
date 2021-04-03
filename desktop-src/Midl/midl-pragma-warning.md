---
title: midl_pragma atributo de aviso
description: Use a opção de aviso de pragma de MIDL \_ para substituir temporariamente o comportamento de mensagem de aviso do MIDL no momento da compilação.
ms.assetid: d32a3d3f-5c4d-4f93-a72a-2224ceed0012
keywords:
- midl_pragma o atributo de aviso MIDL
topic_type:
- apiref
api_name:
- midl_pragma warning
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b7e1e2c2a1d818216245e45a9129018a3ba2e1c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823172"
---
# <a name="midl_pragma-warning-attribute"></a><span data-ttu-id="05e88-104">atributo de aviso de pragma de MIDL \_</span><span class="sxs-lookup"><span data-stu-id="05e88-104">midl\_pragma warning attribute</span></span>

<span data-ttu-id="05e88-105">Use a opção de **\_ aviso de pragma de MIDL** para substituir temporariamente o comportamento de mensagem de aviso do MIDL no momento da compilação.</span><span class="sxs-lookup"><span data-stu-id="05e88-105">Use the **midl\_pragma warning** option to temporarily override MIDL's warning message behavior at compile time.</span></span>

``` syntax
midl_pragma warning ( warning_option : message_list )
```

## <a name="parameters"></a><span data-ttu-id="05e88-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05e88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05e88-107">*opção de aviso \_*</span><span class="sxs-lookup"><span data-stu-id="05e88-107">*warning\_option*</span></span> 
</dt> <dd>

<span data-ttu-id="05e88-108">A opção de aviso pode ser uma das seguintes opções: desabilitar, habilitar, padrão.</span><span class="sxs-lookup"><span data-stu-id="05e88-108">The warning option can be one of the following: disable, enable, default.</span></span>

</dd> <dt>

<span data-ttu-id="05e88-109">*lista de mensagens \_*</span><span class="sxs-lookup"><span data-stu-id="05e88-109">*message\_list*</span></span> 
</dt> <dd>

<span data-ttu-id="05e88-110">Uma lista de números de mensagem separados por espaços.</span><span class="sxs-lookup"><span data-stu-id="05e88-110">A list of message numbers separated by spaces.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="05e88-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="05e88-111">Remarks</span></span>

<span data-ttu-id="05e88-112">O pragma pode ser usado como um pragma do C-Compiler.</span><span class="sxs-lookup"><span data-stu-id="05e88-112">The pragma can be used like a C-compiler pragma.</span></span> <span data-ttu-id="05e88-113">Ou seja, ele desabilita, habilita ou retorna para o comportamento padrão de um determinado aviso de MIDL.</span><span class="sxs-lookup"><span data-stu-id="05e88-113">That is, it disables, enables, or returns to the default behavior for a given MIDL warning.</span></span>

## <a name="examples"></a><span data-ttu-id="05e88-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="05e88-114">Examples</span></span>

``` syntax
#if (__midl >= 501)
midl_pragma warning( disable: 2007 )   // file already imported midl_pragma warning( disable: 2209 )   // ignored redundant attr
#endif
```

## <a name="see-also"></a><span data-ttu-id="05e88-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="05e88-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05e88-116">**pragma**</span><span class="sxs-lookup"><span data-stu-id="05e88-116">**pragma**</span></span>](pragma.md)
</dt> </dl>

 

 




