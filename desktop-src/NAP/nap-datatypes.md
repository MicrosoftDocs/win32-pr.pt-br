---
title: Tipos de datanap (NapTypes. h)
description: 'Observação: a plataforma de proteção de acesso à rede não está disponível a partir do Windows 10 os tipos de DataType para a API NAP (proteção de acesso à rede) são os seguintes.'
ms.assetid: 54f2866b-4333-4fc8-bb25-b7d4ae72b7dc
keywords:
- Experiênciatime
- ProtocolMaxSize
- NapComponentId
- SystemHealthEntityId
- EnforcementEntityId
- SystemHealthEntityCount
- EnforcementEntityCount
- StringCorrelationId
- ConnectionId
- Percentual
- MessageId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5780d73701354a12b244c5e5ea6167c2cfba70d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918947"
---
# <a name="nap-datatypes"></a><span data-ttu-id="0c046-114">Tipos de datanap</span><span class="sxs-lookup"><span data-stu-id="0c046-114">NAP Datatypes</span></span>

> [!Note]  
> <span data-ttu-id="0c046-115">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="0c046-115">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0c046-116">Os tipos de texto da API NAP (proteção de acesso à rede) são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="0c046-116">The datatypes for the Network Access Protection (NAP) API are as follows.</span></span>


```C++
typedef FILETIME ProbationTime;
typedef UINT32 ProtocolMaxSize;
typedef UINT32 NapComponentId;
typedef NapComponentId SystemHealthEntityId;
typedef NapComponentId EnforcementEntityId;
typedef UINT16 SystemHealthEntityCount;
typedef UINT16 EnforcementEntityCount;
typedef CountedString StringCorrelationId;
typedef GUID ConnectionId;
typedef UINT8 Percentage;
typedef UINT32 MessageId;
```



<dl> <dt>

<span data-ttu-id="0c046-117">**Experiênciatime**</span><span class="sxs-lookup"><span data-stu-id="0c046-117">**ProbationTime**</span></span>
</dt> <dd>

