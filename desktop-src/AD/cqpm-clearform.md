---
title: Mensagem de CQPM_CLEARFORM (Cmnquery. h)
description: Enviado para a função de retorno de chamada CQPageProc de uma consulta para a página de extensão quando o conteúdo da página deve ser redefinido para os valores padrão.
ms.assetid: 0fd3ec82-0566-43de-a7a1-4b6b76bf2050
ms.tgt_platform: multiple
keywords:
- Mensagem de CQPM_CLEARFORM Active Directory
topic_type:
- apiref
api_name:
- CQPM_CLEARFORM
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94af3a31a29da4ce5740c4e326bbf1a8961f9f82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918068"
---
# <a name="cqpm_clearform-message"></a><span data-ttu-id="df5c9-104">\_Mensagem CQPM CLEARFORM</span><span class="sxs-lookup"><span data-stu-id="df5c9-104">CQPM\_CLEARFORM message</span></span>

<span data-ttu-id="df5c9-105">A mensagem **CQPM \_ CLEARFORM** é enviada para a função de retorno de chamada [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) de uma consulta para a página extensão quando o conteúdo da página deve ser redefinido para os valores padrão.</span><span class="sxs-lookup"><span data-stu-id="df5c9-105">The **CQPM\_CLEARFORM** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query for extension page when the contents of the page should be reset to the default values.</span></span>

## <a name="parameters"></a><span data-ttu-id="df5c9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df5c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df5c9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="df5c9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df5c9-108">Não usado.</span><span class="sxs-lookup"><span data-stu-id="df5c9-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="df5c9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="df5c9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df5c9-110">Não usado.</span><span class="sxs-lookup"><span data-stu-id="df5c9-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df5c9-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="df5c9-111">Return value</span></span>

<span data-ttu-id="df5c9-112">Retorna **S \_ OK** se for bem-sucedido ou um código de erro **HRESULT** padrão do contrário.</span><span class="sxs-lookup"><span data-stu-id="df5c9-112">Returns **S\_OK** if successful or a standard **HRESULT** error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="df5c9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df5c9-113">Requirements</span></span>



| <span data-ttu-id="df5c9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="df5c9-114">Requirement</span></span> | <span data-ttu-id="df5c9-115">Valor</span><span class="sxs-lookup"><span data-stu-id="df5c9-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df5c9-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df5c9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="df5c9-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df5c9-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="df5c9-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df5c9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="df5c9-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df5c9-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="df5c9-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="df5c9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="df5c9-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="df5c9-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df5c9-122">Consulte também</span><span class="sxs-lookup"><span data-stu-id="df5c9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df5c9-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="df5c9-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





