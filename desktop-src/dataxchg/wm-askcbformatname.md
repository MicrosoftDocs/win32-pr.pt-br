---
title: Mensagem de WM_ASKCBFORMATNAME (WinUser. h)
description: Enviado para o proprietário da área de transferência por uma janela do Visualizador da área de transferência para solicitar o nome de um formato de área de transferência do CF \_ OWNERDISPLAY.
ms.assetid: eee026ec-58db-41b3-9705-30a17eebbd70
keywords:
- Troca de dados de mensagem WM_ASKCBFORMATNAME
topic_type:
- apiref
api_name:
- WM_ASKCBFORMATNAME
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b14a7f2fc2ff57076d6b694061466fd60e09dce0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085349"
---
# <a name="wm_askcbformatname-message"></a><span data-ttu-id="f2203-104">Mensagem do WM \_ ASKCBFORMATNAME</span><span class="sxs-lookup"><span data-stu-id="f2203-104">WM\_ASKCBFORMATNAME message</span></span>

<span data-ttu-id="f2203-105">Enviado para o proprietário da área de transferência por uma janela do Visualizador da área de transferência para solicitar o nome de um formato de área de transferência do [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) .</span><span class="sxs-lookup"><span data-stu-id="f2203-105">Sent to the clipboard owner by a clipboard viewer window to request the name of a [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) clipboard format.</span></span>

<span data-ttu-id="f2203-106">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f2203-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_ASKCBFORMATNAME              0x030C
```



## <a name="parameters"></a><span data-ttu-id="f2203-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2203-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2203-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f2203-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2203-109">O tamanho, em caracteres, do buffer apontado pelo parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="f2203-109">The size, in characters, of the buffer pointed to by the *lParam* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f2203-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2203-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2203-111">Um ponteiro para o buffer que deve receber o nome do formato da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="f2203-111">A pointer to the buffer that is to receive the clipboard format name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2203-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f2203-112">Return value</span></span>

<span data-ttu-id="f2203-113">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="f2203-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2203-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2203-114">Remarks</span></span>

<span data-ttu-id="f2203-115">Em resposta a essa mensagem, o proprietário da área de transferência deve copiar o nome do formato de exibição de proprietário para o buffer especificado, não excedendo o tamanho do buffer especificado pelo parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="f2203-115">In response to this message, the clipboard owner should copy the name of the owner-display format to the specified buffer, not exceeding the buffer size specified by the *wParam* parameter.</span></span>

<span data-ttu-id="f2203-116">Uma janela do Visualizador da área de transferência envia essa mensagem para o proprietário da área de transferência para determinar o nome do formato de [**\_ OWNERDISPLAY do CF**](standard-clipboard-formats.md) , por exemplo, para inicializar um menu que lista os formatos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f2203-116">A clipboard viewer window sends this message to the clipboard owner to determine the name of the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format   for example, to initialize a menu listing available formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2203-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2203-117">Requirements</span></span>



| <span data-ttu-id="f2203-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2203-118">Requirement</span></span> | <span data-ttu-id="f2203-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f2203-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2203-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2203-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f2203-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f2203-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f2203-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2203-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f2203-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f2203-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f2203-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f2203-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2203-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2203-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2203-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2203-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2203-127">Visão geral da área de transferência</span><span class="sxs-lookup"><span data-stu-id="f2203-127">Clipboard Overview</span></span>](clipboard.md)
</dt> </dl>

 

