---
title: Mensagem de RB_SETBARINFO (commctrl. h)
description: Define as características de um controle rebar.
ms.assetid: e4413d46-574f-4ccd-b5fd-3ba6c1e3924b
keywords:
- Controles de RB_SETBARINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_SETBARINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b360bc0b4d14963619aad8f769634d7dd0ad17e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008922"
---
# <a name="rb_setbarinfo-message"></a><span data-ttu-id="f6c59-104">\_Mensagem SETBARINFO RB</span><span class="sxs-lookup"><span data-stu-id="f6c59-104">RB\_SETBARINFO message</span></span>

<span data-ttu-id="f6c59-105">Define as características de um controle rebar.</span><span class="sxs-lookup"><span data-stu-id="f6c59-105">Sets the characteristics of a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f6c59-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6c59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6c59-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f6c59-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f6c59-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f6c59-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f6c59-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f6c59-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6c59-110">Ponteiro para uma estrutura [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) que contém as informações a serem definidas.</span><span class="sxs-lookup"><span data-stu-id="f6c59-110">Pointer to a [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) structure that contains the information to be set.</span></span> <span data-ttu-id="f6c59-111">Você deve definir o membro **cbSize** dessa estrutura como **sizeof**(REBARINFO) antes de enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="f6c59-111">You must set the **cbSize** member of this structure to **sizeof**(REBARINFO) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6c59-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f6c59-112">Return value</span></span>

<span data-ttu-id="f6c59-113">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="f6c59-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6c59-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6c59-114">Requirements</span></span>



| <span data-ttu-id="f6c59-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6c59-115">Requirement</span></span> | <span data-ttu-id="f6c59-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f6c59-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f6c59-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6c59-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f6c59-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f6c59-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f6c59-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6c59-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f6c59-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f6c59-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f6c59-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f6c59-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6c59-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6c59-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





