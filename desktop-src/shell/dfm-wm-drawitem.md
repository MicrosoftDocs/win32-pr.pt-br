---
description: Enviado para a janela pai de um controle ou menu desenhado pelo proprietário quando um aspecto visual do controle ou do menu é alterado.
ms.assetid: 2515bbab-025f-4f00-8564-a732d68edea3
title: Mensagem de DFM_WM_DRAWITEM (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67255fea5c39bebc995e5c53d90378536b12921b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967329"
---
# <a name="dfm_wm_drawitem-message"></a><span data-ttu-id="6ecb9-103">Mensagem do DFM do \_ WM \_ DRAWITEM</span><span class="sxs-lookup"><span data-stu-id="6ecb9-103">DFM\_WM\_DRAWITEM message</span></span>

<span data-ttu-id="6ecb9-104">Enviado para a janela pai de um controle ou menu desenhado pelo proprietário quando um aspecto visual do controle ou do menu é alterado.</span><span class="sxs-lookup"><span data-stu-id="6ecb9-104">Sent to the parent window of an owner-drawn control or menu when a visual aspect of the control or menu has changed.</span></span>


```C++
DFM_WM_DRAWITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPDRAWITEMSTRUCT) lpDrawItem;

            
```



## <a name="parameters"></a><span data-ttu-id="6ecb9-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ecb9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ecb9-106">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6ecb9-106">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ecb9-107">O identificador do controle que enviou a mensagem **DFM do \_ WM \_ DRAWITEM** .</span><span class="sxs-lookup"><span data-stu-id="6ecb9-107">The identifier of the control that sent the **DFM\_WM\_DRAWITEM** message.</span></span> <span data-ttu-id="6ecb9-108">Se a mensagem foi enviada por um menu, esse parâmetro será zero.</span><span class="sxs-lookup"><span data-stu-id="6ecb9-108">If the message was sent by a menu, this parameter is zero.</span></span>

</dd> <dt>

<span data-ttu-id="6ecb9-109">*lpDrawItem* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6ecb9-109">*lpDrawItem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ecb9-110">Um ponteiro para uma estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) que contém informações sobre o item a ser desenhado e o tipo de desenho necessário.</span><span class="sxs-lookup"><span data-stu-id="6ecb9-110">A pointer to a [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure containing information about the item to be drawn and the type of drawing required.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ecb9-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6ecb9-111">Return value</span></span>

<span data-ttu-id="6ecb9-112">Se um aplicativo processar essa mensagem, ele deverá retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="6ecb9-112">If an application processes this message, it should return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ecb9-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ecb9-113">Remarks</span></span>

<span data-ttu-id="6ecb9-114">O membro de **ação** da estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) especifica a operação de desenho que um aplicativo deve executar.</span><span class="sxs-lookup"><span data-stu-id="6ecb9-114">The **itemAction** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure specifies the drawing operation that an application should perform.</span></span>

<span data-ttu-id="6ecb9-115">Antes de retornar do processamento dessa mensagem, um aplicativo deve garantir que o contexto do dispositivo identificado pelo membro **HDC** da estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) esteja no estado padrão.</span><span class="sxs-lookup"><span data-stu-id="6ecb9-115">Before returning from processing this message, an application should ensure that the device context identified by the **hDC** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure is in the default state.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ecb9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ecb9-116">Requirements</span></span>



| <span data-ttu-id="6ecb9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ecb9-117">Requirement</span></span> | <span data-ttu-id="6ecb9-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6ecb9-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6ecb9-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ecb9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6ecb9-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6ecb9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6ecb9-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ecb9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6ecb9-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6ecb9-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6ecb9-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6ecb9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ecb9-124"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ecb9-124"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
