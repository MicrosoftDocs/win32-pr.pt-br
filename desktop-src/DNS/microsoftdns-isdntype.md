---
title: Classe MicrosoftDNS_ISDNType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro de ISDN.
ms.assetid: 8925042c-65d3-465f-aedd-9f7c862620b5
keywords:
- MicrosoftDNS_ISDNType de classe de DNS
- MicrosoftDNS_ISDNType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType
- MicrosoftDNS_ISDNType.CreateInstanceFromPropertyData
- MicrosoftDNS_ISDNType.Modify
- MicrosoftDNS_ISDNType.ISDNNumber
- MicrosoftDNS_ISDNType.SubAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4e8b50d75f7b6d57226247c978ced45e07b1acc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085202"
---
# <a name="microsoftdns_isdntype-class"></a><span data-ttu-id="76d5e-105">\_Classe isdntype MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="76d5e-105">MicrosoftDNS\_ISDNType class</span></span>

<span data-ttu-id="76d5e-106">A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro de ISDN.</span><span class="sxs-lookup"><span data-stu-id="76d5e-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an ISDN record.</span></span>

<span data-ttu-id="76d5e-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="76d5e-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="76d5e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76d5e-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_ISDNType : MicrosoftDNS_ResourceRecord
{
  string ISDNNumber;
  string SubAddress;
};
```

## <a name="members"></a><span data-ttu-id="76d5e-109">Membros</span><span class="sxs-lookup"><span data-stu-id="76d5e-109">Members</span></span>

<span data-ttu-id="76d5e-110">A **classe \_ isdntype MicrosoftDNS** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="76d5e-110">The **MicrosoftDNS\_ISDNType** class has these types of members:</span></span>

-   [<span data-ttu-id="76d5e-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="76d5e-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="76d5e-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="76d5e-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="76d5e-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="76d5e-113">Methods</span></span>

<span data-ttu-id="76d5e-114">A **classe \_ isdntype MicrosoftDNS** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="76d5e-114">The **MicrosoftDNS\_ISDNType** class has these methods.</span></span>



| <span data-ttu-id="76d5e-115">Método</span><span class="sxs-lookup"><span data-stu-id="76d5e-115">Method</span></span>                             | <span data-ttu-id="76d5e-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="76d5e-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76d5e-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="76d5e-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="76d5e-118">Cria uma instância de um registro de recurso de ISDN com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário, a classe (padrão = IN), o valor de vida útil e o número ISDN e Subendereço do proprietário.</span><span class="sxs-lookup"><span data-stu-id="76d5e-118">Instantiates an ISDN Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the ISDN number and subaddress of the owner.</span></span> <span data-ttu-id="76d5e-119">Ele retorna uma referência ao novo objeto como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="76d5e-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="76d5e-120">Qualificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="76d5e-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="76d5e-121">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="76d5e-121">**Modify**</span></span>                         | <span data-ttu-id="76d5e-122">Atualiza o TTL, o número ISDN e o Subendereço para os valores especificados como os parâmetros de entrada deste método.</span><span class="sxs-lookup"><span data-stu-id="76d5e-122">Updates the TTL, ISDN Number, and Subaddress to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="76d5e-123">Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado.</span><span class="sxs-lookup"><span data-stu-id="76d5e-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="76d5e-124">O método retorna uma referência ao objeto modificado como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="76d5e-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="76d5e-125">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="76d5e-125">Qualifiers: Implemented</span></span><br/>                   |



 

### <a name="properties"></a><span data-ttu-id="76d5e-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="76d5e-126">Properties</span></span>

<span data-ttu-id="76d5e-127">A **classe \_ isdntype MicrosoftDNS** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="76d5e-127">The **MicrosoftDNS\_ISDNType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="76d5e-128">**ISDNNumber**</span><span class="sxs-lookup"><span data-stu-id="76d5e-128">**ISDNNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76d5e-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="76d5e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76d5e-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="76d5e-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76d5e-131">Número ISDN e DDI do proprietário do registro.</span><span class="sxs-lookup"><span data-stu-id="76d5e-131">ISDN number and DDI of the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="76d5e-132">**Subendereço**</span><span class="sxs-lookup"><span data-stu-id="76d5e-132">**SubAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76d5e-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="76d5e-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76d5e-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="76d5e-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76d5e-135">Subendereço do proprietário, se definido.</span><span class="sxs-lookup"><span data-stu-id="76d5e-135">Subaddress of the owner, if defined.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="76d5e-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76d5e-136">Requirements</span></span>



| <span data-ttu-id="76d5e-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="76d5e-137">Requirement</span></span> | <span data-ttu-id="76d5e-138">Valor</span><span class="sxs-lookup"><span data-stu-id="76d5e-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="76d5e-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76d5e-139">Minimum supported client</span></span><br/> | <span data-ttu-id="76d5e-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="76d5e-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="76d5e-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76d5e-141">Minimum supported server</span></span><br/> | <span data-ttu-id="76d5e-142">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="76d5e-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="76d5e-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="76d5e-143">Namespace</span></span><br/>                | <span data-ttu-id="76d5e-144">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="76d5e-144">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="76d5e-145">MOF</span><span class="sxs-lookup"><span data-stu-id="76d5e-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76d5e-146"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="76d5e-146"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76d5e-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="76d5e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76d5e-148">**Método CreateInstanceFromPropertyData da \_ classe isdntype MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="76d5e-148">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_ISDNType Class**</span></span>](microsoftdns-isdntype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="76d5e-149">**Método Modify da \_ classe isdntype MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="76d5e-149">**Modify Method of the MicrosoftDNS\_ISDNType Class**</span></span>](microsoftdns-isdntype-modify.md)
</dt> <dt>

[<span data-ttu-id="76d5e-150">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="76d5e-150">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





