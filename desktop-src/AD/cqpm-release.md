---
title: Mensagem de CQPM_RELEASE (Cmnquery. h)
description: Enviado para a função de retorno de chamada CQPageProc de uma página de extensão de formulário de consulta quando a página está prestes a ser descarregada.
ms.assetid: b935ae8d-a07f-4f0d-b379-5512e96a25a5
ms.tgt_platform: multiple
keywords:
- Mensagem de CQPM_RELEASE Active Directory
topic_type:
- apiref
api_name:
- CQPM_RELEASE
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4957f02b57f499d80f7802b4fe9bd2639485b8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009310"
---
# <a name="cqpm_release-message"></a><span data-ttu-id="4aef0-104">Mensagem de liberação do CQPM \_</span><span class="sxs-lookup"><span data-stu-id="4aef0-104">CQPM\_RELEASE message</span></span>

<span data-ttu-id="4aef0-105">A mensagem de **\_ liberação CQPM** é enviada para a função de retorno de chamada [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) de uma página de extensão de formulário de consulta quando a página está prestes a ser descarregada.</span><span class="sxs-lookup"><span data-stu-id="4aef0-105">The **CQPM\_RELEASE** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page when the page is about to be unloaded.</span></span>

## <a name="parameters"></a><span data-ttu-id="4aef0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4aef0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4aef0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4aef0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4aef0-108">Não usado.</span><span class="sxs-lookup"><span data-stu-id="4aef0-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="4aef0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4aef0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4aef0-110">Não usado.</span><span class="sxs-lookup"><span data-stu-id="4aef0-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4aef0-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4aef0-111">Return value</span></span>

<span data-ttu-id="4aef0-112">O valor de retorno para essa mensagem é ignorado.</span><span class="sxs-lookup"><span data-stu-id="4aef0-112">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="4aef0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4aef0-113">Requirements</span></span>



| <span data-ttu-id="4aef0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4aef0-114">Requirement</span></span> | <span data-ttu-id="4aef0-115">Valor</span><span class="sxs-lookup"><span data-stu-id="4aef0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4aef0-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4aef0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4aef0-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4aef0-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="4aef0-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4aef0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4aef0-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4aef0-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="4aef0-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4aef0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4aef0-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="4aef0-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4aef0-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="4aef0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aef0-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="4aef0-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





