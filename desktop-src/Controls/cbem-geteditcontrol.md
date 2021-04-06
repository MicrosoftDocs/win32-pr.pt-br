---
title: Mensagem de CBEM_GETEDITCONTROL (commctrl. h)
description: Obtém o identificador para a parte de controle de edição de um controle ComboBoxEx. Um controle ComboBoxEx usa uma caixa de edição quando ela é definida como o \_ estilo DROPDOWN do CBS.
ms.assetid: def91949-cadc-4297-a504-0680d7d9b815
keywords:
- Controles de CBEM_GETEDITCONTROL de mensagens do Windows
topic_type:
- apiref
api_name:
- CBEM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 412d1183b29c8c89b5977d5f7f2a1b962d54dc01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086195"
---
# <a name="cbem_geteditcontrol-message"></a><span data-ttu-id="42a31-105">\_Mensagem CBEM GETEDITCONTROL</span><span class="sxs-lookup"><span data-stu-id="42a31-105">CBEM\_GETEDITCONTROL message</span></span>

<span data-ttu-id="42a31-106">Obtém o identificador para a parte de controle de edição de um controle ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="42a31-106">Gets the handle to the edit control portion of a ComboBoxEx control.</span></span> <span data-ttu-id="42a31-107">Um controle ComboBoxEx usa uma caixa de edição quando ela é definida como o estilo [**\_ DROPDOWN do CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="42a31-107">A ComboBoxEx control uses an edit box when it is set to the [**CBS\_DROPDOWN**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="42a31-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42a31-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42a31-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="42a31-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="42a31-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="42a31-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="42a31-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="42a31-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="42a31-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="42a31-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42a31-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="42a31-113">Return value</span></span>

<span data-ttu-id="42a31-114">Retorna o identificador para o controle de edição dentro do controle ComboBoxEx se ele usar o estilo [**\_ DROPDOWN do CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="42a31-114">Returns the handle to the edit control within the ComboBoxEx control if it uses the [**CBS\_DROPDOWN**](combo-box-styles.md) style.</span></span> <span data-ttu-id="42a31-115">Caso contrário, a mensagem retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="42a31-115">Otherwise, the message returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="42a31-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42a31-116">Requirements</span></span>



| <span data-ttu-id="42a31-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="42a31-117">Requirement</span></span> | <span data-ttu-id="42a31-118">Valor</span><span class="sxs-lookup"><span data-stu-id="42a31-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42a31-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42a31-119">Minimum supported client</span></span><br/> | <span data-ttu-id="42a31-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="42a31-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="42a31-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42a31-121">Minimum supported server</span></span><br/> | <span data-ttu-id="42a31-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="42a31-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="42a31-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="42a31-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="42a31-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="42a31-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





