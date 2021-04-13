---
description: O método pause pausa a captura atual.
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
ms.openlocfilehash: 0558c5dfe36f26e3aad9f31101364d2e8e5c4967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501344"
---
# <a name="iesppause-method"></a><span data-ttu-id="f3a8b-103">IESP: método ause de:P</span><span class="sxs-lookup"><span data-stu-id="f3a8b-103">IESP::Pause method</span></span>

<span data-ttu-id="f3a8b-104">O método **Pause** pausa a captura atual.</span><span class="sxs-lookup"><span data-stu-id="f3a8b-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3a8b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f3a8b-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause(
   LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="f3a8b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3a8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3a8b-107">*lpStats*</span><span class="sxs-lookup"><span data-stu-id="f3a8b-107">*lpStats*</span></span> 
</dt> <dd>

<span data-ttu-id="f3a8b-108">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="f3a8b-108">Obsolete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3a8b-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f3a8b-109">Return value</span></span>

<span data-ttu-id="f3a8b-110">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="f3a8b-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="f3a8b-111">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="f3a8b-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="f3a8b-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f3a8b-112">Return code</span></span>                                                                                           | <span data-ttu-id="f3a8b-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="f3a8b-113">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f3a8b-114"><dt>**captura de NMERR \_ \_ pausada**</dt></span><span class="sxs-lookup"><span data-stu-id="f3a8b-114"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="f3a8b-115">A captura já está em pausa.</span><span class="sxs-lookup"><span data-stu-id="f3a8b-115">The capture is already paused.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="f3a8b-116"><dt>**NMERR \_ não \_ capturando**</dt></span><span class="sxs-lookup"><span data-stu-id="f3a8b-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="f3a8b-117">O NPP não está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="f3a8b-117">The NPP is not capturing data.</span></span> <span data-ttu-id="f3a8b-118">Chame [IESP:: Start](iesp-start.md) para iniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="f3a8b-118">Call [IESP::Start](iesp-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="f3a8b-119"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="f3a8b-119"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="f3a8b-120">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="f3a8b-120">The NPP is not connected to the network.</span></span> <span data-ttu-id="f3a8b-121">Chame [IESP:: Connect](iesp-connect.md) para conectar o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="f3a8b-121">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="f3a8b-122"><dt>**NMERR \_ não \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="f3a8b-122"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>        | <span data-ttu-id="f3a8b-123">O NPP está conectado à rede, mas não com o método [IESP:: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="f3a8b-123">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="f3a8b-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3a8b-124">Remarks</span></span>

<span data-ttu-id="f3a8b-125">Enquanto a captura está em um estado de pausa, novos dados não são adicionados ao arquivo de [*captura*](c.md) atual até que você chame o método [IESP:: resume](iesp-resume.md) para reiniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="f3a8b-125">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until you call the [IESP::Resume](iesp-resume.md) method to restart the capture.</span></span> <span data-ttu-id="f3a8b-126">Quando **Pause** e **resume** são usados para parar e reiniciar a captura, todas as informações capturadas são colocadas no mesmo arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="f3a8b-126">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="f3a8b-127">Quando você usa os métodos **IESP::P ause** e **IESP:: resume** para controlar a captura, monitor de rede continua a adicionar [*Estatísticas de conversa*](c.md) sempre que a captura está em execução.</span><span class="sxs-lookup"><span data-stu-id="f3a8b-127">When you use the **IESP::Pause** and **IESP::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="f3a8b-128">Para reiniciar a captura, chame [IESP:: resume](iesp-resume.md).</span><span class="sxs-lookup"><span data-stu-id="f3a8b-128">To restart the capture, call [IESP::Resume](iesp-resume.md).</span></span> <span data-ttu-id="f3a8b-129">Para interromper a captura, chame [IESP:: Stop](iesp-stop.md).</span><span class="sxs-lookup"><span data-stu-id="f3a8b-129">To stop the capture, call [IESP::Stop](iesp-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3a8b-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3a8b-130">Requirements</span></span>



| <span data-ttu-id="f3a8b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3a8b-131">Requirement</span></span> | <span data-ttu-id="f3a8b-132">Valor</span><span class="sxs-lookup"><span data-stu-id="f3a8b-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3a8b-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3a8b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f3a8b-134">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f3a8b-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="f3a8b-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3a8b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f3a8b-136">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f3a8b-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="f3a8b-137">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f3a8b-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3a8b-138"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3a8b-138"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="f3a8b-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f3a8b-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3a8b-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3a8b-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3a8b-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3a8b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3a8b-142">IESP</span><span class="sxs-lookup"><span data-stu-id="f3a8b-142">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="f3a8b-143">IESP:: conectar</span><span class="sxs-lookup"><span data-stu-id="f3a8b-143">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="f3a8b-144">IESP:: retomar</span><span class="sxs-lookup"><span data-stu-id="f3a8b-144">IESP::Resume</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="f3a8b-145">IESP:: iniciar</span><span class="sxs-lookup"><span data-stu-id="f3a8b-145">IESP::Start</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="f3a8b-146">IESP:: Stop</span><span class="sxs-lookup"><span data-stu-id="f3a8b-146">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




