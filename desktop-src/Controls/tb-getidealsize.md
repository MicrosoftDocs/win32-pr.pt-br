---
title: Mensagem de TB_GETIDEALSIZE (commctrl. h)
description: Obtém o tamanho ideal da barra de ferramentas.
ms.assetid: d3b5ea4d-fd80-4f07-be4f-89b53a8bdf4d
keywords:
- Controles de TB_GETIDEALSIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a59b8701a4f4debcfb8e43f37068e7e7a4ef4f11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008994"
---
# <a name="tb_getidealsize-message"></a><span data-ttu-id="94d45-104">TB de \_ mensagem GETIDEALSIZE</span><span class="sxs-lookup"><span data-stu-id="94d45-104">TB\_GETIDEALSIZE message</span></span>

<span data-ttu-id="94d45-105">Obtém o tamanho ideal da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="94d45-105">Gets the ideal size of the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="94d45-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94d45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94d45-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="94d45-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="94d45-108">Um **bool** que indica se a altura ou a largura ideal da barra de ferramentas é recuperada.</span><span class="sxs-lookup"><span data-stu-id="94d45-108">A **BOOL** that indicates whether to retrieve the ideal height or width of the toolbar.</span></span> <span data-ttu-id="94d45-109">Use **true** para recuperar a altura ideal, **false** para recuperar a largura ideal.</span><span class="sxs-lookup"><span data-stu-id="94d45-109">Use **TRUE** to retrieve the ideal height, **FALSE** to retrieve the ideal width.</span></span></dd> <dt>

<span data-ttu-id="94d45-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="94d45-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94d45-111">Ponteiro para uma estrutura de [**tamanho**](/previous-versions//dd145106(v=vs.85)) que recebe a altura ou largura na qual todos os botões seriam exibidos.</span><span class="sxs-lookup"><span data-stu-id="94d45-111">Pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure that receives the height or width at which all buttons would be displayed.</span></span> <span data-ttu-id="94d45-112">Se *wParam* for **true**, somente o membro **CY** (Height) será válido.</span><span class="sxs-lookup"><span data-stu-id="94d45-112">If *wParam* is **TRUE**, only the **cy** member (height) is valid.</span></span> <span data-ttu-id="94d45-113">Se *wParam* for **false**, somente o membro **CX** (Width) será válido.</span><span class="sxs-lookup"><span data-stu-id="94d45-113">If *wParam* is **FALSE**, only the **cx** member (width) is valid.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94d45-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="94d45-114">Return value</span></span>

<span data-ttu-id="94d45-115">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="94d45-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="94d45-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94d45-116">Requirements</span></span>



| <span data-ttu-id="94d45-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="94d45-117">Requirement</span></span> | <span data-ttu-id="94d45-118">Valor</span><span class="sxs-lookup"><span data-stu-id="94d45-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="94d45-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94d45-119">Minimum supported client</span></span><br/> | <span data-ttu-id="94d45-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="94d45-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="94d45-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94d45-121">Minimum supported server</span></span><br/> | <span data-ttu-id="94d45-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="94d45-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="94d45-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="94d45-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="94d45-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="94d45-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

