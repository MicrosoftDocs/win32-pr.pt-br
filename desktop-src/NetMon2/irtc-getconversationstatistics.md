---
description: O método GetConversationStatistics recupera informações de sessão e de estação sobre a captura atual.
ms.assetid: 27f364cd-fee9-4262-b181-c5f15fb12e51
title: 'Método IRTC:: GetConversationStatistics (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 758488cb3c3f65922bbf6aac4f39774a5430fc92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827865"
---
# <a name="irtcgetconversationstatistics-method"></a><span data-ttu-id="aa210-103">Método IRTC:: GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="aa210-103">IRTC::GetConversationStatistics method</span></span>

<span data-ttu-id="aa210-104">O método **GetConversationStatistics** recupera informações de [*sessão*](s.md) e de [*estação*](s.md) sobre a captura atual.</span><span class="sxs-lookup"><span data-stu-id="aa210-104">The **GetConversationStatistics** method retrieves [*session*](s.md) and [*station information*](s.md) about the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa210-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa210-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="aa210-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa210-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa210-107">*nSessions* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="aa210-107">*nSessions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa210-108">Ponteiro para um DWORD que contém o número de [*sessões*](s.md) registradas para a captura atual.</span><span class="sxs-lookup"><span data-stu-id="aa210-108">Pointer to a DWORD that contains the number of [*sessions*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="aa210-109">*lpSessionStats* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="aa210-109">*lpSessionStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa210-110">Ponteiro para uma estrutura [SESSIONSTATS](sessionstats.md) .</span><span class="sxs-lookup"><span data-stu-id="aa210-110">Pointer to a [SESSIONSTATS](sessionstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="aa210-111">*nStations* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="aa210-111">*nStations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa210-112">Ponteiro para um DWORD que contém o número de [*estações*](s.md) registradas para a captura atual.</span><span class="sxs-lookup"><span data-stu-id="aa210-112">Pointer to a DWORD that contains the number of [*stations*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="aa210-113">*lpStationStats* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="aa210-113">*lpStationStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa210-114">Ponteiro para uma estrutura [STATIONSTATS](stationstats.md) .</span><span class="sxs-lookup"><span data-stu-id="aa210-114">Pointer to a [STATIONSTATS](stationstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="aa210-115">*fClearAfterReading* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aa210-115">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa210-116">Sinalizador usado para informar Monitor de Rede para limpar o armazenamento interno das estruturas [SESSIONSTATS](sessionstats.md) e [STATIONSTATS](stationstats.md) depois de recuperar as informações atuais.</span><span class="sxs-lookup"><span data-stu-id="aa210-116">Flag used to tell Network Monitor to clear out the internal storage of the [SESSIONSTATS](sessionstats.md) and [STATIONSTATS](stationstats.md) structures after it retrieves the current information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa210-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa210-117">Return value</span></span>

<span data-ttu-id="aa210-118">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="aa210-118">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="aa210-119">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="aa210-119">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="aa210-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="aa210-120">Return code</span></span>                                                                                                   | <span data-ttu-id="aa210-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="aa210-121">Description</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aa210-122"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="aa210-122"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="aa210-123">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="aa210-123">The NPP is not connected to the network.</span></span> <span data-ttu-id="aa210-124">Chame [IRTC:: Connect](irtc-connect.md) para conectar o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="aa210-124">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="aa210-125"><dt>**NMERR \_ não \_ capturando**</dt></span><span class="sxs-lookup"><span data-stu-id="aa210-125"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="aa210-126">O NPP não está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="aa210-126">The NPP is not capturing data.</span></span> <span data-ttu-id="aa210-127">Chame [IRTC:: Start](irtc-start.md) para iniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="aa210-127">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="aa210-128"><dt>**NMERR \_ não está em \_ tempo real**</dt></span><span class="sxs-lookup"><span data-stu-id="aa210-128"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>           | <span data-ttu-id="aa210-129">O NPP está conectado à rede, mas não com o método [IRTC:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="aa210-129">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                                                                                                                          |
| <dl> <span data-ttu-id="aa210-130"><dt>**NMERR \_ sem \_ Estatísticas de conversa \_**</dt></span><span class="sxs-lookup"><span data-stu-id="aa210-130"><dt>**NMERR\_NO\_CONVERSATION\_STATS**</dt></span></span> </dl> | <span data-ttu-id="aa210-131">A configuração dessa conexão é definida para não salvar as estatísticas de conversa.</span><span class="sxs-lookup"><span data-stu-id="aa210-131">The configuration for this connection is set to not save conversation statistics.</span></span> <span data-ttu-id="aa210-132">Para salvar as estatísticas de conversa, pare a captura, defina NoConversationStats = YES no BLOB de configuração e reinicie a captura.</span><span class="sxs-lookup"><span data-stu-id="aa210-132">To save conversation statistics, stop the capture, set NoConversationStats = YES in the configuration BLOB, then restart the capture.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="aa210-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa210-133">Remarks</span></span>

<span data-ttu-id="aa210-134">Esse método só pode ser chamado enquanto você estiver capturando dados; Se você chamar esse método enquanto a captura atual estiver pausada, o método não terá sucesso.</span><span class="sxs-lookup"><span data-stu-id="aa210-134">This method can only be called while you are capturing data; if you call this method while the current capture is paused, the method will not succeed.</span></span> <span data-ttu-id="aa210-135">Para iniciar uma captura, chame o método [IRTC:: Start](irtc-start.md) .</span><span class="sxs-lookup"><span data-stu-id="aa210-135">To start a capture, call the [IRTC::Start](irtc-start.md) method.</span></span>

<span data-ttu-id="aa210-136">Para recuperar outros tipos de estatísticas, chame o método [IRTC:: GetTotalStatistics](irtc-gettotalstatistics.md) .</span><span class="sxs-lookup"><span data-stu-id="aa210-136">To retrieve other types of statistics, call the [IRTC::GetTotalStatistics](irtc-gettotalstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa210-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa210-137">Requirements</span></span>



| <span data-ttu-id="aa210-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa210-138">Requirement</span></span> | <span data-ttu-id="aa210-139">Valor</span><span class="sxs-lookup"><span data-stu-id="aa210-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa210-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa210-140">Minimum supported client</span></span><br/> | <span data-ttu-id="aa210-141">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="aa210-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="aa210-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa210-142">Minimum supported server</span></span><br/> | <span data-ttu-id="aa210-143">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="aa210-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="aa210-144">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="aa210-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa210-145"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa210-145"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="aa210-146">DLL</span><span class="sxs-lookup"><span data-stu-id="aa210-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa210-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa210-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa210-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa210-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa210-149">IRTC</span><span class="sxs-lookup"><span data-stu-id="aa210-149">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="aa210-150">IRTC:: conectar</span><span class="sxs-lookup"><span data-stu-id="aa210-150">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="aa210-151">IRTC::GetTotalStatistics</span><span class="sxs-lookup"><span data-stu-id="aa210-151">IRTC::GetTotalStatistics</span></span>](irtc-gettotalstatistics.md)
</dt> <dt>

[<span data-ttu-id="aa210-152">IRTC:: iniciar</span><span class="sxs-lookup"><span data-stu-id="aa210-152">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="aa210-153">SESSIONSTATS</span><span class="sxs-lookup"><span data-stu-id="aa210-153">SESSIONSTATS</span></span>](sessionstats.md)
</dt> <dt>

[<span data-ttu-id="aa210-154">STATIONSTATS</span><span class="sxs-lookup"><span data-stu-id="aa210-154">STATIONSTATS</span></span>](stationstats.md)
</dt> </dl>

 

 




