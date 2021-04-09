---
title: Classe MicrosoftDNS_NXTType
description: Subclasse de MicrosoftDNS \_ ResourceRecord que representa um próximo RR (NXT).
ms.assetid: bb24509e-083b-4432-89e3-501167f12299
keywords:
- MicrosoftDNS_NXTType de classe de DNS
- MicrosoftDNS_NXTType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType
- MicrosoftDNS_NXTType.CreateInstanceFromPropertyData
- MicrosoftDNS_NXTType.Modify
- MicrosoftDNS_NXTType.NextDomainName
- MicrosoftDNS_NXTType.Types
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79db82b3ae760c31d4e6fef80eb01469cb2bb41d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085717"
---
# <a name="microsoftdns_nxttype-class"></a><span data-ttu-id="abef8-105">\_Classe MicrosoftDNS NXTType</span><span class="sxs-lookup"><span data-stu-id="abef8-105">MicrosoftDNS\_NXTType class</span></span>

<span data-ttu-id="abef8-106">Subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um próximo RR (NXT).</span><span class="sxs-lookup"><span data-stu-id="abef8-106">Subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Next (NXT) RR.</span></span>

<span data-ttu-id="abef8-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="abef8-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="abef8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="abef8-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_NXTType : MicrosoftDNS_ResourceRecord
{
  string NextDomainName;
  string Types;
};
```

## <a name="members"></a><span data-ttu-id="abef8-109">Membros</span><span class="sxs-lookup"><span data-stu-id="abef8-109">Members</span></span>

<span data-ttu-id="abef8-110">A classe **MicrosoftDNS \_ NXTType** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="abef8-110">The **MicrosoftDNS\_NXTType** class has these types of members:</span></span>

-   [<span data-ttu-id="abef8-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="abef8-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="abef8-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="abef8-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="abef8-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="abef8-113">Methods</span></span>

<span data-ttu-id="abef8-114">A classe **MicrosoftDNS \_ NXTType** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="abef8-114">The **MicrosoftDNS\_NXTType** class has these methods.</span></span>



| <span data-ttu-id="abef8-115">Método</span><span class="sxs-lookup"><span data-stu-id="abef8-115">Method</span></span>                             | <span data-ttu-id="abef8-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="abef8-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abef8-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="abef8-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="abef8-118">Cria uma instância de um registro de recurso NXT com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário, a classe (padrão = IN), o valor de vida útil e o sinalizador de mapeamento do WINS, o tempo limite de pesquisa inversa, o tempo limite do cache WINS e o nome de domínio a acrescentar</span><span class="sxs-lookup"><span data-stu-id="abef8-118">Instantiates an NXT Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, reverse look-up time out, WINS cache time out, and domain name to append.</span></span> <span data-ttu-id="abef8-119">Ele retorna uma referência ao novo objeto como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="abef8-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="abef8-120">Qualificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="abef8-120">Qualifiers: Implemented, static</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="abef8-121">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="abef8-121">**Modify**</span></span>                         | <span data-ttu-id="abef8-122">Atualiza o TTL, o sinalizador de mapeamento, o tempo limite de pesquisa, o tempo limite de cache e o domínio de resultado para os valores especificados como os parâmetros de entrada deste método.</span><span class="sxs-lookup"><span data-stu-id="abef8-122">Updates the TTL, Mapping Flag, Look-up Time out, Cache Time out and Result Domain to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="abef8-123">Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado.</span><span class="sxs-lookup"><span data-stu-id="abef8-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="abef8-124">O método retorna uma referência ao objeto modificado como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="abef8-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="abef8-125">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="abef8-125">Qualifiers: Implemented</span></span><br/> <span data-ttu-id="abef8-126">**Windows Server 2003:** Esse método também atualiza o NextDomainName e os tipos para os valores especificados como os parâmetros de entrada desse método.</span><span class="sxs-lookup"><span data-stu-id="abef8-126">**Windows Server 2003:** This method also updates the NextDomainName and Types to the values specified as the input parameters of this method.</span></span><br/> <br/> |



 

### <a name="properties"></a><span data-ttu-id="abef8-127">Propriedades</span><span class="sxs-lookup"><span data-stu-id="abef8-127">Properties</span></span>

<span data-ttu-id="abef8-128">A classe **MicrosoftDNS \_ NXTType** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="abef8-128">The **MicrosoftDNS\_NXTType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="abef8-129">**NextDomainName**</span><span class="sxs-lookup"><span data-stu-id="abef8-129">**NextDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abef8-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="abef8-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abef8-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="abef8-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abef8-132">Próximo nome de domínio.</span><span class="sxs-lookup"><span data-stu-id="abef8-132">Next domain name.</span></span>

</dd> <dt>

<span data-ttu-id="abef8-133">**Types**</span><span class="sxs-lookup"><span data-stu-id="abef8-133">**Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abef8-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="abef8-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abef8-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="abef8-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abef8-136">Lista separada por espaços dos mnemônicos do tipo RR para o nome do proprietário do registro de recurso NXT.</span><span class="sxs-lookup"><span data-stu-id="abef8-136">Space-separated list of the RR-type mnemonics for the owner name of the NXT Resource Record.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="abef8-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abef8-137">Requirements</span></span>



| <span data-ttu-id="abef8-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="abef8-138">Requirement</span></span> | <span data-ttu-id="abef8-139">Valor</span><span class="sxs-lookup"><span data-stu-id="abef8-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="abef8-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="abef8-140">Minimum supported client</span></span><br/> | <span data-ttu-id="abef8-141">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="abef8-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="abef8-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="abef8-142">Minimum supported server</span></span><br/> | <span data-ttu-id="abef8-143">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="abef8-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="abef8-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="abef8-144">Namespace</span></span><br/>                | <span data-ttu-id="abef8-145">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="abef8-145">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="abef8-146">MOF</span><span class="sxs-lookup"><span data-stu-id="abef8-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="abef8-147"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="abef8-147"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abef8-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="abef8-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abef8-149">**Método CreateInstanceFromPropertyData da \_ classe NXTType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="abef8-149">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_NXTType Class**</span></span>](microsoftdns-nxttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="abef8-150">**Método Modify da classe MicrosoftDNS \_ NXTType**</span><span class="sxs-lookup"><span data-stu-id="abef8-150">**Modify Method of the MicrosoftDNS\_NXTType Class**</span></span>](microsoftdns-nxttype-modify.md)
</dt> <dt>

[<span data-ttu-id="abef8-151">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="abef8-151">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





