---
description: Recupera a fonte com a qual o controle está desenhando seu texto no momento.
ms.assetid: a6d05ef5-9933-4d03-a677-a8328bf1cb7d
title: Mensagem de WM_GETFONT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5254b701630f09cc7980470a9f5be68ad377bc03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790632"
---
# <a name="wm_getfont-message"></a><span data-ttu-id="56f4f-103">Mensagem do WM \_ GETfont</span><span class="sxs-lookup"><span data-stu-id="56f4f-103">WM\_GETFONT message</span></span>

<span data-ttu-id="56f4f-104">Recupera a fonte com a qual o controle está desenhando seu texto no momento.</span><span class="sxs-lookup"><span data-stu-id="56f4f-104">Retrieves the font with which the control is currently drawing its text.</span></span>


```C++
#define WM_GETFONT                      0x0031
```



## <a name="parameters"></a><span data-ttu-id="56f4f-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56f4f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56f4f-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="56f4f-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56f4f-107">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="56f4f-107">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="56f4f-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56f4f-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56f4f-109">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="56f4f-109">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56f4f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="56f4f-110">Return value</span></span>

<span data-ttu-id="56f4f-111">Tipo: **HFONT**</span><span class="sxs-lookup"><span data-stu-id="56f4f-111">Type: **HFONT**</span></span>

<span data-ttu-id="56f4f-112">O valor de retorno é um identificador para a fonte usada pelo controle, ou **NULL** se o controle estiver usando a fonte do sistema.</span><span class="sxs-lookup"><span data-stu-id="56f4f-112">The return value is a handle to the font used by the control, or **NULL** if the control is using the system font.</span></span>

## <a name="requirements"></a><span data-ttu-id="56f4f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56f4f-113">Requirements</span></span>



| <span data-ttu-id="56f4f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="56f4f-114">Requirement</span></span> | <span data-ttu-id="56f4f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="56f4f-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56f4f-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56f4f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="56f4f-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="56f4f-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="56f4f-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56f4f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="56f4f-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="56f4f-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="56f4f-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="56f4f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="56f4f-121"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56f4f-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56f4f-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="56f4f-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="56f4f-123">**Referência**</span><span class="sxs-lookup"><span data-stu-id="56f4f-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="56f4f-124">**WM \_ SETfont**</span><span class="sxs-lookup"><span data-stu-id="56f4f-124">**WM\_SETFONT**</span></span>](wm-setfont.md)
</dt> <dt>

<span data-ttu-id="56f4f-125">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="56f4f-125">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="56f4f-126">Windows</span><span class="sxs-lookup"><span data-stu-id="56f4f-126">Windows</span></span>](windows.md)
</dt> </dl>

 

 




