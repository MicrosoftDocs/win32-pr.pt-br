---
title: Mensagem de TCM_SETMINTABWIDTH (commctrl. h)
description: Define a largura mínima dos itens em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ SetMinTabWidth.
ms.assetid: c0be3d4e-774c-4233-820f-01ffbb69ecf0
keywords:
- Controles de TCM_SETMINTABWIDTH de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_SETMINTABWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87208275ed52c638751352761961ce1f42e6944a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749303"
---
# <a name="tcm_setmintabwidth-message"></a><span data-ttu-id="65ef9-105">\_Mensagem SETMINTABWIDTH de TCM</span><span class="sxs-lookup"><span data-stu-id="65ef9-105">TCM\_SETMINTABWIDTH message</span></span>

<span data-ttu-id="65ef9-106">Define a largura mínima dos itens em um controle guia.</span><span class="sxs-lookup"><span data-stu-id="65ef9-106">Sets the minimum width of items in a tab control.</span></span> <span data-ttu-id="65ef9-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ SetMinTabWidth**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setmintabwidth) .</span><span class="sxs-lookup"><span data-stu-id="65ef9-107">You can send this message explicitly or by using the [**TabCtrl\_SetMinTabWidth**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setmintabwidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="65ef9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65ef9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65ef9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="65ef9-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="65ef9-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="65ef9-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="65ef9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="65ef9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="65ef9-112">Largura mínima a ser definida para um item de controle de guia.</span><span class="sxs-lookup"><span data-stu-id="65ef9-112">Minimum width to be set for a tab control item.</span></span> <span data-ttu-id="65ef9-113">Se esse parâmetro for definido como-1, o controle usará a largura de guia padrão.</span><span class="sxs-lookup"><span data-stu-id="65ef9-113">If this parameter is set to -1, the control will use the default tab width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65ef9-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="65ef9-114">Return value</span></span>

<span data-ttu-id="65ef9-115">Retorna um valor INT que representa a largura de tabulação mínima anterior.</span><span class="sxs-lookup"><span data-stu-id="65ef9-115">Returns an INT value that represents the previous minimum tab width.</span></span>

## <a name="requirements"></a><span data-ttu-id="65ef9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65ef9-116">Requirements</span></span>



| <span data-ttu-id="65ef9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="65ef9-117">Requirement</span></span> | <span data-ttu-id="65ef9-118">Valor</span><span class="sxs-lookup"><span data-stu-id="65ef9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65ef9-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65ef9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="65ef9-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="65ef9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="65ef9-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65ef9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="65ef9-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="65ef9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="65ef9-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="65ef9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="65ef9-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="65ef9-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





