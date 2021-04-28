---
description: IDelaydC::P método ause-o método pause pausa a captura atual.
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
ms.openlocfilehash: 21b4cd7b6cb921f7bd71b8670a37da12b2239b92
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098494"
---
# <a name="idelaydcpause-method"></a><span data-ttu-id="bd760-103">IDelaydC: método ause de:P</span><span class="sxs-lookup"><span data-stu-id="bd760-103">IDelaydC::Pause method</span></span>

<span data-ttu-id="bd760-104">O método **Pause** pausa a captura atual.</span><span class="sxs-lookup"><span data-stu-id="bd760-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd760-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bd760-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a><span data-ttu-id="bd760-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bd760-106">Parameters</span></span>

<span data-ttu-id="bd760-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="bd760-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bd760-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="bd760-108">Return value</span></span>

<span data-ttu-id="bd760-109">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="bd760-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="bd760-110">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="bd760-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="bd760-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="bd760-111">Return code</span></span>                                                                                           | <span data-ttu-id="bd760-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="bd760-112">Description</span></span>                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bd760-113"><dt>**captura de NMERR \_ \_ pausada**</dt></span><span class="sxs-lookup"><span data-stu-id="bd760-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="bd760-114">A captura já está em um estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="bd760-114">The capture is already in a paused state.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="bd760-115"><dt>**NMERR \_ não \_ capturando**</dt></span><span class="sxs-lookup"><span data-stu-id="bd760-115"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="bd760-116">O NPP não está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="bd760-116">The NPP is not capturing data.</span></span> <span data-ttu-id="bd760-117">Chame [IDelaydC:: Start](idelaydc-start.md) para iniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="bd760-117">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="bd760-118"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="bd760-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="bd760-119">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="bd760-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="bd760-120">Chame [IDelaydC:: Connect](idelaydc-connect.md) para conectar o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="bd760-120">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="bd760-121"><dt>**NMERR \_ não \_ atrasada**</dt></span><span class="sxs-lookup"><span data-stu-id="bd760-121"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>    | <span data-ttu-id="bd760-122">O NPP está conectado à rede, mas não com o método [IDelaydC:: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="bd760-122">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="bd760-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd760-123">Remarks</span></span>

<span data-ttu-id="bd760-124">Enquanto a captura está em um estado de pausa, novos dados não são adicionados ao arquivo de [*captura*](c.md) atual até que o método **IDelaydC:: resume** seja chamado para reiniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="bd760-124">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until the **IDelaydC::Resume** method is called to restart the capture.</span></span> <span data-ttu-id="bd760-125">Quando **Pause** e **resume** são usados para parar e reiniciar a captura, todas as informações capturadas são colocadas no mesmo arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="bd760-125">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="bd760-126">Ao usar **IDelaydC::P ause** e **IDelaydC:: retomar** para controlar a captura, monitor de rede continuará a adicionar [*Estatísticas de conversa*](c.md) sempre que a captura estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="bd760-126">When using **IDelaydC::Pause** and **IDelaydC::Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="bd760-127">Para reiniciar a captura, chame [IDelaydC:: resume](idelaydc-resume.md).</span><span class="sxs-lookup"><span data-stu-id="bd760-127">To restart the capture, call [IDelaydC::Resume](idelaydc-resume.md).</span></span>

<span data-ttu-id="bd760-128">Para interromper a captura, chame [IDelaydC:: Stop](idelaydc-stop.md).</span><span class="sxs-lookup"><span data-stu-id="bd760-128">To stop the capture, call [IDelaydC::Stop](idelaydc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd760-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd760-129">Requirements</span></span>



| <span data-ttu-id="bd760-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd760-130">Requirement</span></span> | <span data-ttu-id="bd760-131">Valor</span><span class="sxs-lookup"><span data-stu-id="bd760-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd760-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd760-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bd760-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bd760-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="bd760-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd760-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bd760-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bd760-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="bd760-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bd760-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd760-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd760-137"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="bd760-138">DLL</span><span class="sxs-lookup"><span data-stu-id="bd760-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd760-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd760-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd760-140">Consulte também</span><span class="sxs-lookup"><span data-stu-id="bd760-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd760-141">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="bd760-141">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="bd760-142">IDelaydC:: conectar</span><span class="sxs-lookup"><span data-stu-id="bd760-142">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="bd760-143">IDelaydC:: retomar</span><span class="sxs-lookup"><span data-stu-id="bd760-143">IDelaydC::Resume</span></span>](idelaydc-resume.md)
</dt> <dt>

[<span data-ttu-id="bd760-144">IDelaydC:: iniciar</span><span class="sxs-lookup"><span data-stu-id="bd760-144">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="bd760-145">IDelaydC:: Stop</span><span class="sxs-lookup"><span data-stu-id="bd760-145">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




