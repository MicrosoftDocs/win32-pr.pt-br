---
description: Configura a comunicação de memória compartilhada para o contexto do Tablet.
ms.assetid: 63e6b271-d89a-4c91-9a15-9e41dcdfa363
title: 'Método ITabletContextP:: UseNamedSharedMemoryCommunications'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.UseNamedSharedMemoryCommunications
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: 81e8c653dd12600ae02fe7e6038de6e6a38786e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105815571"
---
# <a name="itabletcontextpusenamedsharedmemorycommunications-method"></a><span data-ttu-id="68bd1-103">Método ITabletContextP:: UseNamedSharedMemoryCommunications</span><span class="sxs-lookup"><span data-stu-id="68bd1-103">ITabletContextP::UseNamedSharedMemoryCommunications method</span></span>

<span data-ttu-id="68bd1-104">Configura a comunicação de memória compartilhada para o contexto do Tablet.</span><span class="sxs-lookup"><span data-stu-id="68bd1-104">Sets up shared memory communication for the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="68bd1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="68bd1-105">Syntax</span></span>


```C++
HRESULT UseNamedSharedMemoryCommunications(
  [in]  DWORD  pid,
  [in]  LPCSTR pszCallerSid,
  [in]  LPCSTR pszCallerIntegritySid,
  [out] DWORD  *pdwEventMoreDataId,
  [out] DWORD  *pdwEventClientReadyId,
  [out] DWORD  *pdwMutexAccessId,
  [out] DWORD  *pdwFileMappingId
);
```



## <a name="parameters"></a><span data-ttu-id="68bd1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="68bd1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68bd1-107">*pid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="68bd1-107">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68bd1-108">A ID do processo do cliente que acessa a memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="68bd1-108">The process ID of the client that accesses shared memory.</span></span>

</dd> <dt>

<span data-ttu-id="68bd1-109">*pszCallerSid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="68bd1-109">*pszCallerSid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68bd1-110">O identificador de segurança do chamador da função.</span><span class="sxs-lookup"><span data-stu-id="68bd1-110">The security identifier of the function caller.</span></span>

</dd> <dt>

<span data-ttu-id="68bd1-111">*pszCallerIntegritySid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="68bd1-111">*pszCallerIntegritySid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68bd1-112">O identificador de segurança que pode verificar a integridade da função de chamada.</span><span class="sxs-lookup"><span data-stu-id="68bd1-112">The security identifier that can verify the integrity of the calling function.</span></span>

</dd> <dt>

<span data-ttu-id="68bd1-113">*pdwEventMoreDataId* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="68bd1-113">*pdwEventMoreDataId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68bd1-114">Um inteiro usado para construir o nome de um evento.</span><span class="sxs-lookup"><span data-stu-id="68bd1-114">An integer used to construct the name of an event.</span></span> <span data-ttu-id="68bd1-115">O evento indica se há mais dados.</span><span class="sxs-lookup"><span data-stu-id="68bd1-115">The event indicates whether there is more data.</span></span>

</dd> <dt>

<span data-ttu-id="68bd1-116">*pdwEventClientReadyId* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="68bd1-116">*pdwEventClientReadyId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68bd1-117">Um inteiro usado para construir o nome de um evento.</span><span class="sxs-lookup"><span data-stu-id="68bd1-117">An integer used to construct the name of an event.</span></span> <span data-ttu-id="68bd1-118">O evento sinaliza que o cliente está pronto para receber dados.</span><span class="sxs-lookup"><span data-stu-id="68bd1-118">The event signals that the client is ready to receive data.</span></span> <span data-ttu-id="68bd1-119">O evento é sinalizado após o processamento de novos dados.</span><span class="sxs-lookup"><span data-stu-id="68bd1-119">The event is signaled after processing new data.</span></span>

</dd> <dt>

<span data-ttu-id="68bd1-120">*pdwMutexAccessId* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="68bd1-120">*pdwMutexAccessId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68bd1-121">Um ponteiro para o identificador de acesso da memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="68bd1-121">A pointer to the access identifier of the shared memory.</span></span>

