---
description: 'O método GetInfo recupera informações sobre as configurações de controle de fluxo atuais, incluindo os horários de início e de parada. Esse método implementa o método IAMStreamControl:: GetInfo.'
ms.assetid: 3bc9bb32-eb33-4752-b22c-9033c28b41f7
title: Método CBaseStreamControl. GetInfo (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.GetInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab0ba31fa5692a6bc92372860ec1a28ab776206f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757036"
---
# <a name="cbasestreamcontrolgetinfo-method"></a><span data-ttu-id="11939-104">Método CBaseStreamControl. GetInfo</span><span class="sxs-lookup"><span data-stu-id="11939-104">CBaseStreamControl.GetInfo method</span></span>

<span data-ttu-id="11939-105">O `GetInfo` método recupera informações sobre as configurações de controle de fluxo atuais, incluindo os horários de início e de parada.</span><span class="sxs-lookup"><span data-stu-id="11939-105">The `GetInfo` method retrieves information about the current stream-control settings, including the start and stop times.</span></span> <span data-ttu-id="11939-106">Esse método implementa o método [**IAMStreamControl:: GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-getinfo) .</span><span class="sxs-lookup"><span data-stu-id="11939-106">This method implements the [**IAMStreamControl::GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-getinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="11939-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11939-107">Syntax</span></span>


```C++
HRESULT GetInfo(
   AM_STREAM_INFO *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="11939-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11939-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11939-109">*pInfo*</span><span class="sxs-lookup"><span data-stu-id="11939-109">*pInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="11939-110">Ponteiro para uma estrutura de [**\_ \_ informações de fluxo am**](/windows/desktop/api/strmif/ns-strmif-am_stream_info) , alocada pelo chamador, que recebe as configurações de controle de fluxo atuais.</span><span class="sxs-lookup"><span data-stu-id="11939-110">Pointer to an [**AM\_STREAM\_INFO**](/windows/desktop/api/strmif/ns-strmif-am_stream_info) structure, allocated by the caller, that receives the current stream-control settings.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11939-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="11939-111">Return value</span></span>

<span data-ttu-id="11939-112">Retorna S \_ OK ou o \_ ponteiro.</span><span class="sxs-lookup"><span data-stu-id="11939-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="11939-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11939-113">Requirements</span></span>



| <span data-ttu-id="11939-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="11939-114">Requirement</span></span> | <span data-ttu-id="11939-115">Valor</span><span class="sxs-lookup"><span data-stu-id="11939-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11939-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="11939-116">Header</span></span><br/>  | <dl> <span data-ttu-id="11939-117"><dt>Strmctl. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11939-117"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="11939-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="11939-118">Library</span></span><br/> | <dl> <span data-ttu-id="11939-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="11939-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11939-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="11939-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11939-121">**Classe CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="11939-121">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




