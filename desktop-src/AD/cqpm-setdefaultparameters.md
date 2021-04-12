---
title: Mensagem de CQPM_SETDEFAULTPARAMETERS (Cmnquery. h)
description: Enviado para a função de retorno de chamada CQPageProc de uma página de extensão de formulário de consulta para definir parâmetros padrão alternativos para a página.
ms.assetid: 4d7f1c03-5c67-4f4c-b381-034a142251fe
ms.tgt_platform: multiple
keywords:
- Mensagem de CQPM_SETDEFAULTPARAMETERS Active Directory
topic_type:
- apiref
api_name:
- CQPM_SETDEFAULTPARAMETERS
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4df77b9068c23a0eeac30181d131cb8469dc53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455071"
---
# <a name="cqpm_setdefaultparameters-message"></a><span data-ttu-id="9a80d-104">\_Mensagem CQPM SETdefaultparameters</span><span class="sxs-lookup"><span data-stu-id="9a80d-104">CQPM\_SETDEFAULTPARAMETERS message</span></span>

<span data-ttu-id="9a80d-105">A mensagem **CQPM \_ setpadrãoparameters** é enviada para a função de retorno de chamada [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) de uma página de extensão de formulário de consulta para definir parâmetros padrão alternativos para a página.</span><span class="sxs-lookup"><span data-stu-id="9a80d-105">The **CQPM\_SETDEFAULTPARAMETERS** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to set alternate default parameters for the page.</span></span>

## <a name="parameters"></a><span data-ttu-id="9a80d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a80d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a80d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9a80d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a80d-108">Contém zero se a página for a página padrão ou zero de outra forma.</span><span class="sxs-lookup"><span data-stu-id="9a80d-108">Contains nonzero if the page is the default page or zero otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="9a80d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9a80d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a80d-110">Ponteiro para uma estrutura [**OPENQUERYWINDOW**](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow) que contém dados sobre a caixa de diálogo consulta de serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="9a80d-110">Pointer to an [**OPENQUERYWINDOW**](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow) structure that contains data about the directory service query dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a80d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9a80d-111">Return value</span></span>

<span data-ttu-id="9a80d-112">O valor de retorno para essa mensagem é ignorado.</span><span class="sxs-lookup"><span data-stu-id="9a80d-112">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a80d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a80d-113">Requirements</span></span>



| <span data-ttu-id="9a80d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a80d-114">Requirement</span></span> | <span data-ttu-id="9a80d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="9a80d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a80d-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a80d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9a80d-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a80d-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="9a80d-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a80d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9a80d-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a80d-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="9a80d-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9a80d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a80d-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a80d-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a80d-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a80d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a80d-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="9a80d-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[<span data-ttu-id="9a80d-124">**OPENQUERYWINDOW**</span><span class="sxs-lookup"><span data-stu-id="9a80d-124">**OPENQUERYWINDOW**</span></span>](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow)
</dt> </dl>

 

 





