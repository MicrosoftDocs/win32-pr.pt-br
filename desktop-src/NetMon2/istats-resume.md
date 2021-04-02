---
description: O método retomar reinicia uma captura pausada.
ms.assetid: 128e38c4-7459-4376-a3d7-2c6944fcf535
title: 'Método IStats:: resume (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: db84f51d2a2a2c2d15e3b4164fe1fac09e72bf20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829340"
---
# <a name="istatsresume-method"></a><span data-ttu-id="06989-103">Método IStats:: resume</span><span class="sxs-lookup"><span data-stu-id="06989-103">IStats::Resume method</span></span>

<span data-ttu-id="06989-104">O método **retomar** reinicia uma captura pausada.</span><span class="sxs-lookup"><span data-stu-id="06989-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="06989-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06989-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="06989-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06989-106">Parameters</span></span>

<span data-ttu-id="06989-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="06989-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="06989-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="06989-108">Return value</span></span>

<span data-ttu-id="06989-109">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="06989-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="06989-110">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="06989-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="06989-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="06989-111">Return code</span></span>                                                                                                | <span data-ttu-id="06989-112">Description</span><span class="sxs-lookup"><span data-stu-id="06989-112">Description</span></span>                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="06989-113"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="06989-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="06989-114">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="06989-114">The NPP is not connected to the network.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="06989-115"><dt>**captura de NMERR \_ \_ não \_ pausada**</dt></span><span class="sxs-lookup"><span data-stu-id="06989-115"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="06989-116">A captura não está em pausa.</span><span class="sxs-lookup"><span data-stu-id="06989-116">The capture is not paused.</span></span> <span data-ttu-id="06989-117">Chame o método [IStats::P ause](istats-pause.md) para interromper temporariamente a captura.</span><span class="sxs-lookup"><span data-stu-id="06989-117">Call the [IStats::Pause](istats-pause.md) method to temporarily stop the capture.</span></span><br/>                     |
| <dl> <span data-ttu-id="06989-118"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="06989-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="06989-119">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="06989-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="06989-120">Chame o método [IStats:: Connect](istats-connect.md) para conectar o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="06989-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="06989-121"><dt>**NMERR \_ \_ somente não estatísticas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="06989-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl>     | <span data-ttu-id="06989-122">O NPP está conectado à rede, mas não com o método [IStats:: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="06989-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="06989-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="06989-123">Remarks</span></span>

<span data-ttu-id="06989-124">Enquanto a captura está em um estado de pausa, novos dados não são capturados até que o método IStats:: resume seja chamado para reiniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="06989-124">While the capture is in a paused state, new data is not captured until the IStats::Resume method is called to restart the capture.</span></span>

<span data-ttu-id="06989-125">Ao usar os métodos **Pause** e **resume** para controlar a captura, monitor de rede continua a adicionar [*Estatísticas de conversa*](c.md) às estatísticas existentes para a captura atual.</span><span class="sxs-lookup"><span data-stu-id="06989-125">When using the **Pause** and **Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="06989-126">Para interromper a captura, chame [IStats:: Stop](istats-stop.md).</span><span class="sxs-lookup"><span data-stu-id="06989-126">To stop the capture, call [IStats::Stop](istats-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="06989-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06989-127">Requirements</span></span>



| <span data-ttu-id="06989-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="06989-128">Requirement</span></span> | <span data-ttu-id="06989-129">Valor</span><span class="sxs-lookup"><span data-stu-id="06989-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06989-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06989-130">Minimum supported client</span></span><br/> | <span data-ttu-id="06989-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="06989-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="06989-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06989-132">Minimum supported server</span></span><br/> | <span data-ttu-id="06989-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="06989-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="06989-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="06989-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="06989-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="06989-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="06989-136">DLL</span><span class="sxs-lookup"><span data-stu-id="06989-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06989-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06989-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06989-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="06989-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06989-139">IStats</span><span class="sxs-lookup"><span data-stu-id="06989-139">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="06989-140">IStats:: conectar</span><span class="sxs-lookup"><span data-stu-id="06989-140">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="06989-141">IStats::P ause</span><span class="sxs-lookup"><span data-stu-id="06989-141">IStats::Pause</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="06989-142">IStats:: Stop</span><span class="sxs-lookup"><span data-stu-id="06989-142">IStats::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




