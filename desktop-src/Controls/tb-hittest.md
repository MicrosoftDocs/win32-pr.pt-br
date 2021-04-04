---
title: Mensagem de TB_HITTEST (commctrl. h)
description: Determina onde um ponto reside em um controle ToolBar.
ms.assetid: d08f3805-2042-470e-8f5a-8a6a681d1189
keywords:
- Controles de TB_HITTEST de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6264bc0191f091d3819081ddd67e428b64c84570
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918268"
---
# <a name="tb_hittest-message"></a><span data-ttu-id="cb601-104">\_Mensagem HITTEST TB</span><span class="sxs-lookup"><span data-stu-id="cb601-104">TB\_HITTEST message</span></span>

<span data-ttu-id="cb601-105">Determina onde um ponto reside em um controle ToolBar.</span><span class="sxs-lookup"><span data-stu-id="cb601-105">Determines where a point lies in a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="cb601-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cb601-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb601-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cb601-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cb601-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="cb601-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cb601-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb601-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb601-110">Ponteiro para uma estrutura de [**ponto**](/previous-versions//dd162805(v=vs.85)) que contém a coordenada x do teste de clique no membro **x** e a coordenada y do teste de clique no membro **y** .</span><span class="sxs-lookup"><span data-stu-id="cb601-110">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that contains the x-coordinate of the hit test in the **x** member and the y-coordinate of the hit test in the **y** member.</span></span> <span data-ttu-id="cb601-111">As coordenadas são relativas à área do cliente da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="cb601-111">The coordinates are relative to the toolbar's client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb601-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cb601-112">Return value</span></span>

<span data-ttu-id="cb601-113">Retorna um valor inteiro.</span><span class="sxs-lookup"><span data-stu-id="cb601-113">Returns an integer value.</span></span> <span data-ttu-id="cb601-114">Se o valor de retorno for zero ou um valor positivo, ele será o índice de base zero do item não separador no qual o ponto está.</span><span class="sxs-lookup"><span data-stu-id="cb601-114">If the return value is zero or a positive value, it is the zero-based index of the nonseparator item in which the point lies.</span></span> <span data-ttu-id="cb601-115">Se o valor de retorno for negativo, o ponto não se situa em um botão.</span><span class="sxs-lookup"><span data-stu-id="cb601-115">If the return value is negative, the point does not lie within a button.</span></span> <span data-ttu-id="cb601-116">O valor absoluto do valor de retorno é o índice de um item separador ou o item não separador mais próximo.</span><span class="sxs-lookup"><span data-stu-id="cb601-116">The absolute value of the return value is the index of a separator item or the nearest nonseparator item.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb601-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb601-117">Requirements</span></span>



| <span data-ttu-id="cb601-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb601-118">Requirement</span></span> | <span data-ttu-id="cb601-119">Valor</span><span class="sxs-lookup"><span data-stu-id="cb601-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb601-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb601-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cb601-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cb601-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cb601-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb601-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cb601-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cb601-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cb601-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cb601-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb601-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb601-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

