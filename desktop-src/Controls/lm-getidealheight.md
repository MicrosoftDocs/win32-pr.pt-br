---
title: Mensagem de LM_GETIDEALHEIGHT (commctrl. h)
description: Mensagem de LM_GETIDEALHEIGHT – recupera a altura preferida de um link para a largura atual do controle.
ms.assetid: bf6ef3c1-89bc-4c56-9384-085fd00234e1
keywords:
- Controles de LM_GETIDEALHEIGHT de mensagens do Windows
topic_type:
- apiref
api_name:
- LM_GETIDEALHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d6e82f259124e6da285ed2357d48ca07d5f8c08
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112394"
---
# <a name="lm_getidealheight-message"></a><span data-ttu-id="0edbd-104">\_Mensagem GETIDEALHEIGHT de LM</span><span class="sxs-lookup"><span data-stu-id="0edbd-104">LM\_GETIDEALHEIGHT message</span></span>

<span data-ttu-id="0edbd-105">Recupera a altura preferida de um link para a largura atual do controle.</span><span class="sxs-lookup"><span data-stu-id="0edbd-105">Retrieves the preferred height of a link for the control's current width.</span></span>

## <a name="parameters"></a><span data-ttu-id="0edbd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0edbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0edbd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0edbd-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0edbd-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0edbd-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0edbd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0edbd-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0edbd-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0edbd-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0edbd-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0edbd-111">Return value</span></span>

<span data-ttu-id="0edbd-112">Inteiro que representa a altura preferida do texto do link, em pixels.</span><span class="sxs-lookup"><span data-stu-id="0edbd-112">Integer representing the preferred height of the link text, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="0edbd-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0edbd-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0edbd-114">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="0edbd-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="0edbd-115">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0edbd-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0edbd-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0edbd-116">Requirements</span></span>



| <span data-ttu-id="0edbd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0edbd-117">Requirement</span></span> | <span data-ttu-id="0edbd-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0edbd-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0edbd-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0edbd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0edbd-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0edbd-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0edbd-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0edbd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0edbd-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0edbd-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0edbd-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0edbd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0edbd-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0edbd-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





