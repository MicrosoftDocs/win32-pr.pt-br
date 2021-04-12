---
title: Classe MicrosoftDNS_PTRType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro de ponteiro (PTR).
ms.assetid: 2cb0f13b-e683-473b-9cdd-bc5d805b919d
keywords:
- MicrosoftDNS_PTRType de classe de DNS
- MicrosoftDNS_PTRType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_PTRType
- MicrosoftDNS_PTRType.CreateInstanceFromPropertyData
- MicrosoftDNS_PTRType.Modify
- MicrosoftDNS_PTRType.PTRDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65dc434eb751ed925ab9efcdaf29f04741b749ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499432"
---
# <a name="microsoftdns_ptrtype-class"></a><span data-ttu-id="3ed73-105">\_Classe MicrosoftDNS PTRType</span><span class="sxs-lookup"><span data-stu-id="3ed73-105">MicrosoftDNS\_PTRType class</span></span>

<span data-ttu-id="3ed73-106">A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro de ponteiro (PTR).</span><span class="sxs-lookup"><span data-stu-id="3ed73-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Pointer (PTR) record.</span></span>

<span data-ttu-id="3ed73-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="3ed73-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ed73-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ed73-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_PTRType : MicrosoftDNS_ResourceRecord
{
  string PTRDomainName;
};
```

## <a name="members"></a><span data-ttu-id="3ed73-109">Membros</span><span class="sxs-lookup"><span data-stu-id="3ed73-109">Members</span></span>

<span data-ttu-id="3ed73-110">A classe **MicrosoftDNS \_ PTRType** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3ed73-110">The **MicrosoftDNS\_PTRType** class has these types of members:</span></span>

-   [<span data-ttu-id="3ed73-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="3ed73-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="3ed73-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3ed73-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3ed73-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="3ed73-113">Methods</span></span>

<span data-ttu-id="3ed73-114">A classe **MicrosoftDNS \_ PTRType** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="3ed73-114">The **MicrosoftDNS\_PTRType** class has these methods.</span></span>



| <span data-ttu-id="3ed73-115">Método</span><span class="sxs-lookup"><span data-stu-id="3ed73-115">Method</span></span>                             | <span data-ttu-id="3ed73-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ed73-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ed73-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="3ed73-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="3ed73-118">Cria uma instância de um registro de recurso PTR de DNS com base nos dados dos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário, a classe (padrão = IN), o valor de vida útil e o FQDN do registro PTR.</span><span class="sxs-lookup"><span data-stu-id="3ed73-118">Instantiates a DNS PTR Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value and the FQDN of the PTR record.</span></span> <span data-ttu-id="3ed73-119">Ele retorna uma referência ao novo objeto como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="3ed73-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="3ed73-120">Qualificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="3ed73-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="3ed73-121">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="3ed73-121">**Modify**</span></span>                         | <span data-ttu-id="3ed73-122">Atualiza o TTL e o nome de domínio PTR para os valores especificados como os parâmetros de entrada deste método.</span><span class="sxs-lookup"><span data-stu-id="3ed73-122">Updates the TTL and PTR Domain Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="3ed73-123">Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado.</span><span class="sxs-lookup"><span data-stu-id="3ed73-123">If a new value for a parameter is not specified, the current value for the parameter is not changed.</span></span> <span data-ttu-id="3ed73-124">O método retorna uma referência ao objeto modificado como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="3ed73-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="3ed73-125">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="3ed73-125">Qualifiers: Implemented</span></span><br/>                 |



 

### <a name="properties"></a><span data-ttu-id="3ed73-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3ed73-126">Properties</span></span>

<span data-ttu-id="3ed73-127">A classe **MicrosoftDNS \_ PTRType** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3ed73-127">The **MicrosoftDNS\_PTRType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3ed73-128">**PTRDomainName**</span><span class="sxs-lookup"><span data-stu-id="3ed73-128">**PTRDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed73-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3ed73-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ed73-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3ed73-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ed73-131">FQDN dos dados de registro PTR.</span><span class="sxs-lookup"><span data-stu-id="3ed73-131">FQDN of the PTR record data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3ed73-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ed73-132">Requirements</span></span>



| <span data-ttu-id="3ed73-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ed73-133">Requirement</span></span> | <span data-ttu-id="3ed73-134">Valor</span><span class="sxs-lookup"><span data-stu-id="3ed73-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ed73-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ed73-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3ed73-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3ed73-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3ed73-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ed73-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3ed73-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3ed73-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3ed73-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="3ed73-139">Namespace</span></span><br/>                | <span data-ttu-id="3ed73-140">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="3ed73-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="3ed73-141">MOF</span><span class="sxs-lookup"><span data-stu-id="3ed73-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ed73-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ed73-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ed73-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ed73-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ed73-144">**Método CreateInstanceFromPropertyData da \_ classe PTRType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="3ed73-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_PTRType Class**</span></span>](microsoftdns-ptrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="3ed73-145">**Método Modify da classe MicrosoftDNS \_ PTRType**</span><span class="sxs-lookup"><span data-stu-id="3ed73-145">**Modify Method of the MicrosoftDNS\_PTRType Class**</span></span>](microsoftdns-ptrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="3ed73-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="3ed73-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





