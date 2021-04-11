---
title: Mensagem de DTM_GETIDEALSIZE (commctrl. h)
description: Obtém o tamanho necessário para exibir o controle sem recorte. Envie essa mensagem explicitamente ou usando a macro DateTime \_ GetIdealSize.
ms.assetid: 15ec26a1-645b-4a96-af66-1031e1a46c6c
keywords:
- Controles de DTM_GETIDEALSIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- DTM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a979883f431fea4627f52fe19c3716341e3f2328
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163585"
---
# <a name="dtm_getidealsize-message"></a><span data-ttu-id="49325-105">\_Mensagem DTM GETIDEALSIZE</span><span class="sxs-lookup"><span data-stu-id="49325-105">DTM\_GETIDEALSIZE message</span></span>

<span data-ttu-id="49325-106">Obtém o tamanho necessário para exibir o controle sem recorte.</span><span class="sxs-lookup"><span data-stu-id="49325-106">Gets the size needed to display the control without clipping.</span></span> <span data-ttu-id="49325-107">Envie essa mensagem explicitamente ou usando a macro [**DateTime \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize) .</span><span class="sxs-lookup"><span data-stu-id="49325-107">Send this message explicitly or by using the [**DateTime\_GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="49325-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49325-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49325-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49325-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49325-110">Não usado.</span><span class="sxs-lookup"><span data-stu-id="49325-110">Not used.</span></span> <span data-ttu-id="49325-111">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="49325-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="49325-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49325-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49325-113">Um ponteiro para uma estrutura de [**tamanho**](/previous-versions//dd145106(v=vs.85)) para receber o tamanho ideal.</span><span class="sxs-lookup"><span data-stu-id="49325-113">A pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure to receive the ideal size.</span></span> <span data-ttu-id="49325-114">O aplicativo de chamada é responsável por alocar essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="49325-114">The calling application is responsible for allocating this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49325-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="49325-115">Return value</span></span>

<span data-ttu-id="49325-116">Retorna **true**.</span><span class="sxs-lookup"><span data-stu-id="49325-116">Returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="49325-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49325-117">Requirements</span></span>



| <span data-ttu-id="49325-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="49325-118">Requirement</span></span> | <span data-ttu-id="49325-119">Valor</span><span class="sxs-lookup"><span data-stu-id="49325-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49325-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49325-120">Minimum supported client</span></span><br/> | <span data-ttu-id="49325-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="49325-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="49325-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49325-122">Minimum supported server</span></span><br/> | <span data-ttu-id="49325-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="49325-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="49325-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="49325-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="49325-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="49325-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

