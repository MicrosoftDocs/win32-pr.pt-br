---
description: O método retomar reinicia uma captura pausada.
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
ms.openlocfilehash: 01bbb748fc91bcc5a78b281ec9ebdd2a6d479888
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759671"
---
# <a name="iespresume-method"></a><span data-ttu-id="dab40-103">Método IESP:: resume</span><span class="sxs-lookup"><span data-stu-id="dab40-103">IESP::Resume method</span></span>

<span data-ttu-id="dab40-104">O método **retomar** reinicia uma captura pausada.</span><span class="sxs-lookup"><span data-stu-id="dab40-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="dab40-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dab40-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="dab40-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dab40-106">Parameters</span></span>

<span data-ttu-id="dab40-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="dab40-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dab40-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dab40-108">Return value</span></span>

<span data-ttu-id="dab40-109">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="dab40-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="dab40-110">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="dab40-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="dab40-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="dab40-111">Return code</span></span>                                                                                                | <span data-ttu-id="dab40-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="dab40-112">Description</span></span>                                                                                                               |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dab40-113"><dt>**captura de NMERR \_ \_ não \_ pausada**</dt></span><span class="sxs-lookup"><span data-stu-id="dab40-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="dab40-114">A captura não está em pausa.</span><span class="sxs-lookup"><span data-stu-id="dab40-114">The capture is not paused.</span></span> <span data-ttu-id="dab40-115">Chame [**IESP::P ause**](iesp-pause.md) para pausar a captura.</span><span class="sxs-lookup"><span data-stu-id="dab40-115">Call [**IESP::Pause**](iesp-pause.md) to pause the capture.</span></span><br/>                        |
| <dl> <span data-ttu-id="dab40-116"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="dab40-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="dab40-117">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="dab40-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="dab40-118">Chame [**IESP:: Connect**](iesp-connect.md) para conectar-se à rede.</span><span class="sxs-lookup"><span data-stu-id="dab40-118">Call [**IESP::Connect**](iesp-connect.md) to connect to the network.</span></span><br/> |
| <dl> <span data-ttu-id="dab40-119"><dt>**NMERR \_ não \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="dab40-119"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>             | <span data-ttu-id="dab40-120">O NPP está conectado à rede, mas não com o método [**IESP:: Connect**](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="dab40-120">The NPP is connected to the network, but not with the [**IESP::Connect**](iesp-connect.md) method.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="dab40-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="dab40-121">Remarks</span></span>

<span data-ttu-id="dab40-122">Enquanto a captura está em um estado de pausa, novos dados não são adicionados ao arquivo de [*captura*](c.md) atual até que **IESP:: resume** seja chamado para reiniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="dab40-122">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until **IESP::Resume** is called to restart the capture.</span></span> <span data-ttu-id="dab40-123">Quando **Pause** e **resume** são usados para parar e reiniciar a captura, todas as informações capturadas são colocadas no mesmo arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="dab40-123">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="dab40-124">Ao usar **Pause** e **resume** para controlar a captura, monitor de rede continua a adicionar [*Estatísticas de conversa*](c.md) às estatísticas existentes para a captura atual.</span><span class="sxs-lookup"><span data-stu-id="dab40-124">When using **Pause** and **Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="dab40-125">Para interromper a captura, chame [**IESP:: Stop**](iesp-stop.md).</span><span class="sxs-lookup"><span data-stu-id="dab40-125">To stop the capture, call [**IESP::Stop**](iesp-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dab40-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dab40-126">Requirements</span></span>



| <span data-ttu-id="dab40-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="dab40-127">Requirement</span></span> | <span data-ttu-id="dab40-128">Valor</span><span class="sxs-lookup"><span data-stu-id="dab40-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dab40-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dab40-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dab40-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dab40-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="dab40-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dab40-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dab40-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dab40-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="dab40-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="dab40-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="dab40-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="dab40-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="dab40-135">DLL</span><span class="sxs-lookup"><span data-stu-id="dab40-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dab40-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dab40-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dab40-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="dab40-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dab40-138">IESP</span><span class="sxs-lookup"><span data-stu-id="dab40-138">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="dab40-139">**IESP:: conectar**</span><span class="sxs-lookup"><span data-stu-id="dab40-139">**IESP::Connect**</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="dab40-140">**IESP::P ause**</span><span class="sxs-lookup"><span data-stu-id="dab40-140">**IESP::Pause**</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="dab40-141">**IESP:: Stop**</span><span class="sxs-lookup"><span data-stu-id="dab40-141">**IESP::Stop**</span></span>](iesp-stop.md)
</dt> </dl>

 

 




