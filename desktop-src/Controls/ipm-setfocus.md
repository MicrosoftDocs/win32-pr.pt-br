---
title: Mensagem de IPM_SETFOCUS (commctrl. h)
description: Define o foco do teclado para o campo especificado no controle de endereço IP. Todo o texto nesse campo será selecionado.
ms.assetid: 4b975eb2-85e1-4e33-a803-99b48d2ff5e8
keywords:
- Controles de IPM_SETFOCUS de mensagens do Windows
topic_type:
- apiref
api_name:
- IPM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d713e0a8b7eb838a2db5c4738c801d4fb76b782
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085816"
---
# <a name="ipm_setfocus-message"></a><span data-ttu-id="aaa9a-105">\_Mensagem IPM SETFOCUS</span><span class="sxs-lookup"><span data-stu-id="aaa9a-105">IPM\_SETFOCUS message</span></span>

<span data-ttu-id="aaa9a-106">Define o foco do teclado para o campo especificado no controle de endereço IP.</span><span class="sxs-lookup"><span data-stu-id="aaa9a-106">Sets the keyboard focus to the specified field in the IP address control.</span></span> <span data-ttu-id="aaa9a-107">Todo o texto nesse campo será selecionado.</span><span class="sxs-lookup"><span data-stu-id="aaa9a-107">All of the text in that field will be selected.</span></span>

## <a name="parameters"></a><span data-ttu-id="aaa9a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aaa9a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaa9a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aaa9a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aaa9a-110">Um índice de campo baseado em zero ao qual o foco deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="aaa9a-110">A zero-based field index to which the focus should be set.</span></span> <span data-ttu-id="aaa9a-111">Se esse valor for maior que o número de campos, o foco será definido como o primeiro campo em branco.</span><span class="sxs-lookup"><span data-stu-id="aaa9a-111">If this value is greater than the number of fields, focus is set to the first blank field.</span></span> <span data-ttu-id="aaa9a-112">Se todos os campos não estiverem em branco, o foco será definido como o primeiro campo.</span><span class="sxs-lookup"><span data-stu-id="aaa9a-112">If all fields are nonblank, focus is set to the first field.</span></span>

</dd> <dt>

<span data-ttu-id="aaa9a-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aaa9a-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="aaa9a-114">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="aaa9a-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aaa9a-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aaa9a-115">Return value</span></span>

<span data-ttu-id="aaa9a-116">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="aaa9a-116">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaa9a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aaa9a-117">Requirements</span></span>



| <span data-ttu-id="aaa9a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="aaa9a-118">Requirement</span></span> | <span data-ttu-id="aaa9a-119">Valor</span><span class="sxs-lookup"><span data-stu-id="aaa9a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aaa9a-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aaa9a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aaa9a-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aaa9a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aaa9a-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aaa9a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aaa9a-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="aaa9a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aaa9a-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aaa9a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="aaa9a-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aaa9a-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





