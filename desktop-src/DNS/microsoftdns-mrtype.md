---
title: Classe MicrosoftDNS_MRType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro Sr (renomeação da caixa de correio).
ms.assetid: fa5da18f-121b-477b-8876-6e337382e9b8
keywords:
- MicrosoftDNS_MRType de classe de DNS
- MicrosoftDNS_MRType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_MRType
- MicrosoftDNS_MRType.CreateInstanceFromPropertyData
- MicrosoftDNS_MRType.Modify
- MicrosoftDNS_MRType.MRMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 732f0e6f51963f5ae810e4730406a94264fdde47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086081"
---
# <a name="microsoftdns_mrtype-class"></a><span data-ttu-id="c976c-105">\_Classe MicrosoftDNS MRType</span><span class="sxs-lookup"><span data-stu-id="c976c-105">MicrosoftDNS\_MRType class</span></span>

<span data-ttu-id="c976c-106">A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro Sr (renomeação da caixa de correio).</span><span class="sxs-lookup"><span data-stu-id="c976c-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mailbox Rename (MR) record.</span></span>

<span data-ttu-id="c976c-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="c976c-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c976c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c976c-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MRType : MicrosoftDNS_ResourceRecord
{
  string MRMailbox;
};
```

## <a name="members"></a><span data-ttu-id="c976c-109">Membros</span><span class="sxs-lookup"><span data-stu-id="c976c-109">Members</span></span>

<span data-ttu-id="c976c-110">A classe **MicrosoftDNS \_ MRType** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c976c-110">The **MicrosoftDNS\_MRType** class has these types of members:</span></span>

-   [<span data-ttu-id="c976c-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="c976c-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="c976c-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c976c-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c976c-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="c976c-113">Methods</span></span>

<span data-ttu-id="c976c-114">A classe **MicrosoftDNS \_ MRType** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c976c-114">The **MicrosoftDNS\_MRType** class has these methods.</span></span>



| <span data-ttu-id="c976c-115">Método</span><span class="sxs-lookup"><span data-stu-id="c976c-115">Method</span></span>                             | <span data-ttu-id="c976c-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="c976c-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c976c-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="c976c-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="c976c-118">Esse método instancia um tipo de RR ' MR ' com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário da caixa de correio, a classe (padrão = IN), o valor de vida útil e a caixa de correio renomear.</span><span class="sxs-lookup"><span data-stu-id="c976c-118">This method instantiates an 'MR' Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the mailbox, class (default = IN), time-to-live value and the mailbox rename.</span></span> <span data-ttu-id="c976c-119">Ele retorna uma referência ao novo objeto como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="c976c-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="c976c-120">Qualificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="c976c-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="c976c-121">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="c976c-121">**Modify**</span></span>                         | <span data-ttu-id="c976c-122">Esse método atualiza a caixa de correio TTL e MR para os valores especificados como os parâmetros de entrada deste método.</span><span class="sxs-lookup"><span data-stu-id="c976c-122">This method updates the TTL and MR Mailbox to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="c976c-123">Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado.</span><span class="sxs-lookup"><span data-stu-id="c976c-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="c976c-124">O método retorna uma referência ao objeto modificado como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="c976c-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="c976c-125">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="c976c-125">Qualifiers: Implemented</span></span><br/>                 |



 

### <a name="properties"></a><span data-ttu-id="c976c-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c976c-126">Properties</span></span>

<span data-ttu-id="c976c-127">A classe **MicrosoftDNS \_ MRType** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c976c-127">The **MicrosoftDNS\_MRType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c976c-128">**MRMailbox**</span><span class="sxs-lookup"><span data-stu-id="c976c-128">**MRMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c976c-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c976c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c976c-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c976c-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c976c-131">FQDN que especifica uma caixa de correio que é a renomeação correta da caixa de correio especificada no nome do proprietário do registro.</span><span class="sxs-lookup"><span data-stu-id="c976c-131">FQDN specifying a mailbox that is the proper rename of the mailbox specified in the record's owner name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c976c-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c976c-132">Requirements</span></span>



| <span data-ttu-id="c976c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="c976c-133">Requirement</span></span> | <span data-ttu-id="c976c-134">Valor</span><span class="sxs-lookup"><span data-stu-id="c976c-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c976c-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c976c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c976c-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c976c-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c976c-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c976c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c976c-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c976c-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c976c-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="c976c-139">Namespace</span></span><br/>                | <span data-ttu-id="c976c-140">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="c976c-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c976c-141">MOF</span><span class="sxs-lookup"><span data-stu-id="c976c-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c976c-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c976c-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c976c-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="c976c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c976c-144">**Método CreateInstanceFromPropertyData da \_ classe MRType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c976c-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MRType Class**</span></span>](microsoftdns-mrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="c976c-145">**Método Modify da classe MicrosoftDNS \_ MRType**</span><span class="sxs-lookup"><span data-stu-id="c976c-145">**Modify Method of the MicrosoftDNS\_MRType Class**</span></span>](microsoftdns-mrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="c976c-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="c976c-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





