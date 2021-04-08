---
title: Mensagem de TB_GETITEMDROPDOWNRECT (commctrl. h)
description: Obtém o retângulo delimitador da janela suspensa para um item da barra de ferramentas com a \_ lista suspensa estilo BTNS.
ms.assetid: 4b59c96b-8d75-44c1-b771-c1d62502a2c2
keywords:
- Controles de TB_GETITEMDROPDOWNRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETITEMDROPDOWNRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbcbcef725b0ade0bfc776200fa5b191618d2ccb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008991"
---
# <a name="tb_getitemdropdownrect-message"></a><span data-ttu-id="2069f-104">TB de \_ mensagem GETITEMDROPDOWNRECT</span><span class="sxs-lookup"><span data-stu-id="2069f-104">TB\_GETITEMDROPDOWNRECT message</span></span>

<span data-ttu-id="2069f-105">Obtém o retângulo delimitador da janela suspensa para um item da barra de ferramentas com a [**\_ lista suspensa estilo BTNS**](toolbar-control-and-button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="2069f-105">Gets the bounding rectangle of the dropdown window for a toolbar item with style [**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="2069f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2069f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2069f-107">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2069f-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2069f-108">O índice de base zero do item de controle Toolbar para o qual o retângulo delimitador será recuperado.</span><span class="sxs-lookup"><span data-stu-id="2069f-108">The zero-based index of the toolbar control item for which to retrieve the bounding rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="2069f-109">*lParam* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="2069f-109">*lParam* \[in, out\]</span></span>
</dt> <dd><span data-ttu-id="2069f-110">Um ponteiro para uma estrutura <a href="/previous-versions//dd162897(v=vs.85)">**Rect**</a> para receber as informações do retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="2069f-110">A pointer to a <a href="/previous-versions//dd162897(v=vs.85)">**RECT**</a> structure to receive the bounding rectangle information.</span></span> <span data-ttu-id="2069f-111">O remetente da mensagem é responsável por alocar essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="2069f-111">The message sender is responsible for allocating this structure.</span></span> <span data-ttu-id="2069f-112">As coordenadas retornadas na estrutura **Rect** são expressas como coordenadas do cliente.</span><span class="sxs-lookup"><span data-stu-id="2069f-112">The coordinates returned in the **RECT** structure are expressed as client coordinates.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2069f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2069f-113">Return value</span></span>

<span data-ttu-id="2069f-114">Sempre retorna zero.</span><span class="sxs-lookup"><span data-stu-id="2069f-114">Always returns nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2069f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="2069f-115">Remarks</span></span>

<span data-ttu-id="2069f-116">O item deve ter o [**estilo \_ suspenso BTNS**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="2069f-116">The item must have the [**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="2069f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2069f-117">Requirements</span></span>



| <span data-ttu-id="2069f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2069f-118">Requirement</span></span> | <span data-ttu-id="2069f-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2069f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2069f-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2069f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2069f-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2069f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2069f-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2069f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2069f-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2069f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2069f-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2069f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2069f-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2069f-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

