---
title: Mensagem de TTM_HITTEST (commctrl. h)
description: Testa um ponto para determinar se ele está dentro do retângulo delimitador da ferramenta especificada e, se for, recupera informações sobre a ferramenta.
ms.assetid: d4dcc29b-c64c-41b8-a153-300df68ecdf5
keywords:
- Controles de TTM_HITTEST de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_HITTEST
- TTM_HITTESTA
- TTM_HITTESTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b515ccb5c283b66760f24c02749368e424e6fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455168"
---
# <a name="ttm_hittest-message"></a><span data-ttu-id="ade2f-104">\_Mensagem TTM HITTEST</span><span class="sxs-lookup"><span data-stu-id="ade2f-104">TTM\_HITTEST message</span></span>

<span data-ttu-id="ade2f-105">Testa um ponto para determinar se ele está dentro do retângulo delimitador da ferramenta especificada e, se for, recupera informações sobre a ferramenta.</span><span class="sxs-lookup"><span data-stu-id="ade2f-105">Tests a point to determine whether it is within the bounding rectangle of the specified tool and, if it is, retrieves information about the tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="ade2f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ade2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ade2f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ade2f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ade2f-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ade2f-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ade2f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ade2f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ade2f-110">Ponteiro para uma estrutura [**TTHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa) .</span><span class="sxs-lookup"><span data-stu-id="ade2f-110">Pointer to a [**TTHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa) structure.</span></span> <span data-ttu-id="ade2f-111">Ao enviar a mensagem, o membro **HWND** deve especificar o identificador para uma ferramenta e o membro **pt** deve especificar as coordenadas de um ponto.</span><span class="sxs-lookup"><span data-stu-id="ade2f-111">When sending the message, the **hwnd** member must specify the handle to a tool and the **pt** member must specify the coordinates of a point.</span></span> <span data-ttu-id="ade2f-112">Se o valor de retorno for **true**, o membro de **ti** (uma estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) ) receberá informações sobre a ferramenta que ocupa o ponto.</span><span class="sxs-lookup"><span data-stu-id="ade2f-112">If the return value is **TRUE**, the **ti** member (a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure) receives information about the tool that occupies the point.</span></span> <span data-ttu-id="ade2f-113">O membro **cbSize** da estrutura de **ti** deve ser preenchido antes de enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="ade2f-113">The **cbSize** member of the **ti** structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ade2f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ade2f-114">Return value</span></span>

<span data-ttu-id="ade2f-115">Retornará **true** se a ferramenta ocupar o ponto especificado ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="ade2f-115">Returns **TRUE** if the tool occupies the specified point, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ade2f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ade2f-116">Remarks</span></span>

<span data-ttu-id="ade2f-117">Esta mensagem deve ser enviada quando a ferramenta tiver o sinalizador de faixa de TTF \_ definido.</span><span class="sxs-lookup"><span data-stu-id="ade2f-117">This message must be sent when the tool has the TTF\_TRACK flag set.</span></span> <span data-ttu-id="ade2f-118">Para obter mais informações sobre esse sinalizador, consulte [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa).</span><span class="sxs-lookup"><span data-stu-id="ade2f-118">For more information on this flag, see [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa).</span></span> <span data-ttu-id="ade2f-119">\_O TTM HITTEST falhará se \_ a faixa de TTF não estiver definida, independentemente se o ponto de acesso estiver no retângulo de ferramentas ou não.</span><span class="sxs-lookup"><span data-stu-id="ade2f-119">TTM\_HITTEST will fail if TTF\_TRACK is not set, regardless if the hit point is in the tools rectangle or not.</span></span>

## <a name="requirements"></a><span data-ttu-id="ade2f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ade2f-120">Requirements</span></span>



| <span data-ttu-id="ade2f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ade2f-121">Requirement</span></span> | <span data-ttu-id="ade2f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ade2f-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ade2f-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ade2f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ade2f-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ade2f-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ade2f-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ade2f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ade2f-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ade2f-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ade2f-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ade2f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ade2f-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ade2f-128"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ade2f-129">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="ade2f-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ade2f-130">**TTM \_ HITTESTW** (Unicode) e **TTM \_ hittesta** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ade2f-130">**TTM\_HITTESTW** (Unicode) and **TTM\_HITTESTA** (ANSI)</span></span><br/>                   |



 

 





