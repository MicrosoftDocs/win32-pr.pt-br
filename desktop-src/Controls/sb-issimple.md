---
title: Mensagem de SB_ISSIMPLE (commctrl. h)
description: Verifica um controle de barra de status para determinar se ele está no modo simples.
ms.assetid: f4362bc3-1852-4569-af9b-96d2da4f0606
keywords:
- Controles de SB_ISSIMPLE de mensagens do Windows
topic_type:
- apiref
api_name:
- SB_ISSIMPLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71a5c523bef45065b103051962d7f147816c505d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086021"
---
# <a name="sb_issimple-message"></a><span data-ttu-id="cf906-104">Mensagem do SB \_ ISsimple</span><span class="sxs-lookup"><span data-stu-id="cf906-104">SB\_ISSIMPLE message</span></span>

<span data-ttu-id="cf906-105">Verifica um controle de barra de status para determinar se ele está no modo simples.</span><span class="sxs-lookup"><span data-stu-id="cf906-105">Checks a status bar control to determine if it is in simple mode.</span></span>

## <a name="parameters"></a><span data-ttu-id="cf906-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf906-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf906-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cf906-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cf906-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="cf906-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cf906-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cf906-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="cf906-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="cf906-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf906-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cf906-111">Return value</span></span>

<span data-ttu-id="cf906-112">Retornará zero se o controle da barra de status estiver no modo simples ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="cf906-112">Returns nonzero if the status bar control is in simple mode, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf906-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf906-113">Requirements</span></span>



| <span data-ttu-id="cf906-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf906-114">Requirement</span></span> | <span data-ttu-id="cf906-115">Valor</span><span class="sxs-lookup"><span data-stu-id="cf906-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf906-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf906-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cf906-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cf906-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cf906-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf906-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cf906-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cf906-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cf906-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cf906-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf906-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf906-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





