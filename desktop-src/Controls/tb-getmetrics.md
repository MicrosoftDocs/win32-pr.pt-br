---
title: Mensagem de TB_GETMETRICS (commctrl. h)
description: Recupera as métricas de um controle ToolBar.
ms.assetid: 19c735cf-09f8-443e-8a73-dd64af0193a1
keywords:
- Controles de TB_GETMETRICS de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1ee299f56b367eef649a05657d713e22206a7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824616"
---
# <a name="tb_getmetrics-message"></a><span data-ttu-id="32ba2-104">Mensagem de $ \_ métricas de TB</span><span class="sxs-lookup"><span data-stu-id="32ba2-104">TB\_GETMETRICS message</span></span>

<span data-ttu-id="32ba2-105">Recupera as métricas de um controle ToolBar.</span><span class="sxs-lookup"><span data-stu-id="32ba2-105">Retrieves the metrics of a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="32ba2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32ba2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32ba2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="32ba2-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="32ba2-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="32ba2-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="32ba2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32ba2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32ba2-110">Ponteiro para uma estrutura [**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) que recebe as métricas da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="32ba2-110">Pointer to a [**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) structure that receives the toolbar metrics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32ba2-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="32ba2-111">Return value</span></span>

<span data-ttu-id="32ba2-112">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="32ba2-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="32ba2-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="32ba2-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="32ba2-114">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="32ba2-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="32ba2-115">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="32ba2-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="32ba2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32ba2-116">Requirements</span></span>



| <span data-ttu-id="32ba2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="32ba2-117">Requirement</span></span> | <span data-ttu-id="32ba2-118">Valor</span><span class="sxs-lookup"><span data-stu-id="32ba2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32ba2-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32ba2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="32ba2-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="32ba2-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="32ba2-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32ba2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="32ba2-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="32ba2-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="32ba2-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="32ba2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="32ba2-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="32ba2-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





