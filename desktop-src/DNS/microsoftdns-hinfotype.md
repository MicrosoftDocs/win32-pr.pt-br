---
title: Classe MicrosoftDNS_HINFOType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro de informações de host (HINFO).
ms.assetid: c6591010-0fe6-45b2-9032-9f847237ecf6
keywords:
- MicrosoftDNS_HINFOType de classe de DNS
- MicrosoftDNS_HINFOType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_HINFOType
- MicrosoftDNS_HINFOType.CreateInstanceFromPropertyData
- MicrosoftDNS_HINFOType.Modify
- MicrosoftDNS_HINFOType.CPU
- MicrosoftDNS_HINFOType.OS
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3298e5a7f90dbaee24e5014b1a3aab76ad6997
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756226"
---
# <a name="microsoftdns_hinfotype-class"></a><span data-ttu-id="e78b9-105">\_Classe MicrosoftDNS HINFOType</span><span class="sxs-lookup"><span data-stu-id="e78b9-105">MicrosoftDNS\_HINFOType class</span></span>

<span data-ttu-id="e78b9-106">A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro de informações de host (HINFO).</span><span class="sxs-lookup"><span data-stu-id="e78b9-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Host Information (HINFO) record.</span></span>

<span data-ttu-id="e78b9-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="e78b9-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e78b9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e78b9-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_HINFOType : MicrosoftDNS_ResourceRecord
{
  string CPU;
  string OS;
};
```

## <a name="members"></a><span data-ttu-id="e78b9-109">Membros</span><span class="sxs-lookup"><span data-stu-id="e78b9-109">Members</span></span>

<span data-ttu-id="e78b9-110">A classe **MicrosoftDNS \_ HINFOType** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e78b9-110">The **MicrosoftDNS\_HINFOType** class has these types of members:</span></span>

-   [<span data-ttu-id="e78b9-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="e78b9-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="e78b9-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e78b9-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e78b9-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="e78b9-113">Methods</span></span>

<span data-ttu-id="e78b9-114">A classe **MicrosoftDNS \_ HINFOType** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e78b9-114">The **MicrosoftDNS\_HINFOType** class has these methods.</span></span>



| <span data-ttu-id="e78b9-115">Método</span><span class="sxs-lookup"><span data-stu-id="e78b9-115">Method</span></span>                             | <span data-ttu-id="e78b9-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="e78b9-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e78b9-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="e78b9-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="e78b9-118">Cria uma instância de um HINFO de RR com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário, a classe (padrão = IN), o valor de vida útil e os tipos de CPU e sistema operacional do host.</span><span class="sxs-lookup"><span data-stu-id="e78b9-118">Instantiates an HINFO of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the host's CPU and operating system types.</span></span> <span data-ttu-id="e78b9-119">Ele retorna uma referência ao novo objeto como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="e78b9-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="e78b9-120">Qualificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="e78b9-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="e78b9-121">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="e78b9-121">**Modify**</span></span>                         | <span data-ttu-id="e78b9-122">Atualiza o TTL, a CPU e o sistema operacional para os valores especificados como os parâmetros de entrada deste método.</span><span class="sxs-lookup"><span data-stu-id="e78b9-122">Updates the TTL, CPU, and operating system to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="e78b9-123">Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado.</span><span class="sxs-lookup"><span data-stu-id="e78b9-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="e78b9-124">O método retorna uma referência ao objeto modificado como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="e78b9-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="e78b9-125">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="e78b9-125">Qualifiers: Implemented</span></span><br/>          |



 

### <a name="properties"></a><span data-ttu-id="e78b9-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e78b9-126">Properties</span></span>

<span data-ttu-id="e78b9-127">A classe **MicrosoftDNS \_ HINFOType** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e78b9-127">The **MicrosoftDNS\_HINFOType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e78b9-128">**CPU**</span><span class="sxs-lookup"><span data-stu-id="e78b9-128">**CPU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e78b9-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e78b9-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e78b9-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e78b9-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e78b9-131">Tipo de CPU do proprietário do registro.</span><span class="sxs-lookup"><span data-stu-id="e78b9-131">CPU type of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="e78b9-132">**SO**</span><span class="sxs-lookup"><span data-stu-id="e78b9-132">**OS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e78b9-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e78b9-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e78b9-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e78b9-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e78b9-135">Sistema operacional do proprietário do registro.</span><span class="sxs-lookup"><span data-stu-id="e78b9-135">Operating system of the record owner.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e78b9-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e78b9-136">Requirements</span></span>



| <span data-ttu-id="e78b9-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="e78b9-137">Requirement</span></span> | <span data-ttu-id="e78b9-138">Valor</span><span class="sxs-lookup"><span data-stu-id="e78b9-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e78b9-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e78b9-139">Minimum supported client</span></span><br/> | <span data-ttu-id="e78b9-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e78b9-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e78b9-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e78b9-141">Minimum supported server</span></span><br/> | <span data-ttu-id="e78b9-142">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e78b9-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e78b9-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="e78b9-143">Namespace</span></span><br/>                | <span data-ttu-id="e78b9-144">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="e78b9-144">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="e78b9-145">MOF</span><span class="sxs-lookup"><span data-stu-id="e78b9-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e78b9-146"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e78b9-146"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e78b9-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="e78b9-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e78b9-148">**Método CreateInstanceFromPropertyData da \_ classe HINFOType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="e78b9-148">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_HINFOType Class**</span></span>](microsoftdns-hinfotype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="e78b9-149">**Método Modify da classe MicrosoftDNS \_ HINFOType**</span><span class="sxs-lookup"><span data-stu-id="e78b9-149">**Modify Method of the MicrosoftDNS\_HINFOType Class**</span></span>](microsoftdns-hinfotype-modify.md)
</dt> <dt>

[<span data-ttu-id="e78b9-150">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="e78b9-150">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





