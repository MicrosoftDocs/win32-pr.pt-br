---
title: Mensagem de LVM_SETCOLUMNWIDTH (commctrl. h)
description: Altera a largura de uma coluna no modo de exibição de relatório ou a largura de todas as colunas no modo de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetColumnWidth do ListView.
ms.assetid: 309aebfb-9fed-4c77-acbb-ea905b32b0e2
keywords:
- Controles de LVM_SETCOLUMNWIDTH de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 529e989b3d66562acc7b6f91c3b3b06527235e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085169"
---
# <a name="lvm_setcolumnwidth-message"></a><span data-ttu-id="c2893-105">\_Mensagem SETCOLUMNWIDTH LVM</span><span class="sxs-lookup"><span data-stu-id="c2893-105">LVM\_SETCOLUMNWIDTH message</span></span>

<span data-ttu-id="c2893-106">Altera a largura de uma coluna no modo de exibição de relatório ou a largura de todas as colunas no modo de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="c2893-106">Changes the width of a column in report-view mode or the width of all columns in list-view mode.</span></span> <span data-ttu-id="c2893-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetColumnWidth do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnwidth) .</span><span class="sxs-lookup"><span data-stu-id="c2893-107">You can send this message explicitly or use the [**ListView\_SetColumnWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnwidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c2893-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2893-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2893-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c2893-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2893-110">Índice de base zero de uma coluna válida.</span><span class="sxs-lookup"><span data-stu-id="c2893-110">Zero-based index of a valid column.</span></span> <span data-ttu-id="c2893-111">Para o modo de exibição de lista, esse parâmetro deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="c2893-111">For list-view mode, this parameter must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="c2893-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c2893-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2893-113">Nova largura da coluna, em pixels.</span><span class="sxs-lookup"><span data-stu-id="c2893-113">New width of the column, in pixels.</span></span> <span data-ttu-id="c2893-114">Para o modo de exibição de relatório, há suporte para os seguintes valores especiais:</span><span class="sxs-lookup"><span data-stu-id="c2893-114">For report-view mode, the following special values are supported:</span></span>



| <span data-ttu-id="c2893-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c2893-115">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="c2893-116">Significado</span><span class="sxs-lookup"><span data-stu-id="c2893-116">Meaning</span></span>                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVSCW_AUTOSIZE"></span><span id="lvscw_autosize"></span><dl> <span data-ttu-id="c2893-117"><dt>**\_dimensionamento automático de LVSCW**</dt></span><span class="sxs-lookup"><span data-stu-id="c2893-117"><dt>**LVSCW\_AUTOSIZE**</dt></span></span> </dl>                                | <span data-ttu-id="c2893-118">Dimensiona automaticamente a coluna.</span><span class="sxs-lookup"><span data-stu-id="c2893-118">Automatically sizes the column.</span></span><br/>                                                                                                                                           |
| <span id="LVSCW_AUTOSIZE_USEHEADER"></span><span id="lvscw_autosize_useheader"></span><dl> <span data-ttu-id="c2893-119"><dt>**LVSCW \_ AUTOSIZE \_ USEHEADER**</dt></span><span class="sxs-lookup"><span data-stu-id="c2893-119"><dt>**LVSCW\_AUTOSIZE\_USEHEADER**</dt></span></span> </dl> | <span data-ttu-id="c2893-120">Dimensiona automaticamente a coluna para caber no texto do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="c2893-120">Automatically sizes the column to fit the header text.</span></span> <span data-ttu-id="c2893-121">Se você usar esse valor com a última coluna, sua largura será definida para preencher a largura restante do controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="c2893-121">If you use this value with the last column, its width is set to fill the remaining width of the list-view control.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2893-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c2893-122">Return value</span></span>

<span data-ttu-id="c2893-123">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="c2893-123">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2893-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2893-124">Remarks</span></span>

<span data-ttu-id="c2893-125">Suponha que você tenha um controle de exibição de lista de duas colunas com uma largura de 500 pixels.</span><span class="sxs-lookup"><span data-stu-id="c2893-125">Assume that you have a 2-column list-view control with a width of 500 pixels.</span></span> <span data-ttu-id="c2893-126">Se a largura da coluna zero for definida como 200 pixels e você enviar essa mensagem com *wParam* = 1 e *lParam* = LVSCW \_ AUTOSIZE \_ USEHEADER, a segunda (e última) coluna terá 300 pixels de largura.</span><span class="sxs-lookup"><span data-stu-id="c2893-126">If the width of column zero is set to 200 pixels, and you send this message with *wParam* = 1 and *lParam* = LVSCW\_AUTOSIZE\_USEHEADER, the second (and last) column will be 300 pixels wide.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2893-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2893-127">Requirements</span></span>



| <span data-ttu-id="c2893-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2893-128">Requirement</span></span> | <span data-ttu-id="c2893-129">Valor</span><span class="sxs-lookup"><span data-stu-id="c2893-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2893-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2893-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c2893-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c2893-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c2893-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2893-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c2893-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c2893-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c2893-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c2893-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2893-135"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2893-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





