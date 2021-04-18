---
description: O método pause interrompe temporariamente a captura atual.
ms.assetid: 43176e9e-1502-484c-a8af-4e7bbf5f6474
title: 'IStats: método ause de:P (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d9e9f04ce3d25399866c711dad7a853f2c43c2ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759188"
---
# <a name="istatspause-method"></a><span data-ttu-id="7d895-103">IStats: método ause de:P</span><span class="sxs-lookup"><span data-stu-id="7d895-103">IStats::Pause method</span></span>

<span data-ttu-id="7d895-104">O método **Pause** interrompe temporariamente a captura atual.</span><span class="sxs-lookup"><span data-stu-id="7d895-104">The **Pause** method temporarily stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d895-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7d895-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a><span data-ttu-id="7d895-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7d895-106">Parameters</span></span>

<span data-ttu-id="7d895-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7d895-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7d895-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7d895-108">Return value</span></span>

<span data-ttu-id="7d895-109">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="7d895-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="7d895-110">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="7d895-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="7d895-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7d895-111">Return code</span></span>                                                                                            | <span data-ttu-id="7d895-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d895-112">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7d895-113"><dt>**captura de NMERR \_ \_ pausada**</dt></span><span class="sxs-lookup"><span data-stu-id="7d895-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl>  | <span data-ttu-id="7d895-114">A captura já está em pausa.</span><span class="sxs-lookup"><span data-stu-id="7d895-114">The capture is already paused.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="7d895-115"><dt>**NMERR \_ não \_ capturando**</dt></span><span class="sxs-lookup"><span data-stu-id="7d895-115"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>   | <span data-ttu-id="7d895-116">O NPP não está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="7d895-116">The NPP is not capturing data.</span></span> <span data-ttu-id="7d895-117">Chame o método [IStats:: Start](istats-start.md) para iniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="7d895-117">Call the [IStats::Start](istats-start.md) method to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="7d895-118"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="7d895-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="7d895-119">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="7d895-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="7d895-120">Chame o método [IStats:: Connect](istats-connect.md) para conectar o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="7d895-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="7d895-121"><dt>**NMERR \_ \_ somente não estatísticas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7d895-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="7d895-122">O NPP está conectado à rede, mas não com o método [IStats:: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="7d895-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="7d895-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d895-123">Remarks</span></span>

<span data-ttu-id="7d895-124">Enquanto a captura é pausada, novos quadros não são capturados até que uma chamada para o método [IStats:: resume](istats-resume.md) reinicie a captura.</span><span class="sxs-lookup"><span data-stu-id="7d895-124">While the capture is paused, new frames are not captured until a call to the [IStats::Resume](istats-resume.md) method restarts the capture.</span></span>

<span data-ttu-id="7d895-125">Quando você usa os métodos **IStats::P ause** e **IStats:: resume** para controlar a captura, monitor de rede continua a adicionar [*Estatísticas de conversa*](c.md) sempre que a captura está em execução.</span><span class="sxs-lookup"><span data-stu-id="7d895-125">When you use the **IStats::Pause** and **IStats::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="7d895-126">Para reiniciar a chamada de captura [IStats:: resume](istats-resume.md).</span><span class="sxs-lookup"><span data-stu-id="7d895-126">To restart the capture call [IStats::Resume](istats-resume.md).</span></span> <span data-ttu-id="7d895-127">Para interromper a captura, chame [IStats:: Stop](istats-stop.md).</span><span class="sxs-lookup"><span data-stu-id="7d895-127">To stop the capture, call [IStats::Stop](istats-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d895-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d895-128">Requirements</span></span>



| <span data-ttu-id="7d895-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d895-129">Requirement</span></span> | <span data-ttu-id="7d895-130">Valor</span><span class="sxs-lookup"><span data-stu-id="7d895-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d895-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d895-131">Minimum supported client</span></span><br/> | <span data-ttu-id="7d895-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7d895-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="7d895-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d895-133">Minimum supported server</span></span><br/> | <span data-ttu-id="7d895-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7d895-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="7d895-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7d895-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d895-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d895-136"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="7d895-137">DLL</span><span class="sxs-lookup"><span data-stu-id="7d895-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d895-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d895-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d895-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d895-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d895-140">IStats</span><span class="sxs-lookup"><span data-stu-id="7d895-140">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="7d895-141">IStats:: conectar</span><span class="sxs-lookup"><span data-stu-id="7d895-141">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="7d895-142">IStats:: retomar</span><span class="sxs-lookup"><span data-stu-id="7d895-142">IStats::Resume</span></span>](istats-resume.md)
</dt> <dt>

[<span data-ttu-id="7d895-143">IStats:: iniciar</span><span class="sxs-lookup"><span data-stu-id="7d895-143">IStats::Start</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="7d895-144">IStats:: Stop</span><span class="sxs-lookup"><span data-stu-id="7d895-144">IStats::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




