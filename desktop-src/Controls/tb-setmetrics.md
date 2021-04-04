---
title: Mensagem de TB_SETMETRICS (commctrl. h)
description: Define as métricas de um controle ToolBar.
ms.assetid: 60e35d65-6291-4a55-a4cf-19b5b1db8a65
keywords:
- Controles de TB_SETMETRICS de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5320ecc85f0a44c4c80868ae5699b051e1ac1781
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918165"
---
# <a name="tb_setmetrics-message"></a><span data-ttu-id="e9c5f-104">\_Mensagem de REavaliação de TB</span><span class="sxs-lookup"><span data-stu-id="e9c5f-104">TB\_SETMETRICS message</span></span>

<span data-ttu-id="e9c5f-105">Define as métricas de um controle ToolBar.</span><span class="sxs-lookup"><span data-stu-id="e9c5f-105">Sets the metrics of a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e9c5f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9c5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9c5f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e9c5f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e9c5f-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e9c5f-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e9c5f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9c5f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9c5f-110">Estrutura [**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) que contém as métricas da barra de ferramentas a serem definidas.</span><span class="sxs-lookup"><span data-stu-id="e9c5f-110">[**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) structure that contains the toolbar metrics to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9c5f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e9c5f-111">Return value</span></span>

<span data-ttu-id="e9c5f-112">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="e9c5f-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9c5f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9c5f-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e9c5f-114">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="e9c5f-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="e9c5f-115">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e9c5f-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e9c5f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9c5f-116">Requirements</span></span>



| <span data-ttu-id="e9c5f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9c5f-117">Requirement</span></span> | <span data-ttu-id="e9c5f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e9c5f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9c5f-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9c5f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e9c5f-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e9c5f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e9c5f-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9c5f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e9c5f-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e9c5f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e9c5f-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e9c5f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9c5f-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9c5f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





