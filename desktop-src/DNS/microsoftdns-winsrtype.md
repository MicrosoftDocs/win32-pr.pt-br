---
title: Classe MicrosoftDNS_WINSRType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro WINSR (pesquisa inversa WINS).
ms.assetid: e611dc63-838f-4a79-baca-febd27612111
keywords:
- MicrosoftDNS_WINSRType de classe de DNS
- MicrosoftDNS_WINSRType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType
- MicrosoftDNS_WINSRType.CreateInstanceFromPropertyData
- MicrosoftDNS_WINSRType.Modify
- MicrosoftDNS_WINSRType.MappingFlag
- MicrosoftDNS_WINSRType.LookupTimeout
- MicrosoftDNS_WINSRType.CacheTimeout
- MicrosoftDNS_WINSRType.ResultDomain
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9500c6a36a1c3a7cc243f1cbcfbc0edca6cecf2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369888"
---
# <a name="microsoftdns_winsrtype-class"></a><span data-ttu-id="54e4c-105">\_Classe MicrosoftDNS WINSRType</span><span class="sxs-lookup"><span data-stu-id="54e4c-105">MicrosoftDNS\_WINSRType class</span></span>

<span data-ttu-id="54e4c-106">A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro WINSR (pesquisa inversa WINS).</span><span class="sxs-lookup"><span data-stu-id="54e4c-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a WINS Reverse Look-up (WINSR) record.</span></span>

<span data-ttu-id="54e4c-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="54e4c-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="54e4c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="54e4c-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_WINSRType : MicrosoftDNS_ResourceRecord
{
  uint32 MappingFlag;
  uint32 LookupTimeout;
  uint32 CacheTimeout;
  string ResultDomain;
};
```

## <a name="members"></a><span data-ttu-id="54e4c-109">Membros</span><span class="sxs-lookup"><span data-stu-id="54e4c-109">Members</span></span>

<span data-ttu-id="54e4c-110">A classe **MicrosoftDNS \_ WINSRType** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="54e4c-110">The **MicrosoftDNS\_WINSRType** class has these types of members:</span></span>

-   [<span data-ttu-id="54e4c-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="54e4c-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="54e4c-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="54e4c-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="54e4c-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="54e4c-113">Methods</span></span>

<span data-ttu-id="54e4c-114">A classe **MicrosoftDNS \_ WINSRType** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="54e4c-114">The **MicrosoftDNS\_WINSRType** class has these methods.</span></span>



| <span data-ttu-id="54e4c-115">Método</span><span class="sxs-lookup"><span data-stu-id="54e4c-115">Method</span></span>                             | <span data-ttu-id="54e4c-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="54e4c-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                     |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54e4c-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="54e4c-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="54e4c-118">Cria uma instância de um tipo de RR com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário, a classe (padrão = IN), o valor de vida útil e o sinalizador de mapeamento do WINS, o tempo limite de pesquisa inversa, o tempo limite de cache do WINS e o nome de domínio a acrescentar</span><span class="sxs-lookup"><span data-stu-id="54e4c-118">Instantiates a WINSR Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, reverse look-up time out, WINS cache time out and domain name to append.</span></span> <span data-ttu-id="54e4c-119">Ele retorna uma referência ao novo objeto como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="54e4c-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="54e4c-120">Qualificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="54e4c-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="54e4c-121">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="54e4c-121">**Modify**</span></span>                         | <span data-ttu-id="54e4c-122">Atualiza o TTL, o sinalizador de mapeamento, o tempo limite de pesquisa, o tempo limite de cache e o domínio de resultado para os valores especificados como os parâmetros de entrada deste método.</span><span class="sxs-lookup"><span data-stu-id="54e4c-122">Updates the TTL, Mapping Flag, Look-up Time out, Cache Time out and Result Domain to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="54e4c-123">Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado.</span><span class="sxs-lookup"><span data-stu-id="54e4c-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="54e4c-124">O método retorna uma referência ao objeto modificado como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="54e4c-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="54e4c-125">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="54e4c-125">Qualifiers: Implemented</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="54e4c-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="54e4c-126">Properties</span></span>

<span data-ttu-id="54e4c-127">A classe **MicrosoftDNS \_ WINSRType** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="54e4c-127">The **MicrosoftDNS\_WINSRType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="54e4c-128">**CacheTimeout**</span><span class="sxs-lookup"><span data-stu-id="54e4c-128">**CacheTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54e4c-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="54e4c-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="54e4c-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="54e4c-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54e4c-131">Tempo, em segundos, que um servidor DNS que usa a pesquisa WINS pode armazenar em cache a resposta do servidor WINS.</span><span class="sxs-lookup"><span data-stu-id="54e4c-131">Time, in seconds, that a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="54e4c-132">**LookupTimeout**</span><span class="sxs-lookup"><span data-stu-id="54e4c-132">**LookupTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54e4c-133">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="54e4c-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="54e4c-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="54e4c-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54e4c-135">Tempo limite, em segundos, para um servidor DNS usando a pesquisa inversa do WINS.</span><span class="sxs-lookup"><span data-stu-id="54e4c-135">Time out, in seconds, for a DNS Server using WINS Reverse Look up.</span></span>

</dd> <dt>

<span data-ttu-id="54e4c-136">**MappingFlag**</span><span class="sxs-lookup"><span data-stu-id="54e4c-136">**MappingFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54e4c-137">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="54e4c-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="54e4c-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="54e4c-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54e4c-139">Sinalizador de mapeamento WINSr que especifica se o registro deve ser incluído na replicação de zona.</span><span class="sxs-lookup"><span data-stu-id="54e4c-139">WINSR mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="54e4c-140">Ele pode ter apenas dois valores: 0x80000000 e 0x00010000 correspondentes aos sinalizadores de replicação e sem replicação (registro local), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="54e4c-140">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="54e4c-141">**ResultDomain**</span><span class="sxs-lookup"><span data-stu-id="54e4c-141">**ResultDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54e4c-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="54e4c-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54e4c-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="54e4c-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54e4c-144">Nome de domínio a ser anexado aos nomes NetBIOS retornados.</span><span class="sxs-lookup"><span data-stu-id="54e4c-144">Domain name to append to returned NetBIOS names.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="54e4c-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54e4c-145">Requirements</span></span>



| <span data-ttu-id="54e4c-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="54e4c-146">Requirement</span></span> | <span data-ttu-id="54e4c-147">Valor</span><span class="sxs-lookup"><span data-stu-id="54e4c-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="54e4c-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54e4c-148">Minimum supported client</span></span><br/> | <span data-ttu-id="54e4c-149">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="54e4c-149">None supported</span></span><br/>                                                              |
| <span data-ttu-id="54e4c-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54e4c-150">Minimum supported server</span></span><br/> | <span data-ttu-id="54e4c-151">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="54e4c-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="54e4c-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="54e4c-152">Namespace</span></span><br/>                | <span data-ttu-id="54e4c-153">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="54e4c-153">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="54e4c-154">MOF</span><span class="sxs-lookup"><span data-stu-id="54e4c-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54e4c-155"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="54e4c-155"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54e4c-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="54e4c-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54e4c-157">**Método CreateInstanceFromPropertyData da \_ classe WINSRType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="54e4c-157">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WINSRType Class**</span></span>](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="54e4c-158">**Método Modify da classe MicrosoftDNS \_ WINSRType**</span><span class="sxs-lookup"><span data-stu-id="54e4c-158">**Modify Method of the MicrosoftDNS\_WINSRType Class**</span></span>](microsoftdns-winsrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="54e4c-159">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="54e4c-159">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





