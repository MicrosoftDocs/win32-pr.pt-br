---
title: Mensagem de TB_SETHOTIMAGELIST (commctrl. h)
description: Define a lista de imagens que o controle Toolbar usará para exibir botões quentes.
ms.assetid: 3c29cdde-bd57-4194-984f-220dbf963733
keywords:
- Controles de TB_SETHOTIMAGELIST de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a84c3420eaf64710ac1f8764db20d2cfc88b7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918857"
---
# <a name="tb_sethotimagelist-message"></a><span data-ttu-id="19366-104">TB de \_ mensagem SETHOTIMAGELIST</span><span class="sxs-lookup"><span data-stu-id="19366-104">TB\_SETHOTIMAGELIST message</span></span>

<span data-ttu-id="19366-105">Define a lista de imagens que o controle Toolbar usará para exibir botões quentes.</span><span class="sxs-lookup"><span data-stu-id="19366-105">Sets the image list that the toolbar control will use to display hot buttons.</span></span>

## <a name="parameters"></a><span data-ttu-id="19366-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19366-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19366-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="19366-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="19366-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="19366-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="19366-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="19366-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19366-110">Identificador para a lista de imagens que será definida.</span><span class="sxs-lookup"><span data-stu-id="19366-110">Handle to the image list that will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19366-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="19366-111">Return value</span></span>

<span data-ttu-id="19366-112">Retorna o identificador para a lista de imagens usada anteriormente para exibir botões quentes ou **NULL** se nenhuma lista de imagens tiver sido definida anteriormente.</span><span class="sxs-lookup"><span data-stu-id="19366-112">Returns the handle to the image list previously used to display hot buttons, or **NULL** if no image list was previously set.</span></span>

## <a name="remarks"></a><span data-ttu-id="19366-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="19366-113">Remarks</span></span>

<span data-ttu-id="19366-114">Um botão fica quente quando o cursor está sobre ele.</span><span class="sxs-lookup"><span data-stu-id="19366-114">A button is hot when the cursor is over it.</span></span> <span data-ttu-id="19366-115">Os controles da barra de ferramentas devem ter o estilo de [**\_ lista**](toolbar-control-and-button-styles.md) [**TBSTYLE \_ simples**](toolbar-control-and-button-styles.md) ou TBSTYLE para ter itens quentes.</span><span class="sxs-lookup"><span data-stu-id="19366-115">Toolbar controls must have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) or [**TBSTYLE\_LIST**](toolbar-control-and-button-styles.md) style to have hot items.</span></span>

## <a name="requirements"></a><span data-ttu-id="19366-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19366-116">Requirements</span></span>



| <span data-ttu-id="19366-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="19366-117">Requirement</span></span> | <span data-ttu-id="19366-118">Valor</span><span class="sxs-lookup"><span data-stu-id="19366-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19366-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19366-119">Minimum supported client</span></span><br/> | <span data-ttu-id="19366-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="19366-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="19366-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19366-121">Minimum supported server</span></span><br/> | <span data-ttu-id="19366-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="19366-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="19366-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="19366-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="19366-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="19366-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





