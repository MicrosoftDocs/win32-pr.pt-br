---
title: Mensagem de HDM_LAYOUT (commctrl. h)
description: Recupera informações usadas para definir o tamanho e a posição do controle de cabeçalho dentro do retângulo de destino da janela pai. Você pode enviar essa mensagem explicitamente ou usar a macro de layout de cabeçalho \_ .
ms.assetid: 0763e483-f01d-4739-8c61-1c52d1aad0b4
keywords:
- Controles de HDM_LAYOUT de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_LAYOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a70fc46dee52f52862136dbe583db9f6d7a0e13e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009398"
---
# <a name="hdm_layout-message"></a><span data-ttu-id="51521-105">\_Mensagem de layout HDM</span><span class="sxs-lookup"><span data-stu-id="51521-105">HDM\_LAYOUT message</span></span>

<span data-ttu-id="51521-106">Recupera informações usadas para definir o tamanho e a posição do controle de cabeçalho dentro do retângulo de destino da janela pai.</span><span class="sxs-lookup"><span data-stu-id="51521-106">Retrieves information used to set the size and position of the header control within the target rectangle of the parent window.</span></span> <span data-ttu-id="51521-107">Você pode enviar essa mensagem explicitamente ou usar a macro de [**\_ layout de cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_layout) .</span><span class="sxs-lookup"><span data-stu-id="51521-107">You can send this message explicitly or use the [**Header\_Layout**](/windows/desktop/api/Commctrl/nf-commctrl-header_layout) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="51521-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51521-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51521-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="51521-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="51521-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="51521-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="51521-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51521-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51521-112">Um ponteiro para uma estrutura [**HDLAYOUT**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) .</span><span class="sxs-lookup"><span data-stu-id="51521-112">A pointer to an [**HDLAYOUT**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) structure.</span></span> <span data-ttu-id="51521-113">O membro **prc** especifica as coordenadas de um retângulo e o membro **pwpos** recebe o tamanho e a posição do controle de cabeçalho dentro do retângulo.</span><span class="sxs-lookup"><span data-stu-id="51521-113">The **prc** member specifies the coordinates of a rectangle, and the **pwpos** member receives the size and position for the header control within the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51521-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="51521-114">Return value</span></span>

<span data-ttu-id="51521-115">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="51521-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="51521-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="51521-116">Remarks</span></span>

<span data-ttu-id="51521-117">O membro **pwpos** da estrutura *lParam* recebe valores de tamanho e posição apropriados para posicionar o controle ao longo da parte superior do retângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="51521-117">The **pwpos** member of the *lParam* structure receives size and position values appropriate for positioning the control along the top of the specified rectangle.</span></span> <span data-ttu-id="51521-118">O valor de altura é a soma das alturas das bordas horizontais do controle e a altura média de caracteres na fonte selecionada atualmente no contexto do dispositivo do controle.</span><span class="sxs-lookup"><span data-stu-id="51521-118">The height value is the sum of the heights of the control's horizontal borders and the average height of characters in the font currently selected into the control's device context.</span></span>

<span data-ttu-id="51521-119">Para usar **o \_ layout HDM** para definir o tamanho inicial e a posição de um controle de cabeçalho, defina o estado de visibilidade inicial do controle para que ele fique oculto.</span><span class="sxs-lookup"><span data-stu-id="51521-119">To use **HDM\_LAYOUT** to set the initial size and position of a header control, set the initial visibility state of the control so that it is hidden.</span></span> <span data-ttu-id="51521-120">Depois de enviar o **\_ layout HDM** para recuperar os valores de tamanho e posição, use a função [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para definir o novo tamanho, a posição e o estado de visibilidade.</span><span class="sxs-lookup"><span data-stu-id="51521-120">After sending **HDM\_LAYOUT** to retrieve the size and position values, use the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function to set the new size, position, and visibility state.</span></span>

## <a name="requirements"></a><span data-ttu-id="51521-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51521-121">Requirements</span></span>



| <span data-ttu-id="51521-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="51521-122">Requirement</span></span> | <span data-ttu-id="51521-123">Valor</span><span class="sxs-lookup"><span data-stu-id="51521-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="51521-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51521-124">Minimum supported client</span></span><br/> | <span data-ttu-id="51521-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="51521-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="51521-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51521-126">Minimum supported server</span></span><br/> | <span data-ttu-id="51521-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="51521-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="51521-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="51521-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="51521-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="51521-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

