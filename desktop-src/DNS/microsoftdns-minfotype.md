---
title: Classe MicrosoftDNS_MINFOType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro MINFO (mail information).
ms.assetid: 9c4b70b8-f9cf-4dea-8d2d-43e0de002d52
keywords:
- MicrosoftDNS_MINFOType de classe de DNS
- MicrosoftDNS_MINFOType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType
- MicrosoftDNS_MINFOType.CreateInstanceFromPropertyData
- MicrosoftDNS_MINFOType.Modify
- MicrosoftDNS_MINFOType.ResponsibleMailbox
- MicrosoftDNS_MINFOType.ErrorMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a7d230db9da32ce47cd4cfaf99c4978c4e63385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086308"
---
# <a name="microsoftdns_minfotype-class"></a><span data-ttu-id="cc67f-105">\_Classe MicrosoftDNS MINFOType</span><span class="sxs-lookup"><span data-stu-id="cc67f-105">MicrosoftDNS\_MINFOType class</span></span>

<span data-ttu-id="cc67f-106">A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro MINFO (mail information).</span><span class="sxs-lookup"><span data-stu-id="cc67f-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Information (MINFO) record.</span></span>

<span data-ttu-id="cc67f-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="cc67f-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc67f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc67f-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MINFOType : MicrosoftDNS_ResourceRecord
{
  string ResponsibleMailbox;
  string ErrorMailbox;
};
```

## <a name="members"></a><span data-ttu-id="cc67f-109">Membros</span><span class="sxs-lookup"><span data-stu-id="cc67f-109">Members</span></span>

<span data-ttu-id="cc67f-110">A classe **MicrosoftDNS \_ MINFOType** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cc67f-110">The **MicrosoftDNS\_MINFOType** class has these types of members:</span></span>

-   [<span data-ttu-id="cc67f-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="cc67f-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="cc67f-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cc67f-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cc67f-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="cc67f-113">Methods</span></span>

<span data-ttu-id="cc67f-114">A classe **MicrosoftDNS \_ MINFOType** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="cc67f-114">The **MicrosoftDNS\_MINFOType** class has these methods.</span></span>



| <span data-ttu-id="cc67f-115">Método</span><span class="sxs-lookup"><span data-stu-id="cc67f-115">Method</span></span>                             | <span data-ttu-id="cc67f-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc67f-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc67f-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="cc67f-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="cc67f-118">Cria uma instância de um tipo MINFO de RR com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário da lista/caixa de email, a classe (padrão = IN), o valor de vida útil e as caixas de correio de erro e responsável.</span><span class="sxs-lookup"><span data-stu-id="cc67f-118">Instantiates an MINFO Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the mail list/box, class (default = IN), time-to-live value and the responsible and error mailboxes.</span></span> <span data-ttu-id="cc67f-119">Ele retorna uma referência ao novo objeto como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="cc67f-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="cc67f-120">Qualificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="cc67f-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="cc67f-121">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="cc67f-121">**Modify**</span></span>                         | <span data-ttu-id="cc67f-122">Esse método atualiza a TTL, a caixa de correio responsável e a caixa de correio de erro para os valores especificados como os parâmetros de entrada desse método.</span><span class="sxs-lookup"><span data-stu-id="cc67f-122">This method updates the TTL, Responsible Mailbox, and Error Mailbox to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="cc67f-123">Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado.</span><span class="sxs-lookup"><span data-stu-id="cc67f-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="cc67f-124">O método retorna uma referência ao objeto modificado como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="cc67f-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="cc67f-125">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="cc67f-125">Qualifiers: Implemented</span></span><br/>    |



 

### <a name="properties"></a><span data-ttu-id="cc67f-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cc67f-126">Properties</span></span>

<span data-ttu-id="cc67f-127">A classe **MicrosoftDNS \_ MINFOType** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="cc67f-127">The **MicrosoftDNS\_MINFOType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cc67f-128">**ErrorMailbox**</span><span class="sxs-lookup"><span data-stu-id="cc67f-128">**ErrorMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc67f-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cc67f-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc67f-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc67f-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc67f-131">FQDN que especifica uma caixa de correio para receber mensagens de erro relacionadas à lista de endereçamento ou à caixa de correio especificada pelo nome do proprietário do registro MINFO.</span><span class="sxs-lookup"><span data-stu-id="cc67f-131">FQDN specifying a mailbox to receive error messages related to either the mailing list, or to the mailbox specified by the owner name of the MINFO record.</span></span>

</dd> <dt>

<span data-ttu-id="cc67f-132">**ResponsibleMailbox**</span><span class="sxs-lookup"><span data-stu-id="cc67f-132">**ResponsibleMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc67f-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cc67f-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc67f-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc67f-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc67f-135">FQDN que especifica uma caixa de correio responsável pela lista de endereçamento ou caixa de correio especificada no nome do proprietário do registro.</span><span class="sxs-lookup"><span data-stu-id="cc67f-135">FQDN specifying a mailbox responsible for the mailing list or mailbox specified in the record's Owner Name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cc67f-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc67f-136">Requirements</span></span>



| <span data-ttu-id="cc67f-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc67f-137">Requirement</span></span> | <span data-ttu-id="cc67f-138">Valor</span><span class="sxs-lookup"><span data-stu-id="cc67f-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc67f-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc67f-139">Minimum supported client</span></span><br/> | <span data-ttu-id="cc67f-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="cc67f-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="cc67f-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc67f-141">Minimum supported server</span></span><br/> | <span data-ttu-id="cc67f-142">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cc67f-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cc67f-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="cc67f-143">Namespace</span></span><br/>                | <span data-ttu-id="cc67f-144">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="cc67f-144">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="cc67f-145">MOF</span><span class="sxs-lookup"><span data-stu-id="cc67f-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc67f-146"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cc67f-146"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc67f-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc67f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc67f-148">**Método CreateInstanceFromPropertyData da \_ classe MINFOType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="cc67f-148">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MINFOType Class**</span></span>](microsoftdns-minfotype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="cc67f-149">**Método Modify da classe MicrosoftDNS \_ MINFOType**</span><span class="sxs-lookup"><span data-stu-id="cc67f-149">**Modify Method of the MicrosoftDNS\_MINFOType Class**</span></span>](microsoftdns-minfotype-modify.md)
</dt> <dt>

[<span data-ttu-id="cc67f-150">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="cc67f-150">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





