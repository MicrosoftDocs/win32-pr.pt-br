---
title: Mensagem de TCM_SETIMAGELIST (commctrl. h)
description: Atribui uma lista de imagens a um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ SetImageList.
ms.assetid: b457c73c-4c38-4bc5-af5d-12bbd24504a6
keywords:
- Controles de TCM_SETIMAGELIST de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59172c677998e816b295939c14effe45ff8aa961
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008846"
---
# <a name="tcm_setimagelist-message"></a><span data-ttu-id="3be48-105">Mensagem do TCM \_ SETimagelist</span><span class="sxs-lookup"><span data-stu-id="3be48-105">TCM\_SETIMAGELIST message</span></span>

<span data-ttu-id="3be48-106">Atribui uma lista de imagens a um controle guia.</span><span class="sxs-lookup"><span data-stu-id="3be48-106">Assigns an image list to a tab control.</span></span> <span data-ttu-id="3be48-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setimagelist) .</span><span class="sxs-lookup"><span data-stu-id="3be48-107">You can send this message explicitly or by using the [**TabCtrl\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3be48-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3be48-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3be48-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3be48-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3be48-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3be48-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3be48-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3be48-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3be48-112">Identificador para a lista de imagens a ser atribuída ao controle guia.</span><span class="sxs-lookup"><span data-stu-id="3be48-112">Handle to the image list to assign to the tab control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3be48-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3be48-113">Return value</span></span>

<span data-ttu-id="3be48-114">Retorna o identificador para a lista de imagens anterior, ou **NULL** se não houver nenhuma lista de imagens anterior.</span><span class="sxs-lookup"><span data-stu-id="3be48-114">Returns the handle to the previous image list, or **NULL** if there is no previous image list.</span></span>

## <a name="requirements"></a><span data-ttu-id="3be48-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3be48-115">Requirements</span></span>



| <span data-ttu-id="3be48-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3be48-116">Requirement</span></span> | <span data-ttu-id="3be48-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3be48-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3be48-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3be48-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3be48-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3be48-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3be48-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3be48-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3be48-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3be48-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3be48-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3be48-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3be48-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3be48-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





