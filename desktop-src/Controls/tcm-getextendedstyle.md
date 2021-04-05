---
title: Mensagem de TCM_GETEXTENDEDSTYLE (commctrl. h)
description: Recupera os estilos estendidos que estão em uso no momento para o controle de guia. Você pode enviar essa mensagem explicitamente ou usando a \_ macro Extended TabCtrl.
ms.assetid: 983ffcbe-0d8d-4686-83de-fc564744390f
keywords:
- Controles de TCM_GETEXTENDEDSTYLE de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8280b7043591dd4fdd0b453c5baea5fe014bd3d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919020"
---
# <a name="tcm_getextendedstyle-message"></a><span data-ttu-id="81d91-105">Mensagem do TCM \_ Extended</span><span class="sxs-lookup"><span data-stu-id="81d91-105">TCM\_GETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="81d91-106">Recupera os estilos estendidos que estão em uso no momento para o controle de guia.</span><span class="sxs-lookup"><span data-stu-id="81d91-106">Retrieves the extended styles that are currently in use for the tab control.</span></span> <span data-ttu-id="81d91-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ Extended TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getextendedstyle) .</span><span class="sxs-lookup"><span data-stu-id="81d91-107">You can send this message explicitly or by using the [**TabCtrl\_GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getextendedstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="81d91-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81d91-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81d91-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="81d91-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="81d91-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="81d91-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="81d91-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="81d91-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="81d91-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="81d91-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81d91-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="81d91-113">Return value</span></span>

<span data-ttu-id="81d91-114">Retorna um valor **DWORD** que representa os estilos estendidos em uso no momento para o controle de guia.</span><span class="sxs-lookup"><span data-stu-id="81d91-114">Returns a **DWORD** value that represents the extended styles currently in use for the tab control.</span></span> <span data-ttu-id="81d91-115">Esse valor é uma combinação de [estilos estendidos](tab-control-extended-styles.md)de controle de guia.</span><span class="sxs-lookup"><span data-stu-id="81d91-115">This value is a combination of tab control [extended styles](tab-control-extended-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="81d91-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81d91-116">Requirements</span></span>



| <span data-ttu-id="81d91-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="81d91-117">Requirement</span></span> | <span data-ttu-id="81d91-118">Valor</span><span class="sxs-lookup"><span data-stu-id="81d91-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81d91-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81d91-119">Minimum supported client</span></span><br/> | <span data-ttu-id="81d91-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="81d91-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="81d91-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81d91-121">Minimum supported server</span></span><br/> | <span data-ttu-id="81d91-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="81d91-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="81d91-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="81d91-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="81d91-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="81d91-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81d91-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="81d91-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81d91-126">**TCM \_ SETextendedattribute**</span><span class="sxs-lookup"><span data-stu-id="81d91-126">**TCM\_SETEXTENDEDSTYLE**</span></span>](tcm-setextendedstyle.md)
</dt> </dl>

 

 





