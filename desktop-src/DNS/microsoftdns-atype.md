---
title: Classe MicrosoftDNS_AType
description: Subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro de endereço de host (a).
ms.assetid: c7bd8a26-b0ac-49ef-9068-a0ecddeb6ef4
keywords:
- MicrosoftDNS_AType de classe de DNS
- MicrosoftDNS_AType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType
- MicrosoftDNS_AType.CreateInstanceFromPropertyData
- MicrosoftDNS_AType.Modify
- MicrosoftDNS_AType.IPAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e856968e2c3d4e581d69e0ac7bcbddc256424c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755415"
---
# <a name="microsoftdns_atype-class"></a><span data-ttu-id="9f706-105">\_Classe MicrosoftDNS AType</span><span class="sxs-lookup"><span data-stu-id="9f706-105">MicrosoftDNS\_AType class</span></span>

<span data-ttu-id="9f706-106">Subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro de endereço de host (a).</span><span class="sxs-lookup"><span data-stu-id="9f706-106">Subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a host Address (A) record.</span></span>

<span data-ttu-id="9f706-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="9f706-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f706-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f706-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_AType : MicrosoftDNS_ResourceRecord
{
  string IPAddress;
};
```

## <a name="members"></a><span data-ttu-id="9f706-109">Membros</span><span class="sxs-lookup"><span data-stu-id="9f706-109">Members</span></span>

<span data-ttu-id="9f706-110">A classe **MicrosoftDNS \_ AType** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9f706-110">The **MicrosoftDNS\_AType** class has these types of members:</span></span>

-   [<span data-ttu-id="9f706-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="9f706-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="9f706-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9f706-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9f706-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="9f706-113">Methods</span></span>

<span data-ttu-id="9f706-114">A classe **MicrosoftDNS \_ AType** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="9f706-114">The **MicrosoftDNS\_AType** class has these methods.</span></span>



| <span data-ttu-id="9f706-115">Método</span><span class="sxs-lookup"><span data-stu-id="9f706-115">Method</span></span>                             | <span data-ttu-id="9f706-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f706-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f706-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="9f706-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="9f706-118">Cria uma instância de um RR de endereço de host (A) com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário, a classe (padrão = IN), o valor de vida útil e o endereço IP do host.</span><span class="sxs-lookup"><span data-stu-id="9f706-118">Instantiates a Host Address (A) RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value and the IP address of the host.</span></span> <span data-ttu-id="9f706-119">Ele retorna uma referência ao novo objeto como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="9f706-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="9f706-120">Qualificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="9f706-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="9f706-121">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="9f706-121">**Modify**</span></span>                         | <span data-ttu-id="9f706-122">Atualiza o TTL e o endereço IP para os valores especificados como os parâmetros de entrada deste método.</span><span class="sxs-lookup"><span data-stu-id="9f706-122">Updates the TTL and IP address to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="9f706-123">Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado.</span><span class="sxs-lookup"><span data-stu-id="9f706-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="9f706-124">O método retorna uma referência ao objeto modificado como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="9f706-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="9f706-125">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="9f706-125">Qualifiers: Implemented</span></span><br/>             |



 

### <a name="properties"></a><span data-ttu-id="9f706-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9f706-126">Properties</span></span>

<span data-ttu-id="9f706-127">A classe **MicrosoftDNS \_ AType** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9f706-127">The **MicrosoftDNS\_AType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9f706-128">**EndereçoIP**</span><span class="sxs-lookup"><span data-stu-id="9f706-128">**IPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f706-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f706-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f706-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9f706-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f706-131">Cadeia de caracteres que representa o endereço IPv4 do host.</span><span class="sxs-lookup"><span data-stu-id="9f706-131">String representing the IPv4 address of the host.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9f706-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f706-132">Requirements</span></span>



| <span data-ttu-id="9f706-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f706-133">Requirement</span></span> | <span data-ttu-id="9f706-134">Valor</span><span class="sxs-lookup"><span data-stu-id="9f706-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f706-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f706-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9f706-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9f706-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9f706-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f706-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9f706-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9f706-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9f706-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="9f706-139">Namespace</span></span><br/>                | <span data-ttu-id="9f706-140">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="9f706-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="9f706-141">MOF</span><span class="sxs-lookup"><span data-stu-id="9f706-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f706-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f706-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f706-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f706-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f706-144">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="9f706-144">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="9f706-145">**Método CreateInstanceFromPropertyData da \_ classe AType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="9f706-145">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AType Class**</span></span>](microsoftdns-atype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="9f706-146">**Método Modify da classe MicrosoftDNS \_ AType**</span><span class="sxs-lookup"><span data-stu-id="9f706-146">**Modify Method of the MicrosoftDNS\_AType Class**</span></span>](microsoftdns-atype-modify.md)
</dt> </dl>

 

 





