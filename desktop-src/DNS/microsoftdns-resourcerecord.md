---
title: Classe MicrosoftDNS_ResourceRecord
description: A \_ classe MicrosoftDNS ResourceRecord representa as propriedades gerais de um RR DNS. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 84d6d106-fcc9-44ae-8db2-181c60489aec
keywords:
- MicrosoftDNS_ResourceRecord de classe de DNS
- MicrosoftDNS_ResourceRecord de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
- MicrosoftDNS_ResourceRecord.GetObjectByTextRepresentation
- MicrosoftDNS_ResourceRecord.DnsServerName
- MicrosoftDNS_ResourceRecord.ContainerName
- MicrosoftDNS_ResourceRecord.DomainName
- MicrosoftDNS_ResourceRecord.OwnerName
- MicrosoftDNS_ResourceRecord.RecordClass 1
- MicrosoftDNS_ResourceRecord.TTL
- MicrosoftDNS_ResourceRecord.TimeStamp
- MicrosoftDNS_ResourceRecord.RecordData
- MicrosoftDNS_ResourceRecord.TextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe546ceabb5590ccd4907448af5efd5e2d4fe2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918603"
---
# <a name="microsoftdns_resourcerecord-class"></a><span data-ttu-id="dbc00-105">\_Classe MicrosoftDNS ResourceRecord</span><span class="sxs-lookup"><span data-stu-id="dbc00-105">MicrosoftDNS\_ResourceRecord class</span></span>

<span data-ttu-id="dbc00-106">A classe **MicrosoftDNS \_ ResourceRecord** representa as propriedades gerais de um RR DNS.</span><span class="sxs-lookup"><span data-stu-id="dbc00-106">The **MicrosoftDNS\_ResourceRecord** class represents the general properties of a DNS RR.</span></span>

