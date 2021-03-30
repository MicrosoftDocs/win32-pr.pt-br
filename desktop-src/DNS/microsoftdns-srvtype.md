---
title: Classe MicrosoftDNS_SRVType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro de serviço (SRV).
ms.assetid: 4b36246d-4466-46d9-9267-180e43547ae6
keywords:
- MicrosoftDNS_SRVType de classe de DNS
- MicrosoftDNS_SRVType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType
- MicrosoftDNS_SRVType.CreateInstanceFromPropertyData
- MicrosoftDNS_SRVType.Modify
- MicrosoftDNS_SRVType.Priority
- MicrosoftDNS_SRVType.Weight
- MicrosoftDNS_SRVType.Port
- MicrosoftDNS_SRVType.SRVDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aea955cad281e9361b4fa1ca5b033a4ca0d39719
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455329"
---
# <a name="microsoftdns_srvtype-class"></a><span data-ttu-id="59621-105">\_Classe MicrosoftDNS SRVType</span><span class="sxs-lookup"><span data-stu-id="59621-105">MicrosoftDNS\_SRVType class</span></span>

<span data-ttu-id="59621-106">A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro de serviço (SRV).</span><span class="sxs-lookup"><span data-stu-id="59621-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Service (SRV) record.</span></span>

<span data-ttu-id="59621-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="59621-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="59621-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="59621-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_SRVType : MicrosoftDNS_ResourceRecord
{
  uint16 Priority;
  uint16 Weight;
  uint16 Port;
  string SRVDomainName;
};
```

## <a name="members"></a><span data-ttu-id="59621-109">Membros</span><span class="sxs-lookup"><span data-stu-id="59621-109">Members</span></span>

<span data-ttu-id="59621-110">A classe **MicrosoftDNS \_ SRVType** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="59621-110">The **MicrosoftDNS\_SRVType** class has these types of members:</span></span>

-   [<span data-ttu-id="59621-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="59621-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="59621-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="59621-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="59621-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="59621-113">Methods</span></span>

<span data-ttu-id="59621-114">A classe **MicrosoftDNS \_ SRVType** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="59621-114">The **MicrosoftDNS\_SRVType** class has these methods.</span></span>



| <span data-ttu-id="59621-115">Método</span><span class="sxs-lookup"><span data-stu-id="59621-115">Method</span></span>                             | <span data-ttu-id="59621-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="59621-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59621-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="59621-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="59621-118">Cria uma instância de um tipo SRV de RR com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário/destino, a classe (padrão = IN), o valor de vida útil e a prioridade, o peso, a porta e o nome de domínio do host de destino.</span><span class="sxs-lookup"><span data-stu-id="59621-118">Instantiates an SRV Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/target Name, class (default = IN), time-to-live value, and target host's priority, weight, port, and domain name.</span></span> <span data-ttu-id="59621-119">Ele retorna uma referência ao novo objeto como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="59621-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="59621-120">Qualificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="59621-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="59621-121">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="59621-121">**Modify**</span></span>                         | <span data-ttu-id="59621-122">Atualiza o TTL, a prioridade, o peso, a porta e o nome de domínio para os valores especificados como os parâmetros de entrada desse método.</span><span class="sxs-lookup"><span data-stu-id="59621-122">Updates the TTL, Priority, Weight, Port, and Domain Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="59621-123">Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado.</span><span class="sxs-lookup"><span data-stu-id="59621-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="59621-124">O método retorna uma referência ao objeto modificado como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="59621-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="59621-125">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="59621-125">Qualifiers: Implemented</span></span><br/>                  |



 

### <a name="properties"></a><span data-ttu-id="59621-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="59621-126">Properties</span></span>

<span data-ttu-id="59621-127">A classe **MicrosoftDNS \_ SRVType** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="59621-127">The **MicrosoftDNS\_SRVType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="59621-128">**Porta**</span><span class="sxs-lookup"><span data-stu-id="59621-128">**Port**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59621-129">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59621-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59621-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="59621-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59621-131">Porta usada no host de destino de um serviço de protocolo.</span><span class="sxs-lookup"><span data-stu-id="59621-131">Port used on the target host of a protocol service.</span></span>

</dd> <dt>

<span data-ttu-id="59621-132">**Prioridade**</span><span class="sxs-lookup"><span data-stu-id="59621-132">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59621-133">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59621-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59621-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="59621-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59621-135">Prioridade do host de destino especificado no nome do proprietário.</span><span class="sxs-lookup"><span data-stu-id="59621-135">Priority of the target host specified in the owner name.</span></span> <span data-ttu-id="59621-136">Números inferiores implicam prioridades mais altas.</span><span class="sxs-lookup"><span data-stu-id="59621-136">Lower numbers imply higher priorities.</span></span>

</dd> <dt>

<span data-ttu-id="59621-137">**SRVDomainName**</span><span class="sxs-lookup"><span data-stu-id="59621-137">**SRVDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59621-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="59621-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59621-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="59621-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59621-140">FQDN do host de destino.</span><span class="sxs-lookup"><span data-stu-id="59621-140">FQDN of the target host.</span></span> <span data-ttu-id="59621-141">Um destino de \\ . \\ significa que o serviço está decididamente não disponível neste domínio.</span><span class="sxs-lookup"><span data-stu-id="59621-141">A target of \\.\\ means that the service is decidedly not available at this domain.</span></span>

</dd> <dt>

<span data-ttu-id="59621-142">**Weight**</span><span class="sxs-lookup"><span data-stu-id="59621-142">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59621-143">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59621-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59621-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="59621-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59621-145">Peso do host de destino.</span><span class="sxs-lookup"><span data-stu-id="59621-145">Weight of the target host.</span></span> <span data-ttu-id="59621-146">Isso é útil ao selecionar entre os hosts que têm a mesma prioridade.</span><span class="sxs-lookup"><span data-stu-id="59621-146">This is useful when selecting among hosts that have the same priority.</span></span> <span data-ttu-id="59621-147">As chances de usar esse host devem ser proporcionais ao seu peso.</span><span class="sxs-lookup"><span data-stu-id="59621-147">The chances of using this host should be proportional to its weight.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="59621-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59621-148">Requirements</span></span>



| <span data-ttu-id="59621-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="59621-149">Requirement</span></span> | <span data-ttu-id="59621-150">Valor</span><span class="sxs-lookup"><span data-stu-id="59621-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="59621-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59621-151">Minimum supported client</span></span><br/> | <span data-ttu-id="59621-152">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="59621-152">None supported</span></span><br/>                                                              |
| <span data-ttu-id="59621-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59621-153">Minimum supported server</span></span><br/> | <span data-ttu-id="59621-154">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="59621-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="59621-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="59621-155">Namespace</span></span><br/>                | <span data-ttu-id="59621-156">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="59621-156">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="59621-157">MOF</span><span class="sxs-lookup"><span data-stu-id="59621-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59621-158"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="59621-158"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59621-159">Consulte também</span><span class="sxs-lookup"><span data-stu-id="59621-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59621-160">**Método CreateInstanceFromPropertyData da \_ classe SRVType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="59621-160">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_SRVType Class**</span></span>](microsoftdns-srvtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="59621-161">**Método Modify da classe MicrosoftDNS \_ SRVType**</span><span class="sxs-lookup"><span data-stu-id="59621-161">**Modify Method of the MicrosoftDNS\_SRVType Class**</span></span>](microsoftdns-srvtype-modify.md)
</dt> <dt>

[<span data-ttu-id="59621-162">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="59621-162">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





