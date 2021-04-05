---
title: Sinalizadores de acesso (AccCtrl. h)
description: Esses valores indicam se uma entrada na lista de acesso descreve os direitos permitidos ou negados.
ms.assetid: 460d2c72-3315-4b4c-928e-4bb0640acbe5
topic_type:
- apiref
api_name:
- ACTRL_ACCESS_ALLOWED
- ACTRL_ACCESS_DENIED
api_location:
- AccCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5972bf95efc675d6dd9c2e58c0b7d25c8c305371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086436"
---
# <a name="access-flags"></a><span data-ttu-id="f6032-103">Sinalizadores de acesso</span><span class="sxs-lookup"><span data-stu-id="f6032-103">Access Flags</span></span>

<span data-ttu-id="f6032-104">Esses valores indicam se uma entrada na lista de acesso descreve os direitos permitidos ou negados.</span><span class="sxs-lookup"><span data-stu-id="f6032-104">These values indicate whether an entry in the access list describes rights that are allowed or denied.</span></span>



| <span data-ttu-id="f6032-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="f6032-105">Constant/value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="f6032-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="f6032-106">Description</span></span>                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------|
| <span id="ACTRL_ACCESS_ALLOWED"></span><span id="actrl_access_allowed"></span><dl> <span data-ttu-id="f6032-107"><dt>**ACTRL \_ ACESSO \_ permitido**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="f6032-107"><dt>**ACTRL\_ACCESS\_ALLOWED**</dt> <dt>0x00000000</dt></span></span> </dl> | <span data-ttu-id="f6032-108">Indica uma entrada permitida pelo Access.</span><span class="sxs-lookup"><span data-stu-id="f6032-108">Indicates an access-allowed entry.</span></span><br/> |
| <span id="ACTRL_ACCESS_DENIED"></span><span id="actrl_access_denied"></span><dl> <span data-ttu-id="f6032-109"><dt>**ACTRL \_ ACESSO \_ negado**</dt> <dt>0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="f6032-109"><dt>**ACTRL\_ACCESS\_DENIED**</dt> <dt>0x10000000</dt></span></span> </dl>    | <span data-ttu-id="f6032-110">Indica uma entrada com acesso negado.</span><span class="sxs-lookup"><span data-stu-id="f6032-110">Indicates an access-denied entry.</span></span><br/>  |



## <a name="requirements"></a><span data-ttu-id="f6032-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6032-111">Requirements</span></span>



| <span data-ttu-id="f6032-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6032-112">Requirement</span></span> | <span data-ttu-id="f6032-113">Valor</span><span class="sxs-lookup"><span data-stu-id="f6032-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f6032-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6032-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f6032-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f6032-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f6032-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6032-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f6032-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f6032-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f6032-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f6032-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6032-119"><dt>AccCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6032-119"><dt>AccCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6032-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6032-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6032-121">**\_entrada de acesso ACTRL \_**</span><span class="sxs-lookup"><span data-stu-id="f6032-121">**ACTRL\_ACCESS\_ENTRY**</span></span>](/windows/desktop/api/AccCtrl/ns-accctrl-actrl_access_entrya)
</dt> </dl>

 

 





