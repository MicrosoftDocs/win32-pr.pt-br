---
title: Classe MicrosoftDNS_X25Type
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro de X. 25 (X25).
ms.assetid: 1213dfd7-30b3-413e-b723-f4284fa0b416
keywords:
- MicrosoftDNS_X25Type de classe de DNS
- MicrosoftDNS_X25Type de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_X25Type
- MicrosoftDNS_X25Type.CreateInstanceFromPropertyData
- MicrosoftDNS_X25Type.Modify
- MicrosoftDNS_X25Type.PSDNAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e584119dbd45d5d6c7fae347c506c42fcda4fff7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749294"
---
# <a name="microsoftdns_x25type-class"></a><span data-ttu-id="2ece4-105">\_Classe MicrosoftDNS X25Type</span><span class="sxs-lookup"><span data-stu-id="2ece4-105">MicrosoftDNS\_X25Type class</span></span>

<span data-ttu-id="2ece4-106">A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro de X. 25 (X25).</span><span class="sxs-lookup"><span data-stu-id="2ece4-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an X.25 (X25) record.</span></span>

<span data-ttu-id="2ece4-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="2ece4-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ece4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2ece4-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_X25Type : MicrosoftDNS_ResourceRecord
{
  string PSDNAddress;
};
```

## <a name="members"></a><span data-ttu-id="2ece4-109">Membros</span><span class="sxs-lookup"><span data-stu-id="2ece4-109">Members</span></span>

<span data-ttu-id="2ece4-110">A classe **MicrosoftDNS \_ X25Type** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2ece4-110">The **MicrosoftDNS\_X25Type** class has these types of members:</span></span>

-   [<span data-ttu-id="2ece4-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="2ece4-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="2ece4-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2ece4-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2ece4-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="2ece4-113">Methods</span></span>

<span data-ttu-id="2ece4-114">A classe **MicrosoftDNS \_ X25Type** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="2ece4-114">The **MicrosoftDNS\_X25Type** class has these methods.</span></span>



| <span data-ttu-id="2ece4-115">Método</span><span class="sxs-lookup"><span data-stu-id="2ece4-115">Method</span></span>                             | <span data-ttu-id="2ece4-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="2ece4-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ece4-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="2ece4-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="2ece4-118">Cria uma instância de um tipo "X25" de RR com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário, a classe (padrão = IN), o valor de vida útil e o endereço PSDN.</span><span class="sxs-lookup"><span data-stu-id="2ece4-118">Instantiates an 'X25' Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the PSDN address.</span></span> <span data-ttu-id="2ece4-119">Ele retorna uma referência ao novo objeto como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="2ece4-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="2ece4-120">Qualificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="2ece4-120">Qualifiers: Implemented, static</span></span><br/>              |
| <span data-ttu-id="2ece4-121">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="2ece4-121">**Modify**</span></span>                         | <span data-ttu-id="2ece4-122">Esse método atualiza o TTL e o endereço PSDN para os valores especificados como os parâmetros de entrada deste método.</span><span class="sxs-lookup"><span data-stu-id="2ece4-122">This method updates the TTL and PSDN Address to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="2ece4-123">Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado.</span><span class="sxs-lookup"><span data-stu-id="2ece4-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="2ece4-124">O método retorna uma referência ao objeto modificado como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="2ece4-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="2ece4-125">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="2ece4-125">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2ece4-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2ece4-126">Properties</span></span>

<span data-ttu-id="2ece4-127">A classe **MicrosoftDNS \_ X25Type** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2ece4-127">The **MicrosoftDNS\_X25Type** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2ece4-128">**PSDNAddress**</span><span class="sxs-lookup"><span data-stu-id="2ece4-128">**PSDNAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ece4-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2ece4-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ece4-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2ece4-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2ece4-131">Endereço PSDN do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="2ece4-131">PSDN address of the owner of the RR.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2ece4-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ece4-132">Requirements</span></span>



| <span data-ttu-id="2ece4-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ece4-133">Requirement</span></span> | <span data-ttu-id="2ece4-134">Valor</span><span class="sxs-lookup"><span data-stu-id="2ece4-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ece4-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ece4-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2ece4-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2ece4-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2ece4-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ece4-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2ece4-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2ece4-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2ece4-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="2ece4-139">Namespace</span></span><br/>                | <span data-ttu-id="2ece4-140">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="2ece4-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="2ece4-141">MOF</span><span class="sxs-lookup"><span data-stu-id="2ece4-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2ece4-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2ece4-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ece4-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ece4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ece4-144">**Método CreateInstanceFromPropertyData da \_ classe X25Type MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="2ece4-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_X25Type Class**</span></span>](microsoftdns-x25type-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="2ece4-145">**Método Modify da classe MicrosoftDNS \_ X25Type**</span><span class="sxs-lookup"><span data-stu-id="2ece4-145">**Modify Method of the MicrosoftDNS\_X25Type Class**</span></span>](microsoftdns-x25type-modify.md)
</dt> <dt>

[<span data-ttu-id="2ece4-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="2ece4-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