<span data-ttu-id="dbc00-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="dbc00-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbc00-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dbc00-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_ResourceRecord : CIM_LogicalElement
{
  string DnsServerName;
  string ContainerName;
  string DomainName;
  string OwnerName;
  uint16 RecordClass=1;
  uint32 TTL;
  uint32 TimeStamp;
  string RecordData;
  string TextRepresentation;
};
```

## <a name="members"></a><span data-ttu-id="dbc00-109">Membros</span><span class="sxs-lookup"><span data-stu-id="dbc00-109">Members</span></span>

<span data-ttu-id="dbc00-110">A classe **MicrosoftDNS \_ ResourceRecord** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="dbc00-110">The **MicrosoftDNS\_ResourceRecord** class has these types of members:</span></span>

-   [<span data-ttu-id="dbc00-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="dbc00-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="dbc00-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dbc00-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dbc00-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="dbc00-113">Methods</span></span>

<span data-ttu-id="dbc00-114">A classe **MicrosoftDNS \_ ResourceRecord** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="dbc00-114">The **MicrosoftDNS\_ResourceRecord** class has these methods.</span></span>



| <span data-ttu-id="dbc00-115">Método</span><span class="sxs-lookup"><span data-stu-id="dbc00-115">Method</span></span>                                   | <span data-ttu-id="dbc00-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="dbc00-116">Description</span></span>                                                                                                                                                                                                                                                            |
|:-----------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbc00-117">**CreateInstanceFromTextRepresentation**</span><span class="sxs-lookup"><span data-stu-id="dbc00-117">**CreateInstanceFromTextRepresentation**</span></span> | <span data-ttu-id="dbc00-118">Analisa o RR na cadeia de caracteres textrepresentation e com o servidor DNS de entrada e os nomes de contêiner, define e instancia um objeto ResourceRecord.</span><span class="sxs-lookup"><span data-stu-id="dbc00-118">Parses the RR in the TextRepresentation string, and with the input DNS Server and Container Names, defines, and instantiates a ResourceRecord object.</span></span> <span data-ttu-id="dbc00-119">O método retorna uma referência ao novo objeto como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="dbc00-119">The method returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="dbc00-120">Qualificadores: nenhum</span><span class="sxs-lookup"><span data-stu-id="dbc00-120">Qualifiers: None</span></span><br/> |
| <span data-ttu-id="dbc00-121">**GetObjectByTextRepresentation**</span><span class="sxs-lookup"><span data-stu-id="dbc00-121">**GetObjectByTextRepresentation**</span></span>        | <span data-ttu-id="dbc00-122">Recupera uma instância existente da subclasse MicrosoftDns \_ ResourceRecord, representada pela cadeia de caracteres Textrepresentation, junto com o servidor DNS e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="dbc00-122">Retrieves an existing instance of the MicrosoftDns\_ResourceRecord subclass, represented by the TextRepresentation string along with the DNS Server and Container Name.</span></span> <br/> <span data-ttu-id="dbc00-123">Qualificadores: nenhum</span><span class="sxs-lookup"><span data-stu-id="dbc00-123">Qualifiers: None</span></span><br/>                                                        |



 

### <a name="properties"></a><span data-ttu-id="dbc00-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dbc00-124">Properties</span></span>

<span data-ttu-id="dbc00-125">A classe **MicrosoftDNS \_ ResourceRecord** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="dbc00-125">The **MicrosoftDNS\_ResourceRecord** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dbc00-126">**ContainerName**</span><span class="sxs-lookup"><span data-stu-id="dbc00-126">**ContainerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbc00-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dbc00-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbc00-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbc00-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbc00-129">Indica o nome do contêiner para a zona, o cache ou a instância de RootHints que contém o RR.</span><span class="sxs-lookup"><span data-stu-id="dbc00-129">Indicates the name of the Container for the Zone, Cache, or RootHints instance that contains the RR.</span></span>

</dd> <dt>

<span data-ttu-id="dbc00-130">**DnsServerName**</span><span class="sxs-lookup"><span data-stu-id="dbc00-130">**DnsServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbc00-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dbc00-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbc00-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbc00-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbc00-133">Indica o FQDN ou o endereço IP do servidor DNS que contém o RR.</span><span class="sxs-lookup"><span data-stu-id="dbc00-133">Indicates the FQDN or IP address of the DNS Server that contains the RR.</span></span>

</dd> <dt>

<span data-ttu-id="dbc00-134">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="dbc00-134">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbc00-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dbc00-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbc00-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbc00-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbc00-137">Representa o FQDN do domínio que contém o RR.</span><span class="sxs-lookup"><span data-stu-id="dbc00-137">Represents the FQDN of the Domain that contains the RR.</span></span> <span data-ttu-id="dbc00-138">Essa propriedade pode conter as cadeias de caracteres \\ .. Cache \\ ou \\ .. RootHints \\ se o cache interno ou RootHints contiver o RR, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="dbc00-138">This property may contain the strings \\..Cache\\ or \\..RootHints\\ if the internal cache or RootHints contain the RR, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="dbc00-139">**OwnerName**</span><span class="sxs-lookup"><span data-stu-id="dbc00-139">**OwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbc00-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dbc00-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbc00-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbc00-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbc00-142">Nome do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="dbc00-142">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="dbc00-143">**RecordClass = 1**</span><span class="sxs-lookup"><span data-stu-id="dbc00-143">**RecordClass=1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbc00-144">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbc00-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbc00-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbc00-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbc00-146">\* \* Windows Server 2003: \* \*</span><span class="sxs-lookup"><span data-stu-id="dbc00-146">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="dbc00-147">Essa cadeia de caracteres representa a classe do registro de recurso.</span><span class="sxs-lookup"><span data-stu-id="dbc00-147">This string represents the class of the Resource Record.</span></span> <span data-ttu-id="dbc00-148">Os valores válidos incluem:</span><span class="sxs-lookup"><span data-stu-id="dbc00-148">Valid values include:</span></span>

<span data-ttu-id="dbc00-149">1: IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="dbc00-149">1: IN (Internet)</span></span>

<span data-ttu-id="dbc00-150">2: CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="dbc00-150">2: CS (CSNET)</span></span>

<span data-ttu-id="dbc00-151">3: CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="dbc00-151">3: CH (CHAOS)</span></span>

<span data-ttu-id="dbc00-152">4: HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="dbc00-152">4: HS (Hesiod)</span></span>

</dd> <dt>

<span data-ttu-id="dbc00-153">**RecordData**</span><span class="sxs-lookup"><span data-stu-id="dbc00-153">**RecordData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbc00-154">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dbc00-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbc00-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbc00-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbc00-156">Dados de registro de recurso.</span><span class="sxs-lookup"><span data-stu-id="dbc00-156">Resource record data.</span></span>

</dd> <dt>

<span data-ttu-id="dbc00-157">**Textrepresentation**</span><span class="sxs-lookup"><span data-stu-id="dbc00-157">**TextRepresentation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbc00-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dbc00-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbc00-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbc00-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbc00-160">Representação de texto de todo o RR.</span><span class="sxs-lookup"><span data-stu-id="dbc00-160">Text representation of the entire RR.</span></span>

</dd> <dt>

<span data-ttu-id="dbc00-161">**Estampa**</span><span class="sxs-lookup"><span data-stu-id="dbc00-161">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbc00-162">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dbc00-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dbc00-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbc00-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbc00-164">Hora em que o RR foi atualizado pela última vez, expresso em horas decorridas desde 1º de janeiro de 1601, Greenwich Mean Time (GMT).</span><span class="sxs-lookup"><span data-stu-id="dbc00-164">Time at which the RR was last refreshed, expressed in elapsed hours since January 1, 1601, Greenwich Mean Time (GMT).</span></span>

</dd> <dt>

<span data-ttu-id="dbc00-165">**TTL**</span><span class="sxs-lookup"><span data-stu-id="dbc00-165">**TTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbc00-166">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dbc00-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dbc00-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dbc00-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbc00-168">Tempo, em segundos, que o RR pode ser armazenado em cache por um [*resolvedor*](r-gly.md)de DNS.</span><span class="sxs-lookup"><span data-stu-id="dbc00-168">Time, in seconds, that the RR can be cached by a DNS [*resolver*](r-gly.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dbc00-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbc00-169">Requirements</span></span>



| <span data-ttu-id="dbc00-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbc00-170">Requirement</span></span> | <span data-ttu-id="dbc00-171">Valor</span><span class="sxs-lookup"><span data-stu-id="dbc00-171">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbc00-172">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbc00-172">Minimum supported client</span></span><br/> | <span data-ttu-id="dbc00-173">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="dbc00-173">None supported</span></span><br/>                                                              |
| <span data-ttu-id="dbc00-174">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbc00-174">Minimum supported server</span></span><br/> | <span data-ttu-id="dbc00-175">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dbc00-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dbc00-176">Namespace</span><span class="sxs-lookup"><span data-stu-id="dbc00-176">Namespace</span></span><br/>                | <span data-ttu-id="dbc00-177">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="dbc00-177">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="dbc00-178">MOF</span><span class="sxs-lookup"><span data-stu-id="dbc00-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dbc00-179"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dbc00-179"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbc00-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbc00-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbc00-181">**Método CreateInstanceFromTextRepresentation da \_ classe ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="dbc00-181">**CreateInstanceFromTextRepresentation Method of the MicrosoftDNS\_ResourceRecord Class**</span></span>](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> <dt>

[<span data-ttu-id="dbc00-182">**Método GetObjectByTextRepresentation da \_ classe ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="dbc00-182">**GetObjectByTextRepresentation Method of the MicrosoftDNS\_ResourceRecord Class**</span></span>](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





