---
title: RpcTryExcept (RPC. h)
description: A instrução RpcTryExcept fornece manipulação de exceção estruturada para aplicativos RPC.
ms.assetid: 3addb367-4bdc-4c11-bf4d-b5b94da45b26
keywords:
- RPC RpcTryExcept
topic_type:
- apiref
api_name:
- RpcTryExcept
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5876a3fe0b33f96a5e10a9c712bdcadcbfca10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085788"
---
# <a name="rpctryexcept"></a><span data-ttu-id="b8198-104">RpcTryExcept</span><span class="sxs-lookup"><span data-stu-id="b8198-104">RpcTryExcept</span></span>

<span data-ttu-id="b8198-105">A instrução **RpcTryExcept** fornece manipulação de exceção estruturada para aplicativos RPC.</span><span class="sxs-lookup"><span data-stu-id="b8198-105">The **RpcTryExcept** statement provides structured exception handling for RPC applications.</span></span> <span data-ttu-id="b8198-106">Se qualquer uma das instruções do programa no **RpcTryExcept** causar uma exceção, as instruções no bloco de código [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) serão executadas.</span><span class="sxs-lookup"><span data-stu-id="b8198-106">If any of the program statements in the **RpcTryExcept** cause an exception, the statements in the [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) code block are executed.</span></span> <span data-ttu-id="b8198-107">Todas as instruções **RpcTryExcept** devem ser terminadas pela instrução [**RpcEndExcept**](/previous-versions/aa375629(v=vs.80)) .</span><span class="sxs-lookup"><span data-stu-id="b8198-107">All **RpcTryExcept** statements must be terminated by the [**RpcEndExcept**](/previous-versions/aa375629(v=vs.80)) statement.</span></span>

<span data-ttu-id="b8198-108">Para obter mais informações, consulte [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).</span><span class="sxs-lookup"><span data-stu-id="b8198-108">For more information, see [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).</span></span>

<span data-ttu-id="b8198-109">**Windows Vista e versões posteriores do Windows:** o [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) é recomendado para manipulação de exceção estruturada para as exceções mais comuns como uma alternativa para filtros personalizados com [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).  </span><span class="sxs-lookup"><span data-stu-id="b8198-109">**Windows Vista and later versions of Windows:**  [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) is recommended for structured exception handling for the most common exceptions as an alternative to custom filters with [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8198-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8198-110">Requirements</span></span>



| <span data-ttu-id="b8198-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8198-111">Requirement</span></span> | <span data-ttu-id="b8198-112">Valor</span><span class="sxs-lookup"><span data-stu-id="b8198-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b8198-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8198-113">Minimum supported client</span></span><br/> | <span data-ttu-id="b8198-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b8198-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b8198-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8198-115">Minimum supported server</span></span><br/> | <span data-ttu-id="b8198-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b8198-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b8198-117">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b8198-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8198-118"><dt>RPC. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8198-118"><dt>Rpc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8198-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8198-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8198-120">**RpcExcept**</span><span class="sxs-lookup"><span data-stu-id="b8198-120">**RpcExcept**</span></span>](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)
</dt> <dt>

[<span data-ttu-id="b8198-121">**RpcExceptionFilter**</span><span class="sxs-lookup"><span data-stu-id="b8198-121">**RpcExceptionFilter**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter)
</dt> <dt>

[<span data-ttu-id="b8198-122">**RpcTryFinally**</span><span class="sxs-lookup"><span data-stu-id="b8198-122">**RpcTryFinally**</span></span>](rpctryfinally.md)
</dt> </dl>

 

