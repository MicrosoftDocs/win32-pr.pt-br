---
title: Mensagem de TB_AUTOSIZE (commctrl. h)
description: Faz com que uma barra de ferramentas seja redimensionada.
ms.assetid: 11aff184-6f18-43a2-9bdc-462fc5ba1680
keywords:
- Controles de TB_AUTOSIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_AUTOSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5f901463888338fd9cadf67472232efe9a25f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499864"
---
# <a name="tb_autosize-message"></a><span data-ttu-id="6e0f4-104">\_Mensagem AUTOSIZE de TB</span><span class="sxs-lookup"><span data-stu-id="6e0f4-104">TB\_AUTOSIZE message</span></span>

<span data-ttu-id="6e0f4-105">Faz com que uma barra de ferramentas seja redimensionada.</span><span class="sxs-lookup"><span data-stu-id="6e0f4-105">Causes a toolbar to be resized.</span></span>

## <a name="parameters"></a><span data-ttu-id="6e0f4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e0f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e0f4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6e0f4-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6e0f4-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6e0f4-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6e0f4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6e0f4-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6e0f4-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6e0f4-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e0f4-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6e0f4-111">Return value</span></span>

<span data-ttu-id="6e0f4-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="6e0f4-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e0f4-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e0f4-113">Remarks</span></span>

<span data-ttu-id="6e0f4-114">Um aplicativo envia a **mensagem \_ dimensionamento automático de TB** depois de fazer com que o tamanho de uma barra de ferramentas seja alterado definindo o tamanho do botão ou do bitmap ou adicionando cadeias de caracteres pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="6e0f4-114">An application sends the **TB\_AUTOSIZE** message after causing the size of a toolbar to change either by setting the button or bitmap size or by adding strings for the first time.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e0f4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e0f4-115">Requirements</span></span>



| <span data-ttu-id="6e0f4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e0f4-116">Requirement</span></span> | <span data-ttu-id="6e0f4-117">Valor</span><span class="sxs-lookup"><span data-stu-id="6e0f4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6e0f4-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e0f4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6e0f4-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6e0f4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6e0f4-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e0f4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6e0f4-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6e0f4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6e0f4-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6e0f4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e0f4-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e0f4-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





