---
description: O método SetMediaLength especifica a duração do arquivo de origem.
ms.assetid: 0a68ad50-91d5-4cb3-95ef-35b9460ac3e4
title: 'Método IAMTimelineSrc:: SetMediaLength (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d585e9076606a77c8ecd03701ad41ab421eacd27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758840"
---
# <a name="iamtimelinesrcsetmedialength-method"></a><span data-ttu-id="fbca7-103">Método IAMTimelineSrc:: SetMediaLength</span><span class="sxs-lookup"><span data-stu-id="fbca7-103">IAMTimelineSrc::SetMediaLength method</span></span>

> [!Note]  
> <span data-ttu-id="fbca7-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="fbca7-104">\[Deprecated.</span></span> <span data-ttu-id="fbca7-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fbca7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fbca7-106">O `SetMediaLength` método especifica a duração do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="fbca7-106">The `SetMediaLength` method specifies the duration of the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbca7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fbca7-107">Syntax</span></span>


```C++
HRESULT SetMediaLength(
   REFERENCE_TIME Length
);
```



## <a name="parameters"></a><span data-ttu-id="fbca7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fbca7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbca7-109">*Comprimento*</span><span class="sxs-lookup"><span data-stu-id="fbca7-109">*Length*</span></span> 
</dt> <dd>

<span data-ttu-id="fbca7-110">Comprimento da mídia, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="fbca7-110">Media length, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbca7-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fbca7-111">Return value</span></span>

<span data-ttu-id="fbca7-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fbca7-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fbca7-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fbca7-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbca7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbca7-114">Remarks</span></span>

<span data-ttu-id="fbca7-115">Você pode evitar possíveis erros de renderização definindo o tamanho da mídia antes de definir a hora de parada da mídia.</span><span class="sxs-lookup"><span data-stu-id="fbca7-115">You can avoid potential rendering errors by setting the media length before you set the media stop time.</span></span> <span data-ttu-id="fbca7-116">Quando você define a hora de parada da mídia, o DES a verifica em relação ao comprimento da mídia.</span><span class="sxs-lookup"><span data-stu-id="fbca7-116">When you set the media stop time, DES checks it against the media length.</span></span>

<span data-ttu-id="fbca7-117">Esse método não valida o parâmetro de *comprimento* , mas o valor deve ser igual à duração real do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="fbca7-117">This method does not validate the *Length* parameter, but the value must equal the actual duration of the source file.</span></span> <span data-ttu-id="fbca7-118">Obtenha a duração do arquivo de origem chamando [**IMediaDet:: get \_ streamLength**](imediadet-get-streamlength.md).</span><span class="sxs-lookup"><span data-stu-id="fbca7-118">Obtain the source file duration by calling [**IMediaDet::get\_StreamLength**](imediadet-get-streamlength.md).</span></span>

> [!Note]  
> <span data-ttu-id="fbca7-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="fbca7-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fbca7-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fbca7-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fbca7-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="fbca7-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fbca7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbca7-122">Requirements</span></span>



| <span data-ttu-id="fbca7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbca7-123">Requirement</span></span> | <span data-ttu-id="fbca7-124">Valor</span><span class="sxs-lookup"><span data-stu-id="fbca7-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbca7-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fbca7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="fbca7-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbca7-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fbca7-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fbca7-127">Library</span></span><br/> | <dl> <span data-ttu-id="fbca7-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fbca7-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbca7-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="fbca7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbca7-130">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="fbca7-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="fbca7-131">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="fbca7-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




