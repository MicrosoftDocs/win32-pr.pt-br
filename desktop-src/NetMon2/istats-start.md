---
description: 'Método IStats:: Start – o método Start inicia uma captura.'
ms.assetid: d4086e30-e5ed-4f29-90f0-d65125d9af6d
title: 'Método IStats:: Start (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 64f02529ba10d98092eb30a1bcc350d5c72049fc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094544"
---
# <a name="istatsstart-method"></a><span data-ttu-id="22077-103">Método IStats:: Start</span><span class="sxs-lookup"><span data-stu-id="22077-103">IStats::Start method</span></span>

<span data-ttu-id="22077-104">O método **Start** inicia uma captura.</span><span class="sxs-lookup"><span data-stu-id="22077-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="22077-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="22077-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a><span data-ttu-id="22077-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="22077-106">Parameters</span></span>

<span data-ttu-id="22077-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="22077-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="22077-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="22077-108">Return value</span></span>

<span data-ttu-id="22077-109">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="22077-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="22077-110">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="22077-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="22077-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="22077-111">Return code</span></span>                                                                                            | <span data-ttu-id="22077-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="22077-112">Description</span></span>                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="22077-113"><dt>**captura de NMERR \_ \_ pausada**</dt></span><span class="sxs-lookup"><span data-stu-id="22077-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl>  | <span data-ttu-id="22077-114">A captura foi pausada e deve ser interrompida para que possa ser reiniciada.</span><span class="sxs-lookup"><span data-stu-id="22077-114">The capture has paused and must be stopped before it can be restarted.</span></span> <span data-ttu-id="22077-115">Chame o método [IStats:: Stop](istats-stop.md) para interromper a captura.</span><span class="sxs-lookup"><span data-stu-id="22077-115">Call the [IStats::Stop](istats-stop.md) method to stop the capture.</span></span><br/> |
| <dl> <span data-ttu-id="22077-116"><dt>**captura de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="22077-116"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>        | <span data-ttu-id="22077-117">A captura já foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="22077-117">The capture has already started.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="22077-118"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="22077-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="22077-119">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="22077-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="22077-120">Chame o método [IStats:: Connect](istats-connect.md) para conectar o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="22077-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/>           |
| <dl> <span data-ttu-id="22077-121"><dt>**NMERR \_ \_ somente não estatísticas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="22077-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="22077-122">O NPP está conectado à rede, mas não com o método [IStats:: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="22077-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="22077-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="22077-123">Remarks</span></span>

<span data-ttu-id="22077-124">Ao reiniciar a captura usando os métodos IStats:: Start e [IStats:: Stop](istats-stop.md) , você deve chamar o método [IStats:: Configure](istats-configure.md) para reconfigurar a conexão cada vez que chamar IStats:: Start para reiniciar a captura de dados.</span><span class="sxs-lookup"><span data-stu-id="22077-124">When restarting the capture by using the IStats::Start and [IStats::Stop](istats-stop.md) methods, you must call the [IStats::Configure](istats-configure.md) method to reconfigure the connection each time you call IStats::Start to restart the data capture.</span></span>

> [!Note]  
> <span data-ttu-id="22077-125">Você também pode iniciar e parar a captura usando os métodos [IStats::P ause](istats-pause.md) e [IStats:: resume](istats-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="22077-125">You can also start and stop the capture by using the [IStats::Pause](istats-pause.md) and [IStats::Resume](istats-resume.md) methods.</span></span> <span data-ttu-id="22077-126">Quando você usa esses métodos, os dados capturados são armazenados no mesmo arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="22077-126">When you use these methods, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="22077-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22077-127">Requirements</span></span>



| <span data-ttu-id="22077-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="22077-128">Requirement</span></span> | <span data-ttu-id="22077-129">Valor</span><span class="sxs-lookup"><span data-stu-id="22077-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22077-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22077-130">Minimum supported client</span></span><br/> | <span data-ttu-id="22077-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="22077-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="22077-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22077-132">Minimum supported server</span></span><br/> | <span data-ttu-id="22077-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="22077-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="22077-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="22077-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="22077-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="22077-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="22077-136">DLL</span><span class="sxs-lookup"><span data-stu-id="22077-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22077-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22077-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22077-138">Consulte também</span><span class="sxs-lookup"><span data-stu-id="22077-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22077-139">IStats</span><span class="sxs-lookup"><span data-stu-id="22077-139">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="22077-140">IStats:: configurar</span><span class="sxs-lookup"><span data-stu-id="22077-140">IStats::Configure</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="22077-141">IStats:: conectar</span><span class="sxs-lookup"><span data-stu-id="22077-141">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="22077-142">IStats::P ause</span><span class="sxs-lookup"><span data-stu-id="22077-142">IStats::Pause</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="22077-143">IStats:: retomar</span><span class="sxs-lookup"><span data-stu-id="22077-143">IStats::Resume</span></span>](istats-resume.md)
</dt> <dt>

[<span data-ttu-id="22077-144">IStats:: Stop</span><span class="sxs-lookup"><span data-stu-id="22077-144">IStats::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




