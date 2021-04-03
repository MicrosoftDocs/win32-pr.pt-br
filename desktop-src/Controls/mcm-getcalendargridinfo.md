---
title: Mensagem de MCM_GETCALENDARGRIDINFO (commctrl. h)
description: Obtém informações sobre uma grade de calendário.
ms.assetid: 6b385362-f963-4041-bc9f-d2b7a890c9b4
keywords:
- Controles de MCM_GETCALENDARGRIDINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_GETCALENDARGRIDINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506f6193ab32d059bb85fa4583441bfbe027f224
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645273"
---
# <a name="mcm_getcalendargridinfo-message"></a><span data-ttu-id="ea0e3-104">\_Mensagem MCM GETCALENDARGRIDINFO</span><span class="sxs-lookup"><span data-stu-id="ea0e3-104">MCM\_GETCALENDARGRIDINFO message</span></span>

<span data-ttu-id="ea0e3-105">Obtém informações sobre uma grade de calendário.</span><span class="sxs-lookup"><span data-stu-id="ea0e3-105">Gets information about a calendar grid.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea0e3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea0e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea0e3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea0e3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea0e3-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ea0e3-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ea0e3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea0e3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea0e3-110">Ponteiro para uma estrutura [**MCGRIDINFO**](/windows/win32/api/commctrl/ns-commctrl-mcgridinfo) que contém informações sobre a grade de calendário.</span><span class="sxs-lookup"><span data-stu-id="ea0e3-110">Pointer to an [**MCGRIDINFO**](/windows/win32/api/commctrl/ns-commctrl-mcgridinfo) structure that contains information about the calendar grid.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea0e3-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ea0e3-111">Return value</span></span>

<span data-ttu-id="ea0e3-112">**True** se for bem-sucedido; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="ea0e3-112">**TRUE** if successful, otherwise **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea0e3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea0e3-113">Requirements</span></span>



| <span data-ttu-id="ea0e3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea0e3-114">Requirement</span></span> | <span data-ttu-id="ea0e3-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ea0e3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea0e3-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea0e3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ea0e3-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ea0e3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea0e3-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea0e3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ea0e3-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ea0e3-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea0e3-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ea0e3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea0e3-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea0e3-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





