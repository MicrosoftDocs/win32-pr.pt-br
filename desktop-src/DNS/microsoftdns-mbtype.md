---
title: Classe MicrosoftDNS_MBType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro de recurso de caixa de correio (MB).
ms.assetid: b8f3b106-58f4-44b8-b2db-b00f1a495641
keywords:
- MicrosoftDNS_MBType de classe de DNS
- MicrosoftDNS_MBType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType
- MicrosoftDNS_MBType.CreateInstanceFromPropertyData
- MicrosoftDNS_MBType.Modify
- MicrosoftDNS_MBType.MBHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89ad6599ad058f65beba961f00c1bd6c43663487
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918606"
---
# <a name="microsoftdns_mbtype-class"></a><span data-ttu-id="ca67d-105">\_Classe MicrosoftDNS MBType</span><span class="sxs-lookup"><span data-stu-id="ca67d-105">MicrosoftDNS\_MBType class</span></span>

<span data-ttu-id="ca67d-106">A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro de recurso de caixa de correio (MB).</span><span class="sxs-lookup"><span data-stu-id="ca67d-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Mailbox (MB) resource record.</span></span>

<span data-ttu-id="ca67d-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="ca67d-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca67d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca67d-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_MBType : MicrosoftDNS_ResourceRecord
{
  string MBHost;
};
```

## <a name="members"></a><span data-ttu-id="ca67d-109">Membros</span><span class="sxs-lookup"><span data-stu-id="ca67d-109">Members</span></span>

<span data-ttu-id="ca67d-110">A classe **MicrosoftDNS \_ MBType** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ca67d-110">The **MicrosoftDNS\_MBType** class has these types of members:</span></span>

-   [<span data-ttu-id="ca67d-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="ca67d-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="ca67d-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ca67d-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ca67d-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="ca67d-113">Methods</span></span>

<span data-ttu-id="ca67d-114">A classe **MicrosoftDNS \_ MBType** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ca67d-114">The **MicrosoftDNS\_MBType** class has these methods.</span></span>



| <span data-ttu-id="ca67d-115">Método</span><span class="sxs-lookup"><span data-stu-id="ca67d-115">Method</span></span>                             | <span data-ttu-id="ca67d-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca67d-116">Description</span></span>                                                                                                                                                                                                                                                                                                                               |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca67d-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="ca67d-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="ca67d-118">Cria uma instância de um RR de MB com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário da caixa de correio, a classe (padrão = IN), o valor de vida útil e o host da caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="ca67d-118">Instantiates an MB RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name of the mailbox, class (default = IN), time-to-live value and the mailbox host.</span></span> <span data-ttu-id="ca67d-119">Ele retorna uma referência ao novo objeto como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="ca67d-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="ca67d-120">Qualificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="ca67d-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="ca67d-121">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="ca67d-121">**Modify**</span></span>                         | <span data-ttu-id="ca67d-122">Atualiza o tempo de vida e o host de MB para os valores especificados como os parâmetros de entrada deste método.</span><span class="sxs-lookup"><span data-stu-id="ca67d-122">Updates the TTL and MB host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="ca67d-123">Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado.</span><span class="sxs-lookup"><span data-stu-id="ca67d-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="ca67d-124">O método retorna uma referência ao objeto modificado como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="ca67d-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="ca67d-125">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="ca67d-125">Qualifiers: Implemented</span></span><br/>        |



 

### <a name="properties"></a><span data-ttu-id="ca67d-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ca67d-126">Properties</span></span>

<span data-ttu-id="ca67d-127">A classe **MicrosoftDNS \_ MBType** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ca67d-127">The **MicrosoftDNS\_MBType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ca67d-128">**MBHost**</span><span class="sxs-lookup"><span data-stu-id="ca67d-128">**MBHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca67d-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca67d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca67d-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca67d-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca67d-131">FQDN que especifica um host da caixa de correio especificado no nome do proprietário do registro.</span><span class="sxs-lookup"><span data-stu-id="ca67d-131">FQDN that specifies a host of the mailbox specified in the record's Owner Name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca67d-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca67d-132">Requirements</span></span>



| <span data-ttu-id="ca67d-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca67d-133">Requirement</span></span> | <span data-ttu-id="ca67d-134">Valor</span><span class="sxs-lookup"><span data-stu-id="ca67d-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca67d-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca67d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ca67d-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ca67d-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ca67d-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca67d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ca67d-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ca67d-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ca67d-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="ca67d-139">Namespace</span></span><br/>                | <span data-ttu-id="ca67d-140">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="ca67d-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ca67d-141">MOF</span><span class="sxs-lookup"><span data-stu-id="ca67d-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca67d-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca67d-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca67d-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca67d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca67d-144">**Método CreateInstanceFromPropertyData da \_ classe MBType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ca67d-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MBType Class**</span></span>](microsoftdns-mbtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="ca67d-145">**Método Modify da classe MicrosoftDNS \_ MBType**</span><span class="sxs-lookup"><span data-stu-id="ca67d-145">**Modify Method of the MicrosoftDNS\_MBType Class**</span></span>](microsoftdns-mbtype-modify.md)
</dt> <dt>

[<span data-ttu-id="ca67d-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="ca67d-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





