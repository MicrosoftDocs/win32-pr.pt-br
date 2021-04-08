---
title: Mensagem de SB_SETICON (commctrl. h)
description: Define o ícone de uma parte em uma barra de status.
ms.assetid: d8528cd1-54d2-44ba-b0d6-29111f75616a
keywords:
- Controles de SB_SETICON de mensagens do Windows
topic_type:
- apiref
api_name:
- SB_SETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f720c414238eb89cf98bf0556ebabffefceae4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824620"
---
# <a name="sb_seticon-message"></a><span data-ttu-id="27206-104">\_Mensagem de SETICON SB</span><span class="sxs-lookup"><span data-stu-id="27206-104">SB\_SETICON message</span></span>

<span data-ttu-id="27206-105">Define o ícone de uma parte em uma barra de status.</span><span class="sxs-lookup"><span data-stu-id="27206-105">Sets the icon for a part in a status bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="27206-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27206-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27206-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="27206-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27206-108">O índice de base zero da parte que receberá o ícone.</span><span class="sxs-lookup"><span data-stu-id="27206-108">Zero-based index of the part that will receive the icon.</span></span> <span data-ttu-id="27206-109">Se esse parâmetro for-1, a barra de status será considerada uma barra de status simples.</span><span class="sxs-lookup"><span data-stu-id="27206-109">If this parameter is -1, the status bar is assumed to be a simple status bar.</span></span>

</dd> <dt>

<span data-ttu-id="27206-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="27206-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27206-111">Identificador para o ícone a ser definido.</span><span class="sxs-lookup"><span data-stu-id="27206-111">Handle to the icon to be set.</span></span> <span data-ttu-id="27206-112">Se esse valor for **nulo**, o ícone será removido da parte.</span><span class="sxs-lookup"><span data-stu-id="27206-112">If this value is **NULL**, the icon is removed from the part.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27206-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="27206-113">Return value</span></span>

<span data-ttu-id="27206-114">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="27206-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="27206-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="27206-115">Remarks</span></span>

<span data-ttu-id="27206-116">A barra de status não destruirá o ícone.</span><span class="sxs-lookup"><span data-stu-id="27206-116">The status bar will not destroy the icon.</span></span> <span data-ttu-id="27206-117">É responsabilidade do aplicativo de chamada manter o controle e destruir os ícones.</span><span class="sxs-lookup"><span data-stu-id="27206-117">It is the calling application's responsibility to keep track of and destroy any icons.</span></span>

## <a name="requirements"></a><span data-ttu-id="27206-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27206-118">Requirements</span></span>



| <span data-ttu-id="27206-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="27206-119">Requirement</span></span> | <span data-ttu-id="27206-120">Valor</span><span class="sxs-lookup"><span data-stu-id="27206-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="27206-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27206-121">Minimum supported client</span></span><br/> | <span data-ttu-id="27206-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="27206-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="27206-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27206-123">Minimum supported server</span></span><br/> | <span data-ttu-id="27206-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="27206-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="27206-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="27206-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="27206-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="27206-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





