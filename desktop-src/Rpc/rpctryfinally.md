---
title: RpcTryFinally (RPC. h)
description: A instrução RpcTryFinally fornece manipulação de terminação estruturada.
ms.assetid: e9ed748a-db15-4c91-b8a4-b510f99042d8
keywords:
- RPC RpcTryFinally
topic_type:
- apiref
api_name:
- RpcTryFinally
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 909d65013fb3fb83ffb926fea6a6b3f30980a3b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455409"
---
# <a name="rpctryfinally"></a><span data-ttu-id="34018-104">RpcTryFinally</span><span class="sxs-lookup"><span data-stu-id="34018-104">RpcTryFinally</span></span>

<span data-ttu-id="34018-105">A instrução **RpcTryFinally** fornece manipulação de terminação estruturada.</span><span class="sxs-lookup"><span data-stu-id="34018-105">The **RpcTryFinally** statement provides structured termination handling.</span></span> <span data-ttu-id="34018-106">Ocorre uma exceção durante as instruções de execução do bloco de código associado à instrução **RpcTryFinally** , as instruções no bloco de código associado à instrução [**RpcFinally**](/previous-versions/aa375699(v=vs.80)) são executadas.</span><span class="sxs-lookup"><span data-stu-id="34018-106">It an exception occurs during the execution statements of the code block associated with the **RpcTryFinally** statement, the statements in the code block associated with the [**RpcFinally**](/previous-versions/aa375699(v=vs.80)) statement are executed.</span></span> <span data-ttu-id="34018-107">Todas as instruções **RpcTryFinally** devem ser terminadas por uma instrução [**RpcEndFinally**](/previous-versions/aa375634(v=vs.80)) .</span><span class="sxs-lookup"><span data-stu-id="34018-107">All **RpcTryFinally** statements must be terminated by an [**RpcEndFinally**](/previous-versions/aa375634(v=vs.80)) statement.</span></span>

<span data-ttu-id="34018-108">Para obter mais informações, consulte [**RpcFinally**](/previous-versions/aa375699(v=vs.80)).</span><span class="sxs-lookup"><span data-stu-id="34018-108">For more information, see [**RpcFinally**](/previous-versions/aa375699(v=vs.80)).</span></span>

## <a name="requirements"></a><span data-ttu-id="34018-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34018-109">Requirements</span></span>



| <span data-ttu-id="34018-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="34018-110">Requirement</span></span> | <span data-ttu-id="34018-111">Valor</span><span class="sxs-lookup"><span data-stu-id="34018-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="34018-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34018-112">Minimum supported client</span></span><br/> | <span data-ttu-id="34018-113">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="34018-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="34018-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34018-114">Minimum supported server</span></span><br/> | <span data-ttu-id="34018-115">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="34018-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="34018-116">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="34018-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="34018-117"><dt>RPC. h</dt></span><span class="sxs-lookup"><span data-stu-id="34018-117"><dt>Rpc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34018-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="34018-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="34018-119">[**RpcFinally**](/previous-versions/aa375699(v=vs.80))</span><span class="sxs-lookup"><span data-stu-id="34018-119">[**RpcFinally**](/previous-versions/aa375699(v=vs.80))</span></span>
</dt> <dt>

<span data-ttu-id="34018-120">[**RpcEndFinally**](/previous-versions/aa375634(v=vs.80))</span><span class="sxs-lookup"><span data-stu-id="34018-120">[**RpcEndFinally**](/previous-versions/aa375634(v=vs.80))</span></span>
</dt> </dl>

 

