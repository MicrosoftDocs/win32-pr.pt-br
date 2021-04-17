---
title: Mensagem de SB_SETBKCOLOR (commctrl. h)
description: Define a cor do plano de fundo em uma barra de status.
ms.assetid: 49bcd816-e3e2-45f4-8845-ef67789b8a01
keywords:
- Controles de SB_SETBKCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- SB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc08687c6d228074bc3e4dd7c8442a1c1e35a835
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369819"
---
# <a name="sb_setbkcolor-message"></a><span data-ttu-id="f5c8e-104">\_Mensagem de SETBKCOLOR SB</span><span class="sxs-lookup"><span data-stu-id="f5c8e-104">SB\_SETBKCOLOR message</span></span>

<span data-ttu-id="f5c8e-105">Define a cor do plano de fundo em uma barra de status.</span><span class="sxs-lookup"><span data-stu-id="f5c8e-105">Sets the background color in a status bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f5c8e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5c8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5c8e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f5c8e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f5c8e-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f5c8e-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f5c8e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f5c8e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5c8e-110">Valor [**COLORREF**](/windows/desktop/gdi/colorref) que especifica a nova cor do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="f5c8e-110">[**COLORREF**](/windows/desktop/gdi/colorref) value that specifies the new background color.</span></span> <span data-ttu-id="f5c8e-111">Especifique o \_ valor padrão do CLR para fazer com que a barra de status Use sua cor de plano de fundo padrão.</span><span class="sxs-lookup"><span data-stu-id="f5c8e-111">Specify the CLR\_DEFAULT value to cause the status bar to use its default background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5c8e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f5c8e-112">Return value</span></span>

<span data-ttu-id="f5c8e-113">Retorna a cor do plano de fundo anterior ou o \_ padrão CLR se a cor do plano de fundo for a cor padrão.</span><span class="sxs-lookup"><span data-stu-id="f5c8e-113">Returns the previous background color, or CLR\_DEFAULT if the background color is the default color.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5c8e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5c8e-114">Requirements</span></span>



| <span data-ttu-id="f5c8e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5c8e-115">Requirement</span></span> | <span data-ttu-id="f5c8e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f5c8e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c8e-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5c8e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f5c8e-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f5c8e-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f5c8e-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5c8e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f5c8e-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f5c8e-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f5c8e-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f5c8e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5c8e-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5c8e-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

