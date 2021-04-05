---
title: Classe MicrosoftDNS_RTType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro de rota por meio de (RT).
ms.assetid: 986e2bbf-4f45-4611-906e-66079fda7f4c
keywords:
- MicrosoftDNS_RTType de classe de DNS
- MicrosoftDNS_RTType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType
- MicrosoftDNS_RTType.CreateInstanceFromPropertyData
- MicrosoftDNS_RTType.Modify
- MicrosoftDNS_RTType.Preference
- MicrosoftDNS_RTType.IntermediateHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d867185d8ce07a54a47eb5ea7591ec8d68a11059
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918600"
---
# <a name="microsoftdns_rttype-class"></a><span data-ttu-id="ab744-105">\_Classe MicrosoftDNS RTType</span><span class="sxs-lookup"><span data-stu-id="ab744-105">MicrosoftDNS\_RTType class</span></span>

<span data-ttu-id="ab744-106">A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro de rota por meio de (RT).</span><span class="sxs-lookup"><span data-stu-id="ab744-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Route Through (RT) record.</span></span>

<span data-ttu-id="ab744-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="ab744-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab744-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab744-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_RTType : MicrosoftDNS_ResourceRecord
{
  uint16 Preference;
  string IntermediateHost;
};
```

## <a name="members"></a><span data-ttu-id="ab744-109">Membros</span><span class="sxs-lookup"><span data-stu-id="ab744-109">Members</span></span>

<span data-ttu-id="ab744-110">A classe **MicrosoftDNS \_ RTType** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ab744-110">The **MicrosoftDNS\_RTType** class has these types of members:</span></span>

-   [<span data-ttu-id="ab744-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="ab744-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="ab744-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ab744-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ab744-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="ab744-113">Methods</span></span>

<span data-ttu-id="ab744-114">A classe **MicrosoftDNS \_ RTType** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ab744-114">The **MicrosoftDNS\_RTType** class has these methods.</span></span>



| <span data-ttu-id="ab744-115">Método</span><span class="sxs-lookup"><span data-stu-id="ab744-115">Method</span></span>                             | <span data-ttu-id="ab744-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab744-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab744-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="ab744-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="ab744-118">Cria uma instância de um tipo RT de RR com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do host/proprietário, a classe (padrão = IN), o valor de vida útil, a preferência de registro e o nome de host intermediário.</span><span class="sxs-lookup"><span data-stu-id="ab744-118">Instantiates an RT Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/host Name, class (default = IN), time-to-live value, record preference and intermediate host name.</span></span> <span data-ttu-id="ab744-119">Ele retorna uma referência ao novo objeto como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="ab744-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="ab744-120">Qualificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="ab744-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="ab744-121">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="ab744-121">**Modify**</span></span>                         | <span data-ttu-id="ab744-122">Atualiza o TTL, a preferência e o host intermediário para os valores especificados como os parâmetros de entrada deste método.</span><span class="sxs-lookup"><span data-stu-id="ab744-122">Updates the TTL, Preference, and Intermediate Host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="ab744-123">Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado.</span><span class="sxs-lookup"><span data-stu-id="ab744-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="ab744-124">O método retorna uma referência ao objeto modificado como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="ab744-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="ab744-125">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="ab744-125">Qualifiers: Implemented</span></span><br/>        |



 

### <a name="properties"></a><span data-ttu-id="ab744-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ab744-126">Properties</span></span>

<span data-ttu-id="ab744-127">A classe **MicrosoftDNS \_ RTType** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ab744-127">The **MicrosoftDNS\_RTType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ab744-128">**IntermediateHost**</span><span class="sxs-lookup"><span data-stu-id="ab744-128">**IntermediateHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab744-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ab744-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab744-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ab744-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab744-131">FQDN que especifica um host para servir como intermediário para atingir o host especificado pelo proprietário.</span><span class="sxs-lookup"><span data-stu-id="ab744-131">FQDN specifying a host to serve as an intermediate in reaching the host specified by owner.</span></span>

</dd> <dt>

<span data-ttu-id="ab744-132">**Preferência**</span><span class="sxs-lookup"><span data-stu-id="ab744-132">**Preference**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab744-133">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ab744-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ab744-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ab744-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab744-135">Preferência dada a esse RR entre outros no mesmo proprietário.</span><span class="sxs-lookup"><span data-stu-id="ab744-135">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="ab744-136">Os valores mais baixos são preferenciais.</span><span class="sxs-lookup"><span data-stu-id="ab744-136">Lower values are preferred.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ab744-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab744-137">Requirements</span></span>



| <span data-ttu-id="ab744-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab744-138">Requirement</span></span> | <span data-ttu-id="ab744-139">Valor</span><span class="sxs-lookup"><span data-stu-id="ab744-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab744-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab744-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ab744-141">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ab744-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ab744-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab744-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ab744-143">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ab744-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ab744-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="ab744-144">Namespace</span></span><br/>                | <span data-ttu-id="ab744-145">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="ab744-145">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ab744-146">MOF</span><span class="sxs-lookup"><span data-stu-id="ab744-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab744-147"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab744-147"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab744-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab744-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab744-149">**Método CreateInstanceFromPropertyData da \_ classe RTType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ab744-149">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_RTType Class**</span></span>](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="ab744-150">**Método Modify da classe MicrosoftDNS \_ RTType**</span><span class="sxs-lookup"><span data-stu-id="ab744-150">**Modify Method of the MicrosoftDNS\_RTType Class**</span></span>](microsoftdns-rttype-modify.md)
</dt> <dt>

[<span data-ttu-id="ab744-151">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="ab744-151">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





