---
title: Comportamentos de teste de colisão de toque
description: As constantes a seguir são usadas por aplicativos ou estruturas de interface do usuário para identificar como as mensagens de teste de toque são processadas pelo Windows que são registradas por meio da função RegisterTouchHitTestingWindow.
ms.assetid: D1ECCBFA-CD01-401E-A42E-4F954F5F0A32
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_DEFAULT
- TOUCH_HIT_TESTING_CLIENT
- TOUCH_HIT_TESTING_NONE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 9b49f61870c6c7041d73d6fa8d5c078887360359
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105766572"
---
# <a name="touch-hit-testing-behaviors"></a><span data-ttu-id="17f31-103">Comportamentos de teste de colisão de toque</span><span class="sxs-lookup"><span data-stu-id="17f31-103">Touch Hit Testing Behaviors</span></span>

<span data-ttu-id="17f31-104">As constantes a seguir são usadas por aplicativos ou estruturas de interface do usuário para identificar como as mensagens de teste de toque são processadas pelo Windows que são registradas por meio da função [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .</span><span class="sxs-lookup"><span data-stu-id="17f31-104">The following constants are used by applications or UI frameworks to identify how messages for touch hit testing are processed by windows that are registered through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span>

| <span data-ttu-id="17f31-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="17f31-105">Constant/value</span></span> | <span data-ttu-id="17f31-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="17f31-106">Description</span></span> |
|---|---|
| <span data-ttu-id="17f31-107">**TOUCH_HIT_TESTING_DEFAULT** </dt> <dt>0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="17f31-107">**TOUCH_HIT_TESTING_DEFAULT**</dt> <dt>0 (0x0)</span></span> | <span data-ttu-id="17f31-108">Indica que [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) mensagens não são enviadas para a janela de destino, mas são enviadas para janelas filhas.</span><span class="sxs-lookup"><span data-stu-id="17f31-108">Indicates that [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) messages are not sent to the target window but are sent to child windows.</span></span><br/> |
| <span data-ttu-id="17f31-109">**TOUCH_HIT_TESTING_CLIENT** </dt> <dt>1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="17f31-109">**TOUCH_HIT_TESTING_CLIENT**</dt> <dt>1 (0x1)</span></span>    | <span data-ttu-id="17f31-110">Indica que [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) mensagens são enviadas para a janela de destino.</span><span class="sxs-lookup"><span data-stu-id="17f31-110">Indicates that [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) messages are sent to the target window.</span></span><br/>                                   |
| <span data-ttu-id="17f31-111">**TOUCH_HIT_TESTING_NONE** </dt> <dt>2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="17f31-111">**TOUCH_HIT_TESTING_NONE**</dt> <dt>2 (0x2)</span></span>          | <span data-ttu-id="17f31-112">Indica que [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) mensagens não são enviadas para a janela de destino ou janelas filhas.</span><span class="sxs-lookup"><span data-stu-id="17f31-112">Indicates that [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) messages are not sent to the target window or child windows.</span></span><br/>              |

## <a name="requirements"></a><span data-ttu-id="17f31-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17f31-113">Requirements</span></span>

| <span data-ttu-id="17f31-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="17f31-114">Requirement</span></span> | <span data-ttu-id="17f31-115">Valor</span><span class="sxs-lookup"><span data-stu-id="17f31-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="17f31-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17f31-116">Minimum supported client</span></span><br/> | <span data-ttu-id="17f31-117">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="17f31-117">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="17f31-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17f31-118">Minimum supported server</span></span><br/> | <span data-ttu-id="17f31-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="17f31-119">None supported</span></span><br/>                                                            |
| <span data-ttu-id="17f31-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="17f31-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="17f31-121"><dt>WinUser. h</span><span class="sxs-lookup"><span data-stu-id="17f31-121"><dt>Winuser.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="17f31-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="17f31-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17f31-123">Constantes</span><span class="sxs-lookup"><span data-stu-id="17f31-123">Constants</span></span>](constants.md)