</dd> <dt>

<span data-ttu-id="68bd1-122">*pdwFileMappingId* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="68bd1-122">*pdwFileMappingId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68bd1-123">Um inteiro que identifica a memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="68bd1-123">An integer that identifies the shared memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68bd1-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="68bd1-124">Return value</span></span>

<span data-ttu-id="68bd1-125">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="68bd1-125">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="68bd1-126">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="68bd1-126">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="68bd1-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="68bd1-127">Remarks</span></span>

<span data-ttu-id="68bd1-128">O método **UseNamedSharedMemoryCommunications** faz parte do protocolo de memória compartilhada do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="68bd1-128">The **UseNamedSharedMemoryCommunications** method is part of the Tablet PC shared memory protocol.</span></span> <span data-ttu-id="68bd1-129">Um cliente sem privilégios elevados passa em um identificador de segurança (SID) e um identificador de segurança de nível de integridade (IL-SID) para que o serviço do Tablet possa usar ACLs (listas de controle de acesso) para acessar os objetos de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="68bd1-129">A client without elevated privileges passes in a security identifier (SID) and an integrity level security identifier (IL-SID) so that the Tablet service can use access control lists (ACL) to access the shared memory objects.</span></span> <span data-ttu-id="68bd1-130">Se o cliente tiver privilégios elevados, ele deverá usar UseSharedMemoryCommunications, que é a API que será chamada se o serviço já tiver um privilégio elevado.</span><span class="sxs-lookup"><span data-stu-id="68bd1-130">If the client has elevated privileges, it should use UseSharedMemoryCommunications, which is the API that is called if the service already has an elevated privilege.</span></span>

<span data-ttu-id="68bd1-131">A estrutura de [**\_ cabeçalho SHAREDMEMORY**](sharedmemory-header.md) armazena o cabeçalho de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="68bd1-131">The [**SHAREDMEMORY\_HEADER**](sharedmemory-header.md) structure stores the shared memory header.</span></span>

<span data-ttu-id="68bd1-132">A estrutura de [**\_ cabeçalho SHAREDMEMORY**](sharedmemory-header.md) é convertida dos dados referenciados pelo mapeamento de arquivo.</span><span class="sxs-lookup"><span data-stu-id="68bd1-132">The [**SHAREDMEMORY\_HEADER**](sharedmemory-header.md) structure is cast from the data referenced by the file mapping.</span></span> <span data-ttu-id="68bd1-133">Os dados brutos do pacote seguem o **\_ cabeçalho SHAREDMEMORY**.</span><span class="sxs-lookup"><span data-stu-id="68bd1-133">The raw packet data follows the **SHAREDMEMORY\_HEADER**.</span></span> <span data-ttu-id="68bd1-134">Os dados brutos do pacote podem ser lidos da memória compartilhada quando o evento referenciado por *pdwEventClientReadyId* é gerado.</span><span class="sxs-lookup"><span data-stu-id="68bd1-134">Raw packet data can be read off of the shared memory when the event referenced by *pdwEventClientReadyId* is raised.</span></span>

<span data-ttu-id="68bd1-135">A lista a seguir descreve a sequência de eventos para acessar e usar a memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="68bd1-135">The following list describes the sequence of events for accessing and using shared memory.</span></span>

