---
title: Mensagem de HDM_CREATEDRAGIMAGE (commctrl. h)
description: Cria uma versão semitransparente da imagem de um item para uso como uma imagem de arrastar. Você pode enviar essa mensagem explicitamente ou usar a \_ macro CreateDragImage do cabeçalho.
ms.assetid: 1b9dc515-d327-4634-a424-cc15a32f0f7c
keywords:
- Controles de HDM_CREATEDRAGIMAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9e801ad9771205b5f2e6df8e37bb0a0ad7f0bc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009526"
---
# <a name="hdm_createdragimage-message"></a><span data-ttu-id="a264f-105">\_Mensagem HDM CREATEDRAGIMAGE</span><span class="sxs-lookup"><span data-stu-id="a264f-105">HDM\_CREATEDRAGIMAGE message</span></span>

<span data-ttu-id="a264f-106">Cria uma versão semitransparente da imagem de um item para uso como uma imagem de arrastar.</span><span class="sxs-lookup"><span data-stu-id="a264f-106">Creates a semi-transparent version of an item's image for use as a dragging image.</span></span> <span data-ttu-id="a264f-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ CreateDragImage do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_createdragimage) .</span><span class="sxs-lookup"><span data-stu-id="a264f-107">You can send this message explicitly or use the [**Header\_CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-header_createdragimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a264f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a264f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a264f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a264f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a264f-110">O índice de base zero do item dentro do controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="a264f-110">The zero-based index of the item within the header control.</span></span> <span data-ttu-id="a264f-111">A imagem atribuída a esse item é a base para a imagem transparente.</span><span class="sxs-lookup"><span data-stu-id="a264f-111">The image assigned to this item is the basis for the transparent image.</span></span>

</dd> <dt>

<span data-ttu-id="a264f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a264f-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a264f-113">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a264f-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a264f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a264f-114">Return value</span></span>

<span data-ttu-id="a264f-115">Retorna um identificador para uma lista de imagens que contém a nova imagem como seu único elemento.</span><span class="sxs-lookup"><span data-stu-id="a264f-115">Returns a handle to an image list that contains the new image as its only element.</span></span>

## <a name="requirements"></a><span data-ttu-id="a264f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a264f-116">Requirements</span></span>



| <span data-ttu-id="a264f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a264f-117">Requirement</span></span> | <span data-ttu-id="a264f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a264f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a264f-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a264f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a264f-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a264f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a264f-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a264f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a264f-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a264f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a264f-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a264f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a264f-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a264f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





