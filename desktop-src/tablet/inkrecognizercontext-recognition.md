---
description: Ocorre quando o InkRecognizerContext gerou resultados do método BackgroundRecognize.
ms.assetid: 0cc319af-cd0b-4089-928b-cae6c86f6f61
title: Evento InkRecognizerContext. Recognition (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86da1a7470169f9f978e92a87f3e32f7e63acb42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762200"
---
# <a name="inkrecognizercontextrecognition-event"></a><span data-ttu-id="d088b-103">Evento InkRecognizerContext. Recognition</span><span class="sxs-lookup"><span data-stu-id="d088b-103">InkRecognizerContext.Recognition event</span></span>

<span data-ttu-id="d088b-104">Ocorre quando o [**InkRecognizerContext**](inkrecognizercontext-class.md) gerou resultados do método [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) .</span><span class="sxs-lookup"><span data-stu-id="d088b-104">Occurs when the [**InkRecognizerContext**](inkrecognizercontext-class.md) has generated results from the [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d088b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d088b-105">Syntax</span></span>


```C++
void Recognition(
  [in] BSTR                 RecognizedString,
  [in] VARIANT              CustomData,
  [in] InkRecognitionStatus RecognitionStatus
);
```



## <a name="parameters"></a><span data-ttu-id="d088b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d088b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d088b-107">*Reconhecívelstring* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d088b-107">*RecognizedString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d088b-108">O texto de resultado do reconhecimento com a maior confiança.</span><span class="sxs-lookup"><span data-stu-id="d088b-108">The recognition result text with the highest confidence.</span></span>

<span data-ttu-id="d088b-109">Para obter mais informações sobre o tipo de dados BSTR, consulte [usando a biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="d088b-109">For more information about the BSTR data type, see the [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="d088b-110">*CustomData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d088b-110">*CustomData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d088b-111">O objeto que contém os dados personalizados para o resultado do reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="d088b-111">The object that contains the custom data for the recognition result.</span></span>

<span data-ttu-id="d088b-112">Para obter mais informações sobre a estrutura de VARIAntes, consulte [usando a biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="d088b-112">For more information about the VARIANT structure, see the [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="d088b-113">*RecognitionStatus* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d088b-113">*RecognitionStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d088b-114">O status de reconhecimento a partir do resultado de reconhecimento mais recente.</span><span class="sxs-lookup"><span data-stu-id="d088b-114">The recognition status as of the most recent recognition result.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d088b-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d088b-115">Return value</span></span>

<span data-ttu-id="d088b-116">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d088b-116">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d088b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d088b-117">Remarks</span></span>

<span data-ttu-id="d088b-118">O comportamento da API (interface de programação de aplicativo) é imprevisível se você tentar obter acesso ao objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) original do manipulador de eventos de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="d088b-118">The behavior of the application programming interface (API) is unpredictable if you try to gain access to the original [**InkRecognizerContext**](inkrecognizercontext-class.md) object from the recognition event handler.</span></span> <span data-ttu-id="d088b-119">Não tente fazer isso.</span><span class="sxs-lookup"><span data-stu-id="d088b-119">Do not attempt to do this.</span></span> <span data-ttu-id="d088b-120">Em vez disso, se você precisar fazer isso, crie um sinalizador e defina-o no manipulador de eventos de [reconhecimento](ink-recognition.md) .</span><span class="sxs-lookup"><span data-stu-id="d088b-120">Instead, if you need to do this, create a flag and set it in the [Recognition](ink-recognition.md) event handler.</span></span> <span data-ttu-id="d088b-121">Em seguida, você pode sondar esse sinalizador para determinar quando alterar as propriedades **InkRecognizerContext** fora do manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="d088b-121">Then you can poll that flag to determine when to change the **InkRecognizerContext** properties outside of the event handler.</span></span>

<span data-ttu-id="d088b-122">Esse método de evento é definido na \_ interface IInkEvents.</span><span class="sxs-lookup"><span data-stu-id="d088b-122">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="d088b-123">A \_ interface IInkEvents implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IRERecognition DISPID.</span><span class="sxs-lookup"><span data-stu-id="d088b-123">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IRERecognition.</span></span>

## <a name="requirements"></a><span data-ttu-id="d088b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d088b-124">Requirements</span></span>



| <span data-ttu-id="d088b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d088b-125">Requirement</span></span> | <span data-ttu-id="d088b-126">Valor</span><span class="sxs-lookup"><span data-stu-id="d088b-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d088b-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d088b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d088b-128">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d088b-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d088b-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d088b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d088b-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d088b-130">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d088b-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d088b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d088b-132"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d088b-132"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d088b-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d088b-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="d088b-134"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d088b-134"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d088b-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="d088b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d088b-136">**Classe InkRecognizerContext**</span><span class="sxs-lookup"><span data-stu-id="d088b-136">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> <dt>

[<span data-ttu-id="d088b-137">**Método BackgroundRecognize**</span><span class="sxs-lookup"><span data-stu-id="d088b-137">**BackgroundRecognize Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)
</dt> <dt>

[<span data-ttu-id="d088b-138">**Enumeração InkRecognitionStatus**</span><span class="sxs-lookup"><span data-stu-id="d088b-138">**InkRecognitionStatus Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionstatus)
</dt> <dt>

[<span data-ttu-id="d088b-139">**Método Recognize**</span><span class="sxs-lookup"><span data-stu-id="d088b-139">**Recognize Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[<span data-ttu-id="d088b-140">**Interface IInkRecognitionResult**</span><span class="sxs-lookup"><span data-stu-id="d088b-140">**IInkRecognitionResult Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

