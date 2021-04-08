---
title: Mensagem de RB_HITTEST (commctrl. h)
description: Determina qual parte de uma banda de rebar está em um determinado ponto na tela, se existir uma banda de rebar nesse ponto.
ms.assetid: 8f27db21-50d8-438f-a44c-2e65dd93fa2a
keywords:
- Controles de RB_HITTEST de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e17283bfce255672391ba9d8b6acd60fe41045b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008925"
---
# <a name="rb_hittest-message"></a><span data-ttu-id="8f678-104">Mensagem de HITTEST de RB \_</span><span class="sxs-lookup"><span data-stu-id="8f678-104">RB\_HITTEST message</span></span>

<span data-ttu-id="8f678-105">Determina qual parte de uma banda de rebar está em um determinado ponto na tela, se existir uma banda de rebar nesse ponto.</span><span class="sxs-lookup"><span data-stu-id="8f678-105">Determines which portion of a rebar band is at a given point on the screen, if a rebar band exists at that point.</span></span>

## <a name="parameters"></a><span data-ttu-id="8f678-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f678-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f678-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8f678-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8f678-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="8f678-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8f678-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8f678-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f678-110">Ponteiro para uma estrutura [**RBHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo) .</span><span class="sxs-lookup"><span data-stu-id="8f678-110">Pointer to an [**RBHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo) structure.</span></span> <span data-ttu-id="8f678-111">Antes de enviar a mensagem, o membro **pt** dessa estrutura deve ser inicializado até o ponto que será testado, nas coordenadas do cliente.</span><span class="sxs-lookup"><span data-stu-id="8f678-111">Before sending the message, the **pt** member of this structure must be initialized to the point that will be hit tested, in client coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f678-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8f678-112">Return value</span></span>

<span data-ttu-id="8f678-113">Retorna o índice de base zero da banda no ponto determinado, ou-1 se nenhuma banda do rebar estava no ponto.</span><span class="sxs-lookup"><span data-stu-id="8f678-113">Returns the zero-based index of the band at the given point, or -1 if no rebar band was at the point.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f678-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f678-114">Requirements</span></span>



| <span data-ttu-id="8f678-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f678-115">Requirement</span></span> | <span data-ttu-id="8f678-116">Valor</span><span class="sxs-lookup"><span data-stu-id="8f678-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8f678-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f678-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8f678-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8f678-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8f678-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f678-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8f678-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8f678-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8f678-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8f678-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f678-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f678-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





