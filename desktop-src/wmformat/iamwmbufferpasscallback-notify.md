---
title: Método Notify IAMWMBufferPassCallback
description: O método Notify é chamado pelo PIN para cada buffer que é entregue durante o streaming.
ms.assetid: 3f252754-c784-4ffd-bcfc-fab73fa02b9a
keywords:
- Método Notify Windows Media Format
- Método Notify Windows Media Format, interface IAMWMBufferPassCallback
- IAMWMBufferPassCallback interface formato Windows Media, método Notify
topic_type:
- apiref
api_name:
- IAMWMBufferPassCallback.Notify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8f362262b36dee0bfc9a18e57010d102b2fa2cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084795"
---
# <a name="iamwmbufferpasscallbacknotify-method"></a><span data-ttu-id="bec60-106">Método IAMWMBufferPassCallback:: Notify</span><span class="sxs-lookup"><span data-stu-id="bec60-106">IAMWMBufferPassCallback::Notify method</span></span>

<span data-ttu-id="bec60-107">O método **Notify** é chamado pelo PIN para cada buffer que é entregue durante o streaming.</span><span class="sxs-lookup"><span data-stu-id="bec60-107">The **Notify** method is called by the pin for each buffer that is delivered during streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="bec60-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bec60-108">Syntax</span></span>


```C++
HRESULT Notify(
  [in] INSSBuffer3    *pNSSBuffer3,
  [in] IPin           *pPin,
  [in] REFERENCE_TIME *prtStart,
  [in] REFERENCE_TIME *prtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="bec60-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bec60-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bec60-110">*pNSSBuffer3* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bec60-110">*pNSSBuffer3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bec60-111">Ponteiro para a interface [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) exposta no exemplo de mídia.</span><span class="sxs-lookup"><span data-stu-id="bec60-111">Pointer to the [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface exposed on the media sample.</span></span>

</dd> <dt>

<span data-ttu-id="bec60-112">*pPin* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bec60-112">*pPin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bec60-113">Ponteiro para o PIN associado ao fluxo de mídia ao qual o exemplo pertence.</span><span class="sxs-lookup"><span data-stu-id="bec60-113">Pointer to the pin associated with the media stream that the sample belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="bec60-114">*prtStart* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bec60-114">*prtStart* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bec60-115">Hora de início do exemplo.</span><span class="sxs-lookup"><span data-stu-id="bec60-115">Start time of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="bec60-116">*prtEnd* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bec60-116">*prtEnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bec60-117">Hora de término do exemplo.</span><span class="sxs-lookup"><span data-stu-id="bec60-117">End time of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bec60-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bec60-118">Return value</span></span>

<span data-ttu-id="bec60-119">Nenhum valor de retorno específico foi especificado.</span><span class="sxs-lookup"><span data-stu-id="bec60-119">No particular return value is specified.</span></span> <span data-ttu-id="bec60-120">O PIN de chamada ignora o **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="bec60-120">The calling pin ignores the **HRESULT**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bec60-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="bec60-121">Remarks</span></span>

<span data-ttu-id="bec60-122">Esse método permite que um aplicativo examine e atue em informações no buffer de mídia antes que o conteúdo do buffer seja processado.</span><span class="sxs-lookup"><span data-stu-id="bec60-122">This method enables an application to examine and act on information in the media buffer before the buffer contents are processed.</span></span> <span data-ttu-id="bec60-123">O aplicativo é responsável por saber o tipo de mídia no PIN.</span><span class="sxs-lookup"><span data-stu-id="bec60-123">The application is responsible for knowing the media type on the pin.</span></span> <span data-ttu-id="bec60-124">Essas informações podem ser obtidas primeiro obtendo as informações de fluxo do perfil e, em seguida, chamando o método [**IConfigAsfWriter2:: StreamNumFromPin**](iconfigasfwriter2-streamnumfrompin.md) para determinar qual PIN está associado a cada fluxo.</span><span class="sxs-lookup"><span data-stu-id="bec60-124">This information can be obtained by first getting the stream information from the profile and then calling [**IConfigAsfWriter2::StreamNumFromPin**](iconfigasfwriter2-streamnumfrompin.md) method to determine which pin is associated with each stream.</span></span>

## <a name="see-also"></a><span data-ttu-id="bec60-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="bec60-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bec60-126">**Referência do QASF do DirectShow**</span><span class="sxs-lookup"><span data-stu-id="bec60-126">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="bec60-127">**Interface IAMWMBufferPassCallback**</span><span class="sxs-lookup"><span data-stu-id="bec60-127">**IAMWMBufferPassCallback Interface**</span></span>](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback)
</dt> <dt>

[<span data-ttu-id="bec60-128">**Interface INSSBuffer3**</span><span class="sxs-lookup"><span data-stu-id="bec60-128">**INSSBuffer3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3)
</dt> </dl>

 

 