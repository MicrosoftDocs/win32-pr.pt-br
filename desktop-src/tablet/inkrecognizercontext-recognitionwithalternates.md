---
description: Ocorre quando a classe InkRecognizerContext gerou resultados depois de chamar o método de método BackgroundRecognizeWithAlternates.
ms.assetid: 5e86a4d5-c0a7-4283-81cc-ec3a26f74880
title: Evento InkRecognizerContext. RecognitionWithAlternates (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a7d35d8281305b0cb5f84114bb2f2fa0e718c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170467"
---
# <a name="inkrecognizercontextrecognitionwithalternates-event"></a><span data-ttu-id="1b550-103">Evento InkRecognizerContext. RecognitionWithAlternates</span><span class="sxs-lookup"><span data-stu-id="1b550-103">InkRecognizerContext.RecognitionWithAlternates event</span></span>

<span data-ttu-id="1b550-104">Ocorre quando a [**classe InkRecognizerContext**](inkrecognizercontext-class.md) gerou resultados depois de chamar o método de [**método BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) .</span><span class="sxs-lookup"><span data-stu-id="1b550-104">Occurs when the [**InkRecognizerContext Class**](inkrecognizercontext-class.md) has generated results after calling the [**BackgroundRecognizeWithAlternates Method**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b550-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1b550-105">Syntax</span></span>


```C++
void RecognitionWithAlternates(
  [in] IInkRecognitionResult *RecognitionResult,
  [in] VARIANT               CustomData,
  [in] InkRecognitionStatus  RecognitionStatus
);
```



## <a name="parameters"></a><span data-ttu-id="1b550-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b550-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b550-107">*RecognitionResult* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1b550-107">*RecognitionResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b550-108">O resultado de reconhecimento do evento.</span><span class="sxs-lookup"><span data-stu-id="1b550-108">The recognition result from the event.</span></span>

</dd> <dt>

<span data-ttu-id="1b550-109">*CustomData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1b550-109">*CustomData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b550-110">Os dados personalizados para o resultado do reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="1b550-110">The custom data for the recognition result.</span></span>

<span data-ttu-id="1b550-111">Para obter mais informações sobre a estrutura de VARIAntes, consulte [usando a biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="1b550-111">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="1b550-112">*RecognitionStatus* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1b550-112">*RecognitionStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b550-113">O status de reconhecimento a partir do resultado de reconhecimento mais recente.</span><span class="sxs-lookup"><span data-stu-id="1b550-113">The recognition status as of the most recent recognition result.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b550-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1b550-114">Return value</span></span>

<span data-ttu-id="1b550-115">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1b550-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b550-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b550-116">Remarks</span></span>

<span data-ttu-id="1b550-117">O comportamento da API (interface de programação de aplicativo) é imprevisível se você tentar obter acesso ao objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) original do manipulador de eventos de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="1b550-117">The behavior of the application programming interface (API) is unpredictable if you try to gain access to the original [**InkRecognizerContext**](inkrecognizercontext-class.md) object from the recognition event handler.</span></span> <span data-ttu-id="1b550-118">Não tente fazer isso.</span><span class="sxs-lookup"><span data-stu-id="1b550-118">Do not attempt to do this.</span></span> <span data-ttu-id="1b550-119">Em vez disso, se você precisar fazer isso, crie um sinalizador e defina-o no manipulador de eventos de [**reconhecimento**](inkrecognizercontext-recognition.md) .</span><span class="sxs-lookup"><span data-stu-id="1b550-119">Instead, if you need to do this, create a flag and set it in the [**Recognition**](inkrecognizercontext-recognition.md) event handler.</span></span> <span data-ttu-id="1b550-120">Em seguida, você pode sondar esse sinalizador para determinar quando alterar as propriedades **InkRecognizerContext** fora do manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="1b550-120">Then you can poll that flag to determine when to change the **InkRecognizerContext** properties outside of the event handler.</span></span>

<span data-ttu-id="1b550-121">Esse método de evento é definido na \_ interface IInkEvents.</span><span class="sxs-lookup"><span data-stu-id="1b550-121">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="1b550-122">A \_ interface IInkEvents implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IRERecognitionWithAlternates DISPID.</span><span class="sxs-lookup"><span data-stu-id="1b550-122">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IRERecognitionWithAlternates.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b550-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b550-123">Requirements</span></span>



| <span data-ttu-id="1b550-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b550-124">Requirement</span></span> | <span data-ttu-id="1b550-125">Valor</span><span class="sxs-lookup"><span data-stu-id="1b550-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b550-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b550-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1b550-127">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1b550-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1b550-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b550-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1b550-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1b550-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="1b550-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1b550-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b550-131"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1b550-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1b550-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1b550-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="1b550-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b550-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="1b550-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b550-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b550-135">**Classe InkRecognizerContext**</span><span class="sxs-lookup"><span data-stu-id="1b550-135">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> <dt>

[<span data-ttu-id="1b550-136">**Método BackgroundRecognizeWithAlternates**</span><span class="sxs-lookup"><span data-stu-id="1b550-136">**BackgroundRecognizeWithAlternates Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)
</dt> <dt>

[<span data-ttu-id="1b550-137">**Método Recognize**</span><span class="sxs-lookup"><span data-stu-id="1b550-137">**Recognize Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[<span data-ttu-id="1b550-138">**Interface IInkRecognitionResult**</span><span class="sxs-lookup"><span data-stu-id="1b550-138">**IInkRecognitionResult Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

