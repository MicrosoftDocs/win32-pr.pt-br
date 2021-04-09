---
title: Classe MicrosoftDNS_MDType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro de agente de email para o domínio (MD).
ms.assetid: 11242372-65fe-44ee-845b-2430aec59127
keywords:
- MicrosoftDNS_MDType de classe de DNS
- MicrosoftDNS_MDType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_MDType
- MicrosoftDNS_MDType.CreateInstanceFromPropertyData
- MicrosoftDNS_MDType.Modify
- MicrosoftDNS_MDType.MDHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7641fda7a223fed7c2dc9229c5a3449c575e84ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824390"
---
# <a name="microsoftdns_mdtype-class"></a><span data-ttu-id="dc9ad-105">\_Classe MicrosoftDNS MDType</span><span class="sxs-lookup"><span data-stu-id="dc9ad-105">MicrosoftDNS\_MDType class</span></span>

<span data-ttu-id="dc9ad-106">A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro de agente de email para o domínio (MD).</span><span class="sxs-lookup"><span data-stu-id="dc9ad-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Agent for Domain (MD) record.</span></span>

<span data-ttu-id="dc9ad-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="dc9ad-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc9ad-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dc9ad-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MDType : MicrosoftDNS_ResourceRecord
{
  string MDHost;
};
```

## <a name="members"></a><span data-ttu-id="dc9ad-109">Membros</span><span class="sxs-lookup"><span data-stu-id="dc9ad-109">Members</span></span>

<span data-ttu-id="dc9ad-110">A classe **MicrosoftDNS \_ MDType** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="dc9ad-110">The **MicrosoftDNS\_MDType** class has these types of members:</span></span>

-   [<span data-ttu-id="dc9ad-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="dc9ad-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="dc9ad-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dc9ad-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dc9ad-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="dc9ad-113">Methods</span></span>

<span data-ttu-id="dc9ad-114">A classe **MicrosoftDNS \_ MDType** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="dc9ad-114">The **MicrosoftDNS\_MDType** class has these methods.</span></span>



| <span data-ttu-id="dc9ad-115">Método</span><span class="sxs-lookup"><span data-stu-id="dc9ad-115">Method</span></span>                             | <span data-ttu-id="dc9ad-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="dc9ad-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc9ad-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="dc9ad-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="dc9ad-118">Instancia um registro de recurso de DNS MD com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário do domínio, a classe (padrão = IN), o valor de vida útil e o host do agente de email.</span><span class="sxs-lookup"><span data-stu-id="dc9ad-118">Instantiates a DNS MD Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the domain, class (default = IN), time-to-live value and the host of the mail agent.</span></span> <span data-ttu-id="dc9ad-119">Ele retorna uma referência ao novo objeto como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="dc9ad-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="dc9ad-120">Qualificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="dc9ad-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="dc9ad-121">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="dc9ad-121">**Modify**</span></span>                         | <span data-ttu-id="dc9ad-122">Atualiza o TTL e o host MD para os valores especificados como os parâmetros de entrada deste método.</span><span class="sxs-lookup"><span data-stu-id="dc9ad-122">Updates the TTL and MD host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="dc9ad-123">Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado.</span><span class="sxs-lookup"><span data-stu-id="dc9ad-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="dc9ad-124">O método retorna uma referência ao objeto modificado como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="dc9ad-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="dc9ad-125">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="dc9ad-125">Qualifiers: Implemented</span></span><br/>                                 |



 

### <a name="properties"></a><span data-ttu-id="dc9ad-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dc9ad-126">Properties</span></span>

<span data-ttu-id="dc9ad-127">A classe **MicrosoftDNS \_ MDType** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="dc9ad-127">The **MicrosoftDNS\_MDType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dc9ad-128">**MDHost**</span><span class="sxs-lookup"><span data-stu-id="dc9ad-128">**MDHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc9ad-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dc9ad-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc9ad-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dc9ad-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc9ad-131">FQDN que especifica um host com um agente de email capaz de entregar email para o domínio especificado.</span><span class="sxs-lookup"><span data-stu-id="dc9ad-131">FQDN that specifies a host with a mail agent capable of delivering mail for the specified domain.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc9ad-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc9ad-132">Requirements</span></span>



| <span data-ttu-id="dc9ad-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc9ad-133">Requirement</span></span> | <span data-ttu-id="dc9ad-134">Valor</span><span class="sxs-lookup"><span data-stu-id="dc9ad-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc9ad-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc9ad-135">Minimum supported client</span></span><br/> | <span data-ttu-id="dc9ad-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="dc9ad-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="dc9ad-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc9ad-137">Minimum supported server</span></span><br/> | <span data-ttu-id="dc9ad-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dc9ad-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dc9ad-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="dc9ad-139">Namespace</span></span><br/>                | <span data-ttu-id="dc9ad-140">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="dc9ad-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="dc9ad-141">MOF</span><span class="sxs-lookup"><span data-stu-id="dc9ad-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc9ad-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc9ad-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc9ad-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc9ad-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc9ad-144">**Método CreateInstanceFromPropertyData da \_ classe MDType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="dc9ad-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MDType Class**</span></span>](microsoftdns-mdtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="dc9ad-145">**Método Modify da classe MicrosoftDNS \_ MDType**</span><span class="sxs-lookup"><span data-stu-id="dc9ad-145">**Modify Method of the MicrosoftDNS\_MDType Class**</span></span>](microsoftdns-mdtype-modify.md)
</dt> <dt>

[<span data-ttu-id="dc9ad-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="dc9ad-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





