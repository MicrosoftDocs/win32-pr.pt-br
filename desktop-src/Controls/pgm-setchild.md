---
title: Mensagem de PGM_SETCHILD (commctrl. h)
description: Define a janela contida para o controle de pager.
ms.assetid: 717e6720-aa42-4ecd-9520-4618a04dc28d
keywords:
- Controles de PGM_SETCHILD de mensagens do Windows
topic_type:
- apiref
api_name:
- PGM_SETCHILD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c934c3c5688ac79b5c5ce67aef68e28ad3627ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085461"
---
# <a name="pgm_setchild-message"></a><span data-ttu-id="34a38-104">Mensagem de PGM \_</span><span class="sxs-lookup"><span data-stu-id="34a38-104">PGM\_SETCHILD message</span></span>

<span data-ttu-id="34a38-105">Define a janela contida para o controle de pager.</span><span class="sxs-lookup"><span data-stu-id="34a38-105">Sets the contained window for the pager control.</span></span> <span data-ttu-id="34a38-106">Esta mensagem não vai alterar o pai da janela contida; Ele atribui apenas um identificador de janela ao controle de pager para rolagem.</span><span class="sxs-lookup"><span data-stu-id="34a38-106">This message will not change the parent of the contained window; it only assigns a window handle to the pager control for scrolling.</span></span> <span data-ttu-id="34a38-107">Na maioria dos casos, a janela contida será uma janela filho.</span><span class="sxs-lookup"><span data-stu-id="34a38-107">In most cases, the contained window will be a child window.</span></span> <span data-ttu-id="34a38-108">Se esse for o caso, a janela contida deverá ser um filho do controle de pager.</span><span class="sxs-lookup"><span data-stu-id="34a38-108">If this is the case, the contained window should be a child of the pager control.</span></span> <span data-ttu-id="34a38-109">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetChild do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) .</span><span class="sxs-lookup"><span data-stu-id="34a38-109">You can send this message explicitly or use the [**Pager\_SetChild**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="34a38-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34a38-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34a38-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="34a38-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="34a38-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="34a38-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="34a38-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="34a38-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="34a38-114">Identificador para a janela a ser contida.</span><span class="sxs-lookup"><span data-stu-id="34a38-114">Handle to the window to be contained.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34a38-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="34a38-115">Return value</span></span>

<span data-ttu-id="34a38-116">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="34a38-116">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="34a38-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34a38-117">Requirements</span></span>



| <span data-ttu-id="34a38-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="34a38-118">Requirement</span></span> | <span data-ttu-id="34a38-119">Valor</span><span class="sxs-lookup"><span data-stu-id="34a38-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="34a38-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34a38-120">Minimum supported client</span></span><br/> | <span data-ttu-id="34a38-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="34a38-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="34a38-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34a38-122">Minimum supported server</span></span><br/> | <span data-ttu-id="34a38-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="34a38-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="34a38-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="34a38-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="34a38-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="34a38-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





