---
description: Instrui uma janela de remoção de imagem para atualizar usando as novas informações de DROPDESCRIPTION.
title: DDWM_UPDATEWINDOW mensagem
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3b74f2e1-8121-4b7c-8d7a-b449cda529da
api_name:
- DDWM_UPDATEWINDOW
api_type:
- NA
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2bff0e007c735fcf202aaf16cf304eb4ff5358f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967340"
---
# <a name="ddwm_updatewindow-message"></a><span data-ttu-id="04d34-103">\_Mensagem DDWM UPDATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="04d34-103">DDWM\_UPDATEWINDOW message</span></span>

<span data-ttu-id="04d34-104">Instrui uma janela de remoção de imagem para atualizar usando as novas informações de [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) .</span><span class="sxs-lookup"><span data-stu-id="04d34-104">Instructs a drop image window to update using new [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) information.</span></span>

## <a name="parameters"></a><span data-ttu-id="04d34-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04d34-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04d34-106">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="04d34-106">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04d34-107">Não usado.</span><span class="sxs-lookup"><span data-stu-id="04d34-107">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="04d34-108">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="04d34-108">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04d34-109">Não usado.</span><span class="sxs-lookup"><span data-stu-id="04d34-109">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04d34-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="04d34-110">Remarks</span></span>

<span data-ttu-id="04d34-111">DDWM \_ UPDATEWINDOW é definido como usuário do WM \_ + 3.</span><span class="sxs-lookup"><span data-stu-id="04d34-111">DDWM\_UPDATEWINDOW is defined as WM\_USER+3.</span></span>

<span data-ttu-id="04d34-112">Quando o estado de uma operação de remoção é alterado, como em resposta a uma tecla modificadora,[**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) retorna um novo valor [**DROPEFFECT**](../com/dropeffect-constants.md) (esse valor **DROPEFFECT** também pode ser recebido por meio de [**IDropSource:: GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback)).</span><span class="sxs-lookup"><span data-stu-id="04d34-112">When the state of a drop operation changes—such as in response to a modifier key—[**IDropTarget::DragOver**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) returns a new [**DROPEFFECT**](../com/dropeffect-constants.md) value (this **DROPEFFECT** value can also be received through [**IDropSource::GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback)).</span></span> <span data-ttu-id="04d34-113">Em resposta, o aplicativo atualiza a estrutura [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) da interface "soltar" com um novo valor [**DROPIMAGETYPE**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) que indica a decoração a ser aplicada ao Visual da janela de arrastar; por exemplo, uma indicação de que o arquivo está sendo copiado em vez de movido ou que o objeto não pode ser Descartado para esse local.</span><span class="sxs-lookup"><span data-stu-id="04d34-113">In response, the application updates the drop target's [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) structure with a new [**DROPIMAGETYPE**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) value that indicates the decoration to be applied to the drag window's visual; for instance, an indication that the file is being copied rather than moved or that the object cannot be dropped to that location.</span></span> <span data-ttu-id="04d34-114">No entanto, os visuais não são atualizados até que o objeto receba uma mensagem **DDWM \_ UPDATEWINDOW** .</span><span class="sxs-lookup"><span data-stu-id="04d34-114">However, the visuals are not updated until the object receives a **DDWM\_UPDATEWINDOW** message.</span></span>

<span data-ttu-id="04d34-115">O formato de área de transferência [DragWindow](clipboard.md) fornece o **HWND** da janela de arrastar destinatário para o remetente da mensagem **DDWM \_ UPDATEWINDOW** .</span><span class="sxs-lookup"><span data-stu-id="04d34-115">The [DragWindow](clipboard.md) clipboard format provides the **HWND** of the recipient drag window to the sender of the **DDWM\_UPDATEWINDOW** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="04d34-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04d34-116">Requirements</span></span>



| <span data-ttu-id="04d34-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="04d34-117">Requirement</span></span> | <span data-ttu-id="04d34-118">Valor</span><span class="sxs-lookup"><span data-stu-id="04d34-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="04d34-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04d34-119">Minimum supported client</span></span><br/> | <span data-ttu-id="04d34-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="04d34-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="04d34-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04d34-121">Minimum supported server</span></span><br/> | <span data-ttu-id="04d34-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="04d34-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 
