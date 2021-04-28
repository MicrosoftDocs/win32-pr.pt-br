---
description: 'Método IESP:: resume-o método retomar reinicia uma captura pausada.'
ms.assetid: 047ea5f8-de3d-40db-ada3-fc0ef4deccef
title: 'Método IESP:: resume (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 498beda4f2f6c61af918d542542c4ed7b789ba1a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084244"
---
# <a name="iespresume-method"></a><span data-ttu-id="0f79d-103">Método IESP:: resume</span><span class="sxs-lookup"><span data-stu-id="0f79d-103">IESP::Resume method</span></span>

<span data-ttu-id="0f79d-104">O método **retomar** reinicia uma captura pausada.</span><span class="sxs-lookup"><span data-stu-id="0f79d-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f79d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f79d-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="0f79d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f79d-106">Parameters</span></span>

<span data-ttu-id="0f79d-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0f79d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0f79d-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0f79d-108">Return value</span></span>

<span data-ttu-id="0f79d-109">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="0f79d-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="0f79d-110">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="0f79d-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="0f79d-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0f79d-111">Return code</span></span>                                                                                                | <span data-ttu-id="0f79d-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f79d-112">Description</span></span>                                                                                                               |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0f79d-113"><dt>**captura de NMERR \_ \_ não \_ pausada**</dt></span><span class="sxs-lookup"><span data-stu-id="0f79d-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="0f79d-114">A captura não está em pausa.</span><span class="sxs-lookup"><span data-stu-id="0f79d-114">The capture is not paused.</span></span> <span data-ttu-id="0f79d-115">Chame [**IESP::P ause**](iesp-pause.md) para pausar a captura.</span><span class="sxs-lookup"><span data-stu-id="0f79d-115">Call [**IESP::Pause**](iesp-pause.md) to pause the capture.</span></span><br/>                        |
| <dl> <span data-ttu-id="0f79d-116"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="0f79d-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="0f79d-117">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="0f79d-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="0f79d-118">Chame [**IESP:: Connect**](iesp-connect.md) para conectar-se à rede.</span><span class="sxs-lookup"><span data-stu-id="0f79d-118">Call [**IESP::Connect**](iesp-connect.md) to connect to the network.</span></span><br/> |
| <dl> <span data-ttu-id="0f79d-119"><dt>**NMERR \_ não \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="0f79d-119"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>             | <span data-ttu-id="0f79d-120">O NPP está conectado à rede, mas não com o método [**IESP:: Connect**](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="0f79d-120">The NPP is connected to the network, but not with the [**IESP::Connect**](iesp-connect.md) method.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="0f79d-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f79d-121">Remarks</span></span>

<span data-ttu-id="0f79d-122">Enquanto a captura está em um estado de pausa, novos dados não são adicionados ao arquivo de [*captura*](c.md) atual até que **IESP:: resume** seja chamado para reiniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="0f79d-122">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until **IESP::Resume** is called to restart the capture.</span></span> <span data-ttu-id="0f79d-123">Quando **Pause** e **resume** são usados para parar e reiniciar a captura, todas as informações capturadas são colocadas no mesmo arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="0f79d-123">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="0f79d-124">Ao usar **Pause** e **resume** para controlar a captura, monitor de rede continua a adicionar [*Estatísticas de conversa*](c.md) às estatísticas existentes para a captura atual.</span><span class="sxs-lookup"><span data-stu-id="0f79d-124">When using **Pause** and **Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="0f79d-125">Para interromper a captura, chame [**IESP:: Stop**](iesp-stop.md).</span><span class="sxs-lookup"><span data-stu-id="0f79d-125">To stop the capture, call [**IESP::Stop**](iesp-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f79d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f79d-126">Requirements</span></span>



| <span data-ttu-id="0f79d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f79d-127">Requirement</span></span> | <span data-ttu-id="0f79d-128">Valor</span><span class="sxs-lookup"><span data-stu-id="0f79d-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f79d-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f79d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0f79d-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0f79d-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="0f79d-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f79d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0f79d-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0f79d-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="0f79d-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0f79d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f79d-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f79d-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="0f79d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0f79d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f79d-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f79d-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f79d-137">Consulte também</span><span class="sxs-lookup"><span data-stu-id="0f79d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f79d-138">IESP</span><span class="sxs-lookup"><span data-stu-id="0f79d-138">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="0f79d-139">**IESP:: conectar**</span><span class="sxs-lookup"><span data-stu-id="0f79d-139">**IESP::Connect**</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="0f79d-140">**IESP::P ause**</span><span class="sxs-lookup"><span data-stu-id="0f79d-140">**IESP::Pause**</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="0f79d-141">**IESP:: Stop**</span><span class="sxs-lookup"><span data-stu-id="0f79d-141">**IESP::Stop**</span></span>](iesp-stop.md)
</dt> </dl>

 

 




