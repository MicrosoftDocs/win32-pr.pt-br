---
description: Notifica um AppBar quando ocorreu um evento que pode afetar o tamanho e a posição do AppBar.
ms.assetid: 1016a362-4d2b-410e-aec9-c1cc8f497778
title: Mensagem de ABN_POSCHANGED (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b0a800b1c112cba18fbadbba79a999ec83c77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967369"
---
# <a name="abn_poschanged-message"></a><span data-ttu-id="83166-103">\_Mensagem POSCHANGED do ABN</span><span class="sxs-lookup"><span data-stu-id="83166-103">ABN\_POSCHANGED message</span></span>

<span data-ttu-id="83166-104">Notifica um AppBar quando ocorreu um evento que pode afetar o tamanho e a posição do AppBar.</span><span class="sxs-lookup"><span data-stu-id="83166-104">Notifies an appbar when an event has occurred that may affect the appbar's size and position.</span></span> <span data-ttu-id="83166-105">Os eventos incluem alterações no estado de tamanho, posição e visibilidade da barra de tarefas, bem como a adição, remoção ou redimensionamento de outro AppBar no mesmo lado da tela.</span><span class="sxs-lookup"><span data-stu-id="83166-105">Events include changes in the taskbar's size, position, and visibility state, as well as the addition, removal, or resizing of another appbar on the same side of the screen.</span></span>


```C++
ABN_POSCHANGED
```



## <a name="parameters"></a><span data-ttu-id="83166-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83166-106">Parameters</span></span>

<span data-ttu-id="83166-107">Esta mensagem não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="83166-107">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="83166-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="83166-108">Return value</span></span>

<span data-ttu-id="83166-109">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="83166-109">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="83166-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="83166-110">Remarks</span></span>

<span data-ttu-id="83166-111">Um AppBar deve responder a essa mensagem de notificação enviando as mensagens [**ABM \_ QUERYPOS**](abm-querypos.md) e [**ABM \_ SETPOS**](abm-setpos.md) .</span><span class="sxs-lookup"><span data-stu-id="83166-111">An appbar should respond to this notification message by sending the [**ABM\_QUERYPOS**](abm-querypos.md) and [**ABM\_SETPOS**](abm-setpos.md) messages.</span></span> <span data-ttu-id="83166-112">Se sua posição for alterada, o AppBar deverá chamar a função [**MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) para se mover para a nova posição.</span><span class="sxs-lookup"><span data-stu-id="83166-112">If its position has changed, the appbar should call the [**MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) function to move itself to the new position.</span></span>

## <a name="requirements"></a><span data-ttu-id="83166-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83166-113">Requirements</span></span>



| <span data-ttu-id="83166-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="83166-114">Requirement</span></span> | <span data-ttu-id="83166-115">Valor</span><span class="sxs-lookup"><span data-stu-id="83166-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83166-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83166-116">Minimum supported client</span></span><br/> | <span data-ttu-id="83166-117">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="83166-117">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="83166-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83166-118">Minimum supported server</span></span><br/> | <span data-ttu-id="83166-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="83166-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="83166-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="83166-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="83166-121"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="83166-121"><dt>Shellapi.h</dt></span></span> </dl> |



 

