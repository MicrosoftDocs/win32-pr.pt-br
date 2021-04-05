---
title: Mensagem de CBEM_SETIMAGELIST (commctrl. h)
description: Define uma lista de imagens para um controle ComboBoxEx.
ms.assetid: a4a8ed61-a532-4cf8-8291-c157ab0e7f31
keywords:
- Controles de CBEM_SETIMAGELIST de mensagens do Windows
topic_type:
- apiref
api_name:
- CBEM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33816abe36e2d1e1593e6365061a500d072c155b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919090"
---
# <a name="cbem_setimagelist-message"></a><span data-ttu-id="c8c4f-104">\_Mensagem CBEM SETimagelist</span><span class="sxs-lookup"><span data-stu-id="c8c4f-104">CBEM\_SETIMAGELIST message</span></span>

<span data-ttu-id="c8c4f-105">Define uma lista de imagens para um controle ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="c8c4f-105">Sets an image list for a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c8c4f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8c4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8c4f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c8c4f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c8c4f-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c8c4f-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c8c4f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8c4f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8c4f-110">Um identificador para a lista de imagens a ser definido para o controle.</span><span class="sxs-lookup"><span data-stu-id="c8c4f-110">A handle to the image list to be set for the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8c4f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c8c4f-111">Return value</span></span>

<span data-ttu-id="c8c4f-112">Retorna o identificador para a lista de imagens associada anteriormente ao controle ou retorna **NULL** se nenhuma lista de imagens tiver sido definida anteriormente.</span><span class="sxs-lookup"><span data-stu-id="c8c4f-112">Returns the handle to the image list previously associated with the control, or returns **NULL** if no image list was previously set.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8c4f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8c4f-113">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c8c4f-114">A altura das imagens na sua lista de imagens pode alterar os requisitos de tamanho do controle ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="c8c4f-114">The height of images in your image list might change the size requirements of the ComboBoxEx control.</span></span> <span data-ttu-id="c8c4f-115">É recomendável que você redimensione o controle depois de enviar essa mensagem para garantir que ela seja exibida corretamente.</span><span class="sxs-lookup"><span data-stu-id="c8c4f-115">It is recommended that you resize the control after sending this message to ensure that it is displayed properly.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c8c4f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8c4f-116">Requirements</span></span>



| <span data-ttu-id="c8c4f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8c4f-117">Requirement</span></span> | <span data-ttu-id="c8c4f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c8c4f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c8c4f-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8c4f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c8c4f-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c8c4f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c8c4f-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8c4f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c8c4f-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c8c4f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c8c4f-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c8c4f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8c4f-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8c4f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





