---
title: Mensagem de TB_SETBUTTONSIZE (commctrl. h)
description: Define o tamanho dos botões em uma barra de ferramentas.
ms.assetid: ef6beed7-a3d6-4379-b9c1-c64a5e33ce78
keywords:
- Controles de TB_SETBUTTONSIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db17b943c8a7cc8e71735d08718ece02a8c2582
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754804"
---
# <a name="tb_setbuttonsize-message"></a><span data-ttu-id="0b2b5-104">TB \_ SETbuttonse mensagem</span><span class="sxs-lookup"><span data-stu-id="0b2b5-104">TB\_SETBUTTONSIZE message</span></span>

<span data-ttu-id="0b2b5-105">Define o tamanho dos botões em uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-105">Sets the size of buttons on a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="0b2b5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b2b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b2b5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0b2b5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b2b5-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0b2b5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0b2b5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b2b5-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica a largura, em pixels, dos botões.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the width, in pixels, of the buttons.</span></span> <span data-ttu-id="0b2b5-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a altura, em pixels, dos botões.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the height, in pixels, of the buttons.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b2b5-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0b2b5-112">Return value</span></span>

<span data-ttu-id="0b2b5-113">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b2b5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b2b5-114">Remarks</span></span>

<span data-ttu-id="0b2b5-115">**TB \_ Setbuttonse** deve ser geralmente chamado após a adição de botões.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-115">**TB\_SETBUTTONSIZE** should generally be called after adding buttons.</span></span>

<span data-ttu-id="0b2b5-116">Use [**TB \_ SETBUTTONWIDTH**](tb-setbuttonwidth.md) para definir as larguras máximas e mínimas permitidas para botões antes de serem adicionadas.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-116">Use [**TB\_SETBUTTONWIDTH**](tb-setbuttonwidth.md) to set the maximum and minimum allowed widths for buttons before they are added.</span></span> <span data-ttu-id="0b2b5-117">Use **TB \_ SetButtons** para definir o tamanho real dos botões.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-117">Use **TB\_SETBUTTONSIZE** to set the actual size of buttons.</span></span>

## <a name="examples"></a><span data-ttu-id="0b2b5-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0b2b5-118">Examples</span></span>

<span data-ttu-id="0b2b5-119">O código de exemplo a seguir define a largura dos botões como 80 pixels e a altura como 30 pixels.</span><span class="sxs-lookup"><span data-stu-id="0b2b5-119">The following example code sets the width of buttons to 80 pixels and the height to 30 pixels.</span></span>


```C++
// hWndToolbar is a handle to the toolbar window.
SendMessage(hWndToolbar, TB_SETBUTTONSIZE, 0, MAKELPARAM(80, 30);
```



## <a name="requirements"></a><span data-ttu-id="0b2b5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b2b5-120">Requirements</span></span>



| <span data-ttu-id="0b2b5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b2b5-121">Requirement</span></span> | <span data-ttu-id="0b2b5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0b2b5-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b2b5-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b2b5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0b2b5-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0b2b5-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0b2b5-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b2b5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0b2b5-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0b2b5-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0b2b5-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0b2b5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b2b5-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b2b5-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

