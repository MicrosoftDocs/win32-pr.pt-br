---
description: Fornece acesso à memória compartilhada entre threads do Tablet.
ms.assetid: 047ff598-7d20-49d7-bdd3-498fe5c778c6
title: 'Método ITabletContextP:: UseSharedMemoryCommunications'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.UseSharedMemoryCommunications
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: d7880e1d0377d9d0140a0c82509abd31182c724e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105815569"
---
# <a name="itabletcontextpusesharedmemorycommunications-method"></a><span data-ttu-id="8f992-103">Método ITabletContextP:: UseSharedMemoryCommunications</span><span class="sxs-lookup"><span data-stu-id="8f992-103">ITabletContextP::UseSharedMemoryCommunications method</span></span>

<span data-ttu-id="8f992-104">Fornece acesso à memória compartilhada entre threads do Tablet.</span><span class="sxs-lookup"><span data-stu-id="8f992-104">Provides access to memory shared between tablet threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f992-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f992-105">Syntax</span></span>


```C++
HRESULT UseSharedMemoryCommunications(
  [in]  DWORD pid,
  [out] DWORD *phEventMoreData,
  [out] DWORD *phEventClientReady,
  [out] DWORD *phMutexAccess,
  [out] DWORD *phFileMapping
);
```



## <a name="parameters"></a><span data-ttu-id="8f992-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f992-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f992-107">*pid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8f992-107">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f992-108">ID do processo.</span><span class="sxs-lookup"><span data-stu-id="8f992-108">Process id.</span></span>

</dd> <dt>

<span data-ttu-id="8f992-109">*phEventMoreData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8f992-109">*phEventMoreData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f992-110">Identificador de evento que sinaliza quando novos dados estão disponíveis para serem processados.</span><span class="sxs-lookup"><span data-stu-id="8f992-110">Event handle that signals when new data is available to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="8f992-111">*phEventClientReady* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8f992-111">*phEventClientReady* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f992-112">O identificador de evento retornado usado para sinalizar que o cliente está pronto para receber dados.</span><span class="sxs-lookup"><span data-stu-id="8f992-112">Returned event handle used to signal that the client is ready to receive data.</span></span> <span data-ttu-id="8f992-113">Sinalizado após o processamento de novos dados.</span><span class="sxs-lookup"><span data-stu-id="8f992-113">Signaled after processing new data.</span></span>

</dd> <dt>

<span data-ttu-id="8f992-114">*phMutexAccess* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8f992-114">*phMutexAccess* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f992-115">O mutex que concede acesso à memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="8f992-115">The mutex granting access to shared memory.</span></span>

</dd> <dt>

<span data-ttu-id="8f992-116">*phFileMapping* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8f992-116">*phFileMapping* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f992-117">Ponteiro para o bloco de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="8f992-117">Pointer to the shared memory block.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f992-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8f992-118">Return value</span></span>

<span data-ttu-id="8f992-119">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="8f992-119">This method can return one of these values.</span></span>



| <span data-ttu-id="8f992-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8f992-120">Return code</span></span>                                                                            | <span data-ttu-id="8f992-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f992-121">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="8f992-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8f992-122"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="8f992-123">Êxito.</span><span class="sxs-lookup"><span data-stu-id="8f992-123">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="8f992-124"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="8f992-124"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="8f992-125">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="8f992-125">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8f992-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f992-126">Remarks</span></span>

<span data-ttu-id="8f992-127">O método **UseSharedMemoryCommunications** é usado como parte do protocolo de memória compartilhada do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="8f992-127">The **UseSharedMemoryCommunications** method is used as part of the Tablet PC shared memory protocol.</span></span> <span data-ttu-id="8f992-128">Como o serviço Wisptis tem um IL (nível de integridade alta), ele pode armazenar e acessar dados armazenados na memória compartilhada sem a necessidade de elevar seus privilégios.</span><span class="sxs-lookup"><span data-stu-id="8f992-128">Since the Wisptis service has a high integrity level (IL), it can store and access data stored in shared memory without needing to elevate its privileges.</span></span>