<span data-ttu-id="0c046-118">Uma estrutura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) que contém um tempo relacionado à experiência de um computador cliente.</span><span class="sxs-lookup"><span data-stu-id="0c046-118">A [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that contains a time related to a client machine's probation.</span></span>

</dd> <dt>

<span data-ttu-id="0c046-119">**ProtocolMaxSize**</span><span class="sxs-lookup"><span data-stu-id="0c046-119">**ProtocolMaxSize**</span></span>
</dt> <dd>

<span data-ttu-id="0c046-120">Um valor que especifica o intervalo de valores possíveis para o tamanho máximo, em bytes, de um pacote [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) , conforme definido pelo intervalo ([**minProtocolMaxSize, maxProtocolMaxSize**](nap-type-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="0c046-120">A value that specifies the range of possible values for the maximum size, in bytes, of an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet as defined by range([**minProtocolMaxSize, maxProtocolMaxSize**](nap-type-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="0c046-121">**NapComponentId**</span><span class="sxs-lookup"><span data-stu-id="0c046-121">**NapComponentId**</span></span>
</dt> <dd>

<span data-ttu-id="0c046-122">Um identificador exclusivo de 4 bytes usado por SHAs, SHVs e clientes de imposição para se identificar.</span><span class="sxs-lookup"><span data-stu-id="0c046-122">A unique 4-byte identifier used by SHAs, SHVs and enforcement clients to identify themselves.</span></span> <span data-ttu-id="0c046-123">Os três primeiros bytes são o código de SMI atribuído pela IETF do fornecedor e o último byte identifica o próprio componente.</span><span class="sxs-lookup"><span data-stu-id="0c046-123">The first three bytes are the IETF-assigned SMI code of the vendor, and the last byte identifies the component itself.</span></span>

</dd> <dt>

<span data-ttu-id="0c046-124">**SystemHealthEntityId**</span><span class="sxs-lookup"><span data-stu-id="0c046-124">**SystemHealthEntityId**</span></span>
</dt> <dd>

<span data-ttu-id="0c046-125">Um valor de **NapComponentId** usado para identificar pares de Sha/SHV.</span><span class="sxs-lookup"><span data-stu-id="0c046-125">A **NapComponentId** value used to identify SHA/SHV pairs.</span></span>

</dd> <dt>

<span data-ttu-id="0c046-126">**EnforcementEntityId**</span><span class="sxs-lookup"><span data-stu-id="0c046-126">**EnforcementEntityId**</span></span>
</dt> <dd>

<span data-ttu-id="0c046-127">Um valor de **NapComponentId** usado para identificar clientes de imposição.</span><span class="sxs-lookup"><span data-stu-id="0c046-127">A **NapComponentId** value used to identify enforcement clients.</span></span>

</dd> <dt>

<span data-ttu-id="0c046-128">**SystemHealthEntityCount**</span><span class="sxs-lookup"><span data-stu-id="0c046-128">**SystemHealthEntityCount**</span></span>
</dt> <dd>

<span data-ttu-id="0c046-129">Um valor que especifica o número de SHAs registrados no sistema NAP no intervalo de 0 (zero) a [**maxSystemHealthEntityCount**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0c046-129">A value that specifies the number of registered SHAs in the NAP system in the range 0 (zero) to [**maxSystemHealthEntityCount**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c046-130">**EnforcementEntityCount**</span><span class="sxs-lookup"><span data-stu-id="0c046-130">**EnforcementEntityCount**</span></span>
</dt> <dd>

<span data-ttu-id="0c046-131">Um valor que especifica o número de clientes de imposição no sistema NAP no intervalo de 0 (zero) a [**maxEnforcerCount**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0c046-131">A value that specifies the number of enforcement clients in the NAP system in the range 0 (zero) to [**maxEnforcerCount**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c046-132">**StringCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="0c046-132">**StringCorrelationId**</span></span>
</dt> <dd>

<span data-ttu-id="0c046-133">A versão de [**contado**](/windows/win32/api/naptypes/ns-naptypes-countedstring) de uma estrutura [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) usada para emparelhar [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) com **SoHResponses**.</span><span class="sxs-lookup"><span data-stu-id="0c046-133">The [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) version of a [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) structure used to pair [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) to **SoHResponses**.</span></span>

</dd> <dt>

<span data-ttu-id="0c046-134">**ConnectionId**</span><span class="sxs-lookup"><span data-stu-id="0c046-134">**ConnectionId**</span></span>
</dt> <dd>

<span data-ttu-id="0c046-135">Um GUID (identificador global exclusivo) exclusivo usado para identificar conexões NAP mantidas por clientes de imposição.</span><span class="sxs-lookup"><span data-stu-id="0c046-135">A unique Globally Unique Identifier (GUID) used to identify a NAP connections maintained by enforcement clients.</span></span>

</dd> <dt>

<span data-ttu-id="0c046-136">**Percentual**</span><span class="sxs-lookup"><span data-stu-id="0c046-136">**Percentage**</span></span>
</dt> <dd>

<span data-ttu-id="0c046-137">Um valor que contém a porcentagem entre 0 (zero) e 100 de correções concluídas</span><span class="sxs-lookup"><span data-stu-id="0c046-137">A value that contains the percentage between 0 (zero) and 100 of remediation that is complete</span></span>

</dd> <dt>

<span data-ttu-id="0c046-138">**MessageId**</span><span class="sxs-lookup"><span data-stu-id="0c046-138">**MessageId**</span></span>
</dt> <dd>

<span data-ttu-id="0c046-139">Um valor exclusivo usado para identificar mensagens do sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="0c046-139">A unique value used to identify NAP system messages.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0c046-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c046-140">Requirements</span></span>



| <span data-ttu-id="0c046-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c046-141">Requirement</span></span> | <span data-ttu-id="0c046-142">Valor</span><span class="sxs-lookup"><span data-stu-id="0c046-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c046-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c046-143">Minimum supported client</span></span><br/> | <span data-ttu-id="0c046-144">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0c046-144">Windows Vista \[desktop apps only\]</span></span><br/>                                                                                                                      |
| <span data-ttu-id="0c046-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c046-145">Minimum supported server</span></span><br/> | <span data-ttu-id="0c046-146">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0c046-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                                |
| <span data-ttu-id="0c046-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0c046-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c046-148"><dt>NapTypes. h; </dt> <dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c046-148"><dt>NapTypes.h; </dt> <dt>NapEnforcementClient.h</dt></span></span> </dl> |



 

