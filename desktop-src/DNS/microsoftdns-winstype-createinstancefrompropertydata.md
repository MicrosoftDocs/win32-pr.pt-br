---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_WINSType
description: O método CreateInstanceFromPropertyData instancia um registro de recurso WINS (serviço de cadastramento na Internet do Windows).
ms.assetid: 0b41a6a5-0bb1-467b-9089-2c721d521887
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_WINSType
- MicrosoftDNS_WINSType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf584bd34f59391a49fd5f7ec13cb49e18ef68fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644836"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_winstype-class"></a><span data-ttu-id="9651f-106">Método CreateInstanceFromPropertyData da \_ classe winstype MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="9651f-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_WINSType class</span></span>

<span data-ttu-id="9651f-107">O método **CreateInstanceFromPropertyData** instancia um registro de recurso WINS (serviço de cadastramento na Internet do Windows).</span><span class="sxs-lookup"><span data-stu-id="9651f-107">The **CreateInstanceFromPropertyData** method instantiates a Windows Internet Name Service (WINS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="9651f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9651f-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           uint32                MappingFlag,
  [in]           uint32                LookupTimeout,
  [in]           uint32                CacheTimeout,
  [in]           string                WinsServers,
  [out, ref]     MicrosoftDNS_WINSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="9651f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9651f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9651f-110">*DnsServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9651f-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9651f-111">FQDN ou endereço IP do servidor DNS que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="9651f-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="9651f-112">*ContainerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9651f-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9651f-113">Nome do contêiner para a zona, o cache ou a instância de RootHints que contém esse RR.</span><span class="sxs-lookup"><span data-stu-id="9651f-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="9651f-114">*OwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9651f-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9651f-115">Nome do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="9651f-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="9651f-116">*RecordClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9651f-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9651f-117">Classe do RR.</span><span class="sxs-lookup"><span data-stu-id="9651f-117">Class of the RR.</span></span> <span data-ttu-id="9651f-118">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="9651f-118">Default value is 1.</span></span> <span data-ttu-id="9651f-119">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="9651f-119">The following values are valid.</span></span>



| <span data-ttu-id="9651f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9651f-120">Value</span></span>                                                                                                | <span data-ttu-id="9651f-121">Significado</span><span class="sxs-lookup"><span data-stu-id="9651f-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="9651f-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="9651f-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="9651f-123">NO (Internet)</span><span class="sxs-lookup"><span data-stu-id="9651f-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="9651f-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="9651f-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="9651f-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="9651f-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="9651f-126"><dt>**Beta**</dt></span><span class="sxs-lookup"><span data-stu-id="9651f-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="9651f-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="9651f-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="9651f-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="9651f-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="9651f-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="9651f-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="9651f-130">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9651f-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9651f-131">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="9651f-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="9651f-132">*MappingFlag* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9651f-132">*MappingFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9651f-133">Sinalizador de mapeamento WINS que especifica se o registro deve ser incluído na replicação de zona.</span><span class="sxs-lookup"><span data-stu-id="9651f-133">WINS mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="9651f-134">Ele pode ter apenas dois valores: 0x80000000 e 0x00010000 correspondentes aos sinalizadores de replicação e sem replicação (registro local), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9651f-134">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span> <span data-ttu-id="9651f-135">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="9651f-135">The following values are valid.</span></span>



| <span data-ttu-id="9651f-136">Valor</span><span class="sxs-lookup"><span data-stu-id="9651f-136">Value</span></span>                                                                                                                                               | <span data-ttu-id="9651f-137">Significado</span><span class="sxs-lookup"><span data-stu-id="9651f-137">Meaning</span></span>                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <span data-ttu-id="9651f-138"><dt>**0x80000000**</dt></span><span class="sxs-lookup"><span data-stu-id="9651f-138"><dt>**0x80000000**</dt></span></span> </dl> | <span data-ttu-id="9651f-139">Sinalizador de replicação</span><span class="sxs-lookup"><span data-stu-id="9651f-139">Replication flag</span></span><br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <span data-ttu-id="9651f-140"><dt>**0x00010000**</dt></span><span class="sxs-lookup"><span data-stu-id="9651f-140"><dt>**0x00010000**</dt></span></span> </dl> | <span data-ttu-id="9651f-141">Sinalizador sem replicação (registro local)</span><span class="sxs-lookup"><span data-stu-id="9651f-141">No-replication (local record) flag</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9651f-142">*LookupTimeout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9651f-142">*LookupTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9651f-143">Tempo, em segundos, que um servidor DNS tenta resolução usando a pesquisa WINS.</span><span class="sxs-lookup"><span data-stu-id="9651f-143">Time, in seconds, that a DNS Server attempts resolution using WINS Look up.</span></span>

</dd> <dt>

<span data-ttu-id="9651f-144">*CacheTimeout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9651f-144">*CacheTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9651f-145">Tempo, em segundos, que um servidor DNS que usa a pesquisa WINS pode armazenar em cache a resposta do servidor WINS.</span><span class="sxs-lookup"><span data-stu-id="9651f-145">Time, in seconds, that a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="9651f-146">*WinsServers* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9651f-146">*WinsServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9651f-147">Lista de endereços IP separados por vírgulas de servidores WINS usados na pesquisa WINS.</span><span class="sxs-lookup"><span data-stu-id="9651f-147">List of comma-separated IP addresses of WINS servers used in WINS Look ups.</span></span>

</dd> <dt>

<span data-ttu-id="9651f-148">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="9651f-148">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="9651f-149">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="9651f-149">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9651f-150">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9651f-150">Return value</span></span>

<span data-ttu-id="9651f-151">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9651f-151">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9651f-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9651f-152">Requirements</span></span>



| <span data-ttu-id="9651f-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="9651f-153">Requirement</span></span> | <span data-ttu-id="9651f-154">Valor</span><span class="sxs-lookup"><span data-stu-id="9651f-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9651f-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9651f-155">Minimum supported client</span></span><br/> | <span data-ttu-id="9651f-156">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9651f-156">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9651f-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9651f-157">Minimum supported server</span></span><br/> | <span data-ttu-id="9651f-158">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9651f-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9651f-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="9651f-159">Namespace</span></span><br/>                | <span data-ttu-id="9651f-160">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="9651f-160">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="9651f-161">MOF</span><span class="sxs-lookup"><span data-stu-id="9651f-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9651f-162"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9651f-162"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9651f-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="9651f-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9651f-164">**MicrosoftDNS \_ winstype**</span><span class="sxs-lookup"><span data-stu-id="9651f-164">**MicrosoftDNS\_WINSType**</span></span>](microsoftdns-winstype.md)
</dt> <dt>

[<span data-ttu-id="9651f-165">**Método Modify da \_ classe winstype MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="9651f-165">**Modify Method of the MicrosoftDNS\_WINSType Class**</span></span>](microsoftdns-winstype-modify.md)
</dt> <dt>

[<span data-ttu-id="9651f-166">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="9651f-166">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





