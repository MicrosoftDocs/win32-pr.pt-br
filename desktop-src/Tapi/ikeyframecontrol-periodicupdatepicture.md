---
description: O método PeriodicUpdatePicture é chamado por um aplicativo para configurar um temporizador no fluxo que solicitará atualizações de imagem periodicamente. As atualizações de imagem causam alto uso de largura de banda, portanto, esse método normalmente será usado em vez de UpdatePicture.
ms.assetid: 6ae3b5e9-bc11-4f3f-972b-21c9ac299987
title: 'IKeyFrameControl: método eriodicUpdatePicture de:P (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50bbfb18b0be96d611f0fe385cc825602dc316ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800032"
---
# <a name="ikeyframecontrolperiodicupdatepicture-method"></a><span data-ttu-id="140c1-104">IKeyFrameControl: método eriodicUpdatePicture de:P</span><span class="sxs-lookup"><span data-stu-id="140c1-104">IKeyFrameControl::PeriodicUpdatePicture method</span></span>

<span data-ttu-id="140c1-105">\[O **PeriodicUpdatePicture** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="140c1-105">\[**PeriodicUpdatePicture** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="140c1-106">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="140c1-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="140c1-107">O método **PeriodicUpdatePicture** é chamado por um aplicativo para configurar um temporizador no fluxo que solicitará atualizações de imagem periodicamente.</span><span class="sxs-lookup"><span data-stu-id="140c1-107">The **PeriodicUpdatePicture** method is called by an application to configure a timer in the stream that will ask for picture updates periodically.</span></span> <span data-ttu-id="140c1-108">As atualizações de imagem causam alto uso de largura de banda, portanto, esse método normalmente será usado em vez de [**UpdatePicture**](ikeyframecontrol-updatepicture.md).</span><span class="sxs-lookup"><span data-stu-id="140c1-108">Picture updates cause high bandwidth usage, so this method will normally be used instead of [**UpdatePicture**](ikeyframecontrol-updatepicture.md).</span></span>

<span data-ttu-id="140c1-109">Se o método for chamado quando o fluxo estiver ativo, o temporizador será iniciado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="140c1-109">If the method is called when the stream is active, the timer will start immediately.</span></span> <span data-ttu-id="140c1-110">Se o fluxo não estiver ativo, o temporizador será iniciado quando o fluxo entrar no estado ativo.</span><span class="sxs-lookup"><span data-stu-id="140c1-110">If the stream is not active, the timer will be started when the stream enters the active state.</span></span>

## <a name="syntax"></a><span data-ttu-id="140c1-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="140c1-111">Syntax</span></span>


```C++
HRESULT PeriodicUpdatePicture(
  [in] BOOL  fEnable,
  [in] DWORD dwInterval
);
```



## <a name="parameters"></a><span data-ttu-id="140c1-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="140c1-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="140c1-113">*fEnable* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="140c1-113">*fEnable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="140c1-114">**Verdadeiro** habilita o temporizador.</span><span class="sxs-lookup"><span data-stu-id="140c1-114">**TRUE** enables the timer.</span></span> <span data-ttu-id="140c1-115">**False** desabilita.</span><span class="sxs-lookup"><span data-stu-id="140c1-115">**FALSE** disables it.</span></span>

</dd> <dt>

<span data-ttu-id="140c1-116">*dwInterval* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="140c1-116">*dwInterval* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="140c1-117">O intervalo para o temporizador, em segundos.</span><span class="sxs-lookup"><span data-stu-id="140c1-117">The interval for the timer, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="140c1-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="140c1-118">Return value</span></span>

<span data-ttu-id="140c1-119">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="140c1-119">This method can return one of these values.</span></span>



| <span data-ttu-id="140c1-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="140c1-120">Return code</span></span>                                                                            | <span data-ttu-id="140c1-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="140c1-121">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="140c1-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="140c1-122"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="140c1-123">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="140c1-123">Method succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="140c1-124"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="140c1-124"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="140c1-125">Falha por motivos inesperados.</span><span class="sxs-lookup"><span data-stu-id="140c1-125">Failed for unexpected reasons.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="140c1-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="140c1-126">Requirements</span></span>



| <span data-ttu-id="140c1-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="140c1-127">Requirement</span></span> | <span data-ttu-id="140c1-128">Valor</span><span class="sxs-lookup"><span data-stu-id="140c1-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="140c1-129">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="140c1-129">TAPI version</span></span><br/> | <span data-ttu-id="140c1-130">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="140c1-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="140c1-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="140c1-131">Header</span></span><br/>       | <dl> <span data-ttu-id="140c1-132"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="140c1-132"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="140c1-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="140c1-133">Library</span></span><br/>      | <dl> <span data-ttu-id="140c1-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="140c1-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="140c1-135">DLL</span><span class="sxs-lookup"><span data-stu-id="140c1-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="140c1-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="140c1-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="140c1-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="140c1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="140c1-138">H323 MSP</span><span class="sxs-lookup"><span data-stu-id="140c1-138">H323 MSP</span></span>](h323-msp.md)
</dt> </dl>

 

 




