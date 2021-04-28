---
description: 'Método IDelaydC:: Start – o método Start inicia uma captura.'
ms.assetid: 92b25afc-d5d8-47e4-a155-4ed2a3571038
title: 'Método IDelaydC:: Start (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 25bf778d9cccce20c736c5f8b83e6af9754ac933
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118434"
---
# <a name="idelaydcstart-method"></a><span data-ttu-id="7dcb4-103">Método IDelaydC:: Start</span><span class="sxs-lookup"><span data-stu-id="7dcb4-103">IDelaydC::Start method</span></span>

<span data-ttu-id="7dcb4-104">O método **Start** inicia uma captura.</span><span class="sxs-lookup"><span data-stu-id="7dcb4-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dcb4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7dcb4-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="7dcb4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7dcb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dcb4-107">*pFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7dcb4-107">*pFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7dcb4-108">Ponteiro para o nome do [*arquivo de captura*](c.md) usado para armazenar os dados da rede.</span><span class="sxs-lookup"><span data-stu-id="7dcb4-108">Pointer to the name of the [*capture file*](c.md) used to store the network data.</span></span> <span data-ttu-id="7dcb4-109">Certifique-se de armazenar esse nome de arquivo em cache se for necessário para referência futura.</span><span class="sxs-lookup"><span data-stu-id="7dcb4-109">Be sure to cache this file name if it is needed for future reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dcb4-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7dcb4-110">Return value</span></span>

<span data-ttu-id="7dcb4-111">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="7dcb4-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="7dcb4-112">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="7dcb4-112">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="7dcb4-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7dcb4-113">Return code</span></span>                                                                                           | <span data-ttu-id="7dcb4-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="7dcb4-114">Description</span></span>                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7dcb4-115"><dt>**captura de NMERR \_ \_ pausada**</dt></span><span class="sxs-lookup"><span data-stu-id="7dcb4-115"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="7dcb4-116">A captura está em um estado de pausa e deve ser interrompida para que possa ser reiniciada.</span><span class="sxs-lookup"><span data-stu-id="7dcb4-116">The capture is in a paused state and must be stopped before it can be restarted.</span></span> <span data-ttu-id="7dcb4-117">Chame [**IDelaydC:: Stop**](idelaydc-stop.md) para interromper a captura.</span><span class="sxs-lookup"><span data-stu-id="7dcb4-117">Call [**IDelaydC::Stop**](idelaydc-stop.md) to stop the capture.</span></span> <span data-ttu-id="7dcb4-118">Para obter mais informações, consulte a seção comentários neste tópico.</span><span class="sxs-lookup"><span data-stu-id="7dcb4-118">For more information, see the Remarks section in this topic.</span></span><br/> |
| <dl> <span data-ttu-id="7dcb4-119"><dt>**captura de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7dcb4-119"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>       | <span data-ttu-id="7dcb4-120">A captura já foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="7dcb4-120">The capture is already started.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="7dcb4-121"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="7dcb4-121"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="7dcb4-122">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="7dcb4-122">The NPP is not connected to the network.</span></span> <span data-ttu-id="7dcb4-123">Chame [**IDelaydC:: Connect**](idelaydc-connect.md) para conectar-se à rede.</span><span class="sxs-lookup"><span data-stu-id="7dcb4-123">Call [**IDelaydC::Connect**](idelaydc-connect.md) to connect to the network.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="7dcb4-124"><dt>**NMERR \_ não \_ atrasada**</dt></span><span class="sxs-lookup"><span data-stu-id="7dcb4-124"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>    | <span data-ttu-id="7dcb4-125">O NPP está conectado à rede, mas não com o método [**IDelaydC:: Connect**](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="7dcb4-125">The NPP is connected to the network but not with the [**IDelaydC::Connect**](idelaydc-connect.md) method.</span></span><br/>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="7dcb4-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="7dcb4-126">Remarks</span></span>

<span data-ttu-id="7dcb4-127">O local do [*arquivo de captura*](c.md) é especificado no registro do Windows, mas você pode usar monitor de rede para alterar o local do arquivo.</span><span class="sxs-lookup"><span data-stu-id="7dcb4-127">The location of the [*capture file*](c.md) is specified in your Windows registry, but you can use Network Monitor to change the file's location.</span></span>

<span data-ttu-id="7dcb4-128">Para reiniciar a captura usando **IDelaydC:: Start** e [**IDelaydC:: Stop**](idelaydc-stop.md), você deve chamar o método [**IDelaydC:: Configure**](idelaydc-configure.md) para reconfigurar a conexão cada vez que você chamar o método **IDelaydC:: Start** para reiniciar a captura de dados.</span><span class="sxs-lookup"><span data-stu-id="7dcb4-128">To restart the capture by using **IDelaydC::Start** and [**IDelaydC::Stop**](idelaydc-stop.md), you must call the [**IDelaydC::Configure**](idelaydc-configure.md) method to reconfigure the connection each time you call the **IDelaydC::Start** method to restart capturing data.</span></span> <span data-ttu-id="7dcb4-129">Quando você inicia e interrompe a captura com esses três métodos, um novo arquivo de captura é criado toda vez que a captura é iniciada.</span><span class="sxs-lookup"><span data-stu-id="7dcb4-129">When you start and stop the capture with these three methods, a new capture file is created each time the capture is started.</span></span>

> [!Note]  
> <span data-ttu-id="7dcb4-130">Você também pode iniciar e parar a captura usando os métodos [**IDelaydC::P ause**](idelaydc-pause.md) e [**IDelaydC:: resume**](idelaydc-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="7dcb4-130">You can also start and stop the capture by using the [**IDelaydC::Pause**](idelaydc-pause.md) and [**IDelaydC::Resume**](idelaydc-resume.md) methods.</span></span> <span data-ttu-id="7dcb4-131">Quando você usa esses dois métodos, os dados capturados são armazenados no mesmo arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="7dcb4-131">When you use these two methods, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7dcb4-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7dcb4-132">Requirements</span></span>



| <span data-ttu-id="7dcb4-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="7dcb4-133">Requirement</span></span> | <span data-ttu-id="7dcb4-134">Valor</span><span class="sxs-lookup"><span data-stu-id="7dcb4-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dcb4-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7dcb4-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7dcb4-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7dcb4-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="7dcb4-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7dcb4-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7dcb4-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7dcb4-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="7dcb4-139">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7dcb4-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dcb4-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dcb4-140"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="7dcb4-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7dcb4-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7dcb4-142"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7dcb4-142"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dcb4-143">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7dcb4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dcb4-144">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="7dcb4-144">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="7dcb4-145">**IDelaydC:: configurar**</span><span class="sxs-lookup"><span data-stu-id="7dcb4-145">**IDelaydC::Configure**</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="7dcb4-146">**IDelaydC:: conectar**</span><span class="sxs-lookup"><span data-stu-id="7dcb4-146">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="7dcb4-147">**IDelaydC::P ause**</span><span class="sxs-lookup"><span data-stu-id="7dcb4-147">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="7dcb4-148">**IDelaydC:: retomar**</span><span class="sxs-lookup"><span data-stu-id="7dcb4-148">**IDelaydC::Resume**</span></span>](idelaydc-resume.md)
</dt> <dt>

[<span data-ttu-id="7dcb4-149">**IDelaydC:: Stop**</span><span class="sxs-lookup"><span data-stu-id="7dcb4-149">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




