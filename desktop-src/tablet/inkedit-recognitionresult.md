---
description: 'Ocorre quando o controle InkEdit Obtém os resultados manualmente de uma chamada para o método InkEdit:: Recognize ou automaticamente após o tempo limite do reconhecimento ser acionado.'
ms.assetid: 09618be0-fe49-494f-940f-79ff8352097e
title: Evento InkEdit. RecognitionResult (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40d6206293b604e5540b5e6d0271e1ebe984a987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171541"
---
# <a name="inkeditrecognitionresult-event"></a><span data-ttu-id="7ec60-103">Evento InkEdit. RecognitionResult</span><span class="sxs-lookup"><span data-stu-id="7ec60-103">InkEdit.RecognitionResult event</span></span>

<span data-ttu-id="7ec60-104">Ocorre quando o controle [InkEdit](inkedit-control-reference.md) Obtém os resultados manualmente de uma chamada para o método [**InkEdit:: Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) ou automaticamente após o tempo limite do reconhecimento ser acionado.</span><span class="sxs-lookup"><span data-stu-id="7ec60-104">Occurs when the [InkEdit](inkedit-control-reference.md) control gets results manually from a call to the [**InkEdit::Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) method or automatically after the recognition timeout fires.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ec60-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ec60-105">Syntax</span></span>


```C++
void RecognitionResult(
  [in] IInkRecognitionResult *RecognitionResult
);
```



## <a name="parameters"></a><span data-ttu-id="7ec60-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ec60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ec60-107">*RecognitionResult* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7ec60-107">*RecognitionResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec60-108">Um objeto [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) que contém o resultado do reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="7ec60-108">An [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object that contains the result of the recognition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ec60-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7ec60-109">Return value</span></span>

<span data-ttu-id="7ec60-110">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7ec60-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ec60-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ec60-111">Remarks</span></span>

<span data-ttu-id="7ec60-112">Esse método de evento é definido na interface **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="7ec60-112">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="7ec60-113">A interface **\_ IInkEditEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IeeRecognitionResult DISPID.</span><span class="sxs-lookup"><span data-stu-id="7ec60-113">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeRecognitionResult.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ec60-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ec60-114">Requirements</span></span>



| <span data-ttu-id="7ec60-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ec60-115">Requirement</span></span> | <span data-ttu-id="7ec60-116">Valor</span><span class="sxs-lookup"><span data-stu-id="7ec60-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ec60-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ec60-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7ec60-118">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7ec60-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7ec60-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ec60-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7ec60-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7ec60-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7ec60-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7ec60-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ec60-122"><dt>Inked. h (também requer Inked \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7ec60-122"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7ec60-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7ec60-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="7ec60-124"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ec60-124"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7ec60-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ec60-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ec60-126">InkEdit</span><span class="sxs-lookup"><span data-stu-id="7ec60-126">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

<span data-ttu-id="7ec60-127">[**Reconhecer o \[ controle de método InkEdit\]**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)</span><span class="sxs-lookup"><span data-stu-id="7ec60-127">[**Recognize Method \[InkEdit Control\]**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)</span></span>
</dt> </dl>

 

