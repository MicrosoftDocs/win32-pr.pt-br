---
description: 'Método IDelaydC:: resume-o método retomar reinicia uma captura pausada.'
ms.assetid: 4fa47220-d323-407b-9dae-704969f66bdd
title: 'Método IDelaydC:: resume (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 9c8c3b505e0e9fb306a444111cce22c8c580d015
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109184"
---
# <a name="idelaydcresume-method"></a><span data-ttu-id="aa40c-103">Método IDelaydC:: resume</span><span class="sxs-lookup"><span data-stu-id="aa40c-103">IDelaydC::Resume method</span></span>

<span data-ttu-id="aa40c-104">O método **retomar** reinicia uma captura pausada.</span><span class="sxs-lookup"><span data-stu-id="aa40c-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa40c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa40c-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="aa40c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa40c-106">Parameters</span></span>

<span data-ttu-id="aa40c-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="aa40c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aa40c-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="aa40c-108">Return value</span></span>

<span data-ttu-id="aa40c-109">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="aa40c-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="aa40c-110">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="aa40c-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="aa40c-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="aa40c-111">Return code</span></span>                                                                                                | <span data-ttu-id="aa40c-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="aa40c-112">Description</span></span>                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aa40c-113"><dt>**captura de NMERR \_ \_ não \_ pausada**</dt></span><span class="sxs-lookup"><span data-stu-id="aa40c-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="aa40c-114">A captura não está em pausa.</span><span class="sxs-lookup"><span data-stu-id="aa40c-114">The capture is not paused.</span></span> <span data-ttu-id="aa40c-115">Chame [**IDelaydC::P ause**](idelaydc-pause.md) para pausar a captura.</span><span class="sxs-lookup"><span data-stu-id="aa40c-115">Call [**IDelaydC::Pause**](idelaydc-pause.md) to pause the capture.</span></span><br/>                                |
| <dl> <span data-ttu-id="aa40c-116"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="aa40c-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="aa40c-117">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="aa40c-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="aa40c-118">Chame [**IDelaydC:: Connect**](idelaydc-connect.md) para conectar o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="aa40c-118">Call [**IDelaydC::Connect**](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="aa40c-119"><dt>**NMERR \_ não \_ atrasada**</dt></span><span class="sxs-lookup"><span data-stu-id="aa40c-119"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>         | <span data-ttu-id="aa40c-120">O NPP está conectado à rede, mas não com o método [**IDelaydC:: Connect**](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="aa40c-120">The NPP is connected to the network but not with the [**IDelaydC::Connect**](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="aa40c-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa40c-121">Remarks</span></span>

<span data-ttu-id="aa40c-122">Enquanto a captura é pausada, novos dados não são adicionados ao [*arquivo de captura*](c.md) atual até que o método **IDelaydC:: resume** seja chamado para reiniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="aa40c-122">While the capture is paused, new data is not added to the current [*capture file*](c.md) until the **IDelaydC::Resume** method is called to restart the capture.</span></span> <span data-ttu-id="aa40c-123">Quando [**Pause**](idelaydc-pause.md) e **resume** são usados para parar e reiniciar a captura, todas as informações capturadas são colocadas no mesmo arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="aa40c-123">When [**Pause**](idelaydc-pause.md) and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="aa40c-124">Ao usar [**Pause**](idelaydc-pause.md) e **resume** para controlar a captura, monitor de rede continua a adicionar [*Estatísticas de conversa*](c.md) às estatísticas existentes para a captura atual.</span><span class="sxs-lookup"><span data-stu-id="aa40c-124">When using [**Pause**](idelaydc-pause.md) and **Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="aa40c-125">Para interromper a captura, chame [**IDelaydC:: Stop**](idelaydc-stop.md).</span><span class="sxs-lookup"><span data-stu-id="aa40c-125">To stop the capture, call [**IDelaydC::Stop**](idelaydc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa40c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa40c-126">Requirements</span></span>



| <span data-ttu-id="aa40c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa40c-127">Requirement</span></span> | <span data-ttu-id="aa40c-128">Valor</span><span class="sxs-lookup"><span data-stu-id="aa40c-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa40c-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa40c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="aa40c-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="aa40c-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="aa40c-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa40c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="aa40c-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="aa40c-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="aa40c-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="aa40c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa40c-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa40c-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="aa40c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="aa40c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa40c-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa40c-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa40c-137">Consulte também</span><span class="sxs-lookup"><span data-stu-id="aa40c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa40c-138">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="aa40c-138">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="aa40c-139">**IDelaydC:: conectar**</span><span class="sxs-lookup"><span data-stu-id="aa40c-139">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="aa40c-140">**IDelaydC::P ause**</span><span class="sxs-lookup"><span data-stu-id="aa40c-140">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="aa40c-141">**IDelaydC:: Stop**</span><span class="sxs-lookup"><span data-stu-id="aa40c-141">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