1.  <span data-ttu-id="68bd1-136">O cliente gera o evento clientReady.</span><span class="sxs-lookup"><span data-stu-id="68bd1-136">The client raises the clientReady event.</span></span>
2.  <span data-ttu-id="68bd1-137">O cliente aguarda o evento moreData.</span><span class="sxs-lookup"><span data-stu-id="68bd1-137">The client waits for the moreData event.</span></span>
3.  <span data-ttu-id="68bd1-138">O cliente adquire o mutex.</span><span class="sxs-lookup"><span data-stu-id="68bd1-138">The client acquires the mutex.</span></span>
4.  <span data-ttu-id="68bd1-139">O cliente lê os dados de pacote da seção de memória compartilhada que segue o cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="68bd1-139">The client reads packet data from the section of shared memory that follows the header.</span></span> <span data-ttu-id="68bd1-140">Os números de série aparecem na memória compartilhada após os dados do pacote.</span><span class="sxs-lookup"><span data-stu-id="68bd1-140">Serial numbers appear in the shared memory after the packet data.</span></span>
5.  <span data-ttu-id="68bd1-141">O cliente manipula os dados dependendo do valor de **dwEvent**.</span><span class="sxs-lookup"><span data-stu-id="68bd1-141">The client handles data depending on the value of **dwEvent**.</span></span>
6.  <span data-ttu-id="68bd1-142">O cliente grava-1 (0xFFFFFFFF) em **dwEvent**.</span><span class="sxs-lookup"><span data-stu-id="68bd1-142">The client writes -1 (0xFFFFFFFF) into **dwEvent**.</span></span>
7.  <span data-ttu-id="68bd1-143">O cliente libera o mutex.</span><span class="sxs-lookup"><span data-stu-id="68bd1-143">The client releases the mutex.</span></span>
8.  <span data-ttu-id="68bd1-144">O cliente gera o evento clientReady.</span><span class="sxs-lookup"><span data-stu-id="68bd1-144">The client raises the clientReady event.</span></span>

<span data-ttu-id="68bd1-145">Os nomes de evento são criados por meio da formatação da saída desse método.</span><span class="sxs-lookup"><span data-stu-id="68bd1-145">The event names are created by formatting the output of this method.</span></span> <span data-ttu-id="68bd1-146">As definições a seguir podem ser usadas em conjunto com sprintf ou seu equivalente para criar os nomes de evento.</span><span class="sxs-lookup"><span data-stu-id="68bd1-146">The following definitions can be used in conjunction with sprintf or its equivalent to create the event names.</span></span>


```C++
#define WISPTIS_SM_MORE_DATA_EVENT_NAME     _T("wisptis-1-%d-%u")
#define WISPTIS_SM_CLIENT_DONE_EVENT_NAME   _T("wisptis-2-%d-%u")
#define WISPTIS_SM_SECTION_NAME             _T("wisptis-3-%d-%u")
#define WISPTIS_SM_THREAD_EVENT_NAME        _T("wisptis-4-%u")
```



<span data-ttu-id="68bd1-147">Em cada definição, a seção% d é substituída pela ID do processo e a seção% u é substituída pelo inteiro retornado em *pdwEventMoreDataId* ou *pdwEventClientReadyId*.</span><span class="sxs-lookup"><span data-stu-id="68bd1-147">In each definition, the %d section is replaced with the process ID, and the %u section is replaced with the integer returned in *pdwEventMoreDataId* or *pdwEventClientReadyId*.</span></span>

## <a name="requirements"></a><span data-ttu-id="68bd1-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68bd1-148">Requirements</span></span>



| <span data-ttu-id="68bd1-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="68bd1-149">Requirement</span></span> | <span data-ttu-id="68bd1-150">Valor</span><span class="sxs-lookup"><span data-stu-id="68bd1-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68bd1-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68bd1-151">Minimum supported client</span></span><br/> | <span data-ttu-id="68bd1-152">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="68bd1-152">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="68bd1-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68bd1-153">Minimum supported server</span></span><br/> | <span data-ttu-id="68bd1-154">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="68bd1-154">None supported</span></span><br/>                                                              |
| <span data-ttu-id="68bd1-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="68bd1-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="68bd1-156"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="68bd1-156"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68bd1-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="68bd1-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68bd1-158">**UseSharedMemoryCommunications**</span><span class="sxs-lookup"><span data-stu-id="68bd1-158">**UseSharedMemoryCommunications**</span></span>](itabletcontextp-usesharedmemorycommunications.md)
</dt> <dt>

[<span data-ttu-id="68bd1-159">**ITabletContextP**</span><span class="sxs-lookup"><span data-stu-id="68bd1-159">**ITabletContextP**</span></span>](itabletcontextp.md)
</dt> </dl>

 

 




