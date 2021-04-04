---
title: Classe MicrosoftDNS_WINSType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro WINS (serviço de cadastramento na Internet do Windows).
ms.assetid: 8f891d80-ee4d-4641-8a6c-159c78e5cf86
keywords:
- MicrosoftDNS_WINSType de classe de DNS
- MicrosoftDNS_WINSType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType
- MicrosoftDNS_WINSType.CreateInstanceFromPropertyData
- MicrosoftDNS_WINSType.Modify
- MicrosoftDNS_WINSType.MappingFlag
- MicrosoftDNS_WINSType.LookupTimeout
- MicrosoftDNS_WINSType.CacheTimeout
- MicrosoftDNS_WINSType.WinsServers
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce23132073305142948518327ea5b6c7e46f1289
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824554"
---
# <a name="microsoftdns_winstype-class"></a><span data-ttu-id="8dd6b-105">\_Classe winstype MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="8dd6b-105">MicrosoftDNS\_WINSType class</span></span>

<span data-ttu-id="8dd6b-106">A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro WINS (serviço de cadastramento na Internet do Windows).</span><span class="sxs-lookup"><span data-stu-id="8dd6b-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Windows Internet Name Service (WINS) record.</span></span>

<span data-ttu-id="8dd6b-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="8dd6b-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dd6b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8dd6b-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_WINSType : MicrosoftDNS_ResourceRecord
{
  uint32 MappingFlag;
  uint32 LookupTimeout;
  uint32 CacheTimeout;
  string WinsServers;
};
```

## <a name="members"></a><span data-ttu-id="8dd6b-109">Membros</span><span class="sxs-lookup"><span data-stu-id="8dd6b-109">Members</span></span>

<span data-ttu-id="8dd6b-110">A **classe \_ winstype MicrosoftDNS** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8dd6b-110">The **MicrosoftDNS\_WINSType** class has these types of members:</span></span>

-   [<span data-ttu-id="8dd6b-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="8dd6b-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="8dd6b-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8dd6b-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8dd6b-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="8dd6b-113">Methods</span></span>

<span data-ttu-id="8dd6b-114">A **classe \_ winstype MicrosoftDNS** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="8dd6b-114">The **MicrosoftDNS\_WINSType** class has these methods.</span></span>



| <span data-ttu-id="8dd6b-115">Método</span><span class="sxs-lookup"><span data-stu-id="8dd6b-115">Method</span></span>                             | <span data-ttu-id="8dd6b-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="8dd6b-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dd6b-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="8dd6b-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="8dd6b-118">Cria uma instância de um tipo WINS de RR com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário, a classe (padrão = IN), o valor de vida útil e o sinalizador de mapeamento do WINS, o tempo limite de pesquisa, o tempo limite do cache e a lista de endereços IP para pesquisa.</span><span class="sxs-lookup"><span data-stu-id="8dd6b-118">Instantiates a WINS Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, look-up time out, cache time out and list of IP addresses for look up.</span></span> <span data-ttu-id="8dd6b-119">Ele retorna uma referência ao novo objeto como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="8dd6b-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="8dd6b-120">Qualificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="8dd6b-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="8dd6b-121">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="8dd6b-121">**Modify**</span></span>                         | <span data-ttu-id="8dd6b-122">Atualiza o TTL, o sinalizador de mapeamento, o tempo limite de pesquisa, o tempo limite de cache e os servidores WINS para os valores especificados como os parâmetros de entrada deste método.</span><span class="sxs-lookup"><span data-stu-id="8dd6b-122">Updates the TTL, Mapping Flag, Look-up Time out, Cache Time out and Wins Servers to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="8dd6b-123">Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado.</span><span class="sxs-lookup"><span data-stu-id="8dd6b-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="8dd6b-124">O método retorna uma referência ao objeto modificado como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="8dd6b-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="8dd6b-125">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="8dd6b-125">Qualifiers: Implemented</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="8dd6b-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8dd6b-126">Properties</span></span>

<span data-ttu-id="8dd6b-127">A **classe \_ winstype MicrosoftDNS** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8dd6b-127">The **MicrosoftDNS\_WINSType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8dd6b-128">**CacheTimeout**</span><span class="sxs-lookup"><span data-stu-id="8dd6b-128">**CacheTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd6b-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8dd6b-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dd6b-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8dd6b-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8dd6b-131">Tempo, em segundos, que um servidor DNS que usa a pesquisa WINS pode armazenar em cache a resposta do servidor WINS.</span><span class="sxs-lookup"><span data-stu-id="8dd6b-131">Time, in seconds, that a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="8dd6b-132">**LookupTimeout**</span><span class="sxs-lookup"><span data-stu-id="8dd6b-132">**LookupTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd6b-133">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8dd6b-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dd6b-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8dd6b-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8dd6b-135">Tempo, em segundos, que um servidor DNS tenta resolução usando a pesquisa WINS.</span><span class="sxs-lookup"><span data-stu-id="8dd6b-135">Time, in seconds, that a DNS Server attempts resolution using WINS Look up.</span></span>

</dd> <dt>

<span data-ttu-id="8dd6b-136">**MappingFlag**</span><span class="sxs-lookup"><span data-stu-id="8dd6b-136">**MappingFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd6b-137">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8dd6b-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dd6b-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8dd6b-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8dd6b-139">Sinalizador de mapeamento WINS que especifica se o registro deve ser incluído na replicação de zona.</span><span class="sxs-lookup"><span data-stu-id="8dd6b-139">WINS mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="8dd6b-140">Ele pode ter apenas dois valores: 0x80000000 e 0x00010000 correspondentes aos sinalizadores de replicação e sem replicação (registro local), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="8dd6b-140">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span> <span data-ttu-id="8dd6b-141">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="8dd6b-141">The following values are valid.</span></span>



| <span data-ttu-id="8dd6b-142">Valor</span><span class="sxs-lookup"><span data-stu-id="8dd6b-142">Value</span></span>                                                                                                                                               | <span data-ttu-id="8dd6b-143">Significado</span><span class="sxs-lookup"><span data-stu-id="8dd6b-143">Meaning</span></span>                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <span data-ttu-id="8dd6b-144"><dt>**0x80000000**</dt></span><span class="sxs-lookup"><span data-stu-id="8dd6b-144"><dt>**0x80000000**</dt></span></span> </dl> | <span data-ttu-id="8dd6b-145">Sinalizador de replicação</span><span class="sxs-lookup"><span data-stu-id="8dd6b-145">Replication flag</span></span><br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <span data-ttu-id="8dd6b-146"><dt>**0x00010000**</dt></span><span class="sxs-lookup"><span data-stu-id="8dd6b-146"><dt>**0x00010000**</dt></span></span> </dl> | <span data-ttu-id="8dd6b-147">Sinalizador sem replicação (registro local)</span><span class="sxs-lookup"><span data-stu-id="8dd6b-147">No-replication (local record) flag</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8dd6b-148">**WinsServers**</span><span class="sxs-lookup"><span data-stu-id="8dd6b-148">**WinsServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dd6b-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8dd6b-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dd6b-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8dd6b-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8dd6b-151">Lista de endereços IP separados por vírgulas de servidores WINS usados na pesquisa WINS.</span><span class="sxs-lookup"><span data-stu-id="8dd6b-151">List of comma-separated IP addresses of WINS servers used in WINS Look ups.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8dd6b-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8dd6b-152">Requirements</span></span>



| <span data-ttu-id="8dd6b-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="8dd6b-153">Requirement</span></span> | <span data-ttu-id="8dd6b-154">Valor</span><span class="sxs-lookup"><span data-stu-id="8dd6b-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8dd6b-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8dd6b-155">Minimum supported client</span></span><br/> | <span data-ttu-id="8dd6b-156">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8dd6b-156">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8dd6b-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8dd6b-157">Minimum supported server</span></span><br/> | <span data-ttu-id="8dd6b-158">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8dd6b-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8dd6b-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="8dd6b-159">Namespace</span></span><br/>                | <span data-ttu-id="8dd6b-160">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="8dd6b-160">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="8dd6b-161">MOF</span><span class="sxs-lookup"><span data-stu-id="8dd6b-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8dd6b-162"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8dd6b-162"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8dd6b-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="8dd6b-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dd6b-164">**Método CreateInstanceFromPropertyData da \_ classe winstype MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="8dd6b-164">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WINSType Class**</span></span>](microsoftdns-winstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="8dd6b-165">**Método Modify da \_ classe winstype MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="8dd6b-165">**Modify Method of the MicrosoftDNS\_WINSType Class**</span></span>](microsoftdns-winstype-modify.md)
</dt> <dt>

[<span data-ttu-id="8dd6b-166">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="8dd6b-166">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





