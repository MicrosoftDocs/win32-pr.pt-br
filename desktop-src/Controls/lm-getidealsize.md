---
title: Mensagem de LM_GETIDEALSIZE (commctrl. h)
description: Mensagem de LM_GETIDEALSIZE – recupera a altura preferida de um link para a largura atual do controle.
ms.assetid: 63aad7eb-26ee-41d2-90d4-65fdcf0f182a
keywords:
- Controles de LM_GETIDEALSIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- LM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 761fb5f6e5f7a2e2e9b1b9cc862b9a8f2c0fcd1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112384"
---
# <a name="lm_getidealsize-message"></a><span data-ttu-id="6b951-104">\_Mensagem GETIDEALSIZE de LM</span><span class="sxs-lookup"><span data-stu-id="6b951-104">LM\_GETIDEALSIZE message</span></span>

<span data-ttu-id="6b951-105">Recupera a altura preferida de um link para a largura atual do controle.</span><span class="sxs-lookup"><span data-stu-id="6b951-105">Retrieves the preferred height of a link for the control's current width.</span></span>

## <a name="parameters"></a><span data-ttu-id="6b951-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b951-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b951-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b951-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6b951-108">Largura máxima do link, em pixels.</span><span class="sxs-lookup"><span data-stu-id="6b951-108">Maximum width of the link, in pixels.</span></span></dd> <dt>

<span data-ttu-id="6b951-109">*lParam* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6b951-109">*lParam* \[out\]</span></span>
</dt> <dd><span data-ttu-id="6b951-110">Quando essa mensagem retorna, contém um ponteiro para uma estrutura de <a href="/previous-versions//dd145106(v=vs.85)">**tamanho**</a> .</span><span class="sxs-lookup"><span data-stu-id="6b951-110">When this message returns, contains a pointer to a <a href="/previous-versions//dd145106(v=vs.85)">**SIZE**</a> structure.</span></span> <span data-ttu-id="6b951-111">O membro **CY** desta estrutura indica a altura ideal do controle para a largura especificada.</span><span class="sxs-lookup"><span data-stu-id="6b951-111">The **cy** member of this structure indicates the ideal height of the control for the given width.</span></span> <span data-ttu-id="6b951-112">Ele ajusta o membro do **CX** para a quantidade de espaço realmente necessária.</span><span class="sxs-lookup"><span data-stu-id="6b951-112">It adjusts the **cx** member to the amount of space actually needed.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b951-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6b951-113">Return value</span></span>

<span data-ttu-id="6b951-114">Inteiro que representa a altura preferida do texto do link, em pixels.</span><span class="sxs-lookup"><span data-stu-id="6b951-114">Integer that represents the preferred height of the link text, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b951-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b951-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6b951-116">Para usar essa API, você deve fornecer um manifesto que especifique Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="6b951-116">To use this API, you must provide a manifest that specifies Comclt32.dll version 6.0.</span></span> <span data-ttu-id="6b951-117">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6b951-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6b951-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b951-118">Requirements</span></span>



| <span data-ttu-id="6b951-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b951-119">Requirement</span></span> | <span data-ttu-id="6b951-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6b951-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b951-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b951-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6b951-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6b951-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6b951-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b951-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6b951-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6b951-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6b951-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6b951-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b951-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b951-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

