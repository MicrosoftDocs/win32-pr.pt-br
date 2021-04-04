---
description: O método retomar reinicia uma captura pausada.
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
ms.openlocfilehash: ba0deef666c2e9829cb5a71d91e73da9c1b7d780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646789"
---
# <a name="idelaydcresume-method"></a><span data-ttu-id="dd1fa-103">Método IDelaydC:: resume</span><span class="sxs-lookup"><span data-stu-id="dd1fa-103">IDelaydC::Resume method</span></span>

<span data-ttu-id="dd1fa-104">O método **retomar** reinicia uma captura pausada.</span><span class="sxs-lookup"><span data-stu-id="dd1fa-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd1fa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dd1fa-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="dd1fa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dd1fa-106">Parameters</span></span>

<span data-ttu-id="dd1fa-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="dd1fa-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dd1fa-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dd1fa-108">Return value</span></span>

<span data-ttu-id="dd1fa-109">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="dd1fa-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="dd1fa-110">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="dd1fa-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="dd1fa-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="dd1fa-111">Return code</span></span>                                                                                                | <span data-ttu-id="dd1fa-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="dd1fa-112">Description</span></span>                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dd1fa-113"><dt>**captura de NMERR \_ \_ não \_ pausada**</dt></span><span class="sxs-lookup"><span data-stu-id="dd1fa-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="dd1fa-114">A captura não está em pausa.</span><span class="sxs-lookup"><span data-stu-id="dd1fa-114">The capture is not paused.</span></span> <span data-ttu-id="dd1fa-115">Chame [**IDelaydC::P ause**](idelaydc-pause.md) para pausar a captura.</span><span class="sxs-lookup"><span data-stu-id="dd1fa-115">Call [**IDelaydC::Pause**](idelaydc-pause.md) to pause the capture.</span></span><br/>                                |
| <dl> <span data-ttu-id="dd1fa-116"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="dd1fa-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="dd1fa-117">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="dd1fa-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="dd1fa-118">Chame [**IDelaydC:: Connect**](idelaydc-connect.md) para conectar o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="dd1fa-118">Call [**IDelaydC::Connect**](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="dd1fa-119"><dt>**NMERR \_ não \_ atrasada**</dt></span><span class="sxs-lookup"><span data-stu-id="dd1fa-119"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>         | <span data-ttu-id="dd1fa-120">O NPP está conectado à rede, mas não com o método [**IDelaydC:: Connect**](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="dd1fa-120">The NPP is connected to the network but not with the [**IDelaydC::Connect**](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="dd1fa-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd1fa-121">Remarks</span></span>

<span data-ttu-id="dd1fa-122">Enquanto a captura é pausada, novos dados não são adicionados ao [*arquivo de captura*](c.md) atual até que o método **IDelaydC:: resume** seja chamado para reiniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="dd1fa-122">While the capture is paused, new data is not added to the current [*capture file*](c.md) until the **IDelaydC::Resume** method is called to restart the capture.</span></span> <span data-ttu-id="dd1fa-123">Quando [**Pause**](idelaydc-pause.md) e **resume** são usados para parar e reiniciar a captura, todas as informações capturadas são colocadas no mesmo arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="dd1fa-123">When [**Pause**](idelaydc-pause.md) and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="dd1fa-124">Ao usar [**Pause**](idelaydc-pause.md) e **resume** para controlar a captura, monitor de rede continua a adicionar [*Estatísticas de conversa*](c.md) às estatísticas existentes para a captura atual.</span><span class="sxs-lookup"><span data-stu-id="dd1fa-124">When using [**Pause**](idelaydc-pause.md) and **Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="dd1fa-125">Para interromper a captura, chame [**IDelaydC:: Stop**](idelaydc-stop.md).</span><span class="sxs-lookup"><span data-stu-id="dd1fa-125">To stop the capture, call [**IDelaydC::Stop**](idelaydc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dd1fa-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd1fa-126">Requirements</span></span>



| <span data-ttu-id="dd1fa-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd1fa-127">Requirement</span></span> | <span data-ttu-id="dd1fa-128">Valor</span><span class="sxs-lookup"><span data-stu-id="dd1fa-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd1fa-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd1fa-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dd1fa-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dd1fa-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="dd1fa-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd1fa-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dd1fa-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dd1fa-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="dd1fa-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="dd1fa-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd1fa-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd1fa-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="dd1fa-135">DLL</span><span class="sxs-lookup"><span data-stu-id="dd1fa-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd1fa-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd1fa-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd1fa-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd1fa-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd1fa-138">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="dd1fa-138">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="dd1fa-139">**IDelaydC:: conectar**</span><span class="sxs-lookup"><span data-stu-id="dd1fa-139">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="dd1fa-140">**IDelaydC::P ause**</span><span class="sxs-lookup"><span data-stu-id="dd1fa-140">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="dd1fa-141">**IDelaydC:: Stop**</span><span class="sxs-lookup"><span data-stu-id="dd1fa-141">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




