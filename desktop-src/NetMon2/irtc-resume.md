---
description: 'Método IRTC:: resume-o método retomar reinicia uma captura pausada.'
ms.assetid: 685dfdee-3bd0-44b3-ac4f-c9960cf77c5c
title: 'Método IRTC:: resume (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 55e5cb66eecbee96df9573e9347d1f32e3508d2b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110554"
---
# <a name="irtcresume-method"></a><span data-ttu-id="f911e-103">Método IRTC:: resume</span><span class="sxs-lookup"><span data-stu-id="f911e-103">IRTC::Resume method</span></span>

<span data-ttu-id="f911e-104">O método **retomar** reinicia uma captura pausada.</span><span class="sxs-lookup"><span data-stu-id="f911e-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="f911e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f911e-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="f911e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f911e-106">Parameters</span></span>

<span data-ttu-id="f911e-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f911e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f911e-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f911e-108">Return value</span></span>

<span data-ttu-id="f911e-109">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="f911e-109">If the method is successful the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="f911e-110">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="f911e-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="f911e-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f911e-111">Return code</span></span>                                                                                                | <span data-ttu-id="f911e-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="f911e-112">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f911e-113"><dt>**captura de NMERR \_ \_ não \_ pausada**</dt></span><span class="sxs-lookup"><span data-stu-id="f911e-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="f911e-114">A captura não está em pausa.</span><span class="sxs-lookup"><span data-stu-id="f911e-114">The capture is not paused.</span></span> <span data-ttu-id="f911e-115">Chame [IRTC::P ause](irtc-pause.md) para pausar a captura.</span><span class="sxs-lookup"><span data-stu-id="f911e-115">Call [IRTC::Pause](irtc-pause.md) to pause the capture.</span></span><br/>                                |
| <dl> <span data-ttu-id="f911e-116"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="f911e-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="f911e-117">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="f911e-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="f911e-118">Chame [IRTC:: Connect](irtc-connect.md) para conectar o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="f911e-118">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="f911e-119"><dt>**NMERR \_ não está em \_ tempo real**</dt></span><span class="sxs-lookup"><span data-stu-id="f911e-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>        | <span data-ttu-id="f911e-120">O NPP está conectado à rede, mas não com o método [IRTC:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="f911e-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="f911e-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="f911e-121">Remarks</span></span>

<span data-ttu-id="f911e-122">Enquanto a captura está em um estado de pausa, novos dados não são capturados até que uma chamada para o método [IRTC:: resume](idelaydc-resume.md) reinicie a captura.</span><span class="sxs-lookup"><span data-stu-id="f911e-122">While the capture is in a paused state, new data is not captured until a call to the [IRTC::Resume](idelaydc-resume.md) method restarts the capture.</span></span>

<span data-ttu-id="f911e-123">Ao usar os métodos **Pause** e **resume** para controlar a captura, monitor de rede continua a adicionar [*Estatísticas de conversa*](c.md) às estatísticas existentes para a captura atual.</span><span class="sxs-lookup"><span data-stu-id="f911e-123">When using the **Pause** and **Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="f911e-124">Para interromper a captura, chame o método [IRTC:: Stop](irtc-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="f911e-124">To stop the capture, call the [IRTC::Stop](irtc-stop.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f911e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f911e-125">Requirements</span></span>



| <span data-ttu-id="f911e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f911e-126">Requirement</span></span> | <span data-ttu-id="f911e-127">Valor</span><span class="sxs-lookup"><span data-stu-id="f911e-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f911e-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f911e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f911e-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f911e-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="f911e-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f911e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f911e-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f911e-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="f911e-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f911e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f911e-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f911e-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="f911e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f911e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f911e-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f911e-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f911e-136">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f911e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f911e-137">IRTC</span><span class="sxs-lookup"><span data-stu-id="f911e-137">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="f911e-138">IRTC:: conectar</span><span class="sxs-lookup"><span data-stu-id="f911e-138">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="f911e-139">IRTC::P ause</span><span class="sxs-lookup"><span data-stu-id="f911e-139">IRTC::Pause</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="f911e-140">IRTC:: Stop</span><span class="sxs-lookup"><span data-stu-id="f911e-140">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




