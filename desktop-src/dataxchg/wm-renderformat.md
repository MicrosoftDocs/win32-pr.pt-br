---
title: Mensagem de WM_RENDERFORMAT (WinUser. h)
description: Enviado ao proprietário da área de transferência se ele tiver um processamento atrasado em um formato de área de transferência específico e se um aplicativo tiver solicitado dados nesse formato.
ms.assetid: 81638109-4c5e-4b4c-b2db-4208b6ee83cc
keywords:
- Troca de dados de mensagem WM_RENDERFORMAT
topic_type:
- apiref
api_name:
- WM_RENDERFORMAT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9d0e8539dc666c7a791a24c9ba7ac772c3c2c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295790"
---
# <a name="wm_renderformat-message"></a><span data-ttu-id="6089d-104">Mensagem do WM \_ RENDERFORMAT</span><span class="sxs-lookup"><span data-stu-id="6089d-104">WM\_RENDERFORMAT message</span></span>

<span data-ttu-id="6089d-105">Enviado ao proprietário da área de transferência se ele tiver um processamento atrasado em um formato de área de transferência específico e se um aplicativo tiver solicitado dados nesse formato.</span><span class="sxs-lookup"><span data-stu-id="6089d-105">Sent to the clipboard owner if it has delayed rendering a specific clipboard format and if an application has requested data in that format.</span></span> <span data-ttu-id="6089d-106">O proprietário da área de transferência deve renderizar dados no formato especificado e colocá-los na área de transferência chamando a função [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) .</span><span class="sxs-lookup"><span data-stu-id="6089d-106">The clipboard owner must render data in the specified format and place it on the clipboard by calling the [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) function.</span></span>


```C++
#define WM_RENDERFORMAT                 0x0305
```



## <a name="parameters"></a><span data-ttu-id="6089d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6089d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6089d-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6089d-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6089d-109">O [formato da área de transferência](standard-clipboard-formats.md) a ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="6089d-109">The [clipboard format](standard-clipboard-formats.md) to be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="6089d-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6089d-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6089d-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="6089d-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6089d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6089d-112">Return value</span></span>

<span data-ttu-id="6089d-113">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="6089d-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6089d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6089d-114">Remarks</span></span>

<span data-ttu-id="6089d-115">Ao responder a uma mensagem do **WM \_ RENDERFORMAT** , o proprietário da área de transferência não deve abrir a área de transferência antes de chamar [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).</span><span class="sxs-lookup"><span data-stu-id="6089d-115">When responding to a **WM\_RENDERFORMAT** message, the clipboard owner must not open the clipboard before calling [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).</span></span> <span data-ttu-id="6089d-116">Não é necessário abrir a área de transferência antes de colocar dados em resposta ao **WM \_ RENDERFORMAT**, e qualquer tentativa de abrir a área de transferência falhará porque a área de transferência está sendo mantida no momento aberta pelo aplicativo que solicitou o formato a ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="6089d-116">Opening the clipboard is not necessary before placing data in response to **WM\_RENDERFORMAT**, and any attempt to open the clipboard will fail because the clipboard is currently being held open by the application that requested the format to be rendered.</span></span>

## <a name="requirements"></a><span data-ttu-id="6089d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6089d-117">Requirements</span></span>



| <span data-ttu-id="6089d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6089d-118">Requirement</span></span> | <span data-ttu-id="6089d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6089d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6089d-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6089d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6089d-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6089d-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6089d-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6089d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6089d-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6089d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6089d-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6089d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6089d-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6089d-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6089d-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6089d-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="6089d-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="6089d-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6089d-128">**SetClipboardData**</span><span class="sxs-lookup"><span data-stu-id="6089d-128">**SetClipboardData**</span></span>](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[<span data-ttu-id="6089d-129">**RENDERALLFORMATS do WM \_**</span><span class="sxs-lookup"><span data-stu-id="6089d-129">**WM\_RENDERALLFORMATS**</span></span>](wm-renderallformats.md)
</dt> <dt>

<span data-ttu-id="6089d-130">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="6089d-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6089d-131">Área de transferência</span><span class="sxs-lookup"><span data-stu-id="6089d-131">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

 





