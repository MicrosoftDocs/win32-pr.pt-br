---
description: 'Método IRTC:: GetTotalStatistics – o método GetTotalStatistics recupera o total de estatísticas para a captura atual.'
ms.assetid: e5098984-c69e-4cd5-9143-d85dfcbd7b92
title: 'Método IRTC:: GetTotalStatistics (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 8ed659efe388f4eb9c9ac8afd6aa2c74fd0af7d3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110684"
---
# <a name="irtcgettotalstatistics-method"></a><span data-ttu-id="b57de-103">Método IRTC:: GetTotalStatistics</span><span class="sxs-lookup"><span data-stu-id="b57de-103">IRTC::GetTotalStatistics method</span></span>

<span data-ttu-id="b57de-104">O método **GetTotalStatistics** recupera o [*total de estatísticas*](t.md) para a [*captura*](c.md)atual.</span><span class="sxs-lookup"><span data-stu-id="b57de-104">The **GetTotalStatistics** method retrieves the [*total statistics*](t.md) for the current [*capture*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b57de-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b57de-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="b57de-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b57de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b57de-107">*lpStats* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b57de-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b57de-108">Ponteiro para uma estrutura de [estatísticas](statistics.md) que fornece o total de estatísticas para a captura.</span><span class="sxs-lookup"><span data-stu-id="b57de-108">Pointer to a [STATISTICS](statistics.md) structure that provides the total statistics for the capture.</span></span> <span data-ttu-id="b57de-109">É responsabilidade dos chamadores alocar e liberar a memória usada pela estrutura de **estatísticas** .</span><span class="sxs-lookup"><span data-stu-id="b57de-109">It is the callers responsibility to allocate and free the memory used by the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="b57de-110">*fClearAfterReading* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b57de-110">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b57de-111">Sinalizador usado para informar Monitor de Rede como lidar com o armazenamento interno do total de estatísticas.</span><span class="sxs-lookup"><span data-stu-id="b57de-111">Flag used to tell Network Monitor how to handle the internal storage of the total statistics.</span></span> <span data-ttu-id="b57de-112">Uma configuração de **true** informa monitor de rede para limpar o armazenamento interno do total de estatísticas depois que as informações atuais são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="b57de-112">A setting of **TRUE** tells Network Monitor to clear out the internal storage of the total statistics after the current information is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b57de-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b57de-113">Return value</span></span>

<span data-ttu-id="b57de-114">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="b57de-114">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="b57de-115">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="b57de-115">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="b57de-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b57de-116">Return code</span></span>                                                                                          | <span data-ttu-id="b57de-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="b57de-117">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b57de-118"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="b57de-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="b57de-119">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="b57de-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="b57de-120">Chame [IRTC:: Connect](irtc-connect.md) para conectar o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="b57de-120">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="b57de-121"><dt>**NMERR \_ não está em \_ tempo real**</dt></span><span class="sxs-lookup"><span data-stu-id="b57de-121"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="b57de-122">O NPP está conectado à rede, mas não com o método [IRTC:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="b57de-122">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |
| <dl> <span data-ttu-id="b57de-123"><dt>**NMERR \_ não \_ capturando**</dt></span><span class="sxs-lookup"><span data-stu-id="b57de-123"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="b57de-124">O NPP não está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="b57de-124">The NPP is not capturing data.</span></span> <span data-ttu-id="b57de-125">Chame [IRTC:: Start](irtc-start.md) para iniciar a captura de dados.</span><span class="sxs-lookup"><span data-stu-id="b57de-125">Call [IRTC::Start](irtc-start.md) to start capturing data.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="b57de-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="b57de-126">Remarks</span></span>

<span data-ttu-id="b57de-127">Esse método retorna dados somente enquanto uma captura está em andamento, incluindo enquanto a captura é pausada.</span><span class="sxs-lookup"><span data-stu-id="b57de-127">This method returns data only while a capture is in progress, including while the capture is paused.</span></span>

<span data-ttu-id="b57de-128">Monitor de Rede também armazena [*Estatísticas de conversa*](c.md).</span><span class="sxs-lookup"><span data-stu-id="b57de-128">Network Monitor also stores [*conversation statistics*](c.md).</span></span> <span data-ttu-id="b57de-129">Para recuperar as estatísticas de conversa, chame o método [IRTC:: GetConversationStatistics](irtc-getconversationstatistics.md) .</span><span class="sxs-lookup"><span data-stu-id="b57de-129">To retrieve conversation statistics, call the [IRTC::GetConversationStatistics](irtc-getconversationstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b57de-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b57de-130">Requirements</span></span>



| <span data-ttu-id="b57de-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b57de-131">Requirement</span></span> | <span data-ttu-id="b57de-132">Valor</span><span class="sxs-lookup"><span data-stu-id="b57de-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b57de-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b57de-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b57de-134">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b57de-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="b57de-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b57de-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b57de-136">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b57de-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="b57de-137">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b57de-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="b57de-138"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b57de-138"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="b57de-139">DLL</span><span class="sxs-lookup"><span data-stu-id="b57de-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b57de-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b57de-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b57de-141">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b57de-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b57de-142">IRTC</span><span class="sxs-lookup"><span data-stu-id="b57de-142">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="b57de-143">IRTC:: conectar</span><span class="sxs-lookup"><span data-stu-id="b57de-143">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="b57de-144">IRTC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="b57de-144">IRTC::GetConversationStatistics</span></span>](irtc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="b57de-145">IRTC:: iniciar</span><span class="sxs-lookup"><span data-stu-id="b57de-145">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="b57de-146">ESTATÍSTICA</span><span class="sxs-lookup"><span data-stu-id="b57de-146">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




