---
description: O \_ método Get MediaName Obtém o nome da mídia. As mídias definidas são áudio, vídeo, quadro de comunicações, texto e dados.
ms.assetid: 4afb24f9-582e-420d-8bda-772a3dc4d96c
title: 'Método ITMedia:: get_MediaName (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9152994eac98d5e846ac147072a51a3334930da9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758119"
---
# <a name="itmediaget_medianame-method"></a><span data-ttu-id="1fa7a-104">Método ITMedia:: get \_ MediaName</span><span class="sxs-lookup"><span data-stu-id="1fa7a-104">ITMedia::get\_MediaName method</span></span>

<span data-ttu-id="1fa7a-105">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1fa7a-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1fa7a-106">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="1fa7a-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1fa7a-107">O método **Get \_ MediaName** Obtém o nome da mídia.</span><span class="sxs-lookup"><span data-stu-id="1fa7a-107">The **get\_MediaName** method gets the media name.</span></span> <span data-ttu-id="1fa7a-108">As mídias definidas são áudio, vídeo, quadro de comunicações, texto e dados.</span><span class="sxs-lookup"><span data-stu-id="1fa7a-108">Defined media are audio, video, whiteboard, text, and data.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fa7a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1fa7a-109">Syntax</span></span>


```C++
HRESULT get_MediaName(
  [out] BSTR *ppMediaName
);
```



## <a name="parameters"></a><span data-ttu-id="1fa7a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1fa7a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fa7a-111">*ppMediaName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1fa7a-111">*ppMediaName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1fa7a-112">Ponteiro para um **BSTR** que contém o nome da mídia, como áudio.</span><span class="sxs-lookup"><span data-stu-id="1fa7a-112">Pointer to a **BSTR** containing the name of the media, such as audio.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fa7a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1fa7a-113">Return value</span></span>

<span data-ttu-id="1fa7a-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="1fa7a-114">This method can return one of these values.</span></span>



| <span data-ttu-id="1fa7a-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1fa7a-115">Return code</span></span>                                                                                   | <span data-ttu-id="1fa7a-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="1fa7a-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="1fa7a-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1fa7a-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1fa7a-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="1fa7a-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1fa7a-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="1fa7a-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1fa7a-120">O parâmetro *ppMediaName* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="1fa7a-120">The *ppMediaName* parameter is not a valid pointer.</span></span><br/>  |
| <dl> <span data-ttu-id="1fa7a-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1fa7a-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1fa7a-122">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="1fa7a-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="1fa7a-123"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="1fa7a-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="1fa7a-124">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="1fa7a-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="1fa7a-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="1fa7a-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="1fa7a-126">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="1fa7a-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="1fa7a-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="1fa7a-127">Remarks</span></span>

<span data-ttu-id="1fa7a-128">O aplicativo deve usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória alocada para o parâmetro *ppMediaName* .</span><span class="sxs-lookup"><span data-stu-id="1fa7a-128">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppMediaName* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fa7a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fa7a-129">Requirements</span></span>



| <span data-ttu-id="1fa7a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fa7a-130">Requirement</span></span> | <span data-ttu-id="1fa7a-131">Valor</span><span class="sxs-lookup"><span data-stu-id="1fa7a-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1fa7a-132">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="1fa7a-132">TAPI version</span></span><br/> | <span data-ttu-id="1fa7a-133">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="1fa7a-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="1fa7a-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1fa7a-134">Header</span></span><br/>       | <dl> <span data-ttu-id="1fa7a-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fa7a-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="1fa7a-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1fa7a-136">Library</span></span><br/>      | <dl> <span data-ttu-id="1fa7a-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1fa7a-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1fa7a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="1fa7a-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="1fa7a-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fa7a-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fa7a-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="1fa7a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fa7a-141">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="1fa7a-141">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="1fa7a-142">**ITMedia::p UT \_ MediaName**</span><span class="sxs-lookup"><span data-stu-id="1fa7a-142">**ITMedia::put\_MediaName**</span></span>](itmedia-put-medianame.md)
</dt> </dl>

 

