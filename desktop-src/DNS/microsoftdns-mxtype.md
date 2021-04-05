---
title: Classe MicrosoftDNS_MXType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um RR de troca de mensagens (Mr).
ms.assetid: 7c147628-5bda-48dd-beb4-e630d1886da8
keywords:
- MicrosoftDNS_MXType de classe de DNS
- MicrosoftDNS_MXType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType
- MicrosoftDNS_MXType.CreateInstanceFromPropertyData
- MicrosoftDNS_MXType.Modify
- MicrosoftDNS_MXType.Preference
- MicrosoftDNS_MXType.MailExchange
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652743178b71b2f9fed296ecfa4427f85b5cf1c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918451"
---
# <a name="microsoftdns_mxtype-class"></a><span data-ttu-id="f5049-105">\_Classe MicrosoftDNS MXType</span><span class="sxs-lookup"><span data-stu-id="f5049-105">MicrosoftDNS\_MXType class</span></span>

<span data-ttu-id="f5049-106">A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um RR de troca de mensagens (Mr).</span><span class="sxs-lookup"><span data-stu-id="f5049-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mail Exchanger (MR) RR.</span></span>

<span data-ttu-id="f5049-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="f5049-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5049-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5049-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MXType : MicrosoftDNS_ResourceRecord
{
  uint16 Preference;
  string MailExchange;
};
```

## <a name="members"></a><span data-ttu-id="f5049-109">Membros</span><span class="sxs-lookup"><span data-stu-id="f5049-109">Members</span></span>

<span data-ttu-id="f5049-110">A classe **MicrosoftDNS \_ MXType** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f5049-110">The **MicrosoftDNS\_MXType** class has these types of members:</span></span>

-   [<span data-ttu-id="f5049-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="f5049-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="f5049-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f5049-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f5049-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="f5049-113">Methods</span></span>

<span data-ttu-id="f5049-114">A classe **MicrosoftDNS \_ MXType** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f5049-114">The **MicrosoftDNS\_MXType** class has these methods.</span></span>



| <span data-ttu-id="f5049-115">Método</span><span class="sxs-lookup"><span data-stu-id="f5049-115">Method</span></span>                             | <span data-ttu-id="f5049-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5049-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5049-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="f5049-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="f5049-118">Cria uma instância de um tipo MX de RR com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário, a classe (padrão = IN), o valor de vida útil, a preferência de registro e o nome do host que está disposto a ser uma troca de email.</span><span class="sxs-lookup"><span data-stu-id="f5049-118">Instantiates an MX Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, record preference, and host name willing to be a mail exchange.</span></span> <span data-ttu-id="f5049-119">Ele retorna uma referência ao novo objeto como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="f5049-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="f5049-120">Qualificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="f5049-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="f5049-121">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="f5049-121">**Modify**</span></span>                         | <span data-ttu-id="f5049-122">Atualiza o TTL, a preferência e a troca de email para os valores especificados como os parâmetros de entrada deste método.</span><span class="sxs-lookup"><span data-stu-id="f5049-122">Updates the TTL, Preference, and Mail Exchange to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="f5049-123">Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado.</span><span class="sxs-lookup"><span data-stu-id="f5049-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="f5049-124">O método retorna uma referência ao objeto modificado como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="f5049-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="f5049-125">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="f5049-125">Qualifiers: Implemented</span></span><br/>                         |



 

### <a name="properties"></a><span data-ttu-id="f5049-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f5049-126">Properties</span></span>

<span data-ttu-id="f5049-127">A classe **MicrosoftDNS \_ MXType** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f5049-127">The **MicrosoftDNS\_MXType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f5049-128">**MailExchange**</span><span class="sxs-lookup"><span data-stu-id="f5049-128">**MailExchange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5049-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f5049-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5049-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f5049-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5049-131">FQDN que especifica um host que está disposto a atuar como uma troca de email para o nome do proprietário.</span><span class="sxs-lookup"><span data-stu-id="f5049-131">FQDN specifying a host willing to act as a mail exchange for the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="f5049-132">**Preferência**</span><span class="sxs-lookup"><span data-stu-id="f5049-132">**Preference**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5049-133">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f5049-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f5049-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f5049-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5049-135">Preferência dada a esse RR entre outros no mesmo proprietário.</span><span class="sxs-lookup"><span data-stu-id="f5049-135">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="f5049-136">Os valores mais baixos são preferenciais.</span><span class="sxs-lookup"><span data-stu-id="f5049-136">Lower values are preferred.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5049-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5049-137">Requirements</span></span>



| <span data-ttu-id="f5049-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5049-138">Requirement</span></span> | <span data-ttu-id="f5049-139">Valor</span><span class="sxs-lookup"><span data-stu-id="f5049-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5049-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5049-140">Minimum supported client</span></span><br/> | <span data-ttu-id="f5049-141">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f5049-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f5049-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5049-142">Minimum supported server</span></span><br/> | <span data-ttu-id="f5049-143">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f5049-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f5049-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="f5049-144">Namespace</span></span><br/>                | <span data-ttu-id="f5049-145">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="f5049-145">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="f5049-146">MOF</span><span class="sxs-lookup"><span data-stu-id="f5049-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5049-147"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5049-147"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5049-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5049-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5049-149">**Método CreateInstanceFromPropertyData da \_ classe MXType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="f5049-149">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MXType Class**</span></span>](microsoftdns-mxtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="f5049-150">**Método Modify da classe MicrosoftDNS \_ MXType**</span><span class="sxs-lookup"><span data-stu-id="f5049-150">**Modify Method of the MicrosoftDNS\_MXType Class**</span></span>](microsoftdns-mxtype-modify.md)
</dt> <dt>

[<span data-ttu-id="f5049-151">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="f5049-151">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





