---
title: RPC_STATUS (rpcdce. h)
description: O status de RPC do tipo de dados \_ representa um tipo de código de status específico da plataforma.
ms.assetid: 0f929916-f3aa-477f-9c61-742f3fbbab29
keywords:
- RPC_STATUS
- RPC_STATUS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 066022ce33676caadcf25a6814f3b4974701998e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009334"
---
# <a name="rpc_status"></a><span data-ttu-id="c9e5a-105">STATUS do RPC \_</span><span class="sxs-lookup"><span data-stu-id="c9e5a-105">RPC\_STATUS</span></span>

<span data-ttu-id="c9e5a-106">O status de **RPC \_** do tipo de dados representa um tipo de código de status específico da plataforma.</span><span class="sxs-lookup"><span data-stu-id="c9e5a-106">The data type **RPC\_STATUS** represents a platform-specific status code type.</span></span>


```C++
typedef long RPC_STATUS;
typedef unsigned short RPC_STATUS;
```



## <a name="remarks"></a><span data-ttu-id="c9e5a-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9e5a-107">Remarks</span></span>

<span data-ttu-id="c9e5a-108">O tipo de **\_ status RPC** é retornado pela maioria das funções RPC e faz parte da definição do tipo de função do [**\_ objeto RPC \_ INQ \_ FN**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn) .</span><span class="sxs-lookup"><span data-stu-id="c9e5a-108">The **RPC\_STATUS** type is returned by most RPC functions and is part of the [**RPC\_OBJECT\_INQ\_FN**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn) function type definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9e5a-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9e5a-109">Requirements</span></span>



| <span data-ttu-id="c9e5a-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9e5a-110">Requirement</span></span> | <span data-ttu-id="c9e5a-111">Valor</span><span class="sxs-lookup"><span data-stu-id="c9e5a-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9e5a-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9e5a-112">Minimum supported client</span></span><br/> | <span data-ttu-id="c9e5a-113">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c9e5a-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c9e5a-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9e5a-114">Minimum supported server</span></span><br/> | <span data-ttu-id="c9e5a-115">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c9e5a-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c9e5a-116">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c9e5a-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9e5a-117"><dt>Rpcdce. h (incluir RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9e5a-117"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9e5a-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9e5a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9e5a-119">**\_objeto RPC \_ INQ \_ FN**</span><span class="sxs-lookup"><span data-stu-id="c9e5a-119">**RPC\_OBJECT\_INQ\_FN**</span></span>](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn)
</dt> </dl>

 

 





