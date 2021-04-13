---
title: Mensagem de UDM_GETRANGE32 (commctrl. h)
description: Recupera o intervalo de 32 bits de um controle acima-abaixo.
ms.assetid: a94b50c9-cd2f-430d-875f-720e51f544f1
keywords:
- Controles de UDM_GETRANGE32 de mensagens do Windows
topic_type:
- apiref
api_name:
- UDM_GETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca418cd08dc4c81b3ff734d74f3ca9deeef7d848
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455004"
---
# <a name="udm_getrange32-message"></a><span data-ttu-id="cc27d-104">\_Mensagem de GETRANGE32 UDM</span><span class="sxs-lookup"><span data-stu-id="cc27d-104">UDM\_GETRANGE32 message</span></span>

<span data-ttu-id="cc27d-105">Recupera o intervalo de 32 bits de um controle acima-abaixo.</span><span class="sxs-lookup"><span data-stu-id="cc27d-105">Retrieves the 32-bit range of an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="cc27d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc27d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc27d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cc27d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc27d-108">Ponteiro para um inteiro assinado que recebe o limite inferior do intervalo de controle acima-abaixo.</span><span class="sxs-lookup"><span data-stu-id="cc27d-108">Pointer to a signed integer that receives the lower limit of the up-down control range.</span></span> <span data-ttu-id="cc27d-109">Esse parâmetro pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="cc27d-109">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cc27d-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cc27d-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc27d-111">Ponteiro para um inteiro assinado que recebe o limite superior do intervalo de controle acima-abaixo.</span><span class="sxs-lookup"><span data-stu-id="cc27d-111">Pointer to a signed integer that receives the upper limit of the up-down control range.</span></span> <span data-ttu-id="cc27d-112">Esse parâmetro pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="cc27d-112">This parameter may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc27d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cc27d-113">Return value</span></span>

<span data-ttu-id="cc27d-114">O valor retornado para esta mensagem não é usado.</span><span class="sxs-lookup"><span data-stu-id="cc27d-114">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc27d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc27d-115">Requirements</span></span>



| <span data-ttu-id="cc27d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc27d-116">Requirement</span></span> | <span data-ttu-id="cc27d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="cc27d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc27d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc27d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cc27d-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cc27d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cc27d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc27d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cc27d-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cc27d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cc27d-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc27d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc27d-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc27d-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





