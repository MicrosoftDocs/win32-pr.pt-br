---
description: O método SetMediaTimes define as horas de parada e de início da mídia.
ms.assetid: 9fa7938c-8128-4c26-a738-771d57b315b5
title: 'Método IAMTimelineSrc:: SetMediaTimes (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd8255c7744a155ff8328682005e2aacafaf2d13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810223"
---
# <a name="iamtimelinesrcsetmediatimes-method"></a><span data-ttu-id="99953-103">Método IAMTimelineSrc:: SetMediaTimes</span><span class="sxs-lookup"><span data-stu-id="99953-103">IAMTimelineSrc::SetMediaTimes method</span></span>

> [!Note]  
> <span data-ttu-id="99953-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="99953-104">\[Deprecated.</span></span> <span data-ttu-id="99953-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="99953-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="99953-106">O `SetMediaTimes` método define as horas de parada e de início da mídia.</span><span class="sxs-lookup"><span data-stu-id="99953-106">The `SetMediaTimes` method sets the media stop and start times.</span></span>

## <a name="syntax"></a><span data-ttu-id="99953-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="99953-107">Syntax</span></span>


```C++
HRESULT SetMediaTimes(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="99953-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99953-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99953-109">*Iniciar*</span><span class="sxs-lookup"><span data-stu-id="99953-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="99953-110">Hora de início da mídia, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="99953-110">Media start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="99953-111">*Parar*</span><span class="sxs-lookup"><span data-stu-id="99953-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="99953-112">Hora de parada da mídia, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="99953-112">Media stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99953-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="99953-113">Return value</span></span>

<span data-ttu-id="99953-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="99953-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="99953-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="99953-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="99953-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="99953-116">Remarks</span></span>

<span data-ttu-id="99953-117">As horas de mídia são as horas de parada e de início relativas ao arquivo de mídia original.</span><span class="sxs-lookup"><span data-stu-id="99953-117">The media times are the stop and start times relative to the original media file.</span></span> <span data-ttu-id="99953-118">Sempre defina os horários de mídia ao adicionar uma fonte de vídeo ou áudio à linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="99953-118">Always set the media times when you add a video or audio source to the timeline.</span></span> <span data-ttu-id="99953-119">Caso contrário, podem ocorrer problemas de renderização.</span><span class="sxs-lookup"><span data-stu-id="99953-119">Otherwise, rendering problems might occur.</span></span> <span data-ttu-id="99953-120">A hora de parada deve ser maior que a hora de início.</span><span class="sxs-lookup"><span data-stu-id="99953-120">The stop time must be greater than the start time.</span></span>

<span data-ttu-id="99953-121">Para usar um quadro ainda de uma fonte de vídeo, defina a hora de parada como um valor fracionário mais do que a hora de início, como 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="99953-121">To use a still frame from a video source, set the stop time to a fractional amount more than the start time, such as 100 nanoseconds.</span></span> <span data-ttu-id="99953-122">Configurá-los com o mesmo valor causa um erro de renderização.</span><span class="sxs-lookup"><span data-stu-id="99953-122">Setting them to the same value causes a rendering error.</span></span>

<span data-ttu-id="99953-123">Se a duração da linha do tempo não corresponder à duração da mídia, a origem será ampliada ou reduzida adequadamente.</span><span class="sxs-lookup"><span data-stu-id="99953-123">If the timeline duration does not match the media duration, the source stretches or shrinks accordingly.</span></span> <span data-ttu-id="99953-124">Isso faz com que o clipe seja reproduzido mais devagar ou mais rápido do que a taxa de criação.</span><span class="sxs-lookup"><span data-stu-id="99953-124">This causes the clip to play slower or faster than the authored rate.</span></span> <span data-ttu-id="99953-125">(A mudança de densidade ocorrerá em uma fonte de áudio.) Para obter mais informações, consulte [tempo em serviços de edição do DirectShow](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="99953-125">(Pitch shifting will occur in an audio source.) For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="99953-126">Você pode especificar a duração do arquivo de origem chamando o método [**SetMediaLength**](iamtimelinesrc-setmedialength.md) .</span><span class="sxs-lookup"><span data-stu-id="99953-126">You can specify the duration of the source file by calling the [**SetMediaLength**](iamtimelinesrc-setmedialength.md) method.</span></span> <span data-ttu-id="99953-127">Se você definir uma hora de parada de mídia que exceda a duração, o DES truncará a hora de parada.</span><span class="sxs-lookup"><span data-stu-id="99953-127">If you set a media stop time that exceeds the duration, DES truncates the stop time.</span></span>

> [!Note]  
> <span data-ttu-id="99953-128">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="99953-128">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="99953-129">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="99953-129">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="99953-130">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="99953-130">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="99953-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99953-131">Requirements</span></span>



| <span data-ttu-id="99953-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="99953-132">Requirement</span></span> | <span data-ttu-id="99953-133">Valor</span><span class="sxs-lookup"><span data-stu-id="99953-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99953-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="99953-134">Header</span></span><br/>  | <dl> <span data-ttu-id="99953-135"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="99953-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="99953-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="99953-136">Library</span></span><br/> | <dl> <span data-ttu-id="99953-137"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99953-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99953-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="99953-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99953-139">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="99953-139">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="99953-140">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="99953-140">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




