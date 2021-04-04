---
title: Mensagem de CQPM_GETPARAMETERS (Cmnquery. h)
description: Enviado para a função de retorno de chamada CQPageProc de uma página de extensão de formulário de consulta para recuperar dados sobre a consulta executada pela página.
ms.assetid: 6b94b318-8356-4554-99fe-f82364325e6e
ms.tgt_platform: multiple
keywords:
- Mensagem de CQPM_GETPARAMETERS Active Directory
topic_type:
- apiref
api_name:
- CQPM_GETPARAMETERS
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2aac8961e2299e4a8a69ead9426698e8c932346e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824228"
---
# <a name="cqpm_getparameters-message"></a><span data-ttu-id="39e1f-104">\_Mensagem CQPM Parameters</span><span class="sxs-lookup"><span data-stu-id="39e1f-104">CQPM\_GETPARAMETERS message</span></span>

<span data-ttu-id="39e1f-105">A mensagem **Parameters de CQPM \_** é enviada para a função de retorno de chamada [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) de uma página de extensão de formulário de consulta para recuperar dados sobre a consulta executada pela página.</span><span class="sxs-lookup"><span data-stu-id="39e1f-105">The **CQPM\_GETPARAMETERS** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to retrieve data about the query performed by the page.</span></span>

## <a name="parameters"></a><span data-ttu-id="39e1f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39e1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39e1f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="39e1f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39e1f-108">Não usado.</span><span class="sxs-lookup"><span data-stu-id="39e1f-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="39e1f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39e1f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39e1f-110">Ponteiro para um valor [**LPDSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams) que recebe dados sobre a consulta executada pela página.</span><span class="sxs-lookup"><span data-stu-id="39e1f-110">Pointer to a [**LPDSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams) value that receives data about the query performed by the page.</span></span> <span data-ttu-id="39e1f-111">Se esse parâmetro for **nulo**, a estrutura **DSQUERYPARAMS** deverá ser alocada pela extensão usando a função [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) .</span><span class="sxs-lookup"><span data-stu-id="39e1f-111">If this parameter is **NULL**, the **DSQUERYPARAMS** structure must be allocated by the extension using the [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39e1f-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="39e1f-112">Return value</span></span>

<span data-ttu-id="39e1f-113">Retorna **S \_ OK** se for bem-sucedido ou um código de erro **HRESULT** padrão do contrário.</span><span class="sxs-lookup"><span data-stu-id="39e1f-113">Returns **S\_OK** if successful or a standard **HRESULT** error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="39e1f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39e1f-114">Requirements</span></span>



| <span data-ttu-id="39e1f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="39e1f-115">Requirement</span></span> | <span data-ttu-id="39e1f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="39e1f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39e1f-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39e1f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="39e1f-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39e1f-118">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="39e1f-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39e1f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="39e1f-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39e1f-120">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="39e1f-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="39e1f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="39e1f-122"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="39e1f-122"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39e1f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="39e1f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39e1f-124">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="39e1f-124">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[<span data-ttu-id="39e1f-125">**DSQUERYPARAMS**</span><span class="sxs-lookup"><span data-stu-id="39e1f-125">**DSQUERYPARAMS**</span></span>](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams)
</dt> <dt>

[<span data-ttu-id="39e1f-126">**CoTaskMemAlloc**</span><span class="sxs-lookup"><span data-stu-id="39e1f-126">**CoTaskMemAlloc**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
</dt> </dl>

 

