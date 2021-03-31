---
title: WS_SECURITY_CONTEXT (WebServices. h)
description: Um tipo opaco usado para fazer referência a um objeto de contexto de segurança.
ms.assetid: 8d23357b-bff8-45fe-80ef-df3f3b0edde1
keywords:
- WS_SECURITY_CONTEXT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c041307eadd1ebcea379f9de0880fc011bd137ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085742"
---
# <a name="ws_security_context"></a><span data-ttu-id="8c48d-104">\_contexto de segurança do WS \_</span><span class="sxs-lookup"><span data-stu-id="8c48d-104">WS\_SECURITY\_CONTEXT</span></span>

<span data-ttu-id="8c48d-105">Um tipo opaco usado para fazer referência a um [objeto de contexto de segurança](security-context.md).</span><span class="sxs-lookup"><span data-stu-id="8c48d-105">An opaque type used to reference a [security context object](security-context.md).</span></span>


```C++
typedef struct _WS_SECURITY_CONTEXT WS_SECURITY_CONTEXT;
```



## <a name="remarks"></a><span data-ttu-id="8c48d-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c48d-106">Remarks</span></span>

<span data-ttu-id="8c48d-107">Este objeto não é thread-safe.</span><span class="sxs-lookup"><span data-stu-id="8c48d-107">This object is not thread safe.</span></span> <span data-ttu-id="8c48d-108">Para obter mais informações, consulte [segurança do thread](thread-safety.md).</span><span class="sxs-lookup"><span data-stu-id="8c48d-108">For more information, see [thread safety](thread-safety.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c48d-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c48d-109">Requirements</span></span>



| <span data-ttu-id="8c48d-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c48d-110">Requirement</span></span> | <span data-ttu-id="8c48d-111">Valor</span><span class="sxs-lookup"><span data-stu-id="8c48d-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c48d-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c48d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="8c48d-113">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8c48d-113">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="8c48d-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c48d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="8c48d-115">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="8c48d-115">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="8c48d-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8c48d-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c48d-117"><dt>WebServices. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c48d-117"><dt>WebServices.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c48d-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c48d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c48d-119">Contexto de segurança</span><span class="sxs-lookup"><span data-stu-id="8c48d-119">Security Context</span></span>](security-context.md)
</dt> <dt>

[<span data-ttu-id="8c48d-120">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="8c48d-120">Thread Safety</span></span>](thread-safety.md)
</dt> </dl>

 

 





