---
title: Mensagem de LVM_CREATEDRAGIMAGE (commctrl. h)
description: Cria uma lista de imagens de arrastar para o item especificado. Você pode enviar essa mensagem explicitamente ou usando a \_ macro CreateDragImage do ListView.
ms.assetid: face4c8f-01ff-4f5a-a468-e306a50dae35
keywords:
- Controles de LVM_CREATEDRAGIMAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace975b178fee85e2794b518a78b40b375c65ae7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085176"
---
# <a name="lvm_createdragimage-message"></a><span data-ttu-id="2fa2b-105">\_Mensagem CREATEDRAGIMAGE LVM</span><span class="sxs-lookup"><span data-stu-id="2fa2b-105">LVM\_CREATEDRAGIMAGE message</span></span>

<span data-ttu-id="2fa2b-106">Cria uma lista de imagens de arrastar para o item especificado.</span><span class="sxs-lookup"><span data-stu-id="2fa2b-106">Creates a drag image list for the specified item.</span></span> <span data-ttu-id="2fa2b-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ CreateDragImage do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_createdragimage) .</span><span class="sxs-lookup"><span data-stu-id="2fa2b-107">You can send this message explicitly or by using the [**ListView\_CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_createdragimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2fa2b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2fa2b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fa2b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2fa2b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2fa2b-110">O índice do item.</span><span class="sxs-lookup"><span data-stu-id="2fa2b-110">The index of the item.</span></span>

</dd> <dt>

<span data-ttu-id="2fa2b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2fa2b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2fa2b-112">Um ponteiro para uma estrutura de [**ponto**](/previous-versions//dd162805(v=vs.85)) que recebe o local inicial do canto superior esquerdo da imagem, em Exibir coordenadas.</span><span class="sxs-lookup"><span data-stu-id="2fa2b-112">A pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that receives the initial location of the upper-left corner of the image, in view coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fa2b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2fa2b-113">Return value</span></span>

<span data-ttu-id="2fa2b-114">Retorna o identificador para a lista de imagens de arrastar, se for bem-sucedido, ou **NULL** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="2fa2b-114">Returns the handle to the drag image list if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fa2b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="2fa2b-115">Remarks</span></span>

<span data-ttu-id="2fa2b-116">Seu aplicativo é responsável por destruir a lista de imagens quando ela não é mais necessária.</span><span class="sxs-lookup"><span data-stu-id="2fa2b-116">Your application is responsible for destroying the image list when it is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fa2b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fa2b-117">Requirements</span></span>



| <span data-ttu-id="2fa2b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fa2b-118">Requirement</span></span> | <span data-ttu-id="2fa2b-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2fa2b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2fa2b-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2fa2b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2fa2b-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2fa2b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2fa2b-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2fa2b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2fa2b-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2fa2b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2fa2b-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2fa2b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fa2b-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fa2b-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

