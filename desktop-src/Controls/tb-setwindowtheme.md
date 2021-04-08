---
title: Mensagem de TB_SETWINDOWTHEME (commctrl. h)
description: Define o estilo visual de um controle ToolBar.
ms.assetid: 8b05c561-af66-47e7-8ef3-7f9f81da4840
keywords:
- Controles de TB_SETWINDOWTHEME de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0c293e974eee2e7827225efb06cc439fdf2c39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086523"
---
# <a name="tb_setwindowtheme-message"></a><span data-ttu-id="01064-104">TB de \_ mensagem SETWINDOWTHEME</span><span class="sxs-lookup"><span data-stu-id="01064-104">TB\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="01064-105">Define o estilo visual de um controle ToolBar.</span><span class="sxs-lookup"><span data-stu-id="01064-105">Sets the visual style of a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="01064-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01064-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01064-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="01064-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="01064-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="01064-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="01064-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="01064-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01064-110">Ponteiro para uma cadeia de caracteres Unicode que contém o estilo visual da barra de ferramentas a ser definido.</span><span class="sxs-lookup"><span data-stu-id="01064-110">Pointer to a Unicode string that contains the toolbar visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01064-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="01064-111">Return value</span></span>

<span data-ttu-id="01064-112">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="01064-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="01064-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="01064-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="01064-114">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="01064-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="01064-115">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="01064-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

<span data-ttu-id="01064-116">O envio dessa mensagem é equivalente a chamar [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) na barra de ferramentas e seu controle ToolTip, se houver.</span><span class="sxs-lookup"><span data-stu-id="01064-116">Sending this message is equivalent to calling [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) on the toolbar and its tooltip control, if any.</span></span>

## <a name="requirements"></a><span data-ttu-id="01064-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01064-117">Requirements</span></span>



| <span data-ttu-id="01064-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="01064-118">Requirement</span></span> | <span data-ttu-id="01064-119">Valor</span><span class="sxs-lookup"><span data-stu-id="01064-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="01064-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01064-120">Minimum supported client</span></span><br/> | <span data-ttu-id="01064-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="01064-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="01064-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01064-122">Minimum supported server</span></span><br/> | <span data-ttu-id="01064-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="01064-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="01064-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="01064-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="01064-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="01064-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





