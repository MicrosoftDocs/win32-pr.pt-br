---
title: Classe MicrosoftDNS_TXTType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro de texto (txt).
ms.assetid: e4bd445f-71c4-48dc-b210-e3ad4452d2e5
keywords:
- MicrosoftDNS_TXTType de classe de DNS
- MicrosoftDNS_TXTType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType
- MicrosoftDNS_TXTType.CreateInstanceFromPropertyData
- MicrosoftDNS_TXTType.Modify
- MicrosoftDNS_TXTType.DescriptiveText
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d89563240b8e6d6bedb51cbe802180cd7577b57e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756017"
---
# <a name="microsoftdns_txttype-class"></a><span data-ttu-id="01a3b-105">\_Classe MicrosoftDNS TXTType</span><span class="sxs-lookup"><span data-stu-id="01a3b-105">MicrosoftDNS\_TXTType class</span></span>

<span data-ttu-id="01a3b-106">A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro de texto (txt).</span><span class="sxs-lookup"><span data-stu-id="01a3b-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Text (TXT) record.</span></span>

<span data-ttu-id="01a3b-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="01a3b-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="01a3b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01a3b-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_TXTType : MicrosoftDNS_ResourceRecord
{
  string DescriptiveText;
};
```

## <a name="members"></a><span data-ttu-id="01a3b-109">Membros</span><span class="sxs-lookup"><span data-stu-id="01a3b-109">Members</span></span>

<span data-ttu-id="01a3b-110">A classe **MicrosoftDNS \_ TXTType** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="01a3b-110">The **MicrosoftDNS\_TXTType** class has these types of members:</span></span>

-   [<span data-ttu-id="01a3b-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="01a3b-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="01a3b-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="01a3b-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="01a3b-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="01a3b-113">Methods</span></span>

<span data-ttu-id="01a3b-114">A classe **MicrosoftDNS \_ TXTType** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="01a3b-114">The **MicrosoftDNS\_TXTType** class has these methods.</span></span>



| <span data-ttu-id="01a3b-115">Método</span><span class="sxs-lookup"><span data-stu-id="01a3b-115">Method</span></span>                             | <span data-ttu-id="01a3b-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="01a3b-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01a3b-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="01a3b-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="01a3b-118">Cria uma instância de um tipo TXT de RR com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário, a classe (padrão = IN), o valor de vida útil e o texto do registro.</span><span class="sxs-lookup"><span data-stu-id="01a3b-118">Instantiates a TXT Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the record's text.</span></span> <span data-ttu-id="01a3b-119">Ele retorna uma referência ao novo objeto como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="01a3b-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="01a3b-120">Qualificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="01a3b-120">Qualifiers: Implemented, static</span></span><br/>        |
| <span data-ttu-id="01a3b-121">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="01a3b-121">**Modify**</span></span>                         | <span data-ttu-id="01a3b-122">Atualiza o TTL e o texto descritivo para os valores especificados como os parâmetros de entrada deste método.</span><span class="sxs-lookup"><span data-stu-id="01a3b-122">Updates the TTL and Descriptive Text to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="01a3b-123">Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado.</span><span class="sxs-lookup"><span data-stu-id="01a3b-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="01a3b-124">O método retorna uma referência ao objeto modificado como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="01a3b-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="01a3b-125">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="01a3b-125">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="01a3b-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="01a3b-126">Properties</span></span>

<span data-ttu-id="01a3b-127">A classe **MicrosoftDNS \_ TXTType** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="01a3b-127">The **MicrosoftDNS\_TXTType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="01a3b-128">**DescriptiveText**</span><span class="sxs-lookup"><span data-stu-id="01a3b-128">**DescriptiveText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a3b-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01a3b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01a3b-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01a3b-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01a3b-131">Texto descritivo, a semântica que depende do domínio do proprietário.</span><span class="sxs-lookup"><span data-stu-id="01a3b-131">Descriptive text, the semantics of which depend on the owner domain.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="01a3b-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01a3b-132">Requirements</span></span>



| <span data-ttu-id="01a3b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="01a3b-133">Requirement</span></span> | <span data-ttu-id="01a3b-134">Valor</span><span class="sxs-lookup"><span data-stu-id="01a3b-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="01a3b-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01a3b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="01a3b-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="01a3b-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="01a3b-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01a3b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="01a3b-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="01a3b-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="01a3b-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="01a3b-139">Namespace</span></span><br/>                | <span data-ttu-id="01a3b-140">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="01a3b-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="01a3b-141">MOF</span><span class="sxs-lookup"><span data-stu-id="01a3b-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01a3b-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01a3b-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01a3b-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="01a3b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01a3b-144">**Método CreateInstanceFromPropertyData da \_ classe TXTType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="01a3b-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_TXTType Class**</span></span>](microsoftdns-txttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="01a3b-145">**Método Modify da classe MicrosoftDNS \_ TXTType**</span><span class="sxs-lookup"><span data-stu-id="01a3b-145">**Modify Method of the MicrosoftDNS\_TXTType Class**</span></span>](microsoftdns-txttype-modify.md)
</dt> <dt>

[<span data-ttu-id="01a3b-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="01a3b-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





