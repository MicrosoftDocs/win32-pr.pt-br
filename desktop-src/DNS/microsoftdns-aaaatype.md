---
title: Classe MicrosoftDNS_AAAAType
description: Subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro de endereço IPv6 (aaaa). O registro AAAA é geralmente pronunciado \ 0034; Quad-a Record \ 0034;.
ms.assetid: e16a7a69-18df-43dc-add9-700a702724ce
keywords:
- MicrosoftDNS_AAAAType de classe de DNS
- MicrosoftDNS_AAAAType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType
- MicrosoftDNS_AAAAType.CreateInstanceFromPropertyData
- MicrosoftDNS_AAAAType.Modify
- MicrosoftDNS_AAAAType.IPv6Address
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0131177c342730c08868946c29356554cbfb9cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105762738"
---
# <a name="microsoftdns_aaaatype-class"></a><span data-ttu-id="2267f-106">\_Classe aaaatype MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="2267f-106">MicrosoftDNS\_AAAAType class</span></span>

<span data-ttu-id="2267f-107">Subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro de endereço IPv6 (aaaa).</span><span class="sxs-lookup"><span data-stu-id="2267f-107">Subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an IPv6 Address (AAAA) record.</span></span> <span data-ttu-id="2267f-108">O registro AAAA é geralmente pronunciado como "quad-a Record".</span><span class="sxs-lookup"><span data-stu-id="2267f-108">The AAAA record is commonly pronounced "quad-a record".</span></span>

<span data-ttu-id="2267f-109">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="2267f-109">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2267f-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2267f-110">Syntax</span></span>

``` syntax
class MicrosoftDNS_AAAAType : MicrosoftDNS_ResourceRecord
{
  string IPv6Address;
};
```

## <a name="members"></a><span data-ttu-id="2267f-111">Membros</span><span class="sxs-lookup"><span data-stu-id="2267f-111">Members</span></span>

<span data-ttu-id="2267f-112">A **classe \_ aaaatype MicrosoftDNS** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2267f-112">The **MicrosoftDNS\_AAAAType** class has these types of members:</span></span>

-   [<span data-ttu-id="2267f-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="2267f-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="2267f-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2267f-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2267f-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="2267f-115">Methods</span></span>

<span data-ttu-id="2267f-116">A **classe \_ aaaatype MicrosoftDNS** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="2267f-116">The **MicrosoftDNS\_AAAAType** class has these methods.</span></span>



| <span data-ttu-id="2267f-117">Método</span><span class="sxs-lookup"><span data-stu-id="2267f-117">Method</span></span>                             | <span data-ttu-id="2267f-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="2267f-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2267f-119">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="2267f-119">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="2267f-120">Cria uma instância de um tipo ' AAAA ' de RR com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do host/proprietário, a classe (padrão = IN), o valor de vida útil e o endereço IPv6.</span><span class="sxs-lookup"><span data-stu-id="2267f-120">Instantiates an 'AAAA' type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/Host Name, class (default = IN), time-to-live value, and the IPv6 address.</span></span> <span data-ttu-id="2267f-121">Ele retorna uma referência ao novo objeto como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="2267f-121">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="2267f-122">Qualificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="2267f-122">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="2267f-123">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="2267f-123">**Modify**</span></span>                         | <span data-ttu-id="2267f-124">Atualiza o TTL e o endereço IPv6 para os valores especificados como os parâmetros de entrada deste método.</span><span class="sxs-lookup"><span data-stu-id="2267f-124">Updates the TTL and IPv6 address to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="2267f-125">Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado.</span><span class="sxs-lookup"><span data-stu-id="2267f-125">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="2267f-126">O método retorna uma referência ao objeto modificado como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="2267f-126">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="2267f-127">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="2267f-127">Qualifiers: Implemented</span></span><br/>      |



 

### <a name="properties"></a><span data-ttu-id="2267f-128">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2267f-128">Properties</span></span>

<span data-ttu-id="2267f-129">A **classe \_ aaaatype MicrosoftDNS** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2267f-129">The **MicrosoftDNS\_AAAAType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2267f-130">**IPv6Address**</span><span class="sxs-lookup"><span data-stu-id="2267f-130">**IPv6Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2267f-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2267f-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2267f-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2267f-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2267f-133">Endereço IPv6 para o host.</span><span class="sxs-lookup"><span data-stu-id="2267f-133">IPv6 address for the host.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2267f-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2267f-134">Requirements</span></span>



| <span data-ttu-id="2267f-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="2267f-135">Requirement</span></span> | <span data-ttu-id="2267f-136">Valor</span><span class="sxs-lookup"><span data-stu-id="2267f-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2267f-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2267f-137">Minimum supported client</span></span><br/> | <span data-ttu-id="2267f-138">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2267f-138">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2267f-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2267f-139">Minimum supported server</span></span><br/> | <span data-ttu-id="2267f-140">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2267f-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2267f-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="2267f-141">Namespace</span></span><br/>                | <span data-ttu-id="2267f-142">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="2267f-142">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="2267f-143">MOF</span><span class="sxs-lookup"><span data-stu-id="2267f-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2267f-144"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2267f-144"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2267f-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="2267f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2267f-146">**Método CreateInstanceFromPropertyData da \_ classe aaaatype MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="2267f-146">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AAAAType Class**</span></span>](microsoftdns-aaaatype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="2267f-147">**Método Modify da classe MicrosoftDNS \_ aaaatype**</span><span class="sxs-lookup"><span data-stu-id="2267f-147">**Modify Method of the MicrosoftDNS\_AAAAType Class**</span></span>](microsoftdns-aaaatype-modify.md)
</dt> <dt>

[<span data-ttu-id="2267f-148">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="2267f-148">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





