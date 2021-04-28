---
description: 'Método IDelaydC:: GetTotalStatistics – o método GetTotalStatistics recupera o total de estatísticas para a captura atual.'
ms.assetid: 904c7496-5603-41b9-8481-06fa31f6f112
title: 'Método IDelaydC:: GetTotalStatistics (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b3a0ce4f230236e276fede528a5e778ecafd51fb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113524"
---
# <a name="idelaydcgettotalstatistics-method"></a><span data-ttu-id="1af63-103">Método IDelaydC:: GetTotalStatistics</span><span class="sxs-lookup"><span data-stu-id="1af63-103">IDelaydC::GetTotalStatistics method</span></span>

<span data-ttu-id="1af63-104">O método **GetTotalStatistics** recupera o [*total de estatísticas*](t.md) para a [*captura*](c.md)atual.</span><span class="sxs-lookup"><span data-stu-id="1af63-104">The **GetTotalStatistics** method retrieves the [*total statistics*](t.md) for the current [*capture*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1af63-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1af63-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="1af63-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1af63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1af63-107">*lpStats* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1af63-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1af63-108">Ponteiro para uma estrutura de [estatísticas](statistics.md)que fornece o total de estatísticas para a captura.</span><span class="sxs-lookup"><span data-stu-id="1af63-108">Pointer to a [STATISTICS](statistics.md)structure that provides the total statistics for the capture.</span></span> <span data-ttu-id="1af63-109">É responsabilidade do chamador alocar e liberar a memória usada pela estrutura de **estatísticas** .</span><span class="sxs-lookup"><span data-stu-id="1af63-109">It is the caller's responsibility to allocate and free the memory used by the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="1af63-110">*fClearAfterReading* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1af63-110">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1af63-111">Sinalizador usado para informar Monitor de Rede como lidar com o armazenamento interno do total de estatísticas.</span><span class="sxs-lookup"><span data-stu-id="1af63-111">Flag used to tell Network Monitor how to handle the internal storage of the total statistics.</span></span> <span data-ttu-id="1af63-112">Uma configuração de **true** informa monitor de rede para limpar o armazenamento interno do total de estatísticas depois que as informações atuais são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="1af63-112">A setting of **TRUE** tells Network Monitor to clear out the internal storage of the total statistics after the current information is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1af63-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1af63-113">Return value</span></span>

<span data-ttu-id="1af63-114">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="1af63-114">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="1af63-115">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="1af63-115">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="1af63-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1af63-116">Return code</span></span>                                                                                          | <span data-ttu-id="1af63-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="1af63-117">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1af63-118"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="1af63-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="1af63-119">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="1af63-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="1af63-120">Chame [IDelaydC:: Connect](idelaydc-connect.md) para conectar-se à rede.</span><span class="sxs-lookup"><span data-stu-id="1af63-120">Call [IDelaydC::Connect](idelaydc-connect.md) to connect to the network.</span></span><br/> |
| <dl> <span data-ttu-id="1af63-121"><dt>**NMERR \_ não \_ atrasada**</dt></span><span class="sxs-lookup"><span data-stu-id="1af63-121"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="1af63-122">O NPP está conectado à rede, mas não com o método [IDelaydC:: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="1af63-122">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>             |
| <dl> <span data-ttu-id="1af63-123"><dt>**NMERR \_ não \_ capturando**</dt></span><span class="sxs-lookup"><span data-stu-id="1af63-123"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="1af63-124">O NPP não está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="1af63-124">The NPP is not capturing data.</span></span> <span data-ttu-id="1af63-125">Chame [IDelaydC:: Start](idelaydc-start.md) para iniciar a captura de dados.</span><span class="sxs-lookup"><span data-stu-id="1af63-125">Call [IDelaydC::Start](idelaydc-start.md) to start capturing data.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="1af63-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="1af63-126">Remarks</span></span>

<span data-ttu-id="1af63-127">Esse método retorna dados somente enquanto uma captura está em andamento; Quando a captura for pausada, as chamadas para esse método não serão realizadas com sucesso.</span><span class="sxs-lookup"><span data-stu-id="1af63-127">This method returns data only while a capture is in progress; when the capture is paused, calls to this method will not succeed.</span></span>

<span data-ttu-id="1af63-128">Monitor de Rede também armazena [*Estatísticas de conversa*](c.md), que podem ser recuperadas chamando o método [IDelaydC:: GetConversationStatistics](idelaydc-getconversationstatistics.md) .</span><span class="sxs-lookup"><span data-stu-id="1af63-128">Network Monitor also stores [*conversation statistics*](c.md), which can be retrieved by calling the [IDelaydC::GetConversationStatistics](idelaydc-getconversationstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1af63-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1af63-129">Requirements</span></span>



| <span data-ttu-id="1af63-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1af63-130">Requirement</span></span> | <span data-ttu-id="1af63-131">Valor</span><span class="sxs-lookup"><span data-stu-id="1af63-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1af63-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1af63-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1af63-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1af63-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="1af63-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1af63-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1af63-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1af63-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="1af63-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1af63-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="1af63-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1af63-137"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="1af63-138">DLL</span><span class="sxs-lookup"><span data-stu-id="1af63-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1af63-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1af63-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1af63-140">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1af63-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1af63-141">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="1af63-141">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="1af63-142">IDelaydC:: conectar</span><span class="sxs-lookup"><span data-stu-id="1af63-142">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="1af63-143">IDelaydC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="1af63-143">IDelaydC::GetConversationStatistics</span></span>](idelaydc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="1af63-144">IDelaydC:: iniciar</span><span class="sxs-lookup"><span data-stu-id="1af63-144">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="1af63-145">ESTATÍSTICA</span><span class="sxs-lookup"><span data-stu-id="1af63-145">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




