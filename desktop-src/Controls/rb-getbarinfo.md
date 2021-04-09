---
title: Mensagem de RB_GETBARINFO (commctrl. h)
description: Recupera informações sobre o controle rebar e a lista de imagens que ele usa.
ms.assetid: d3d56b95-7540-4e45-bb2e-b9d41cfcca0d
keywords:
- Controles de RB_GETBARINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_GETBARINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d224c7c826bad0d5d6ae76ce5a4c2266632fa8a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009553"
---
# <a name="rb_getbarinfo-message"></a><span data-ttu-id="7b475-104">\_Mensagem GETBARINFO RB</span><span class="sxs-lookup"><span data-stu-id="7b475-104">RB\_GETBARINFO message</span></span>

<span data-ttu-id="7b475-105">Recupera informações sobre o controle rebar e a lista de imagens que ele usa.</span><span class="sxs-lookup"><span data-stu-id="7b475-105">Retrieves information about the rebar control and the image list it uses.</span></span>

## <a name="parameters"></a><span data-ttu-id="7b475-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b475-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b475-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7b475-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7b475-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7b475-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7b475-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7b475-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7b475-110">Ponteiro para uma estrutura [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) que receberá as informações de controle rebar.</span><span class="sxs-lookup"><span data-stu-id="7b475-110">Pointer to a [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) structure that will receive the rebar control information.</span></span> <span data-ttu-id="7b475-111">Você deve definir o membro **cbSize** dessa estrutura como **sizeof**(REBARINFO) antes de enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="7b475-111">You must set the **cbSize** member of this structure to **sizeof**(REBARINFO) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b475-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7b475-112">Return value</span></span>

<span data-ttu-id="7b475-113">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="7b475-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b475-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b475-114">Requirements</span></span>



| <span data-ttu-id="7b475-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b475-115">Requirement</span></span> | <span data-ttu-id="7b475-116">Valor</span><span class="sxs-lookup"><span data-stu-id="7b475-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7b475-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b475-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7b475-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7b475-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7b475-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b475-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7b475-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7b475-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7b475-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7b475-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b475-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b475-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





