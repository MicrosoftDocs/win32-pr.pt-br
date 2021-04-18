---
description: O método GetConnectedMediaType recupera o tipo de mídia para a conexão no pino de entrada do exemplo de apoio.
ms.assetid: 65f5603a-1151-4ffd-a662-84e265663b04
title: 'Método ISampleGrabber:: GetConnectedMediaType (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetConnectedMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 85e30820afdca865f438ac40521a9be540fd4a1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810170"
---
# <a name="isamplegrabbergetconnectedmediatype-method"></a><span data-ttu-id="bb4b2-103">Método ISampleGrabber:: GetConnectedMediaType</span><span class="sxs-lookup"><span data-stu-id="bb4b2-103">ISampleGrabber::GetConnectedMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="bb4b2-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="bb4b2-104">\[Deprecated.</span></span> <span data-ttu-id="bb4b2-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bb4b2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bb4b2-106">O `GetConnectedMediaType` método recupera o tipo de mídia para a conexão no pino de entrada do exemplo de apoio.</span><span class="sxs-lookup"><span data-stu-id="bb4b2-106">The `GetConnectedMediaType` method retrieves the media type for the connection on the input pin of the Sample Grabber.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb4b2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb4b2-107">Syntax</span></span>


```C++
HRESULT GetConnectedMediaType(
   AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a><span data-ttu-id="bb4b2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb4b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb4b2-109">*pType*</span><span class="sxs-lookup"><span data-stu-id="bb4b2-109">*pType*</span></span> 
</dt> <dd>

<span data-ttu-id="bb4b2-110">Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) alocada pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="bb4b2-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure allocated by the caller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb4b2-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bb4b2-111">Return value</span></span>

<span data-ttu-id="bb4b2-112">Retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="bb4b2-112">Returns one of the following values.</span></span>



| <span data-ttu-id="bb4b2-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="bb4b2-113">Return code</span></span>                                                                                           | <span data-ttu-id="bb4b2-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb4b2-114">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="bb4b2-115"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="bb4b2-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="bb4b2-116">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="bb4b2-116">**NULL** pointer argument.</span></span><br/>   |
| <dl> <span data-ttu-id="bb4b2-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bb4b2-117"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="bb4b2-118">Êxito.</span><span class="sxs-lookup"><span data-stu-id="bb4b2-118">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="bb4b2-119"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="bb4b2-119"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="bb4b2-120">O filtro não está conectado.</span><span class="sxs-lookup"><span data-stu-id="bb4b2-120">The filter is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bb4b2-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb4b2-121">Remarks</span></span>

<span data-ttu-id="bb4b2-122">Esse método copia o tipo de mídia para a estrutura do **\_ \_ tipo de mídia am** especificada por *pType*.</span><span class="sxs-lookup"><span data-stu-id="bb4b2-122">This method copies the media type into the **AM\_MEDIA\_TYPE** structure specified by *pType*.</span></span> <span data-ttu-id="bb4b2-123">O chamador deve liberar o bloco de formato do tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="bb4b2-123">The caller must free the format block of the media type.</span></span> <span data-ttu-id="bb4b2-124">Você pode usar a função **CoTaskMemFree** ou a função [**FreeMediaType**](freemediatype.md) na biblioteca de classe base.</span><span class="sxs-lookup"><span data-stu-id="bb4b2-124">You can use the **CoTaskMemFree** function, or the [**FreeMediaType**](freemediatype.md) function in the base-class library.</span></span>

> [!Note]  
> <span data-ttu-id="bb4b2-125">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="bb4b2-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="bb4b2-126">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="bb4b2-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="bb4b2-127">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="bb4b2-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bb4b2-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb4b2-128">Requirements</span></span>



| <span data-ttu-id="bb4b2-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb4b2-129">Requirement</span></span> | <span data-ttu-id="bb4b2-130">Valor</span><span class="sxs-lookup"><span data-stu-id="bb4b2-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb4b2-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bb4b2-131">Header</span></span><br/>  | <dl> <span data-ttu-id="bb4b2-132"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb4b2-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="bb4b2-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bb4b2-133">Library</span></span><br/> | <dl> <span data-ttu-id="bb4b2-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb4b2-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb4b2-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb4b2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb4b2-136">Usando o exemplo de apoio</span><span class="sxs-lookup"><span data-stu-id="bb4b2-136">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="bb4b2-137">**Interface ISampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="bb4b2-137">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




