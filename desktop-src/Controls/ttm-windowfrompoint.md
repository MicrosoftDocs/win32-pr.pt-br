---
title: Mensagem de TTM_WINDOWFROMPOINT (commctrl. h)
description: Permite que um procedimento de subclasse faça com que uma dica de ferramenta exiba texto para uma janela diferente daquela abaixo do cursor do mouse.
ms.assetid: f3bf6917-1745-4e4f-a9c1-8fe86b2b3906
keywords:
- Controles de TTM_WINDOWFROMPOINT de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_WINDOWFROMPOINT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68679f6b6c2477a8279c22f11d0d300e44c8370d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644839"
---
# <a name="ttm_windowfrompoint-message"></a><span data-ttu-id="cf82b-104">\_Mensagem TTM WINDOWFROMPOINT</span><span class="sxs-lookup"><span data-stu-id="cf82b-104">TTM\_WINDOWFROMPOINT message</span></span>

<span data-ttu-id="cf82b-105">Permite que um procedimento de subclasse faça com que uma dica de ferramenta exiba texto para uma janela diferente daquela abaixo do cursor do mouse.</span><span class="sxs-lookup"><span data-stu-id="cf82b-105">Allows a subclass procedure to cause a tooltip to display text for a window other than the one beneath the mouse cursor.</span></span>

## <a name="parameters"></a><span data-ttu-id="cf82b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf82b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf82b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cf82b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cf82b-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="cf82b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cf82b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cf82b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf82b-110">Ponteiro para uma estrutura de [**ponto**](/previous-versions//dd162805(v=vs.85)) que define o ponto a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="cf82b-110">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that defines the point to be checked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf82b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cf82b-111">Return value</span></span>

<span data-ttu-id="cf82b-112">O valor de retorno é o identificador para a janela que contém o ponto, ou **NULL** se não existir nenhuma janela no ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="cf82b-112">The return value is the handle to the window that contains the point, or **NULL** if no window exists at the specified point.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf82b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf82b-113">Remarks</span></span>

<span data-ttu-id="cf82b-114">Essa mensagem destina-se a ser processada por um aplicativo que subfaz uma subclasse de ToolTip.</span><span class="sxs-lookup"><span data-stu-id="cf82b-114">This message is intended to be processed by an application that subclasses a tooltip.</span></span> <span data-ttu-id="cf82b-115">Ele não se destina a ser enviado por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cf82b-115">It is not intended to be sent by an application.</span></span> <span data-ttu-id="cf82b-116">Uma dica de ferramenta envia essa mensagem para ela mesma antes de exibir o texto de uma janela.</span><span class="sxs-lookup"><span data-stu-id="cf82b-116">A tooltip sends this message to itself before displaying the text for a window.</span></span> <span data-ttu-id="cf82b-117">Ao alterar as coordenadas do ponto especificado por *lParam*, o procedimento de subclasse pode fazer com que a dica de ferramenta exiba texto para uma janela diferente daquela abaixo do cursor do mouse.</span><span class="sxs-lookup"><span data-stu-id="cf82b-117">By changing the coordinates of the point specified by *lParam*, the subclass procedure can cause the tooltip to display text for a window other than the one beneath the mouse cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf82b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf82b-118">Requirements</span></span>



| <span data-ttu-id="cf82b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf82b-119">Requirement</span></span> | <span data-ttu-id="cf82b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="cf82b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf82b-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf82b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cf82b-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cf82b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cf82b-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf82b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cf82b-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cf82b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cf82b-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cf82b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf82b-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf82b-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

