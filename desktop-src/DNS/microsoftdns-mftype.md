---
title: Classe MicrosoftDNS_MFType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um agente de encaminhamento de email para registro de domínio (MF).
ms.assetid: 0ba0fddd-c316-4a5b-ad65-6344dbe949c1
keywords:
- MicrosoftDNS_MFType de classe de DNS
- MicrosoftDNS_MFType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_MFType
- MicrosoftDNS_MFType.CreateInstanceFromPropertyData
- MicrosoftDNS_MFType.Modify
- MicrosoftDNS_MFType.MFHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e030f695e95ee736b1c53a345201e0bd1addfe3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085909"
---
# <a name="microsoftdns_mftype-class"></a><span data-ttu-id="ed26f-105">\_Classe MicrosoftDNS MFType</span><span class="sxs-lookup"><span data-stu-id="ed26f-105">MicrosoftDNS\_MFType class</span></span>

<span data-ttu-id="ed26f-106">A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um agente de encaminhamento de email para registro de domínio (MF).</span><span class="sxs-lookup"><span data-stu-id="ed26f-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Forwarding Agent for Domain (MF) record.</span></span>

<span data-ttu-id="ed26f-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="ed26f-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed26f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed26f-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MFType : MicrosoftDNS_ResourceRecord
{
  string MFHost;
};
```

## <a name="members"></a><span data-ttu-id="ed26f-109">Membros</span><span class="sxs-lookup"><span data-stu-id="ed26f-109">Members</span></span>

<span data-ttu-id="ed26f-110">A classe **MicrosoftDNS \_ MFType** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ed26f-110">The **MicrosoftDNS\_MFType** class has these types of members:</span></span>

-   [<span data-ttu-id="ed26f-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="ed26f-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="ed26f-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ed26f-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ed26f-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="ed26f-113">Methods</span></span>

<span data-ttu-id="ed26f-114">A classe **MicrosoftDNS \_ MFType** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ed26f-114">The **MicrosoftDNS\_MFType** class has these methods.</span></span>



| <span data-ttu-id="ed26f-115">Método</span><span class="sxs-lookup"><span data-stu-id="ed26f-115">Method</span></span>                             | <span data-ttu-id="ed26f-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed26f-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed26f-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="ed26f-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="ed26f-118">Esse método instancia um tipo de RR MF com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário do domínio, a classe (padrão = IN), o valor de vida útil e o host do agente de email.</span><span class="sxs-lookup"><span data-stu-id="ed26f-118">This method instantiates an MF Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the domain, class (default = IN), time-to-live value and the host of the mail agent.</span></span> <span data-ttu-id="ed26f-119">Ele retorna uma referência ao novo objeto como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="ed26f-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="ed26f-120">Qualificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="ed26f-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="ed26f-121">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="ed26f-121">**Modify**</span></span>                         | <span data-ttu-id="ed26f-122">Esse método atualiza o TTL e o host MF para os valores especificados como os parâmetros de entrada deste método.</span><span class="sxs-lookup"><span data-stu-id="ed26f-122">This method updates the TTL and MF Host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="ed26f-123">Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado.</span><span class="sxs-lookup"><span data-stu-id="ed26f-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="ed26f-124">O método retorna uma referência ao objeto modificado como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="ed26f-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="ed26f-125">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="ed26f-125">Qualifiers: Implemented</span></span><br/>                         |



 

### <a name="properties"></a><span data-ttu-id="ed26f-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ed26f-126">Properties</span></span>

<span data-ttu-id="ed26f-127">A classe **MicrosoftDNS \_ MFType** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ed26f-127">The **MicrosoftDNS\_MFType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ed26f-128">**MFHost**</span><span class="sxs-lookup"><span data-stu-id="ed26f-128">**MFHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed26f-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ed26f-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed26f-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ed26f-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed26f-131">FQDN que especifica um host com um agente de email que aceitará email para encaminhamento ao domínio especificado.</span><span class="sxs-lookup"><span data-stu-id="ed26f-131">FQDN specifying a host with a mail agent that will accept mail for forwarding to the specified domain.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed26f-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed26f-132">Requirements</span></span>



| <span data-ttu-id="ed26f-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed26f-133">Requirement</span></span> | <span data-ttu-id="ed26f-134">Valor</span><span class="sxs-lookup"><span data-stu-id="ed26f-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed26f-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed26f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ed26f-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ed26f-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ed26f-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed26f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ed26f-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ed26f-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ed26f-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="ed26f-139">Namespace</span></span><br/>                | <span data-ttu-id="ed26f-140">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="ed26f-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ed26f-141">MOF</span><span class="sxs-lookup"><span data-stu-id="ed26f-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed26f-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed26f-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed26f-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed26f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed26f-144">**Método CreateInstanceFromPropertyData da \_ classe MFType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ed26f-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MFType Class**</span></span>](microsoftdns-mftype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="ed26f-145">**Método Modify da classe MicrosoftDNS \_ MFType**</span><span class="sxs-lookup"><span data-stu-id="ed26f-145">**Modify Method of the MicrosoftDNS\_MFType Class**</span></span>](microsoftdns-mftype-modify.md)
</dt> <dt>

[<span data-ttu-id="ed26f-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="ed26f-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





