---
title: Mensagem de TTM_GETTITLE (commctrl. h)
description: Recupere informações relativas ao título de um controle ToolTip.
ms.assetid: d8992dd1-1610-44e8-8c0f-8ae1ac4b5898
keywords:
- Controles de TTM_GETTITLE de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_GETTITLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0048925ed3dc267ac07b10b85e2ea1ca1449996c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918467"
---
# <a name="ttm_gettitle-message"></a><span data-ttu-id="0f98c-104">\_Mensagem de GETtitle do TTM</span><span class="sxs-lookup"><span data-stu-id="0f98c-104">TTM\_GETTITLE message</span></span>

<span data-ttu-id="0f98c-105">Recupere informações relativas ao título de um controle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="0f98c-105">Retrieve information concerning the title of a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="0f98c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f98c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f98c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0f98c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0f98c-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0f98c-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0f98c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0f98c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f98c-110">Ponteiro para uma estrutura [**TTGETTITLE**](/windows/desktop/api/Commctrl/ns-commctrl-ttgettitle) que contém informações sobre um título de dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="0f98c-110">Pointer to a [**TTGETTITLE**](/windows/desktop/api/Commctrl/ns-commctrl-ttgettitle) structure that contains information about a tooltip title.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f98c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0f98c-111">Return value</span></span>

<span data-ttu-id="0f98c-112">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="0f98c-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f98c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f98c-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0f98c-114">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="0f98c-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="0f98c-115">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0f98c-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0f98c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f98c-116">Requirements</span></span>



| <span data-ttu-id="0f98c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f98c-117">Requirement</span></span> | <span data-ttu-id="0f98c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0f98c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0f98c-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f98c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0f98c-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0f98c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0f98c-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f98c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0f98c-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0f98c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0f98c-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0f98c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f98c-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f98c-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





