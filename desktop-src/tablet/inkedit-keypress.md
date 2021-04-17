---
description: Ocorre quando o usuário pressiona e libera uma tecla enquanto o controle InkEdit tem foco.
ms.assetid: 8284ab41-dfac-4da2-b101-6968a43b15d7
title: Evento InkEdit. KeyPress (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e49264f82b2cfe3c6998666339f08340a540791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812039"
---
# <a name="inkeditkeypress-event"></a><span data-ttu-id="a6dfd-103">Evento InkEdit. KeyPress</span><span class="sxs-lookup"><span data-stu-id="a6dfd-103">InkEdit.KeyPress event</span></span>

<span data-ttu-id="a6dfd-104">Ocorre quando o usuário pressiona e libera uma tecla enquanto o controle [InkEdit](inkedit-control-reference.md) tem foco.</span><span class="sxs-lookup"><span data-stu-id="a6dfd-104">Occurs when the user presses and releases a key while the [InkEdit](inkedit-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6dfd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6dfd-105">Syntax</span></span>


```C++
HRESULT KeyPress(
   Long *Char
);
```



## <a name="parameters"></a><span data-ttu-id="a6dfd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6dfd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6dfd-107">*Char*</span><span class="sxs-lookup"><span data-stu-id="a6dfd-107">*Char*</span></span> 
</dt> <dd>

<span data-ttu-id="a6dfd-108">Um inteiro que retorna um código de keyansi numérico padrão.</span><span class="sxs-lookup"><span data-stu-id="a6dfd-108">An integer that returns a standard numeric ANSI keycode.</span></span> <span data-ttu-id="a6dfd-109">O parâmetro *Char* é passado por referência; alterá-lo envia um caractere diferente para o controle.</span><span class="sxs-lookup"><span data-stu-id="a6dfd-109">The *Char* parameter is passed by reference; changing it sends a different character to the control.</span></span> <span data-ttu-id="a6dfd-110">Alterar o parâmetro *Char* para 0 cancela o evento.</span><span class="sxs-lookup"><span data-stu-id="a6dfd-110">Changing the *Char* parameter to 0 cancels the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6dfd-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a6dfd-111">Return value</span></span>

<span data-ttu-id="a6dfd-112">Se esse evento for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a6dfd-112">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a6dfd-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a6dfd-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6dfd-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6dfd-114">Remarks</span></span>

<span data-ttu-id="a6dfd-115">Esse método de evento é definido na interface **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="a6dfd-115">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="a6dfd-116">A interface **\_ IInkEditEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IeeKeyPress DISPID.</span><span class="sxs-lookup"><span data-stu-id="a6dfd-116">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeKeyPress.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6dfd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6dfd-117">Requirements</span></span>



| <span data-ttu-id="a6dfd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6dfd-118">Requirement</span></span> | <span data-ttu-id="a6dfd-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a6dfd-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6dfd-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6dfd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a6dfd-121">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a6dfd-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a6dfd-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6dfd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a6dfd-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a6dfd-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a6dfd-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6dfd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6dfd-125"><dt>Inked. h (também requer Inked \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a6dfd-125"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a6dfd-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a6dfd-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="a6dfd-127"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6dfd-127"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a6dfd-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6dfd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6dfd-129">InkEdit</span><span class="sxs-lookup"><span data-stu-id="a6dfd-129">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

<span data-ttu-id="a6dfd-130">[**Controle de evento InkEdit de KeyDown \[\]**](inkedit-keydown.md)</span><span class="sxs-lookup"><span data-stu-id="a6dfd-130">[**KeyDown Event \[InkEdit Control\]**](inkedit-keydown.md)</span></span>
</dt> <dt>

<span data-ttu-id="a6dfd-131">[**Controle de evento InkEdit de KeyUp \[\]**](inkedit-keyup.md)</span><span class="sxs-lookup"><span data-stu-id="a6dfd-131">[**KeyUp Event \[InkEdit Control\]**](inkedit-keyup.md)</span></span>
</dt> </dl>

 