<span data-ttu-id="8f992-129">A estrutura de [**\_ cabeçalho SHAREDMEMORY**](sharedmemory-header.md) é convertida dos dados referenciados pelo mapeamento de arquivo e os dados de pacote brutos seguem o **\_ cabeçalho SHAREDMEMORY**.</span><span class="sxs-lookup"><span data-stu-id="8f992-129">The [**SHAREDMEMORY\_HEADER**](sharedmemory-header.md) structure is cast from the data referenced by the file mapping and the raw packet data follows the **SHAREDMEMORY\_HEADER**.</span></span> <span data-ttu-id="8f992-130">Os dados brutos do pacote podem ser lidos da memória compartilhada quando o evento referenciado por *pdwEventClientReady* é gerado.</span><span class="sxs-lookup"><span data-stu-id="8f992-130">Raw packet data can be read off of the shared memory when the event referenced by *pdwEventClientReady* is raised.</span></span>

<span data-ttu-id="8f992-131">A lista a seguir descreve a sequência de eventos para acessar e usar a memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="8f992-131">The following list describes the sequence of events for accessing and using shared memory.</span></span>

-   <span data-ttu-id="8f992-132">O cliente define o evento clientReady.</span><span class="sxs-lookup"><span data-stu-id="8f992-132">The client sets the clientReady event.</span></span>
-   <span data-ttu-id="8f992-133">O cliente aguarda o evento moreData.</span><span class="sxs-lookup"><span data-stu-id="8f992-133">The client waits for the moreData event.</span></span>
-   <span data-ttu-id="8f992-134">O cliente adquire o mutex.</span><span class="sxs-lookup"><span data-stu-id="8f992-134">The client acquires the mutex.</span></span>
-   <span data-ttu-id="8f992-135">O cliente lê os dados de pacote da seção de memória compartilhada após o cabeçalho e os números de série após os pacotes.</span><span class="sxs-lookup"><span data-stu-id="8f992-135">The client reads packet data from the section of shared memory after the header and serial numbers after the packets.</span></span>
-   <span data-ttu-id="8f992-136">O cliente manipula os dados dependendo do valor de **dwEvent**.</span><span class="sxs-lookup"><span data-stu-id="8f992-136">The client handles data depending on the value of **dwEvent**.</span></span>
-   <span data-ttu-id="8f992-137">O cliente grava-1 (0xFFFFFFFF) em **dwEvent**.</span><span class="sxs-lookup"><span data-stu-id="8f992-137">The client writes -1 (0xFFFFFFFF) into **dwEvent**.</span></span>
-   <span data-ttu-id="8f992-138">O cliente libera o mutex.</span><span class="sxs-lookup"><span data-stu-id="8f992-138">The client releases the mutex.</span></span>
-   <span data-ttu-id="8f992-139">O cliente define o evento clientReady.</span><span class="sxs-lookup"><span data-stu-id="8f992-139">The client sets the clientReady event.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f992-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f992-140">Requirements</span></span>



| <span data-ttu-id="8f992-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f992-141">Requirement</span></span> | <span data-ttu-id="8f992-142">Valor</span><span class="sxs-lookup"><span data-stu-id="8f992-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f992-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f992-143">Minimum supported client</span></span><br/> | <span data-ttu-id="8f992-144">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8f992-144">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8f992-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f992-145">Minimum supported server</span></span><br/> | <span data-ttu-id="8f992-146">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8f992-146">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8f992-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8f992-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="8f992-148"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8f992-148"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f992-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f992-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f992-150">**Interface ITabletContextP**</span><span class="sxs-lookup"><span data-stu-id="8f992-150">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> <dt>

[<span data-ttu-id="8f992-151">**UseNamedSharedMemoryCommunications**</span><span class="sxs-lookup"><span data-stu-id="8f992-151">**UseNamedSharedMemoryCommunications**</span></span>](itabletcontextp-usenamedsharedmemorycommunications.md)
</dt> </dl>

 

 




