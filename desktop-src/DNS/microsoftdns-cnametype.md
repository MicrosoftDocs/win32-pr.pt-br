---
title: Classe MicrosoftDNS_CNAMEType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro de nome canônico (CNAME).
ms.assetid: 93a972e3-abb1-425f-beb7-32abe7d0b485
keywords:
- MicrosoftDNS_CNAMEType de classe de DNS
- MicrosoftDNS_CNAMEType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_CNAMEType
- MicrosoftDNS_CNAMEType.CreateInstanceFromPropertyData
- MicrosoftDNS_CNAMEType.Modify
- MicrosoftDNS_CNAMEType.PrimaryName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dca8729c2c750e1cef774b5f0f3eadc3e2f6fbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824418"
---
# <a name="microsoftdns_cnametype-class"></a><span data-ttu-id="b1f25-105">\_Classe cnametype MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="b1f25-105">MicrosoftDNS\_CNAMEType class</span></span>

<span data-ttu-id="b1f25-106">A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro de nome canônico (CNAME).</span><span class="sxs-lookup"><span data-stu-id="b1f25-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Canonical Name (CNAME) record.</span></span>

<span data-ttu-id="b1f25-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="b1f25-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1f25-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1f25-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_CNAMEType : MicrosoftDNS_ResourceRecord
{
  string PrimaryName;
};
```

## <a name="members"></a><span data-ttu-id="b1f25-109">Membros</span><span class="sxs-lookup"><span data-stu-id="b1f25-109">Members</span></span>

<span data-ttu-id="b1f25-110">A **classe \_ cnametype MicrosoftDNS** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b1f25-110">The **MicrosoftDNS\_CNAMEType** class has these types of members:</span></span>

-   [<span data-ttu-id="b1f25-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="b1f25-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="b1f25-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b1f25-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b1f25-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="b1f25-113">Methods</span></span>

<span data-ttu-id="b1f25-114">A **classe \_ cnametype MicrosoftDNS** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="b1f25-114">The **MicrosoftDNS\_CNAMEType** class has these methods.</span></span>



| <span data-ttu-id="b1f25-115">Método</span><span class="sxs-lookup"><span data-stu-id="b1f25-115">Method</span></span>                             | <span data-ttu-id="b1f25-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1f25-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                    |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1f25-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="b1f25-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="b1f25-118">Cria uma instância de um registro de recurso CNAME com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário, a classe (padrão = IN), o valor de vida útil e o nome primário do registro CNAME.</span><span class="sxs-lookup"><span data-stu-id="b1f25-118">Instantiates a CNAME Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the primary name of the CNAME record.</span></span> <span data-ttu-id="b1f25-119">Ele retorna uma referência ao novo objeto como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="b1f25-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="b1f25-120">Qualificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="b1f25-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="b1f25-121">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="b1f25-121">**Modify**</span></span>                         | <span data-ttu-id="b1f25-122">Atualiza o TTL e o nome primário para os valores especificados como os parâmetros de entrada deste método.</span><span class="sxs-lookup"><span data-stu-id="b1f25-122">Updates the TTL and Primary Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="b1f25-123">Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado.</span><span class="sxs-lookup"><span data-stu-id="b1f25-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="b1f25-124">O método retorna uma referência ao objeto modificado como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="b1f25-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="b1f25-125">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="b1f25-125">Qualifiers: Implemented</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="b1f25-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b1f25-126">Properties</span></span>

<span data-ttu-id="b1f25-127">A **classe \_ cnametype MicrosoftDNS** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b1f25-127">The **MicrosoftDNS\_CNAMEType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b1f25-128">**Primárioname**</span><span class="sxs-lookup"><span data-stu-id="b1f25-128">**PrimaryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1f25-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b1f25-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1f25-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1f25-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1f25-131">Canônico ou nome primário para o proprietário do registro CNAME.</span><span class="sxs-lookup"><span data-stu-id="b1f25-131">Canonical, or primary name for the owner of the CNAME record.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1f25-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1f25-132">Requirements</span></span>



| <span data-ttu-id="b1f25-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1f25-133">Requirement</span></span> | <span data-ttu-id="b1f25-134">Valor</span><span class="sxs-lookup"><span data-stu-id="b1f25-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1f25-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1f25-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b1f25-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b1f25-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b1f25-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1f25-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b1f25-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b1f25-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b1f25-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="b1f25-139">Namespace</span></span><br/>                | <span data-ttu-id="b1f25-140">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="b1f25-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="b1f25-141">MOF</span><span class="sxs-lookup"><span data-stu-id="b1f25-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1f25-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b1f25-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1f25-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1f25-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1f25-144">**Método CreateInstanceFromPropertyData da \_ classe cnametype MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="b1f25-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_CNAMEType Class**</span></span>](microsoftdns-cnametype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="b1f25-145">**Método Modify da classe MicrosoftDNS \_ cnametype**</span><span class="sxs-lookup"><span data-stu-id="b1f25-145">**Modify Method of the MicrosoftDNS\_CNAMEType Class**</span></span>](microsoftdns-cnametype-modify.md)
</dt> <dt>

[<span data-ttu-id="b1f25-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="b1f25-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





