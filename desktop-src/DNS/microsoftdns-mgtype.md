---
title: Classe MicrosoftDNS_MGType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro de grupo de emails (mg).
ms.assetid: ce5795d1-e575-46ef-ad82-62b329e261d6
keywords:
- MicrosoftDNS_MGType de classe de DNS
- MicrosoftDNS_MGType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType
- MicrosoftDNS_MGType.CreateInstanceFromPropertyData
- MicrosoftDNS_MGType.Modify
- MicrosoftDNS_MGType.MGMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4772f8841977fbeae1f0bf609a65a9511bc704a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499772"
---
# <a name="microsoftdns_mgtype-class"></a><span data-ttu-id="f98df-105">\_Classe MicrosoftDNS MGType</span><span class="sxs-lookup"><span data-stu-id="f98df-105">MicrosoftDNS\_MGType class</span></span>

<span data-ttu-id="f98df-106">A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro de grupo de emails (mg).</span><span class="sxs-lookup"><span data-stu-id="f98df-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Group (MG) record.</span></span>

<span data-ttu-id="f98df-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="f98df-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f98df-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f98df-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MGType : MicrosoftDNS_ResourceRecord
{
  string MGMailbox;
};
```

## <a name="members"></a><span data-ttu-id="f98df-109">Membros</span><span class="sxs-lookup"><span data-stu-id="f98df-109">Members</span></span>

<span data-ttu-id="f98df-110">A classe **MicrosoftDNS \_ MGType** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f98df-110">The **MicrosoftDNS\_MGType** class has these types of members:</span></span>

-   [<span data-ttu-id="f98df-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="f98df-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="f98df-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f98df-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f98df-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="f98df-113">Methods</span></span>

<span data-ttu-id="f98df-114">A classe **MicrosoftDNS \_ MGType** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f98df-114">The **MicrosoftDNS\_MGType** class has these methods.</span></span>



| <span data-ttu-id="f98df-115">Método</span><span class="sxs-lookup"><span data-stu-id="f98df-115">Method</span></span>                             | <span data-ttu-id="f98df-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="f98df-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f98df-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="f98df-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="f98df-118">Esse método instancia um tipo MG de RR com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário do grupo de emails, a classe (padrão = IN), o valor de vida útil e o nome da caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="f98df-118">This method instantiates an MG Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the mail group, class (default = IN), time-to-live value and the mailbox name.</span></span> <span data-ttu-id="f98df-119">Ele retorna uma referência ao novo objeto como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="f98df-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="f98df-120">Qualificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="f98df-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="f98df-121">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="f98df-121">**Modify**</span></span>                         | <span data-ttu-id="f98df-122">Esse método atualiza a caixa de correio TTL e MG para os valores especificados como os parâmetros de entrada desse método.</span><span class="sxs-lookup"><span data-stu-id="f98df-122">This method updates the TTL and MG Mailbox to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="f98df-123">Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado.</span><span class="sxs-lookup"><span data-stu-id="f98df-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="f98df-124">O método retorna uma referência ao objeto modificado como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="f98df-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="f98df-125">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="f98df-125">Qualifiers: Implemented</span></span><br/>                |



 

### <a name="properties"></a><span data-ttu-id="f98df-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f98df-126">Properties</span></span>

<span data-ttu-id="f98df-127">A classe **MicrosoftDNS \_ MGType** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f98df-127">The **MicrosoftDNS\_MGType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f98df-128">**MGMailbox**</span><span class="sxs-lookup"><span data-stu-id="f98df-128">**MGMailbox**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f98df-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f98df-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f98df-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f98df-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f98df-131">FQDN que especifica uma caixa de correio que é membro do grupo de emails especificado pelo nome do proprietário do registro.</span><span class="sxs-lookup"><span data-stu-id="f98df-131">FQDN specifying a mailbox that is a member of the mail group specified by the record's owner name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f98df-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f98df-132">Requirements</span></span>



| <span data-ttu-id="f98df-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="f98df-133">Requirement</span></span> | <span data-ttu-id="f98df-134">Valor</span><span class="sxs-lookup"><span data-stu-id="f98df-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f98df-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f98df-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f98df-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f98df-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f98df-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f98df-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f98df-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f98df-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f98df-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="f98df-139">Namespace</span></span><br/>                | <span data-ttu-id="f98df-140">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="f98df-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="f98df-141">MOF</span><span class="sxs-lookup"><span data-stu-id="f98df-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f98df-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f98df-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f98df-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="f98df-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f98df-144">**Método CreateInstanceFromPropertyData da \_ classe MGType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="f98df-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MGType Class**</span></span>](microsoftdns-mgtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="f98df-145">**Método Modify da classe MicrosoftDNS \_ MGType**</span><span class="sxs-lookup"><span data-stu-id="f98df-145">**Modify Method of the MicrosoftDNS\_MGType Class**</span></span>](microsoftdns-mgtype-modify.md)
</dt> <dt>

[<span data-ttu-id="f98df-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="f98df-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





