---
title: Mensagem de TTM_GETTEXT (commctrl. h)
description: Recupera as informações que um controle ToolTip mantém sobre uma ferramenta.
ms.assetid: f2afa706-4209-4761-a981-df3d5b938c88
keywords:
- Controles de TTM_GETTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_GETTEXT
- TTM_GETTEXTA
- TTM_GETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f774671d34f89306593d23481fa917190ae69aaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753784"
---
# <a name="ttm_gettext-message"></a><span data-ttu-id="65d51-104">\_Mensagem GETTEXT TTM</span><span class="sxs-lookup"><span data-stu-id="65d51-104">TTM\_GETTEXT message</span></span>

<span data-ttu-id="65d51-105">Recupera as informações que um controle ToolTip mantém sobre uma ferramenta.</span><span class="sxs-lookup"><span data-stu-id="65d51-105">Retrieves the information a tooltip control maintains about a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="65d51-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65d51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65d51-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="65d51-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="65d51-108">O número de **TCHARs**, incluindo o **nulo** de terminação, a ser copiado para o buffer apontado por **lpszText**.</span><span class="sxs-lookup"><span data-stu-id="65d51-108">The number of **TCHARs**, including the terminating **NULL**, to copy to the buffer pointed to by **lpszText**.</span></span> </dd> <dt>

<span data-ttu-id="65d51-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="65d51-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="65d51-110">Ponteiro para uma estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="65d51-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="65d51-111">Defina o membro **cbSize** dessa estrutura como `sizeof(TOOLINFO)` antes de enviar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="65d51-111">Set the **cbSize** member of this structure to `sizeof(TOOLINFO)` before sending this message.</span></span> <span data-ttu-id="65d51-112">Defina os membros de **HWND** e **UID** para identificar a ferramenta para a qual recuperar informações.</span><span class="sxs-lookup"><span data-stu-id="65d51-112">Set the **hwnd** and **uId** members to identify the tool for which to retrieve information.</span></span> <span data-ttu-id="65d51-113">Aloque um buffer de tamanho especificado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="65d51-113">Allocate a buffer of size specified by *wParam*.</span></span> <span data-ttu-id="65d51-114">Defina o membro **lpszText** para apontar para o buffer para receber o texto da ferramenta.</span><span class="sxs-lookup"><span data-stu-id="65d51-114">Set the **lpszText** member to point to the buffer to receive the tool text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65d51-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="65d51-115">Return value</span></span>

<span data-ttu-id="65d51-116">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="65d51-116">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="65d51-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65d51-117">Requirements</span></span>



| <span data-ttu-id="65d51-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="65d51-118">Requirement</span></span> | <span data-ttu-id="65d51-119">Valor</span><span class="sxs-lookup"><span data-stu-id="65d51-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65d51-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65d51-120">Minimum supported client</span></span><br/> | <span data-ttu-id="65d51-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="65d51-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="65d51-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65d51-122">Minimum supported server</span></span><br/> | <span data-ttu-id="65d51-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="65d51-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="65d51-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="65d51-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="65d51-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="65d51-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="65d51-126">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="65d51-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="65d51-127">**TTM \_ GETTEXTW** (Unicode) e **TTM \_ gettexta** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="65d51-127">**TTM\_GETTEXTW** (Unicode) and **TTM\_GETTEXTA** (ANSI)</span></span><br/>                   |



 

 





