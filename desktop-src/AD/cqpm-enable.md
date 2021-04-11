---
title: Mensagem de CQPM_ENABLE (Cmnquery. h)
description: Enviado para a função de retorno de chamada CQPageProc de uma página de extensão de formulário de consulta para habilitar ou desabilitar a página.
ms.assetid: dc75fab7-6de7-4138-86df-84d44e774120
ms.tgt_platform: multiple
keywords:
- Mensagem de CQPM_ENABLE Active Directory
topic_type:
- apiref
api_name:
- CQPM_ENABLE
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0252c5e1ec7fd9633241416fbf01bb4ead52c45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009007"
---
# <a name="cqpm_enable-message"></a><span data-ttu-id="ffe2e-104">CQPM \_ habilitar mensagem</span><span class="sxs-lookup"><span data-stu-id="ffe2e-104">CQPM\_ENABLE message</span></span>

<span data-ttu-id="ffe2e-105">A mensagem de **\_ habilitação CQPM** é enviada para a função de retorno de chamada [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) de uma página de extensão de formulário de consulta para habilitar ou desabilitar a página.</span><span class="sxs-lookup"><span data-stu-id="ffe2e-105">The **CQPM\_ENABLE** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to enable or disable the page.</span></span>

## <a name="parameters"></a><span data-ttu-id="ffe2e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ffe2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffe2e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ffe2e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ffe2e-108">Contém zero para desabilitar a página ou diferente de zero para habilitar a página.</span><span class="sxs-lookup"><span data-stu-id="ffe2e-108">Contains zero to disable the page or nonzero to enable the page.</span></span>

</dd> <dt>

<span data-ttu-id="ffe2e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ffe2e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ffe2e-110">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ffe2e-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffe2e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ffe2e-111">Return value</span></span>

<span data-ttu-id="ffe2e-112">O valor de retorno para essa mensagem é ignorado.</span><span class="sxs-lookup"><span data-stu-id="ffe2e-112">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffe2e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffe2e-113">Requirements</span></span>



| <span data-ttu-id="ffe2e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffe2e-114">Requirement</span></span> | <span data-ttu-id="ffe2e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ffe2e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ffe2e-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ffe2e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ffe2e-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ffe2e-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="ffe2e-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ffe2e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ffe2e-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ffe2e-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="ffe2e-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ffe2e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffe2e-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffe2e-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffe2e-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="ffe2e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffe2e-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="ffe2e-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





