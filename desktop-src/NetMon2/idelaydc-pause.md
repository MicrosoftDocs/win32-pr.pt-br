---
description: O método pause pausa a captura atual.
ms.assetid: 9d5e11d1-8c45-4cf5-9fea-10c9e7a6fe86
title: 'IDelaydC: método ause de:P (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d44ae7792388d9ca637232b45e63d618a37acb6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826827"
---
# <a name="idelaydcpause-method"></a><span data-ttu-id="f8fb3-103">IDelaydC: método ause de:P</span><span class="sxs-lookup"><span data-stu-id="f8fb3-103">IDelaydC::Pause method</span></span>

<span data-ttu-id="f8fb3-104">O método **Pause** pausa a captura atual.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8fb3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8fb3-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a><span data-ttu-id="f8fb3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8fb3-106">Parameters</span></span>

<span data-ttu-id="f8fb3-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f8fb3-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f8fb3-108">Return value</span></span>

<span data-ttu-id="f8fb3-109">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="f8fb3-110">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="f8fb3-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="f8fb3-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f8fb3-111">Return code</span></span>                                                                                           | <span data-ttu-id="f8fb3-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="f8fb3-112">Description</span></span>                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f8fb3-113"><dt>**captura de NMERR \_ \_ pausada**</dt></span><span class="sxs-lookup"><span data-stu-id="f8fb3-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="f8fb3-114">A captura já está em um estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-114">The capture is already in a paused state.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="f8fb3-115"><dt>**NMERR \_ não \_ capturando**</dt></span><span class="sxs-lookup"><span data-stu-id="f8fb3-115"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="f8fb3-116">O NPP não está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-116">The NPP is not capturing data.</span></span> <span data-ttu-id="f8fb3-117">Chame [IDelaydC:: Start](idelaydc-start.md) para iniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-117">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="f8fb3-118"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="f8fb3-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="f8fb3-119">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="f8fb3-120">Chame [IDelaydC:: Connect](idelaydc-connect.md) para conectar o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-120">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="f8fb3-121"><dt>**NMERR \_ não \_ atrasada**</dt></span><span class="sxs-lookup"><span data-stu-id="f8fb3-121"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>    | <span data-ttu-id="f8fb3-122">O NPP está conectado à rede, mas não com o método [IDelaydC:: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="f8fb3-122">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="f8fb3-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8fb3-123">Remarks</span></span>

<span data-ttu-id="f8fb3-124">Enquanto a captura está em um estado de pausa, novos dados não são adicionados ao arquivo de [*captura*](c.md) atual até que o método **IDelaydC:: resume** seja chamado para reiniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-124">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until the **IDelaydC::Resume** method is called to restart the capture.</span></span> <span data-ttu-id="f8fb3-125">Quando **Pause** e **resume** são usados para parar e reiniciar a captura, todas as informações capturadas são colocadas no mesmo arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-125">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="f8fb3-126">Ao usar **IDelaydC::P ause** e **IDelaydC:: retomar** para controlar a captura, monitor de rede continuará a adicionar [*Estatísticas de conversa*](c.md) sempre que a captura estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-126">When using **IDelaydC::Pause** and **IDelaydC::Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="f8fb3-127">Para reiniciar a captura, chame [IDelaydC:: resume](idelaydc-resume.md).</span><span class="sxs-lookup"><span data-stu-id="f8fb3-127">To restart the capture, call [IDelaydC::Resume](idelaydc-resume.md).</span></span>

<span data-ttu-id="f8fb3-128">Para interromper a captura, chame [IDelaydC:: Stop](idelaydc-stop.md).</span><span class="sxs-lookup"><span data-stu-id="f8fb3-128">To stop the capture, call [IDelaydC::Stop](idelaydc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8fb3-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8fb3-129">Requirements</span></span>



| <span data-ttu-id="f8fb3-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8fb3-130">Requirement</span></span> | <span data-ttu-id="f8fb3-131">Valor</span><span class="sxs-lookup"><span data-stu-id="f8fb3-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8fb3-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8fb3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f8fb3-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f8fb3-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="f8fb3-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8fb3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f8fb3-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f8fb3-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="f8fb3-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f8fb3-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8fb3-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8fb3-137"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="f8fb3-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f8fb3-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8fb3-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8fb3-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8fb3-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8fb3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8fb3-141">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="f8fb3-141">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="f8fb3-142">IDelaydC:: conectar</span><span class="sxs-lookup"><span data-stu-id="f8fb3-142">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="f8fb3-143">IDelaydC:: retomar</span><span class="sxs-lookup"><span data-stu-id="f8fb3-143">IDelaydC::Resume</span></span>](idelaydc-resume.md)
</dt> <dt>

[<span data-ttu-id="f8fb3-144">IDelaydC:: iniciar</span><span class="sxs-lookup"><span data-stu-id="f8fb3-144">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="f8fb3-145">IDelaydC:: Stop</span><span class="sxs-lookup"><span data-stu-id="f8fb3-145">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




