---
description: A mensagem do WM \_ PALETTEISCHANGING informa os aplicativos que um aplicativo vai perceber sua paleta lógica.
ms.assetid: 64ec1042-0ab5-496f-9a88-2f293b412704
title: Mensagem de WM_PALETTEISCHANGING (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa2127dc9c682bba1fc4cea4e10b2b96ecc92102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662614"
---
# <a name="wm_paletteischanging-message"></a><span data-ttu-id="913f1-103">Mensagem do WM \_ PALETTEISCHANGING</span><span class="sxs-lookup"><span data-stu-id="913f1-103">WM\_PALETTEISCHANGING message</span></span>

<span data-ttu-id="913f1-104">A mensagem do **WM \_ PALETTEISCHANGING** informa os aplicativos que um aplicativo vai perceber sua paleta lógica.</span><span class="sxs-lookup"><span data-stu-id="913f1-104">The **WM\_PALETTEISCHANGING** message informs applications that an application is going to realize its logical palette.</span></span>

<span data-ttu-id="913f1-105">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="913f1-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="913f1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="913f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="913f1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="913f1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="913f1-108">Um identificador para a janela que vai perceber sua paleta lógica.</span><span class="sxs-lookup"><span data-stu-id="913f1-108">A handle to the window that is going to realize its logical palette.</span></span>

</dd> <dt>

<span data-ttu-id="913f1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="913f1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="913f1-110">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="913f1-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="913f1-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="913f1-111">Return value</span></span>

<span data-ttu-id="913f1-112">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="913f1-112">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="913f1-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="913f1-113">Remarks</span></span>

<span data-ttu-id="913f1-114">O aplicativo que altera sua paleta não aguarda a confirmação desta mensagem antes de alterar a paleta e enviar a mensagem [**de \_ paletachanged do WM**](wm-palettechanged.md) .</span><span class="sxs-lookup"><span data-stu-id="913f1-114">The application changing its palette does not wait for acknowledgment of this message before changing the palette and sending the [**WM\_PALETTECHANGED**](wm-palettechanged.md) message.</span></span> <span data-ttu-id="913f1-115">Como resultado, a paleta pode já ser alterada no momento em que um aplicativo recebe essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="913f1-115">As a result, the palette may already be changed by the time an application receives this message.</span></span>

<span data-ttu-id="913f1-116">Se o aplicativo ignorar ou não processar essa mensagem e um segundo aplicativo perceber sua paleta enquanto o primeiro estiver usando índices de paleta, haverá uma grande possibilidade de que o usuário verá cores inesperadas durante operações de desenho subsequentes.</span><span class="sxs-lookup"><span data-stu-id="913f1-116">If the application either ignores or fails to process this message and a second application realizes its palette while the first is using palette indexes, there is a strong possibility that the user will see unexpected colors during subsequent drawing operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="913f1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="913f1-117">Requirements</span></span>



| <span data-ttu-id="913f1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="913f1-118">Requirement</span></span> | <span data-ttu-id="913f1-119">Valor</span><span class="sxs-lookup"><span data-stu-id="913f1-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="913f1-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="913f1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="913f1-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="913f1-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="913f1-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="913f1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="913f1-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="913f1-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="913f1-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="913f1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="913f1-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="913f1-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="913f1-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="913f1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="913f1-127">Visão geral das cores</span><span class="sxs-lookup"><span data-stu-id="913f1-127">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="913f1-128">Mensagens de cores</span><span class="sxs-lookup"><span data-stu-id="913f1-128">Color Messages</span></span>](color-messages.md)
</dt> <dt>

[<span data-ttu-id="913f1-129">**paleta do WMchanged \_**</span><span class="sxs-lookup"><span data-stu-id="913f1-129">**WM\_PALETTECHANGED**</span></span>](wm-palettechanged.md)
</dt> <dt>

[<span data-ttu-id="913f1-130">**QUERYNEWPALETTE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="913f1-130">**WM\_QUERYNEWPALETTE**</span></span>](wm-querynewpalette.md)
</dt> </dl>

 

 
