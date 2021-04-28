---
description: IRTC::P método ause-o método pause pausa a captura atual.
ms.assetid: 8c7b310e-de04-4bd8-9c96-3c5948e610be
title: 'IRTC: método ause de:P (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d42af1912365a4237889e4e46d0fb3343377c772
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110674"
---
# <a name="irtcpause-method"></a><span data-ttu-id="c7551-103">IRTC: método ause de:P</span><span class="sxs-lookup"><span data-stu-id="c7551-103">IRTC::Pause method</span></span>

<span data-ttu-id="c7551-104">O método **Pause** pausa a captura atual.</span><span class="sxs-lookup"><span data-stu-id="c7551-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7551-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7551-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a><span data-ttu-id="c7551-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7551-106">Parameters</span></span>

<span data-ttu-id="c7551-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c7551-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c7551-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c7551-108">Return value</span></span>

<span data-ttu-id="c7551-109">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="c7551-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c7551-110">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="c7551-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="c7551-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c7551-111">Return code</span></span>                                                                                           | <span data-ttu-id="c7551-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="c7551-112">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c7551-113"><dt>**captura de NMERR \_ \_ pausada**</dt></span><span class="sxs-lookup"><span data-stu-id="c7551-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="c7551-114">A captura já está em pausa.</span><span class="sxs-lookup"><span data-stu-id="c7551-114">The capture is already paused.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="c7551-115"><dt>**NMERR \_ não \_ capturando**</dt></span><span class="sxs-lookup"><span data-stu-id="c7551-115"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="c7551-116">O NPP não está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="c7551-116">The NPP is not capturing data.</span></span> <span data-ttu-id="c7551-117">Chame [IRTC:: Start](irtc-start.md) para iniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="c7551-117">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="c7551-118"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="c7551-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="c7551-119">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="c7551-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="c7551-120">Chame [IRTC:: Connect](irtc-connect.md) para conectar o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="c7551-120">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="c7551-121"><dt>**NMERR \_ não está em \_ tempo real**</dt></span><span class="sxs-lookup"><span data-stu-id="c7551-121"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>   | <span data-ttu-id="c7551-122">O NPP está conectado à rede, mas não com o método [IRTC:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="c7551-122">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="c7551-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7551-123">Remarks</span></span>

<span data-ttu-id="c7551-124">Enquanto a captura está em um estado de pausa, novos quadros não são capturados até que o método [IRTC:: resume](irtc-resume.md) seja chamado para reiniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="c7551-124">While the capture is in a paused state, new frames are not captured until the [IRTC::Resume](irtc-resume.md) method is called to restart the capture.</span></span>

<span data-ttu-id="c7551-125">Quando você usa os métodos **IRTC::P ause** e **IRTC:: resume** para controlar a captura, monitor de rede continua a adicionar [*Estatísticas de conversa*](c.md) sempre que a captura está em execução.</span><span class="sxs-lookup"><span data-stu-id="c7551-125">When you use the **IRTC::Pause** and **IRTC::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="c7551-126">Para reiniciar a chamada de captura [IRTC:: resume](irtc-resume.md).</span><span class="sxs-lookup"><span data-stu-id="c7551-126">To restart the capture call [IRTC::Resume](irtc-resume.md).</span></span> <span data-ttu-id="c7551-127">Para interromper a captura, chame [IRTC:: Stop](irtc-stop.md).</span><span class="sxs-lookup"><span data-stu-id="c7551-127">To stop the capture, call [IRTC::Stop](irtc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7551-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7551-128">Requirements</span></span>



| <span data-ttu-id="c7551-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7551-129">Requirement</span></span> | <span data-ttu-id="c7551-130">Valor</span><span class="sxs-lookup"><span data-stu-id="c7551-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7551-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7551-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c7551-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c7551-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="c7551-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7551-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c7551-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c7551-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="c7551-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c7551-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7551-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7551-136"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="c7551-137">DLL</span><span class="sxs-lookup"><span data-stu-id="c7551-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7551-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7551-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7551-139">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c7551-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7551-140">IRTC</span><span class="sxs-lookup"><span data-stu-id="c7551-140">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="c7551-141">IRTC:: conectar</span><span class="sxs-lookup"><span data-stu-id="c7551-141">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="c7551-142">IRTC:: retomar</span><span class="sxs-lookup"><span data-stu-id="c7551-142">IRTC::Resume</span></span>](irtc-resume.md)
</dt> <dt>

[<span data-ttu-id="c7551-143">IRTC:: iniciar</span><span class="sxs-lookup"><span data-stu-id="c7551-143">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="c7551-144">IRTC:: Stop</span><span class="sxs-lookup"><span data-stu-id="c7551-144">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




