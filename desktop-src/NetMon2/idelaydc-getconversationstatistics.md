---
description: 'Método IDelaydC:: GetConversationStatistics – o método GetConversationStatistics recupera informações de sessão e de estação sobre a captura atual.'
ms.assetid: 0164fa0e-90f2-4b97-be9d-55d172f8112d
title: 'Método IDelaydC:: GetConversationStatistics (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d4d4c1bb1ad7ecb45b640c16322e297f9f640ef1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103804"
---
# <a name="idelaydcgetconversationstatistics-method"></a><span data-ttu-id="e167c-103">Método IDelaydC:: GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="e167c-103">IDelaydC::GetConversationStatistics method</span></span>

<span data-ttu-id="e167c-104">O método **GetConversationStatistics** recupera informações de [*sessão*](s.md) e de [*estação*](s.md) sobre a captura atual.</span><span class="sxs-lookup"><span data-stu-id="e167c-104">The **GetConversationStatistics** method retrieves [*session*](s.md) and [*station information*](s.md) about the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="e167c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e167c-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="e167c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e167c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e167c-107">*nSessions* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e167c-107">*nSessions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e167c-108">Ponteiro para um DWORD que contém o número de [*sessões*](s.md) registradas para a captura atual.</span><span class="sxs-lookup"><span data-stu-id="e167c-108">Pointer to a DWORD that contains the number of [*sessions*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="e167c-109">*lpSessionStats* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e167c-109">*lpSessionStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e167c-110">Ponteiro para uma estrutura [SESSIONSTATS](sessionstats.md) .</span><span class="sxs-lookup"><span data-stu-id="e167c-110">Pointer to a [SESSIONSTATS](sessionstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e167c-111">*nStations* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e167c-111">*nStations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e167c-112">Ponteiro para um DWORD que contém o número de [*estações*](s.md) registradas para a captura atual.</span><span class="sxs-lookup"><span data-stu-id="e167c-112">Pointer to a DWORD that contains the number of [*stations*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="e167c-113">*lpStationStats* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e167c-113">*lpStationStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e167c-114">Ponteiro para uma estrutura [STATIONSTATS](stationstats.md) .</span><span class="sxs-lookup"><span data-stu-id="e167c-114">Pointer to a [STATIONSTATS](stationstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e167c-115">*fClearAfterReading* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e167c-115">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e167c-116">Sinalizador usado para informar Monitor de Rede para limpar o armazenamento interno das estruturas [SESSIONSTATS](sessionstats.md) e [STATIONSTATS](stationstats.md) depois de recuperar as informações atuais.</span><span class="sxs-lookup"><span data-stu-id="e167c-116">Flag used to tell Network Monitor to clear out the internal storage of the [SESSIONSTATS](sessionstats.md) and [STATIONSTATS](stationstats.md) structures after it retrieves the current information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e167c-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e167c-117">Return value</span></span>

<span data-ttu-id="e167c-118">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="e167c-118">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="e167c-119">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="e167c-119">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="e167c-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e167c-120">Return code</span></span>                                                                                                   | <span data-ttu-id="e167c-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="e167c-121">Description</span></span>                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e167c-122"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="e167c-122"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="e167c-123">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="e167c-123">The NPP is not connected to the network.</span></span> <span data-ttu-id="e167c-124">Chame [IDelaydC:: Connect](idelaydc-connect.md) para conectar o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="e167c-124">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="e167c-125"><dt>**NMERR \_ não \_ capturando**</dt></span><span class="sxs-lookup"><span data-stu-id="e167c-125"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="e167c-126">O NPP não está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="e167c-126">The NPP is not capturing data.</span></span> <span data-ttu-id="e167c-127">Chame [IDelaydC:: Start](idelaydc-start.md) para iniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="e167c-127">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="e167c-128"><dt>**NMERR \_ não \_ atrasada**</dt></span><span class="sxs-lookup"><span data-stu-id="e167c-128"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>            | <span data-ttu-id="e167c-129">O NPP está conectado à rede, mas não com o método [IDelaydC:: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="e167c-129">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="e167c-130"><dt>**NMERR \_ sem \_ Estatísticas de conversa \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e167c-130"><dt>**NMERR\_NO\_CONVERSATION\_STATS**</dt></span></span> </dl> | <span data-ttu-id="e167c-131">A configuração dessa conexão é definida para não salvar as estatísticas de conversa.</span><span class="sxs-lookup"><span data-stu-id="e167c-131">The configuration for this connection is set to not save conversation statistics.</span></span> <span data-ttu-id="e167c-132">Para salvar as estatísticas de conversa, pare a captura, defina NoConversationStats = YES no BLOB de configuração e reinicie a captura.</span><span class="sxs-lookup"><span data-stu-id="e167c-132">To save conversation statistics, stop the capture, set NoConversationStats = YES in the configuration BLOB, and then restart the capture.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e167c-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="e167c-133">Remarks</span></span>

<span data-ttu-id="e167c-134">Este método só pode ser chamado quando a captura de dados está em andamento; Quando a captura atual for pausada, as chamadas para esse método não serão realizadas com sucesso.</span><span class="sxs-lookup"><span data-stu-id="e167c-134">This method can only be called only while data capture is in progress; when the current capture is paused, calls to this method will not succeed.</span></span> <span data-ttu-id="e167c-135">Para iniciar uma captura, chame o método [IDelaydC:: Start](idelaydc-start.md) .</span><span class="sxs-lookup"><span data-stu-id="e167c-135">To start a capture, call the [IDelaydC::Start](idelaydc-start.md) method.</span></span>

<span data-ttu-id="e167c-136">Para recuperar outros tipos de estatísticas, chame [IDelaydC:: GetTotalStatistics](idelaydc-gettotalstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="e167c-136">To retrieve other types of statistics, call [IDelaydC::GetTotalStatistics](idelaydc-gettotalstatistics.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e167c-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e167c-137">Requirements</span></span>



| <span data-ttu-id="e167c-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="e167c-138">Requirement</span></span> | <span data-ttu-id="e167c-139">Valor</span><span class="sxs-lookup"><span data-stu-id="e167c-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e167c-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e167c-140">Minimum supported client</span></span><br/> | <span data-ttu-id="e167c-141">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e167c-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="e167c-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e167c-142">Minimum supported server</span></span><br/> | <span data-ttu-id="e167c-143">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e167c-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="e167c-144">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e167c-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="e167c-145"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e167c-145"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="e167c-146">DLL</span><span class="sxs-lookup"><span data-stu-id="e167c-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e167c-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e167c-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e167c-148">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e167c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e167c-149">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="e167c-149">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="e167c-150">IDelaydC:: conectar</span><span class="sxs-lookup"><span data-stu-id="e167c-150">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="e167c-151">IDelaydC::GetTotalStatistics</span><span class="sxs-lookup"><span data-stu-id="e167c-151">IDelaydC::GetTotalStatistics</span></span>](idelaydc-gettotalstatistics.md)
</dt> <dt>

[<span data-ttu-id="e167c-152">IDelaydC:: iniciar</span><span class="sxs-lookup"><span data-stu-id="e167c-152">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="e167c-153">SESSIONSTATS</span><span class="sxs-lookup"><span data-stu-id="e167c-153">SESSIONSTATS</span></span>](sessionstats.md)
</dt> <dt>

[<span data-ttu-id="e167c-154">STATIONSTATS</span><span class="sxs-lookup"><span data-stu-id="e167c-154">STATIONSTATS</span></span>](stationstats.md)
</dt> </dl>

 

 




