---
title: Mensagem de TB_GETBUTTONSIZE (commctrl. h)
description: Recupera a largura e a altura atuais dos botões da barra de ferramentas, em pixels.
ms.assetid: c1b72494-670b-4cf8-a78f-c67b6eee0677
keywords:
- Controles de TB_GETBUTTONSIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6a414f5b338353d7d8ce22a081e9b711a2b56a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824845"
---
# <a name="tb_getbuttonsize-message"></a><span data-ttu-id="80eb8-104">A \_ mensagem de TB GETbuttons</span><span class="sxs-lookup"><span data-stu-id="80eb8-104">TB\_GETBUTTONSIZE message</span></span>

<span data-ttu-id="80eb8-105">Recupera a largura e a altura atuais dos botões da barra de ferramentas, em pixels.</span><span class="sxs-lookup"><span data-stu-id="80eb8-105">Retrieves the current width and height of toolbar buttons, in pixels.</span></span>

## <a name="parameters"></a><span data-ttu-id="80eb8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80eb8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80eb8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="80eb8-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="80eb8-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="80eb8-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="80eb8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="80eb8-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="80eb8-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="80eb8-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80eb8-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="80eb8-111">Return value</span></span>

<span data-ttu-id="80eb8-112">Retorna um valor **DWORD** que contém os valores de largura e altura na palavra inferior e na palavra alta, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="80eb8-112">Returns a **DWORD** value that contains the width and height values in the low word and high word, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="80eb8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80eb8-113">Requirements</span></span>



| <span data-ttu-id="80eb8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="80eb8-114">Requirement</span></span> | <span data-ttu-id="80eb8-115">Valor</span><span class="sxs-lookup"><span data-stu-id="80eb8-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="80eb8-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80eb8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="80eb8-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="80eb8-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="80eb8-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80eb8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="80eb8-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="80eb8-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="80eb8-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="80eb8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="80eb8-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="80eb8-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





