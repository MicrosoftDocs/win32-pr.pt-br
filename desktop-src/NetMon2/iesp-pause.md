---
description: IESP::P método ause-o método pause pausa a captura atual.
ms.assetid: efbc8947-b9fe-4dbd-8097-375b5f99845e
title: 'IESP: método ause de:P (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 486c7aedc7092e0dd0f9f68cc1ea2ccad08d9438
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084234"
---
# <a name="iesppause-method"></a><span data-ttu-id="72bf4-103">IESP: método ause de:P</span><span class="sxs-lookup"><span data-stu-id="72bf4-103">IESP::Pause method</span></span>

<span data-ttu-id="72bf4-104">O método **Pause** pausa a captura atual.</span><span class="sxs-lookup"><span data-stu-id="72bf4-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="72bf4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72bf4-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause(
   LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="72bf4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72bf4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72bf4-107">*lpStats*</span><span class="sxs-lookup"><span data-stu-id="72bf4-107">*lpStats*</span></span> 
</dt> <dd>

<span data-ttu-id="72bf4-108">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="72bf4-108">Obsolete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72bf4-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="72bf4-109">Return value</span></span>

<span data-ttu-id="72bf4-110">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="72bf4-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="72bf4-111">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="72bf4-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="72bf4-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="72bf4-112">Return code</span></span>                                                                                           | <span data-ttu-id="72bf4-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="72bf4-113">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="72bf4-114"><dt>**captura de NMERR \_ \_ pausada**</dt></span><span class="sxs-lookup"><span data-stu-id="72bf4-114"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="72bf4-115">A captura já está em pausa.</span><span class="sxs-lookup"><span data-stu-id="72bf4-115">The capture is already paused.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="72bf4-116"><dt>**NMERR \_ não \_ capturando**</dt></span><span class="sxs-lookup"><span data-stu-id="72bf4-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="72bf4-117">O NPP não está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="72bf4-117">The NPP is not capturing data.</span></span> <span data-ttu-id="72bf4-118">Chame [IESP:: Start](iesp-start.md) para iniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="72bf4-118">Call [IESP::Start](iesp-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="72bf4-119"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="72bf4-119"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="72bf4-120">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="72bf4-120">The NPP is not connected to the network.</span></span> <span data-ttu-id="72bf4-121">Chame [IESP:: Connect](iesp-connect.md) para conectar o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="72bf4-121">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="72bf4-122"><dt>**NMERR \_ não \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="72bf4-122"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>        | <span data-ttu-id="72bf4-123">O NPP está conectado à rede, mas não com o método [IESP:: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="72bf4-123">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="72bf4-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="72bf4-124">Remarks</span></span>

<span data-ttu-id="72bf4-125">Enquanto a captura está em um estado de pausa, novos dados não são adicionados ao arquivo de [*captura*](c.md) atual até que você chame o método [IESP:: resume](iesp-resume.md) para reiniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="72bf4-125">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until you call the [IESP::Resume](iesp-resume.md) method to restart the capture.</span></span> <span data-ttu-id="72bf4-126">Quando **Pause** e **resume** são usados para parar e reiniciar a captura, todas as informações capturadas são colocadas no mesmo arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="72bf4-126">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="72bf4-127">Quando você usa os métodos **IESP::P ause** e **IESP:: resume** para controlar a captura, monitor de rede continua a adicionar [*Estatísticas de conversa*](c.md) sempre que a captura está em execução.</span><span class="sxs-lookup"><span data-stu-id="72bf4-127">When you use the **IESP::Pause** and **IESP::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="72bf4-128">Para reiniciar a captura, chame [IESP:: resume](iesp-resume.md).</span><span class="sxs-lookup"><span data-stu-id="72bf4-128">To restart the capture, call [IESP::Resume](iesp-resume.md).</span></span> <span data-ttu-id="72bf4-129">Para interromper a captura, chame [IESP:: Stop](iesp-stop.md).</span><span class="sxs-lookup"><span data-stu-id="72bf4-129">To stop the capture, call [IESP::Stop](iesp-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="72bf4-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72bf4-130">Requirements</span></span>



| <span data-ttu-id="72bf4-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="72bf4-131">Requirement</span></span> | <span data-ttu-id="72bf4-132">Valor</span><span class="sxs-lookup"><span data-stu-id="72bf4-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72bf4-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72bf4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="72bf4-134">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="72bf4-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="72bf4-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72bf4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="72bf4-136">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="72bf4-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="72bf4-137">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="72bf4-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="72bf4-138"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="72bf4-138"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="72bf4-139">DLL</span><span class="sxs-lookup"><span data-stu-id="72bf4-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72bf4-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72bf4-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72bf4-141">Consulte também</span><span class="sxs-lookup"><span data-stu-id="72bf4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72bf4-142">IESP</span><span class="sxs-lookup"><span data-stu-id="72bf4-142">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="72bf4-143">IESP:: conectar</span><span class="sxs-lookup"><span data-stu-id="72bf4-143">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="72bf4-144">IESP:: retomar</span><span class="sxs-lookup"><span data-stu-id="72bf4-144">IESP::Resume</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="72bf4-145">IESP:: iniciar</span><span class="sxs-lookup"><span data-stu-id="72bf4-145">IESP::Start</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="72bf4-146">IESP:: Stop</span><span class="sxs-lookup"><span data-stu-id="72bf4-146">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




