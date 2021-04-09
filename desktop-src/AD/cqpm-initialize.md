---
title: Mensagem de CQPM_INITIALIZE (Cmnquery. h)
description: Enviado para a função de retorno de chamada CQPageProc de uma página de extensão de formulário de consulta quando a página é adicionada a um formulário.
ms.assetid: 29cb39d5-9bc4-472e-8a2f-dc6cd505144a
ms.tgt_platform: multiple
keywords:
- Mensagem de CQPM_INITIALIZE Active Directory
topic_type:
- apiref
api_name:
- CQPM_INITIALIZE
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e95c7087a9cd2d40387c8d7dd07aa93c8f697fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009312"
---
# <a name="cqpm_initialize-message"></a><span data-ttu-id="75393-104">CQPM \_ inicializar mensagem</span><span class="sxs-lookup"><span data-stu-id="75393-104">CQPM\_INITIALIZE message</span></span>

<span data-ttu-id="75393-105">A mensagem de **\_ inicialização CQPM** é enviada para a função de retorno de chamada [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) de uma página de extensão de formulário de consulta quando a página é adicionada a um formulário.</span><span class="sxs-lookup"><span data-stu-id="75393-105">The **CQPM\_INITIALIZE** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page when the page is added to a form.</span></span>

## <a name="parameters"></a><span data-ttu-id="75393-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75393-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75393-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="75393-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75393-108">Não usado.</span><span class="sxs-lookup"><span data-stu-id="75393-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="75393-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="75393-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75393-110">Não usado.</span><span class="sxs-lookup"><span data-stu-id="75393-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75393-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="75393-111">Return value</span></span>

<span data-ttu-id="75393-112">O valor de retorno para essa mensagem é ignorado.</span><span class="sxs-lookup"><span data-stu-id="75393-112">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="75393-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75393-113">Requirements</span></span>



| <span data-ttu-id="75393-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="75393-114">Requirement</span></span> | <span data-ttu-id="75393-115">Valor</span><span class="sxs-lookup"><span data-stu-id="75393-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="75393-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75393-116">Minimum supported client</span></span><br/> | <span data-ttu-id="75393-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75393-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="75393-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75393-118">Minimum supported server</span></span><br/> | <span data-ttu-id="75393-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75393-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="75393-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="75393-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="75393-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="75393-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75393-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="75393-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75393-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="75393-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





