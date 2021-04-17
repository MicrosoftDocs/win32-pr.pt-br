---
description: O método GetTotalStatistics recupera o total de estatísticas para a captura atual.
ms.assetid: 494634f6-a9b3-4a50-8920-2387be9ba30f
title: 'Método IStats:: GetTotalStatistics (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 51cdbfdcc796aa7d8091e8da5837809efaa63379
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770143"
---
# <a name="istatsgettotalstatistics-method"></a><span data-ttu-id="e42fb-103">Método IStats:: GetTotalStatistics</span><span class="sxs-lookup"><span data-stu-id="e42fb-103">IStats::GetTotalStatistics method</span></span>

<span data-ttu-id="e42fb-104">O método **GetTotalStatistics** recupera o [*total de estatísticas*](t.md) para a [*captura*](c.md)atual.</span><span class="sxs-lookup"><span data-stu-id="e42fb-104">The **GetTotalStatistics** method retrieves the [*total statistics*](t.md) for the current [*capture*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e42fb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e42fb-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="e42fb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e42fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e42fb-107">*lpStats* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e42fb-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e42fb-108">Ponteiro para uma estrutura de [estatísticas](statistics.md)que fornece o total de estatísticas para a captura.</span><span class="sxs-lookup"><span data-stu-id="e42fb-108">Pointer to a [STATISTICS](statistics.md)structure that provides the total statistics for the capture.</span></span> <span data-ttu-id="e42fb-109">É responsabilidade do chamador alocar e liberar a memória usada pela estrutura de **estatísticas** .</span><span class="sxs-lookup"><span data-stu-id="e42fb-109">It is the caller's responsibility to allocate and free the memory used by the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="e42fb-110">*fClearAfterReading* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e42fb-110">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e42fb-111">Sinalizador usado para informar Monitor de Rede como lidar com o armazenamento interno do total de estatísticas.</span><span class="sxs-lookup"><span data-stu-id="e42fb-111">Flag used to tell Network Monitor how to handle the internal storage of the total statistics.</span></span> <span data-ttu-id="e42fb-112">Uma configuração de TRUE informa Monitor de Rede para limpar o armazenamento interno do total de estatísticas depois que as informações atuais são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="e42fb-112">A setting of TRUE tells Network Monitor to clear out the internal storage of the total statistics after the current information is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e42fb-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e42fb-113">Return value</span></span>

<span data-ttu-id="e42fb-114">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="e42fb-114">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="e42fb-115">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="e42fb-115">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="e42fb-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e42fb-116">Return code</span></span>                                                                                            | <span data-ttu-id="e42fb-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="e42fb-117">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e42fb-118"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="e42fb-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="e42fb-119">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="e42fb-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="e42fb-120">Chame o método [IStats:: Connect](istats-connect.md) para conectar o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="e42fb-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="e42fb-121"><dt>**NMERR \_ \_ somente não estatísticas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e42fb-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="e42fb-122">O NPP está conectado à rede, mas não com o método [IStats:: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="e42fb-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |
| <dl> <span data-ttu-id="e42fb-123"><dt>**NMERR \_ não \_ capturando**</dt></span><span class="sxs-lookup"><span data-stu-id="e42fb-123"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>   | <span data-ttu-id="e42fb-124">O NPP não está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="e42fb-124">The NPP is not capturing data.</span></span> <span data-ttu-id="e42fb-125">Chame o método [IStats:: Start](istats-start.md) para iniciar a captura de dados.</span><span class="sxs-lookup"><span data-stu-id="e42fb-125">Call the [IStats::Start](istats-start.md) method to start capturing data.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="e42fb-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="e42fb-126">Remarks</span></span>

<span data-ttu-id="e42fb-127">Esse método retorna dados somente enquanto uma captura está em andamento, incluindo enquanto a captura é pausada.</span><span class="sxs-lookup"><span data-stu-id="e42fb-127">This method returns data only while a capture is in progress, including while the capture is paused.</span></span>

<span data-ttu-id="e42fb-128">Monitor de Rede também armazena [*Estatísticas de conversa*](c.md), que podem ser recuperadas chamando o método [IStats:: GetConversationStatistics](istats-getconversationstatistics.md) .</span><span class="sxs-lookup"><span data-stu-id="e42fb-128">Network Monitor also stores [*conversation statistics*](c.md), which can be retrieved by calling the [IStats::GetConversationStatistics](istats-getconversationstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e42fb-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e42fb-129">Requirements</span></span>



| <span data-ttu-id="e42fb-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e42fb-130">Requirement</span></span> | <span data-ttu-id="e42fb-131">Valor</span><span class="sxs-lookup"><span data-stu-id="e42fb-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e42fb-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e42fb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e42fb-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e42fb-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="e42fb-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e42fb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e42fb-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e42fb-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="e42fb-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e42fb-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e42fb-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e42fb-137"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="e42fb-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e42fb-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e42fb-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e42fb-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e42fb-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="e42fb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e42fb-141">IStats</span><span class="sxs-lookup"><span data-stu-id="e42fb-141">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="e42fb-142">IStats:: conectar</span><span class="sxs-lookup"><span data-stu-id="e42fb-142">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="e42fb-143">IStats::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="e42fb-143">IStats::GetConversationStatistics</span></span>](istats-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="e42fb-144">IStats:: Iniciar,</span><span class="sxs-lookup"><span data-stu-id="e42fb-144">IStats::Start,</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="e42fb-145">ESTATÍSTICA</span><span class="sxs-lookup"><span data-stu-id="e42fb-145">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




