---
description: Recupera as informações de sessão e de estação sobre a captura atual.
ms.assetid: 7fc436fc-b569-402d-a1ea-c1bb65de8a9e
title: 'Método IStats:: GetConversationStatistics (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 030fafb4ccf041c2804179f8adf0088ca3fba845
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105775674"
---
# <a name="istatsgetconversationstatistics-method"></a><span data-ttu-id="579d9-103">Método IStats:: GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="579d9-103">IStats::GetConversationStatistics method</span></span>

<span data-ttu-id="579d9-104">O método **GetConversationStatistics** recupera informações de sessão e de estação sobre a captura atual.</span><span class="sxs-lookup"><span data-stu-id="579d9-104">The **GetConversationStatistics** method retrieves session and station information about the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="579d9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="579d9-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="579d9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="579d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="579d9-107">*nSessions* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="579d9-107">*nSessions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="579d9-108">Um ponteiro para um DWORD que contém o número de [*sessões*](s.md) registradas para a captura atual.</span><span class="sxs-lookup"><span data-stu-id="579d9-108">A pointer to a DWORD that contains the number of [*sessions*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="579d9-109">*lpSessionStats* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="579d9-109">*lpSessionStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="579d9-110">Um ponteiro para uma estrutura [**SESSIONSTATS**](sessionstats.md) .</span><span class="sxs-lookup"><span data-stu-id="579d9-110">A pointer to a [**SESSIONSTATS**](sessionstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="579d9-111">*nStations* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="579d9-111">*nStations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="579d9-112">Um ponteiro para um DWORD que contém o número de [*estações*](s.md) registradas para a captura atual.</span><span class="sxs-lookup"><span data-stu-id="579d9-112">A pointer to a DWORD that contains the number of [*stations*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="579d9-113">*lpStationStats* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="579d9-113">*lpStationStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="579d9-114">Um ponteiro para uma estrutura [**STATIONSTATS**](stationstats.md) .</span><span class="sxs-lookup"><span data-stu-id="579d9-114">A pointer to a [**STATIONSTATS**](stationstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="579d9-115">*fClearAfterReading* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="579d9-115">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="579d9-116">Sinalizador usado para instruir Monitor de Rede a limpar o armazenamento interno das estruturas [**SESSIONSTATS**](sessionstats.md) e [**STATIONSTATS**](stationstats.md) depois que os dados atuais forem recuperados.</span><span class="sxs-lookup"><span data-stu-id="579d9-116">Flag used to instruct Network Monitor to clear the internal storage of the [**SESSIONSTATS**](sessionstats.md) and [**STATIONSTATS**](stationstats.md) structures after the current data is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="579d9-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="579d9-117">Return value</span></span>

<span data-ttu-id="579d9-118">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="579d9-118">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="579d9-119">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="579d9-119">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="579d9-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="579d9-120">Return code</span></span>                                                                                                   | <span data-ttu-id="579d9-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="579d9-121">Description</span></span>                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="579d9-122"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="579d9-122"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="579d9-123">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="579d9-123">The NPP is not connected to the network.</span></span> <span data-ttu-id="579d9-124">Chame [**IStats:: Connect**](istats-connect.md) para conectar o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="579d9-124">Call [**IStats::Connect**](istats-connect.md) to connect the NPP to the network.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="579d9-125"><dt>**NMERR \_ não \_ capturando**</dt></span><span class="sxs-lookup"><span data-stu-id="579d9-125"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="579d9-126">O NPP não está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="579d9-126">The NPP is not capturing data.</span></span> <span data-ttu-id="579d9-127">Chame [**IStats:: Start**](istats-start.md) para iniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="579d9-127">Call [**IStats::Start**](istats-start.md) to start the capture.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="579d9-128"><dt>**NMERR \_ \_ somente não estatísticas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="579d9-128"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl>        | <span data-ttu-id="579d9-129">O NPP está conectado à rede, mas não com o método [**IStats:: Connect**](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="579d9-129">The NPP is connected to the network, but not with the [**IStats::Connect**](istats-connect.md) method.</span></span><br/>                                                                                                                         |
| <dl> <span data-ttu-id="579d9-130"><dt>**NMERR \_ sem \_ Estatísticas de conversa \_**</dt></span><span class="sxs-lookup"><span data-stu-id="579d9-130"><dt>**NMERR\_NO\_CONVERSATION\_STATS**</dt></span></span> </dl> | <span data-ttu-id="579d9-131">A configuração dessa conexão é definida para não salvar as estatísticas de conversa.</span><span class="sxs-lookup"><span data-stu-id="579d9-131">The configuration for this connection is set to not save conversation statistics.</span></span> <span data-ttu-id="579d9-132">Para salvar as estatísticas de conversa, pare a captura, defina **NoConversationStats = Yes** no blob de configuração e reinicie a captura.</span><span class="sxs-lookup"><span data-stu-id="579d9-132">To save conversation statistics, stop the capture, set **NoConversationStats = YES** in the configuration BLOB, and then restart the capture.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="579d9-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="579d9-133">Remarks</span></span>

<span data-ttu-id="579d9-134">Esse método pode ser chamado somente enquanto a captura de dados está em andamento; Quando a captura atual for pausada, uma chamada para esse método não terá sucesso.</span><span class="sxs-lookup"><span data-stu-id="579d9-134">This method can be called only while data capture is in progress; when the current capture is paused, a call to this method will not succeed.</span></span>

<span data-ttu-id="579d9-135">Para iniciar uma captura, chame o método [**IStats:: Start**](istats-start.md) .</span><span class="sxs-lookup"><span data-stu-id="579d9-135">To start a capture, call the [**IStats::Start**](istats-start.md) method.</span></span> <span data-ttu-id="579d9-136">Para recuperar outros tipos de estatísticas, chame [**IStats:: GetTotalStatistics**](istats-gettotalstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="579d9-136">To retrieve other types of statistics, call [**IStats::GetTotalStatistics**](istats-gettotalstatistics.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="579d9-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="579d9-137">Requirements</span></span>



| <span data-ttu-id="579d9-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="579d9-138">Requirement</span></span> | <span data-ttu-id="579d9-139">Valor</span><span class="sxs-lookup"><span data-stu-id="579d9-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="579d9-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="579d9-140">Minimum supported client</span></span><br/> | <span data-ttu-id="579d9-141">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="579d9-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="579d9-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="579d9-142">Minimum supported server</span></span><br/> | <span data-ttu-id="579d9-143">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="579d9-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="579d9-144">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="579d9-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="579d9-145"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="579d9-145"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="579d9-146">DLL</span><span class="sxs-lookup"><span data-stu-id="579d9-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="579d9-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="579d9-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="579d9-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="579d9-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="579d9-149">**IStats**</span><span class="sxs-lookup"><span data-stu-id="579d9-149">**IStats**</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="579d9-150">**IStats::GetTotalStatistics**</span><span class="sxs-lookup"><span data-stu-id="579d9-150">**IStats::GetTotalStatistics**</span></span>](istats-gettotalstatistics.md)
</dt> <dt>

[<span data-ttu-id="579d9-151">**IStats:: iniciar**</span><span class="sxs-lookup"><span data-stu-id="579d9-151">**IStats::Start**</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="579d9-152">**IStats:: conectar**</span><span class="sxs-lookup"><span data-stu-id="579d9-152">**IStats::Connect**</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="579d9-153">**SESSIONSTATS**</span><span class="sxs-lookup"><span data-stu-id="579d9-153">**SESSIONSTATS**</span></span>](sessionstats.md)
</dt> <dt>

[<span data-ttu-id="579d9-154">**STATIONSTATS**</span><span class="sxs-lookup"><span data-stu-id="579d9-154">**STATIONSTATS**</span></span>](stationstats.md)
</dt> </dl>

 

 




