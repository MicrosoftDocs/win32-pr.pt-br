---
title: Mensagem de SB_GETICON (commctrl. h)
description: Recupera o ícone de uma parte em uma barra de status.
ms.assetid: f99508e3-afa8-48fd-b87a-fce41c4410ff
keywords:
- Controles de SB_GETICON de mensagens do Windows
topic_type:
- apiref
api_name:
- SB_GETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab86809df54d796b8e83f05f2a2b9041450ce2fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824623"
---
# <a name="sb_geticon-message"></a><span data-ttu-id="72e1b-104">\_Mensagem de GETICON SB</span><span class="sxs-lookup"><span data-stu-id="72e1b-104">SB\_GETICON message</span></span>

<span data-ttu-id="72e1b-105">Recupera o ícone de uma parte em uma barra de status.</span><span class="sxs-lookup"><span data-stu-id="72e1b-105">Retrieves the icon for a part in a status bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="72e1b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72e1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72e1b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="72e1b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="72e1b-108">Índice de base zero da parte que contém o ícone a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="72e1b-108">Zero-based index of the part that contains the icon to be retrieved.</span></span> <span data-ttu-id="72e1b-109">Se esse parâmetro for-1, a barra de status será considerada uma barra de status de [modo simples](status-bars.md) .</span><span class="sxs-lookup"><span data-stu-id="72e1b-109">If this parameter is -1, the status bar is assumed to be a [Simple Mode](status-bars.md) status bar.</span></span>

</dd> <dt>

<span data-ttu-id="72e1b-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="72e1b-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="72e1b-111">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="72e1b-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72e1b-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="72e1b-112">Return value</span></span>

<span data-ttu-id="72e1b-113">Retorna o identificador para o ícone, se for bem-sucedido, ou **NULL** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="72e1b-113">Returns the handle to the icon if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="72e1b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72e1b-114">Requirements</span></span>



| <span data-ttu-id="72e1b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="72e1b-115">Requirement</span></span> | <span data-ttu-id="72e1b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="72e1b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="72e1b-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72e1b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="72e1b-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="72e1b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="72e1b-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72e1b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="72e1b-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="72e1b-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="72e1b-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="72e1b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="72e1b-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="72e1b-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





