---
description: O método IsNormalRate indica se o clipe será reproduzido na taxa de reprodução normal; ou seja, a taxa de reprodução do arquivo original.
ms.assetid: 4a8fe415-f9eb-450d-9a75-e528577050d9
title: 'Método IAMTimelineSrc:: IsNormalRate (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.IsNormalRate
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e368efcf29d836cc23fa60ed34dae1a172978f77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780057"
---
# <a name="iamtimelinesrcisnormalrate-method"></a><span data-ttu-id="49eeb-103">Método IAMTimelineSrc:: IsNormalRate</span><span class="sxs-lookup"><span data-stu-id="49eeb-103">IAMTimelineSrc::IsNormalRate method</span></span>

> [!Note]  
> <span data-ttu-id="49eeb-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="49eeb-104">\[Deprecated.</span></span> <span data-ttu-id="49eeb-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="49eeb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="49eeb-106">O `IsNormalRate` método indica se o clipe será reproduzido na taxa de reprodução normal; ou seja, a taxa de reprodução do arquivo original.</span><span class="sxs-lookup"><span data-stu-id="49eeb-106">The `IsNormalRate` method indicates whether the clip will play at the normal playback rate; that is, the playback rate of the original file.</span></span>

## <a name="syntax"></a><span data-ttu-id="49eeb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49eeb-107">Syntax</span></span>


```C++
HRESULT IsNormalRate(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="49eeb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49eeb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49eeb-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="49eeb-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="49eeb-110">Recebe um valor booliano que indica como o clipe será renderizado.</span><span class="sxs-lookup"><span data-stu-id="49eeb-110">Receives a Boolean value indicating how the clip will render.</span></span> <span data-ttu-id="49eeb-111">Se o valor for **true**, o clipe será reproduzido na taxa normal.</span><span class="sxs-lookup"><span data-stu-id="49eeb-111">If the value is **TRUE**, the clip will play at the normal rate.</span></span> <span data-ttu-id="49eeb-112">Caso contrário, ele será executado mais rápido ou mais devagar do que o normal.</span><span class="sxs-lookup"><span data-stu-id="49eeb-112">Otherwise, it will play faster or slower than normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49eeb-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="49eeb-113">Return value</span></span>

<span data-ttu-id="49eeb-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="49eeb-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="49eeb-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="49eeb-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="49eeb-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="49eeb-116">Remarks</span></span>

<span data-ttu-id="49eeb-117">A taxa de reprodução de um clipe é determinada por seus horários de início e parada de mídia, em relação às horas da linha do tempo:</span><span class="sxs-lookup"><span data-stu-id="49eeb-117">A clip's playback rate is determined by its media start and stop times, relative to its timeline times:</span></span>


```C++
Playback rate = (Media Stop <entity type="mdash"/> Media Start) / (Timeline Stop <entity type="mdash"/> Timeline Start)
```



<span data-ttu-id="49eeb-118">Se essa taxa for igual a 1, o clipe será reproduzido na velocidade criada.</span><span class="sxs-lookup"><span data-stu-id="49eeb-118">If this ratio is equal to 1, the clip plays at the authored speed.</span></span> <span data-ttu-id="49eeb-119">Caso contrário, ele será executado mais rápido ou mais devagar.</span><span class="sxs-lookup"><span data-stu-id="49eeb-119">Otherwise, it plays faster or slower.</span></span> <span data-ttu-id="49eeb-120">Para obter mais informações, consulte [tempo em serviços de edição do DirectShow](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="49eeb-120">For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

> [!Note]  
> <span data-ttu-id="49eeb-121">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="49eeb-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="49eeb-122">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="49eeb-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="49eeb-123">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="49eeb-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="49eeb-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49eeb-124">Requirements</span></span>



| <span data-ttu-id="49eeb-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="49eeb-125">Requirement</span></span> | <span data-ttu-id="49eeb-126">Valor</span><span class="sxs-lookup"><span data-stu-id="49eeb-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49eeb-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="49eeb-127">Header</span></span><br/>  | <dl> <span data-ttu-id="49eeb-128"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="49eeb-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="49eeb-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="49eeb-129">Library</span></span><br/> | <dl> <span data-ttu-id="49eeb-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49eeb-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49eeb-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="49eeb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49eeb-132">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="49eeb-132">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="49eeb-133">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="49eeb-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




