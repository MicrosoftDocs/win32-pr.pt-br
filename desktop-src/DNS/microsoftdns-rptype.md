---
title: Classe MicrosoftDNS_RPType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro de RP (pessoa responsável).
ms.assetid: 2b1c1bbc-a69f-4480-a7f2-6420240d4ad8
keywords:
- MicrosoftDNS_RPType de classe de DNS
- MicrosoftDNS_RPType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType
- MicrosoftDNS_RPType.CreateInstanceFromPropertyData
- MicrosoftDNS_RPType.Modify
- MicrosoftDNS_RPType.RPMailbox
- MicrosoftDNS_RPType.TXTDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9aae8686016d26cb9007b21a06c125d56ed5207f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824504"
---
# <a name="microsoftdns_rptype-class"></a><span data-ttu-id="26165-105">\_Classe MicrosoftDNS RPType</span><span class="sxs-lookup"><span data-stu-id="26165-105">MicrosoftDNS\_RPType class</span></span>

<span data-ttu-id="26165-106">A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro de RP (pessoa responsável).</span><span class="sxs-lookup"><span data-stu-id="26165-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Responsible Person (RP) record.</span></span>

<span data-ttu-id="26165-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="26165-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="26165-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26165-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_RPType : MicrosoftDNS_ResourceRecord
{
  string RPMailbox;
  string TXTDomainName;
};
```

## <a name="members"></a><span data-ttu-id="26165-109">Membros</span><span class="sxs-lookup"><span data-stu-id="26165-109">Members</span></span>

<span data-ttu-id="26165-110">A classe **MicrosoftDNS \_ RPType** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="26165-110">The **MicrosoftDNS\_RPType** class has these types of members:</span></span>

-   [<span data-ttu-id="26165-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="26165-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="26165-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="26165-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="26165-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="26165-113">Methods</span></span>

<span data-ttu-id="26165-114">A classe **MicrosoftDNS \_ RPType** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="26165-114">The **MicrosoftDNS\_RPType** class has these methods.</span></span>



| <span data-ttu-id="26165-115">Método</span><span class="sxs-lookup"><span data-stu-id="26165-115">Method</span></span>                             | <span data-ttu-id="26165-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="26165-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26165-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="26165-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="26165-118">Cria uma instância de um tipo de RR de RP com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário/pessoa responsável, a classe (padrão = IN), o valor de vida útil e os nomes de domínio para a caixa de correio e os locais RR do TXT da pessoa.</span><span class="sxs-lookup"><span data-stu-id="26165-118">Instantiates an RP Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/responsible person Name, class (default = IN), time-to-live value and the domain names for the person's mailbox and TXT RR locations.</span></span> <span data-ttu-id="26165-119">Ele retorna uma referência ao novo objeto como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="26165-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="26165-120">Qualificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="26165-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="26165-121">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="26165-121">**Modify**</span></span>                         | <span data-ttu-id="26165-122">Esse método atualiza o TTL, a caixa de correio RP e o nome de domínio TXT para os valores especificados como os parâmetros de entrada desse método.</span><span class="sxs-lookup"><span data-stu-id="26165-122">This method updates the TTL, RP Mailbox and TXT Domain Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="26165-123">Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado.</span><span class="sxs-lookup"><span data-stu-id="26165-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="26165-124">O método retorna uma referência ao objeto modificado como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="26165-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="26165-125">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="26165-125">Qualifiers: Implemented</span></span><br/>                                  |



 

### <a name="properties"></a><span data-ttu-id="26165-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="26165-126">Properties</span></span>

<span data-ttu-id="26165-127">A classe **MicrosoftDNS \_ RPType** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="26165-127">The **MicrosoftDNS\_RPType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="26165-128">**RPMailbox**</span><span class="sxs-lookup"><span data-stu-id="26165-128">**RPMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26165-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="26165-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26165-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="26165-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26165-131">FQDN que especifica a caixa de correio da pessoa responsável.</span><span class="sxs-lookup"><span data-stu-id="26165-131">FQDN specifying the mailbox for the responsible person.</span></span>

</dd> <dt>

<span data-ttu-id="26165-132">**TXTDomainName**</span><span class="sxs-lookup"><span data-stu-id="26165-132">**TXTDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26165-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="26165-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26165-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="26165-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26165-135">FQDN para o qual os registros de recurso TXT existem.</span><span class="sxs-lookup"><span data-stu-id="26165-135">FQDN for which TXT Resource Records exist.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26165-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26165-136">Requirements</span></span>



| <span data-ttu-id="26165-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="26165-137">Requirement</span></span> | <span data-ttu-id="26165-138">Valor</span><span class="sxs-lookup"><span data-stu-id="26165-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="26165-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26165-139">Minimum supported client</span></span><br/> | <span data-ttu-id="26165-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="26165-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="26165-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26165-141">Minimum supported server</span></span><br/> | <span data-ttu-id="26165-142">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="26165-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="26165-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="26165-143">Namespace</span></span><br/>                | <span data-ttu-id="26165-144">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="26165-144">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="26165-145">MOF</span><span class="sxs-lookup"><span data-stu-id="26165-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26165-146"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26165-146"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26165-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="26165-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26165-148">**Método CreateInstanceFromPropertyData da \_ classe RPType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="26165-148">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_RPType Class**</span></span>](microsoftdns-rptype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="26165-149">**Método Modify da classe MicrosoftDNS \_ RPType**</span><span class="sxs-lookup"><span data-stu-id="26165-149">**Modify Method of the MicrosoftDNS\_RPType Class**</span></span>](microsoftdns-rptype-modify.md)
</dt> <dt>

[<span data-ttu-id="26165-150">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="26165-150">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





