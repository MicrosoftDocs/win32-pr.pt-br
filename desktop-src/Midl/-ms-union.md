---
title: opção/ms_union
description: A \_ opção Union/MS controla o alinhamento de NDR de uniões não encapsuladas. Observe que esse atributo é fornecido para compatibilidade com versões anteriores.
ms.assetid: 683d1498-6419-4600-ad5b-c0b6ea44a8e1
keywords:
- /ms_union MIDL do comutador
topic_type:
- apiref
api_name:
- /ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968618af5c2bb5b32ec14b293225bc09c2997aa5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823334"
---
# <a name="ms_union-switch"></a><span data-ttu-id="6397f-104">\_opção de União/MS</span><span class="sxs-lookup"><span data-stu-id="6397f-104">/ms\_union switch</span></span>

<span data-ttu-id="6397f-105">A **opção \_ Union/MS** controla o alinhamento de NDR de uniões não encapsuladas.</span><span class="sxs-lookup"><span data-stu-id="6397f-105">The **/ms\_union** switch controls the NDR alignment of nonencapsulated unions.</span></span>

> [!Note]  
> <span data-ttu-id="6397f-106">Esse atributo é fornecido para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="6397f-106">This attribute is provided for backwards compatibility.</span></span> <span data-ttu-id="6397f-107">Não é recomendável para uso em uma nova interface.</span><span class="sxs-lookup"><span data-stu-id="6397f-107">It is not recommended for use in a new interface.</span></span>

 

``` syntax
midl /ms_union
```

## <a name="switch-options"></a><span data-ttu-id="6397f-108">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="6397f-108">Switch Options</span></span>

<span data-ttu-id="6397f-109">Essa opção não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6397f-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="6397f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6397f-110">Remarks</span></span>

<span data-ttu-id="6397f-111">O compilador MIDL espelha o comportamento do compilador de IDL uso-DCE para uniões não encapsuladas.</span><span class="sxs-lookup"><span data-stu-id="6397f-111">The MIDL compiler mirrors the behavior of the OSF-DCE IDL compiler for nonencapsulated unions.</span></span> <span data-ttu-id="6397f-112">No entanto, como as versões anteriores do compilador MIDL não faziam isso, a opção **\_ Union/MS** fornece compatibilidade com interfaces criadas em versões anteriores do compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="6397f-112">However, because earlier versions of the MIDL compiler did not do so, the **/ms\_union** switch provides compatibility with interfaces built on previous versions of the MIDL compiler.</span></span>

<span data-ttu-id="6397f-113">O \_ recurso de União MS pode ser usado como uma opção de linha de comando (**/MS \_ Union**), um atributo de interface IDL ou como um atributo de tipo IDL.</span><span class="sxs-lookup"><span data-stu-id="6397f-113">The ms\_union feature can be used as a command-line switch (**/ms\_union**), an IDL interface attribute, or as an IDL-type attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="6397f-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6397f-114">Examples</span></span>

<span data-ttu-id="6397f-115">**arquivo de \_ União MIDL/MS. idl**</span><span class="sxs-lookup"><span data-stu-id="6397f-115">**midl /ms\_union file.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="6397f-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="6397f-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6397f-117">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="6397f-117">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="6397f-118">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="6397f-118">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> </dl>

 

 




