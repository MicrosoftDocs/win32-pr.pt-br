---
description: O método Start inicia uma captura.
ms.assetid: 8bf8c0c7-20be-4404-8ea5-b28b4c658523
title: 'Método IESP:: Start (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 2d9fc3a75fc82964f6fc5a5660ef77414ae065d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811078"
---
# <a name="iespstart-method"></a><span data-ttu-id="5d53f-103">Método IESP:: Start</span><span class="sxs-lookup"><span data-stu-id="5d53f-103">IESP::Start method</span></span>

<span data-ttu-id="5d53f-104">O método **Start** inicia uma captura.</span><span class="sxs-lookup"><span data-stu-id="5d53f-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d53f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d53f-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="5d53f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d53f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d53f-107">*pFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5d53f-107">*pFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d53f-108">Ponteiro para o nome do [*arquivo de captura*](c.md) usado para armazenar os dados da rede.</span><span class="sxs-lookup"><span data-stu-id="5d53f-108">Pointer to the name of the [*capture file*](c.md) used to store the network data.</span></span> <span data-ttu-id="5d53f-109">Certifique-se de armazenar esse nome de arquivo em cache se for necessário para referência futura.</span><span class="sxs-lookup"><span data-stu-id="5d53f-109">Be sure to cache this file name if it is needed for future reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d53f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5d53f-110">Return value</span></span>

<span data-ttu-id="5d53f-111">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="5d53f-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="5d53f-112">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="5d53f-112">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="5d53f-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5d53f-113">Return code</span></span>                                                                                           | <span data-ttu-id="5d53f-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="5d53f-114">Description</span></span>                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5d53f-115"><dt>**captura de NMERR \_ \_ pausada**</dt></span><span class="sxs-lookup"><span data-stu-id="5d53f-115"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="5d53f-116">A captura está pausada e deve ser interrompida para que possa ser reiniciada.</span><span class="sxs-lookup"><span data-stu-id="5d53f-116">The capture is paused and must be stopped before it can be restarted.</span></span> <span data-ttu-id="5d53f-117">Chame [IESP:: Stop](iesp-stop.md) para interromper a captura.</span><span class="sxs-lookup"><span data-stu-id="5d53f-117">Call [IESP::Stop](iesp-stop.md) to stop the capture.</span></span><br/> |
| <dl> <span data-ttu-id="5d53f-118"><dt>**captura de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5d53f-118"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>       | <span data-ttu-id="5d53f-119">A captura já foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="5d53f-119">The capture is already started.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="5d53f-120"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="5d53f-120"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="5d53f-121">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="5d53f-121">The NPP is not connected to the network.</span></span> <span data-ttu-id="5d53f-122">Chame [IESP:: Connect](iesp-connect.md) para conectar o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="5d53f-122">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/>          |
| <dl> <span data-ttu-id="5d53f-123"><dt>**NMERR \_ não \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="5d53f-123"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>        | <span data-ttu-id="5d53f-124">O NPP está conectado à rede, mas não com o método [IESP:: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="5d53f-124">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="5d53f-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d53f-125">Remarks</span></span>

<span data-ttu-id="5d53f-126">O local do [*arquivo de captura*](c.md) é especificado no registro do Windows, mas você pode usar monitor de rede para alterar o local do diretório.</span><span class="sxs-lookup"><span data-stu-id="5d53f-126">The location of the [*capture file*](c.md) is specified in the Windows registry, but you can use Network Monitor to change the directory location.</span></span>

<span data-ttu-id="5d53f-127">Ao reiniciar a captura usando os métodos IESP:: Start e [IESP:: Stop](iesp-stop.md) , você deve chamar o método [IESP:: Configure](iesp-configure.md) para reconfigurar a conexão cada vez que chamar IESP:: Start para reiniciar a captura de dados.</span><span class="sxs-lookup"><span data-stu-id="5d53f-127">When you restart the capture by using the IESP::Start and [IESP::Stop](iesp-stop.md) methods, you must call the [IESP::Configure](iesp-configure.md) method to reconfigure the connection each time you call IESP::Start to restart capturing data.</span></span> <span data-ttu-id="5d53f-128">Quando você inicia e interrompe a captura com esses três métodos, um novo arquivo de captura é criado toda vez que a captura é iniciada.</span><span class="sxs-lookup"><span data-stu-id="5d53f-128">When you start and stop the capture with these three methods, a new capture file is created each time the capture is started.</span></span>

> [!Note]  
> <span data-ttu-id="5d53f-129">Você também pode iniciar e parar a captura usando os métodos [IESP::P ause](iesp-pause.md) e [IESP:: resume](iesp-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="5d53f-129">You can also start and stop the capture by using the [IESP::Pause](iesp-pause.md) and [IESP::Resume](iesp-resume.md) methods.</span></span> <span data-ttu-id="5d53f-130">Quando esses dois métodos são usados, os dados capturados são armazenados no mesmo arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="5d53f-130">When these two methods are used, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5d53f-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d53f-131">Requirements</span></span>



| <span data-ttu-id="5d53f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d53f-132">Requirement</span></span> | <span data-ttu-id="5d53f-133">Valor</span><span class="sxs-lookup"><span data-stu-id="5d53f-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d53f-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d53f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5d53f-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5d53f-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="5d53f-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d53f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5d53f-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5d53f-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="5d53f-138">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5d53f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d53f-139"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d53f-139"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="5d53f-140">DLL</span><span class="sxs-lookup"><span data-stu-id="5d53f-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d53f-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d53f-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d53f-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d53f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d53f-143">IESP</span><span class="sxs-lookup"><span data-stu-id="5d53f-143">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="5d53f-144">IESP:: configurar</span><span class="sxs-lookup"><span data-stu-id="5d53f-144">IESP::Configure</span></span>](iesp-configure.md)
</dt> <dt>

[<span data-ttu-id="5d53f-145">IESP:: conectar</span><span class="sxs-lookup"><span data-stu-id="5d53f-145">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="5d53f-146">IESP::P ause</span><span class="sxs-lookup"><span data-stu-id="5d53f-146">IESP::Pause</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="5d53f-147">IESP:: retomar</span><span class="sxs-lookup"><span data-stu-id="5d53f-147">IESP::Resume</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="5d53f-148">IESP:: Stop</span><span class="sxs-lookup"><span data-stu-id="5d53f-148">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




