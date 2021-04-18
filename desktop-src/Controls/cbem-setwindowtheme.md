---
title: Mensagem de CBEM_SETWINDOWTHEME (commctrl. h)
description: Define o estilo visual de um controle ComboBoxEx.
ms.assetid: 064f9a24-42be-42f4-bee3-e7320fe8c366
keywords:
- Controles de CBEM_SETWINDOWTHEME de mensagens do Windows
topic_type:
- apiref
api_name:
- CBEM_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cda1e5c46bb6216c413737c44b5785ac26925f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756426"
---
# <a name="cbem_setwindowtheme-message"></a><span data-ttu-id="d3ac0-104">\_Mensagem CBEM SETWINDOWTHEME</span><span class="sxs-lookup"><span data-stu-id="d3ac0-104">CBEM\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="d3ac0-105">Define o estilo visual de um controle ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="d3ac0-105">Sets the visual style of a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d3ac0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3ac0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3ac0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d3ac0-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d3ac0-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d3ac0-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d3ac0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d3ac0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3ac0-110">Um ponteiro para uma cadeia de caracteres Unicode que contém o estilo visual de controle a ser definido.</span><span class="sxs-lookup"><span data-stu-id="d3ac0-110">A pointer to a Unicode string that contains the control visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3ac0-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d3ac0-111">Return value</span></span>

<span data-ttu-id="d3ac0-112">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="d3ac0-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3ac0-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3ac0-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d3ac0-114">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32 versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="d3ac0-114">To use this message, you must provide a manifest specifying Comclt32 version 6.0.</span></span> <span data-ttu-id="d3ac0-115">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d3ac0-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d3ac0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3ac0-116">Requirements</span></span>



| <span data-ttu-id="d3ac0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3ac0-117">Requirement</span></span> | <span data-ttu-id="d3ac0-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d3ac0-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d3ac0-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3ac0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d3ac0-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d3ac0-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d3ac0-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3ac0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d3ac0-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d3ac0-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d3ac0-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d3ac0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3ac0-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3ac0-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





